# Project P — Architecture Direction

This document is intentionally high-level. It defines constraints and responsibilities without prematurely locking every implementation detail.

## 1. Primary stack

- Arch Linux
- Wayland
- Hyprland
- Quickshell

## 2. Architectural goals

Project P should be:

- modular
- centralized where appropriate
- easy to extend
- easy to debug
- visually consistent
- resistant to duplication
- easy to reason about

## 3. Suggested high-level layers

```
Project P
│
├── shell/
│   ├── bar/
│   ├── notch/
│   ├── control-center/
│   ├── notifications/
│   ├── lockscreen/
│   └── launcher/
│
├── components/
│   ├── capsule/
│   ├── card/
│   ├── slider/
│   ├── toggle/
│   ├── header/
│   └── navigation/
│
├── services/
│   ├── audio/
│   ├── network/
│   ├── bluetooth/
│   ├── power/
│   ├── media/
│   ├── display/
│   └── notifications/
│
├── themes/
│
├── scripts/
│
├── config/
│
└── docs/
```

This is a direction, not a requirement to copy this exact tree.

## 4. UI layer

UI components should be reusable and theme-aware.

Avoid:

- hardcoded colours
- service commands scattered throughout QML
- duplicated controls
- giant components that do everything

UI should consume services through clear interfaces.

## 5. Service layer

Services should centralize interaction with Linux infrastructure.

Examples:

- PipeWire / WirePlumber for audio
- NetworkManager for networking
- BlueZ for Bluetooth
- MPRIS for media
- UPower or appropriate system interfaces for power
- Hyprland IPC for compositor state

The exact implementation should be chosen after repository and environment inspection.

## 6. Theme layer

Themes should expose semantic design tokens.

UI components should never need to know the raw colour values of a theme.

Conceptually:

```
Theme.background
Theme.surface
Theme.foreground
Theme.foregroundMuted
Theme.accent
Theme.success
Theme.warning
Theme.error
```

The actual implementation can differ.

## 7. Configuration

Configuration should be centralized and predictable.

The system should not require editing many unrelated files to make a coherent change.

At the same time, do not create a single huge configuration file containing unrelated concerns.

Use clear modules with a coherent entry point.

## 8. Scripts

Scripts should:

- have one clear responsibility
- use stable paths
- avoid hidden state
- avoid duplicating service logic
- be easy to test independently

## 9. External dependencies

Prefer mature Linux components when they already solve a problem well.

Project P should provide the experience layer rather than reinventing the underlying operating system.

## 10. Growth rule

When adding a feature, first ask:

1. Does an existing service already provide this?
2. Does an existing Project P component already solve the UI problem?
3. Does this belong in the service layer or UI layer?
4. Will this create duplicate state?
5. Can the feature be reused elsewhere?

Do not solve every feature as an isolated plugin.

## 11. Initial implementation principle

The visual foundation comes first.

Do not implement a complete desktop before the following are validated:

- design tokens
- theme architecture
- capsule component
- notch
- top bar composition
- motion language
- basic Control Center shell

A polished small foundation is preferable to a huge unfinished feature set.
