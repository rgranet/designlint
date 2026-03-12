# DesignLint — Design Decision Protocol

> Source: DesignLint v1.1 by Ruben Granet

## When This Applies

Whenever you are asked to build, design, create, or modify any user interface — including web apps, landing pages, dashboards, iOS/SwiftUI screens, Android/Compose screens, React Native apps, or any UI component.

## What To Do

**STOP before writing UI code.** Complete the Design Decision Protocol first.

### Step 1 — Read References

- Read `designlint/SKILL.md` for the full protocol.
- Read `designlint/references/archetypes.md` to select a design archetype.
- Read `designlint/references/ux.md` to select a UX paradigm.
- Read the platform-specific reference file:
  - Web → `designlint/references/web.md`
  - iOS → `designlint/references/ios.md`
  - Android → `designlint/references/compose.md`
  - React Native → `designlint/references/react-native.md`
  - Dashboards → `designlint/references/dashboards.md`

### Step 2 — Make 7 Decisions

Document these in a comment block at the top of your code:

1. **Aesthetic Axis** — Mood + treatment (e.g., Industrial-Editorial)
2. **Typography** — Display + body font (NOT Inter, Roboto, Arial, system-ui, Poppins, Space Grotesk)
3. **Color System** — 5 tokens: bg / surface / primary / accent / text (NOT purple gradients, NOT default blues)
4. **Spatial Grammar** — Asymmetric / Breathing room / Dense / Editorial bleed / Layered / Off-grid
5. **Motion Character** — Snappy / Elastic / Cinematic / Mechanical / Playful / None
6. **Signature Detail** — One unexpected, memorable element
7. **UX Paradigm** — Navigation, interaction, data entry, feedback, and onboarding models

### Step 3 — Write Code

Only after documenting all 7 decisions.

### Step 4 — Audit Before Delivering

Verify:
- No Inter/Roboto as primary font
- No purple/blue gradient on white backgrounds
- No tab bar with 5 generic icons as the only navigation
- No modal for every secondary action
- No global toasts for success/error feedback
- No 3-screen onboarding carousel
- WCAG AA contrast ratios met (4.5:1 body text, 3:1 large text)
- If you stripped all styling, would the UX still feel distinct?

Fix any failures before delivering.

## Quick Start (Express Mode)

If the task is small or time-constrained, make 3 decisions minimum:
1. Pick an archetype from `designlint/references/archetypes.md`
2. Pick a palette from the Palette Library in the same file
3. Pick a UX paradigm from `designlint/references/ux.md`

Document as: `/* Quick DDP: Archetype=[X] | Palette=[Y] | UX=[Z] */`
