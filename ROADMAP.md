# Project P — Roadmap

The roadmap is deliberately phased. Do not skip the visual foundation simply to add more system integrations.

## Phase 0 — Discovery

- Inspect the repository
- Inspect the current Hyprland / Quickshell environment
- Identify reusable infrastructure
- Identify things to discard
- Audit dependencies
- Propose final architecture
- Validate design direction

**No major implementation yet.**

## Phase 1 — Design system

Establish:

- semantic design tokens
- theme structure
- typography
- spacing
- geometry
- capsule primitive
- surface hierarchy
- animation primitives

Deliverable:

A small reusable visual component foundation.

## Phase 2 — Top bar prototype

Build only:

- workspace capsule
- focused application capsule
- central notch
- clock
- right-side status area

Focus heavily on:

- proportions
- spacing
- capsule geometry
- visual hierarchy
- animation quality

The prototype should look convincing before adding complex functionality.

## Phase 3 — Dynamic notch

Implement contextual states:

- idle clock
- media
- volume
- Bluetooth/device connection
- notification
- return to idle

Focus on smooth expansion, transformation and collapse.

## Phase 4 — Control Center

Build the three-tab foundation:

- System
- Media
- Notifications

Start with mocked or minimal data if necessary.

Prioritize navigation and visual hierarchy before full service integration.

## Phase 5 — Service integration

Centralize integrations for:

- audio
- networking
- Bluetooth
- media
- power
- display
- notifications

Avoid duplicated implementations.

## Phase 6 — System surfaces

Build/refine:

- lock screen
- launcher
- session/power menu
- notification system
- media controls

## Phase 7 — Theme system

Create the first polished curated themes.

Themes should share the same component system while having distinct personalities.

## Phase 8 — Polish

Audit:

- spacing
- typography
- animation timing
- focus states
- hover states
- active states
- transitions
- edge cases
- service failures
- reload/restart behaviour

## Phase 9 — Packaging and maintenance

Only once the experience is stable:

- installation
- update mechanism
- configuration handling
- diagnostics
- documentation

## Current priority

**Do not jump ahead.**

The immediate target is:

> Design system → capsule → notch → top bar prototype.

If that foundation feels right, the rest of Project P can grow around it.
