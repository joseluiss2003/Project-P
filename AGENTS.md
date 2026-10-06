# AGENTS.md — Project P

## Role

You are working on Project P, a personal Hyprland desktop environment built with Quickshell.

The repository is a design-led personal project.

## Before changing code

Always read:

- PROJECT.md
- DESIGN.md
- ARCHITECTURE.md
- ROADMAP.md

Then inspect the existing repository and relevant environment before making architectural changes.

## Core rule

Do not implement the entire project at once.

Follow the roadmap.

The visual foundation must be validated before large amounts of functionality are added.

## Design rules

Project P uses:

- floating capsules
- industrial-inspired geometry
- modern Android interaction patterns
- Nothing OS 4 as a major visual reference
- contextual information
- subtle transparency
- restrained blur
- curated themes
- purposeful motion

Do not introduce a visual style that conflicts with the design system.

## References

Nothing OS, Android, Apple Dynamic Island and Omarchy are references for ideas and interaction patterns.

Do not clone their branding, exact UI, or visual identity.

Project P must remain its own design.

## Architecture rules

Prefer:

- reusable QML components
- semantic design tokens
- centralized theme definitions
- centralized service integrations
- small focused scripts
- clear module boundaries
- explicit interfaces
- predictable configuration

Avoid:

- hardcoded colours
- duplicated service logic
- duplicated UI components
- giant monolithic QML files
- one-off scripts that recreate existing services
- unnecessary dependencies
- plugin-specific design systems

## Services

Use mature Linux services underneath Project P where appropriate.

Do not reinvent:

- PipeWire
- NetworkManager
- BlueZ
- MPRIS
- UPower
- Hyprland IPC

Instead, create a coherent Project P integration layer.

## UI

The shell should feel like one system.

New components must reuse existing design primitives whenever possible.

If a component needs a new visual primitive, consider whether that primitive belongs in the shared design system.

## Themes

Never hardcode raw theme colours into individual UI components.

Use semantic theme tokens.

## Motion

Motion should communicate state and hierarchy.

Avoid animation for decoration alone.

Keep interactions responsive.

## Working style

Before a significant implementation:

1. Inspect.
2. Explain the proposed approach.
3. Check existing components for reuse.
4. Implement the smallest coherent step.
5. Test it.
6. Review for duplication and architectural drift.

When uncertain about a design decision, prefer the principles in DESIGN.md and the current project vision rather than inventing a new style.

## Important

Project P is personal.

Do not optimize decisions for hypothetical users, broad distribution, or compatibility requirements that the project does not need.

The objective is a polished personal desktop environment.
