# Project P — Design Reference Library

This is a curated reference map for Project P.

The goal is not to copy products or collect inspiration for its own sake. Each source should help answer a concrete design question: hierarchy, interaction, motion, information density, surfaces, typography, system UI, or component architecture.

## How to use this library

When researching a new Project P surface:

1. Start with the sources tagged **Primary**.
2. Study real shipped interfaces before visual galleries.
3. Extract principles, not screenshots or visual copies.
4. Record what Project P adopts, adapts, and rejects.
5. Prefer a small number of strong references over an endless inspiration feed.

---

## 1. Real product UI & pattern research

### Mobbin — Primary
https://mobbin.com/

**Use for:** real shipped mobile/web interfaces, flows, UI patterns, settings, notifications, sliders, navigation and information hierarchy.

**Why it matters to Project P:** Project P is a desktop shell, but many of its interaction problems are closer to a product UI than to a traditional Linux panel.

**Study:** compact controls, settings flows, contextual surfaces, media controls, notification hierarchy.

**Do not copy:** mobile layouts literally. Desktop spatial constraints are different.

---

### Page Flows / former Screenlane — Secondary
https://pageflows.com/

**Use for:** user flows and real interface patterns.

**Why it matters:** useful for studying how an interaction evolves through states rather than looking at isolated screenshots.

**Study:** state transitions, onboarding, settings, confirmation, error and empty states.

**Note:** Screenlane was merged into Page Flows in 2024, so Page Flows is the current destination.

---

## 2. Visual exploration

### Godly — Secondary
https://godly.design/

**Use for:** highly curated web/app/visual design.

**Why it matters:** useful for discovering strong composition, typography, motion and visual hierarchy.

**Study:** restraint, type scale, composition, transitions, unusual but coherent visual systems.

**Do not copy:** flashy web interactions that have no value in a desktop shell.

---

### Dribbble — Tertiary
https://dribbble.com/

**Use for:** visual exploration and early concepts.

**Why it matters:** good for generating alternatives when a component feels visually unresolved.

**Risk:** Dribbble contains a lot of concept-only UI. Treat it as visual exploration, not proof of good UX.

---

### Behance — Tertiary
https://www.behance.net/

**Use for:** complete visual identities and larger product/design projects.

**Study:** how typography, color, iconography, motion and layout form one visual language.

**Risk:** many projects are presentation pieces rather than real products.

---

## 3. Design systems & component thinking

### Figma Community — Primary
https://www.figma.com/community/

**Use for:** UI kits, design systems, component libraries and real design resources.

Figma's UI kits expose reusable components, styles, variables and example screens. Use them to study how systems are structured rather than to copy their appearance.

**Study:** component variants, semantic tokens, spacing scales, states, naming and documentation.

---

### Figma Design Systems — Primary
https://www.figma.com/design-systems/

**Use for:** system-level thinking.

**Project P lesson:** components and tokens should be designed as a system, not as isolated QML objects.

---

### Figma Design System Examples — Secondary
https://www.figma.com/resource-library/design-system-examples/

**Use for:** comparing mature design-system structures.

**Study:** tokens, components, patterns and documentation.

---

## 4. Platform references

### Android / Material 3 Expressive — Primary
https://developer.android.com/develop/ui/compose/designsystems/material3

https://design.google/library/expressive-material-design-google-research

**Use for:** expressive system UI, responsive components, motion, typography, color and containment.

**Project P adopts:** expressive interaction, meaningful motion, strong hierarchy, contextual information and coherent semantic tokens.

**Project P rejects:** becoming Material Design for Linux.

Material 3 Expressive is a reference for principles, not the visual identity of Project P.

---

### Android Material You — Secondary
https://source.android.com/docs/core/display/material

**Use for:** personalization, system-wide theming and semantic color thinking.

**Project P difference:** Project P prefers curated harmonious themes over wallpaper-derived dynamic color as its primary visual mechanism.

---

### Apple Human Interface Guidelines — Primary
https://developer.apple.com/design/human-interface-guidelines/

**Use for:** hierarchy, adaptive layouts, system surfaces, safe areas and interaction consistency.

**Project P adopts:** contextual presentation and careful spatial hierarchy.

**Project P rejects:** Apple visual language as a target.

---

### Apple Live Activities / Dynamic Island — Primary
https://developer.apple.com/design/human-interface-guidelines/live-activities

**Use for:** the conceptual model behind Project P's dynamic notch.

**Study:** compact, minimal and expanded states; contextual information; transitions between states.

**Project P difference:** the notch is Project P's own shell primitive and should not visually imitate Dynamic Island.

---

### Nothing
https://nothing.tech/

**Use for:** visual inspiration.

**Why it matters:** Nothing OS is one of Project P's strongest aesthetic references: industrial, restrained, expressive and highly branded.

**Project P adopts:** industrial character, strong typography, restraint and confidence.

**Project P rejects:** direct imitation of Nothing's glyphs, layouts, icons or branding.

---

## 5. Product interfaces worth studying

### Linear
https://linear.app/

**Use for:** hierarchy, density, keyboard-first interaction, command surfaces and product polish.

**Study:** information density without visual noise, predictable hierarchy and fast interaction.

---

### Raycast — Primary
https://www.raycast.com/

**Use for:** launcher/search surfaces, command interaction, compact lists, keyboard-first UX and responsive feedback.

Raycast's UI model is explicitly component-oriented and optimized for fast interaction.

**Study:** list/detail relationships, action panels, loading states, keyboard-first navigation.

---

## 6. Linux desktop & shell references

### Omarchy — Primary functional reference
https://omarchy.org/

**Use for:** shell architecture, desktop integration, workflow and practical system UX.

Omarchy is an Arch/Hyprland/Quickshell desktop system with a strong opinionated workflow.

**Project P adopts:** the idea that a Linux desktop can be a coherent product rather than a collection of packages.

**Project P rejects:** Omarchy's visual identity, TUI-heavy philosophy and one-to-one UI replication.

---

### Quickshell
https://quickshell.org/

**Use for:** technical implementation of shell UI.

**Study:** how Quickshell can expose reusable shell components and interact with system services.

**Project P rule:** Quickshell is the implementation substrate, not the design language.

---

### Hyprland
https://hyprland.org/

**Use for:** compositor capabilities and system interaction.

**Study:** IPC, workspace state, window rules, animations and compositor-level integration.

**Project P rule:** use Hyprland as infrastructure; Project P should own the experience above it.

---

## 7. Linux shell projects for implementation research

These are implementation references, not visual targets:

- Quickshell projects
- DankMaterialShell
- Caelestia
- AGS / Astal
- Waybar

**Use them to study:** service abstractions, IPC, shell organization, reusable widgets, notification systems, media integration, power/network/audio integration.

**Do not use them as a reason to reproduce another rice.**

---

# Reference hierarchy

When references conflict, use this priority:

1. Project P principles and design system
2. Real product UX patterns
3. Platform HIG/design-system principles
4. Project P's chosen visual identity
5. Linux implementation references
6. Visual galleries

The project should never change direction merely because a gallery contains something fashionable.

---

# Core research questions

Whenever a new Project P component is designed, ask:

- What information matters first?
- What can remain hidden until relevant?
- What is the component's compact state?
- What is its expanded state?
- How does it transition between states?
- What is the semantic surface hierarchy?
- Which token controls its appearance?
- How does it behave with keyboard interaction?
- What happens when information is unavailable?
- Does it still look coherent in every Project P theme?
- Is the interaction useful, or merely decorative?

---

# Anti-reference list

Project P should avoid drifting toward:

- generic Linux rice aesthetics
- giant rounded cards everywhere
- excessive glassmorphism
- permanent status-bar clutter
- random gradients
- wallpaper-derived colors as the default identity
- TUI aesthetics in graphical shell surfaces
- copying Nothing OS
- copying Apple's Dynamic Island
- copying Material Design
- copying Omarchy
- one-off components with hardcoded colors
