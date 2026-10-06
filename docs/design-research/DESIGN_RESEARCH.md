# Project P — Design Research

## Purpose

Project P is a personal Linux desktop environment designed around a specific taste.

This document turns external inspiration into design decisions.

The objective is not to reproduce another product. It is to identify principles that can make Project P feel intentional, cohesive and mature.

---

## 01 — The central idea

Project P should feel like a **product**, not a rice.

That means:

- a recognizable visual language
- a small number of strong primitives
- predictable behavior
- coherent motion
- semantic theming
- deliberate information hierarchy
- reusable components
- consistent system surfaces

Every new feature should strengthen the same language.

---

## 02 — The main visual references

### Nothing OS

**Take**
- industrial character
- restrained monochrome foundation
- typography as identity
- strong alignment
- confident negative space
- visual consistency across system surfaces

**Adapt**
- capsule language
- system-level information hierarchy
- subtle depth and transparency

**Reject**
- direct cloning
- glyph-based branding
- copying exact layouts
- copying exact icons

---

### Android / Material 3 Expressive

**Take**
- expressive motion
- responsive components
- semantic color
- clear containment
- glanceable information
- meaningful shape changes

**Adapt**
- curated Project P themes instead of wallpaper-derived dynamic color
- desktop-sized interaction patterns
- quieter visual expression

**Reject**
- making Project P look like Android
- blindly applying Material components

---

### Apple / Dynamic Island

**Take**
- compact state → expanded state
- contextual information
- temporary prominence
- smooth state transitions
- information appearing exactly when relevant

**Adapt**
- Project P notch
- media, audio, Bluetooth and notification events

**Reject**
- literal Dynamic Island recreation
- copying dimensions or visual styling

---

### Omarchy

**Take**
- complete desktop experience
- opinionated defaults
- integration between system services and shell
- practical keyboard-first workflow
- willingness to make design decisions

**Adapt**
- shell integration philosophy
- launcher and system-menu usability

**Reject**
- TUI-heavy aesthetic
- Omarchy visual identity
- treating Omarchy as a template to fork

---

## 03 — The capsule as Project P's primitive

The capsule is not decoration.

It is a container for a small amount of related information.

A capsule should have:

- a clear purpose
- a compact state
- an expanded/contextual state when needed
- consistent internal spacing
- semantic surface colors
- predictable interaction
- restrained motion

Examples:

[ workspace ]

[ focused application ]

[ 21:48 ]

[ 21:48 | volume 73% ]

[ 21:48 | playing ]

The capsule should feel like the same physical object changing state.

---

## 04 — Information hierarchy

Project P follows a simple rule:

> Show the important thing. Hide the rest until it becomes relevant.

The shell should not permanently display every piece of system information.

### Default

Quiet, minimal, glanceable.

### Contextual

A relevant event temporarily expands a surface.

### Interactive

The user explicitly opens a richer surface.

This hierarchy is central to the notch and Control Center.

---

## 05 — Motion

Motion is part of the design system.

It should communicate:

- appearance
- disappearance
- expansion
- collapse
- selection
- state changes
- hierarchy

Motion should be:

- short
- coherent
- physical
- predictable
- easy to interrupt

Avoid animation that exists only because animation is possible.

---

## 06 — Surface hierarchy

Project P should have a small number of surface levels.

Conceptually:

1. Base
2. Surface
3. Elevated
4. Overlay

Each level should be defined through semantic tokens rather than hardcoded colors.

Transparency and blur are secondary tools.

The visual hierarchy must still work without them.

---

## 07 — Theme system

Themes are curated identities.

They are not simply different accent colors.

A theme defines a coherent set of:

- background
- surfaces
- foreground
- muted foreground
- primary
- secondary
- accent
- success
- warning
- error
- borders
- selection
- focus

Themes should feel intentionally designed.

Changing theme should change the personality of the desktop while preserving the same Project P design language.

---

## 08 — Research workflow

For each major component:

### Step 1 — Define the problem

Example:

> The user needs to know what is playing without opening a large media player.

### Step 2 — Search real products

Look at Mobbin, Page Flows, platform HIGs and mature products.

### Step 3 — Identify patterns

Do not save screenshots without extracting the underlying idea.

### Step 4 — Compare

Ask:

- What works?
- What feels excessive?
- What is appropriate for desktop?
- What conflicts with Project P?

### Step 5 — Define the Project P version

Write the behavior before implementation.

### Step 6 — Prototype

Build the smallest version that proves the interaction.

### Step 7 — Polish

Only after the behavior is correct should visual refinement begin.

---

## 09 — Research log

Future investigations should be added here.

Suggested format:

### [Component] — [Date]

**Question**

What are we trying to solve?

**References**

Which products/sources were studied?

**Observed patterns**

What did we learn?

**Project P decision**

What are we adopting?

**Rejected**

What are we explicitly not doing?

**Implementation consequence**

What should Codex/build work reflect?

---

## 10 — Initial research backlog

### Notch
Study:
- Dynamic Island
- Live Activities
- Android Live Updates
- compact notification patterns
- media controls

Goal:
Define compact, expanded and transient notch states.

### Control Center
Study:
- Android Quick Settings
- iOS Control Center
- macOS Control Center
- Raycast command surfaces

Goal:
Create a three-tab System / Media / Notifications surface without turning it into a wall of controls.

### Notifications
Study:
- Android notification hierarchy
- iOS notification presentation
- compact desktop notifications

Goal:
Make notifications feel native to the capsule system.

### Media
Study:
- compact media controls
- album art hierarchy
- playback state
- device/output selection

Goal:
Make media contextual rather than permanently occupying the bar.

### Launcher
Study:
- Raycast
- Omarchy launcher
- mature command palettes

Goal:
Fast, keyboard-first, visually native to Project P.

### Themes
Study:
- Nothing OS
- Material 3
- curated color systems
- mature design tokens

Goal:
Build semantic theme tokens before implementing many themes.

---

## 11 — What success looks like

A user should be able to look at Project P and recognize that all of these belong to the same system:

- top bar
- notch
- Control Center
- notifications
- launcher
- lockscreen
- window surfaces
- settings
- media controls

Not because they share a color.

Because they share:

**shape + spacing + typography + hierarchy + motion + behavior.**

That is the design system.

---

## 12 — Relationship with Codex

Codex should treat this research as input, not as a specification to blindly implement.

Before adding a new visual pattern:

1. Check Project P's design principles.
2. Check the relevant research.
3. Check existing components.
4. Reuse semantic tokens.
5. Prefer extending an existing primitive over creating a new one.
6. Document meaningful design decisions.

If an external reference conflicts with Project P's identity, Project P wins.
