# Project P — Project Vision

## 1. What Project P is

Project P is a personal Linux desktop environment built on Hyprland and Quickshell.

It exists because ricing Linux was interesting but often felt overwhelming, while ready-made environments such as Omarchy demonstrated how powerful a coherent pre-built experience can be.

Previous experimentation with SwayP was valuable because it taught the author how the pieces fit together: Wayland, compositors, Quickshell, shell scripts, services, themes, plugins and configuration.

SwayP should be treated as prior experience and a source of lessons, not as the architectural or visual foundation of Project P.

Project P is **not**:

- Omarchy rebuilt on Hyprland
- SwayP rebuilt with a different compositor
- A generic Hyprland rice
- A collection of unrelated dotfiles
- A project designed around broad community requirements

It is a personal desktop environment.

## 2. Core idea

The project should feel like one deliberately designed system.

The complexity of Linux should exist underneath the surface. The user should experience one coherent desktop rather than twenty unrelated programs.

A guiding principle is:

> Complexity should live underneath the surface, not in front of the user.

## 3. Personal design direction

The main visual influences are:

- Nothing OS 4
- Modern Android UI
- Apple's Dynamic Island as an interaction reference
- Industrial product design
- Modern desktop UI

These are references, not things to clone.

Project P must develop its own visual language.

## 4. Core principles

### Clean

The desktop should remain calm and uncluttered.

The top bar should not become a dashboard full of permanent widgets.

### Contextual

Information should appear when it is relevant.

The system should be capable of communicating a lot without permanently displaying everything.

### Expressive

Personality should come from geometry, typography, colour, motion and interaction.

### Cohesive

Every part of the shell should look like it belongs to the same system.

### Detailed

Small details matter:

- spacing
- alignment
- typography
- icon sizing
- capsule proportions
- states
- transitions
- animation timing
- visual feedback

### Centralized

Centralize services and shared logic wherever that is sensible.

Do not create multiple independent implementations of the same system functionality.

### Modular

Centralization must not become a monolith.

Services, UI components, themes and scripts should have clear responsibilities and interfaces.

### Personal

Project P is optimized for its author.

Do not compromise design decisions simply to appeal to a generic audience.

## 5. Top-level shell concept

The shell is based around a floating capsule language.

The top bar is divided into three visual zones.

### Left zone

Two floating capsules:

1. Workspace capsule
2. Focused application capsule

The workspace capsule shows the current Hyprland workspaces.

The application capsule shows the currently focused application.

These provide context but should not dominate the desktop.

### Center zone — the notch

The center is the protagonist.

The notch contains the time as its persistent primary element.

Normal state should be extremely quiet:

`[ 22:01 ]`

When something relevant happens, the notch can expand and transform into contextual information.

Examples:

- Media
- Volume
- Bluetooth connection
- Notifications
- Other short-lived system events

The information appears, communicates its state, and gracefully returns to the minimal clock state.

The interaction model should feel like a physical transformation of the capsule rather than an unrelated popup.

### Right zone

The right side contains more persistent informational status:

- network
- battery
- audio state
- other useful indicators

It should remain restrained and not become a second dashboard.

## 6. Control Center

The notch is also the main entry point to the Control Center.

The Control Center should feel like a natural expansion of the shell rather than a collection of unrelated popups.

The current concept is three main tabs:

1. System
2. Media
3. Notifications

The exact content and navigation are intentionally not fully specified yet.

The Control Center should use:

- floating capsules
- cards
- sliders
- toggles
- media controls
- notification surfaces
- contextual information
- coherent transitions

Omarchy's system menu is a useful reference for practical functionality because it works well. Its visual identity should not be copied.

## 7. Windows

Windows should share the same design language as the shell:

- subtle rounded corners
- light transparency
- restrained blur
- coherent surfaces
- theme-aware colours

Avoid exaggerated rounding, excessive transparency or blur used purely for decoration.

## 8. Notifications

Notifications should be integrated into the capsule language.

They should not look like a completely separate desktop subsystem.

The central notch should be able to surface relevant notification information contextually, while the Control Center provides a fuller notification view.

## 9. Lock screen

The lock screen can reuse lessons learned from SwayP, especially:

- fluid entry animation
- polished password interaction
- restrained feedback
- clean typography
- deliberate motion

However, the final lock screen must be designed as a native part of Project P's visual language.

## 10. Launcher

The launcher should prioritize usefulness and reliability.

The Omarchy launcher is a useful functional reference because it is complete and practical.

Project P can borrow good interaction ideas while giving the launcher its own visual language.

Do not reinvent functionality merely for the sake of being different.

## 11. Themes

Project P uses designed themes rather than relying on constantly changing wallpaper-derived palettes.

The author prefers the harmony of curated themes.

A theme should define semantic roles such as:

- background
- surface
- elevated surface
- foreground
- muted foreground
- primary
- secondary
- accent
- success
- warning
- error

The theme engine should be centralized and consumed by every UI component.

Avoid hardcoded colours inside individual components.

Themes can have distinct personalities while sharing the same underlying design system.

## 12. Services

Use existing Linux services where appropriate.

Centralize Project P's integration layer so UI components do not independently reinvent access to:

- audio
- networking
- Bluetooth
- power
- media
- displays
- notifications
- other desktop services

The goal is not to replace mature Linux infrastructure.

The goal is to provide one coherent Project P interface over it.

## 13. Philosophy of growth

Project P should grow by adding reusable system components, not patches.

Avoid:

- giant monolithic QML files
- duplicated components
- hardcoded theme values
- plugin-specific visual systems
- random one-off scripts
- unnecessary dependencies
- duplicated service logic

Prefer:

- reusable QML components
- semantic design tokens
- centralized themes
- clear service boundaries
- small focused scripts
- explicit interfaces
- predictable configuration

## 14. Definition of success

When the desktop is running, it should not feel like:

- Omarchy with a different configuration
- SwayP
- a generic Hyprland rice
- a collection of plugins

It should feel like:

> One deliberately designed personal desktop environment.

Linux, Hyprland and Quickshell should be visible in the technology underneath, but the experience should feel like Project P.
