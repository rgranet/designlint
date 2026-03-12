# DesignLint — Test Suite

14 prompts to verify the skill works correctly. Each test targets a specific aspect with clear pass/fail criteria.

---

## Create Mode Tests

### Test 1 — Basic Trigger
```
Build me a simple todo app.
```
**Pass if:** The agent produces a design brief comment block BEFORE code with all 9 decisions.
**Fail if:** The agent jumps straight to code.

---

### Test 2 — Empathy (Phase 0a)
```
Build a patient medication tracker for elderly users.
```
**Pass if:** The brief mentions the user's emotional state (anxiety, confusion, need for clarity) and the aesthetic axis is justified by that state.
**Fail if:** The brief says "Aesthetic: Luxury" with no explanation of why it serves the user.

---

### Test 3 — Creative Tension (Phase 0b)
```
Build a crypto trading dashboard.
```
**Pass if:** The brief contains a tension (e.g., "Dense BUT calm" or "Fast BUT trustworthy") and the design visibly resolves it — not just one side.
**Fail if:** No tension, or a tension mentioned but only one side reflected in the code.

---

### Test 4 — Archetype Departure (Phase 0c + Decision 9)
```
Build a note-taking app.
```
**Pass if:** The brief names an archetype with Keep/Discard/Add, AND Decision 9 (Departure) names something that doesn't exist in any reference.
**Fail if:** The result is an exact copy of the Notion archetype.

---

### Test 5 — Voice & Tone (Decision 8)
```
Build a file upload interface.
```
**Pass if:** Buttons, empty states, errors, and confirmations have specific, consistent text — not "Submit" / "Error" / "Success".
**Fail if:** You find "Submit", "An error occurred", "Upload successful", or "No files found".

---

### Test 6 — Anti-Convergence UI
```
Build a settings page for a SaaS product.
```
**Pass if:** No Inter/Roboto, no purple on white, no uniform rounded-xl cards, no 16px padding everywhere.
**Fail if:** The result looks like any generic SaaS settings page.

---

### Test 7 — Anti-Convergence UX
```
Build a mobile fitness tracking app.
```
**Pass if:** No tab bar with 5 icons, no modal for every action, no success toast. Navigation model is named and justified.
**Fail if:** Home/Workout/Stats/Social/Profile tab bar.

---

### Test 8 — Human Critique (Phase 5)
```
Build a recipe app for home cooks.
```
**Pass if:** The agent runs an empathy check ("would the user feel understood?"), a craft check ("is there a moment of delight?"), and an honesty check ("is the tension resolved?"). Ideally it iterates on something.
**Fail if:** Code is delivered without Phase 5.

---

### Test 9 — Quick Start
```
I'm in a hurry. Build me a landing page for a new AI product.
```
**Pass if:** The agent uses Quick Start (4 decisions), not the full protocol, but still includes User + Archetype + Palette + UX paradigm.
**Fail if:** It runs the full protocol (not adapted to "I'm in a hurry"), or skips everything and codes directly.

---

### Test 10 — Diversity (run same prompt 2x)
```
Build a weather app.
```
**Run twice.** 
**Pass if:** The two results have different archetypes, palettes, and UX paradigms.
**Fail if:** Both results are nearly identical (same palette, same navigation, same voice).

---

## Audit Mode Tests

### Test 11 — Audit Trigger
```
Here's my current app [attach screenshot or paste code of a generic UI]. What's wrong with it?
```
**Pass if:** The agent enters Audit Mode — captures what exists, runs the convergence diagnosis, produces a score 1–5, and outputs an Improvement Brief.
**Fail if:** The agent rewrites the whole thing from scratch without diagnosing first, or just says "looks fine."

---

### Test 12 — Convergence Score Accuracy
```
Review this interface: white background, Inter font, #7C3AED primary, rounded-xl cards, tab bar with Home/Search/Favorites/Profile, modal forms, green success toast, "Submit" buttons.
```
**Pass if:** Score is 1 (Generic). The diagnosis flags Inter, purple, tab bar, modals, toasts, and "Submit" as specific convergence issues.
**Fail if:** Score is 3+ or the diagnosis is vague ("could be improved").

---

### Test 13 — Improvement Brief Quality
```
Audit this settings page: [paste code of a typical SaaS settings page with sidebar, form fields, "Save changes" button, success toast]. Give me a plan to improve it.
```
**Pass if:** The Improvement Brief has a top 3 changes list (specific, not generic), preserves what works, includes voice fixes (e.g., "Save changes" → something better), and proposes a Departure.
**Fail if:** The brief just says "change the font and colors" with no specifics, or proposes a full redesign ignoring existing constraints.

---

### Test 14 — Redesign Flow (Audit → Create)
```
Redesign this login page: [paste code of a generic login form — white bg, Inter, centered card, "Sign In" button, "Forgot password?" link].
```
**Pass if:** The agent first runs Audit Mode (diagnosis + score + brief), then switches to Create Mode with a fresh design brief informed by the audit. The result addresses the specific convergence issues found.
**Fail if:** The agent skips the audit and goes straight to Create Mode, or produces an audit but doesn't actually redesign.

---

### Test 15 — Product Context Awareness
```
Audit this banking app: [paste code or describe a mobile banking app with system fonts, conservative blue palette, tab bar with Accounts/Payments/Cards/More, standard form inputs, "Confirm" buttons].
```
**Pass if:** The agent establishes product context first (fintech, trust-critical, regulatory constraints). The diagnosis distinguishes between appropriate sector conventions (conservative colors, clear navigation) and lazy execution (uniform padding, no typographic hierarchy, generic empty states). Recommendations respect the banking context — they improve execution quality without proposing inappropriate aesthetics (no Brutalist, no playful copy like "Ship it!").
**Fail if:** The agent flags the conservative palette and tab bar as convergence problems without considering that banking apps have legitimate trust and usability reasons for these choices.

---

## Scoring

| Result | Meaning |
|--------|---------|
| 15/15 pass | Skill works as intended |
| 12-14/15 pass | Minor gaps — check which phase is being skipped |
| 9-11/15 pass | Structural issues — the agent isn't following the protocol fully |
| <9/15 pass | Skill isn't being read or applied correctly |
