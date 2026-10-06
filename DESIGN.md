# Project P — Design System Direction

## Design DNA

Project P's visual language is built around:

1. Floating capsules
2. Industrial geometry
3. Modern Android interaction patterns
4. Nothing OS 4-inspired restraint and expressiveness
5. Contextual information
6. Subtle depth
7. Designed colour themes
8. Smooth, purposeful motion
9. Strong hierarchy
10. Careful spacing

## 1. Capsule language

Capsules are one of the defining visual primitives of Project P.

They should feel:

- compact
- physical
- floating
- intentional
- slightly rounded rather than excessively pill-shaped

The provided visual reference image represents the desired general physical feel and proportions.

Reference:

`docs/references/capsule-reference.png`

The reference is inspiration only. Do not copy its branding, exact UI or implementation.

## 2. Bar composition

The top bar should not look like a traditional Linux panel.

It should be composed of visually separated floating groups.

Conceptually:

`[ workspaces ] [ focused app ]              [ clock/notch ]              [ status ]`

The center has the strongest visual hierarchy.

### Left

Workspace capsule:

- compact
- active workspace clearly visible
- subtle transition when changing workspace

Focused application capsule:

- shows the current application
- smoothly resizes when the application changes
- remains visually subordinate to the center

### Center

The notch is the visual protagonist.

Default state:

`[ 21:48 ]`

It should be possible for the notch to temporarily transform into:

- media information
- volume
- device connection
- notification
- other relevant context

The transition should feel like the same object changing state.

### Right

Persistent status information can live here.

Examples:

- Wi-Fi
- battery
- audio
- other useful indicators

Keep it restrained.

## 3. Contextual information

The system should follow this principle:

> Show a lot without constantly displaying a lot.

Examples:

Clock:

`[ 21:48 ]`

Volume event:

`[ 21:48  |  🔊 73% ]`

Media event:

`[ 21:48  |  ♫ After Dark ]`

Bluetooth event:

`[ 21:48  |  ● WH-1000XM5 ]`

After the relevant state has been communicated, the notch can gracefully return to the clock.

## 4. Control Center

The Control Center should feel like a larger, richer expression of the same capsule language.

Current conceptual tabs:

- System
- Media
- Notifications

It should contain appropriate:

- capsules
- cards
- sliders
- toggles
- device selectors
- media controls
- notification groups

The Control Center should have strong hierarchy and avoid becoming a wall of controls.

## 5. Windows

Window language:

- subtle rounded corners
- restrained transparency
- restrained blur
- coherent surface hierarchy
- theme-aware colours

The visual effect should feel refined rather than glassmorphic for its own sake.

## 6. Notifications

Notifications should visually belong to the same system.

They should use the same:

- typography
- spacing
- surfaces
- capsule/card geometry
- semantic colours
- motion principles

The notch can provide short contextual notification feedback.

The Control Center provides the full notification experience.

## 7. Lock screen

The lock screen should use the Project P design language while improving on the lessons learned from SwayP.

Prioritize:

- polished entry
- fluid feedback
- restrained motion
- clean password interaction
- clear hierarchy

## 8. Launcher

The launcher should prioritize usefulness.

Visual direction:

- fast
- clean
- capsule/card language
- strong search hierarchy
- coherent theme integration

Use proven launcher interaction patterns where appropriate.

## 9. Colour

Project P should not be based on mandatory wallpaper-generated dynamic colour.

Curated themes are the primary colour system.

Themes should be harmonious and intentionally designed.

The design system should use semantic roles instead of component-specific colours.

Example roles:

`background`
`surface`
`surfaceElevated`
`foreground`
`foregroundMuted`
`primary`
`secondary`
`accent`
`success`
`warning`
`error`

The visual language can use colour more expressively than a strictly monochrome system, but neutral surfaces and clear hierarchy should remain foundational.

## 10. Typography

Typography should be treated as a major design element.

It must be:

- highly legible
- consistent
- hierarchical
- appropriately weighted
- integrated with capsule geometry

Do not choose typography merely because it is trendy.

## 11. Motion

Motion is part of the design system.

Prioritize:

- notch expansion
- notch collapse
- capsule resizing
- workspace transitions
- focused application changes
- notification arrival
- notification dismissal
- media state changes
- toggle changes
- slider interaction
- Control Center navigation

Motion should be:

- smooth
- fast enough to feel responsive
- visually connected to the source element
- consistent across components

Avoid:

- excessive bounce
- gratuitous animation
- inconsistent easing
- animations that delay normal interaction

## 12. Visual hierarchy

Hierarchy should generally follow:

1. Current context / important event
2. Primary system state
3. Secondary status
4. Supporting information

The central notch should remain the strongest element of the top bar.

## 13. What Project P should avoid

Do not drift into:

- TUI aesthetics
- generic Linux rice aesthetics
- excessive glassmorphism
- giant rounded cards
- permanent widget clutter
- excessive colour everywhere
- dynamic palette noise
- copying Nothing OS literally
- copying Apple's Dynamic Island literally
- copying Omarchy's visual identity

Use references to understand principles, not to reproduce products.
