# DesignLint — Marketing Content

---

## Tweet (standalone)

Every AI-generated UI looks the same. Inter. Purple gradient. Tab bar. "Submit."

I built DesignLint — an open-source skill that forces AI agents to understand the user, make 9 design decisions, and critique the result before writing code.

Now with Audit Mode: paste your existing UI and get a convergence score + improvement plan.

Works with Claude Code, Cursor, Codex.

github.com/rgranet/designlint

#DesignLint #AI #UIDesign #UXDesign #OpenSource #ClaudeCode #Cursor #Codex #BuildInPublic #IndieHacker #WebDev #SwiftUI #ReactJS #FrontendDev #JetpackCompose

---

## Thread X (9 tweets)

---

🧵 1/9

I got tired of every AI-generated UI looking the same.

Inter font. Purple gradient. White bg. Tab bar with 5 icons. "Submit" button. Green toast.

So I built DesignLint — an open-source protocol that forces AI agents to design like humans.

Two modes: Create from scratch. Audit what exists.

Here's how it works 👇

---

2/9

The root cause: AI agents skip the design brief.

A human designer never opens Figma without knowing:
— Who is the user?
— How do they feel?
— What should this look and feel like?

AI agents go straight to their statistical defaults. DesignLint blocks that.

#UIDesign #UXDesign #AI

---

3/9 — CREATE MODE

Phase 0: Understand before you design.

Before any aesthetic choice, the agent must answer:

→ "Who is this person, and what's their emotional state?"
→ Pick a creative tension: "Dense BUT calm" or "Technical BUT warm"
→ Choose an archetype as a DEPARTURE POINT — not a template to copy

#DesignLint #BuildInPublic

---

4/9

Phase 1: 9 mandatory decisions.

1. Aesthetic axis (justified by the user)
2. Typography (Inter/Roboto = banned)
3. Color system (purple gradients = banned)
4. Spatial grammar
5. Motion character
6. Signature detail
7. UX paradigm
8. Voice & tone (no more "Submit" / "An error occurred")
9. The Departure — something you INVENTED, not copied

---

5/9

The Departure is the key decision.

The agent must name ONE thing in the design that doesn't exist in any archetype or reference.

If it can't — it's reproducing, not designing.

This is what separates "anti-generic" from "actually human."

#IndieHacker #OpenSource

---

6/9 — AUDIT MODE (new)

Already have a UI? Paste the code or screenshot.

DesignLint runs the full convergence scan:

→ UI scan (fonts, colors, layout, components, motion)
→ UX scan (navigation, actions, feedback, empty states)
→ Human scan (empathy, voice, tension, memorability)

Then scores it 1–5: Generic → Human.

---

7/9

The Improvement Brief:

→ Top 3 highest-impact changes (specific, not "make it better")
→ Targeted UI/UX/voice fixes
→ One Departure — an original idea that transforms "fixed" into "distinctive"

Ask the agent to execute, and it rebuilds using the brief as the design brief.

#FrontendDev #WebDev #ClaudeCode

---

8/9

Before DesignLint:
→ Inter · #7C3AED · tab bar · "Submit" · "No items found"

After:
→ Cormorant Garamond · Chalk & Ink palette · Today-First nav
→ CTA = "Done" · Empty = "A clear day — nice."
→ Priority = font-weight, not color badges

Same prompt. Completely different result.

---

9/9

DesignLint works with:
✅ Claude Code (native .skill)
✅ Cursor (.cursorrules)
✅ OpenAI Codex (AGENTS.md)

Covers Web, iOS, Android, React Native, dashboards.

Two modes: Create + Audit.
MIT licensed. Feedback welcome.

github.com/rgranet/designlint

#DesignLint #AI #UIDesign #UXDesign #OpenSource #ClaudeCode #Cursor #Codex #BuildInPublic #IndieHacker #WebDev #SwiftUI #ReactJS #FrontendDev #JetpackCompose

---

## Reddit Post

### Subreddits: r/webdev, r/reactjs, r/SwiftUI, r/programming, r/sideproject

**Title:** I built an open-source skill that stops AI agents from generating the same UI every time — now with an Audit Mode to fix existing interfaces

**Body:**

If you've used Claude Code, Cursor, or Codex to build UI, you've seen the pattern: Inter font, purple gradient, white background, tab bar with 5 icons, modal for everything, "Submit" button, green success toast. Every time.

The root cause isn't the model — it's the lack of a design brief. A human designer never starts coding without deciding who the user is, what the product should feel like, and what makes it different. AI agents skip all of that and go straight to their statistical defaults.

I built **DesignLint** to fix this. It's an open-source skill/ruleset that works in two modes:

**Create Mode** — intercepts the agent before it writes code:

- **Phase 0**: Who is the user and what are they feeling? What's the creative tension? (e.g., "Dense BUT calm") Pick an archetype as a starting point, not a template — and name what you'd keep, discard, and add.
- **Phase 1**: 9 explicit decisions — aesthetic axis, typography, color system, spatial grammar, motion, signature detail, UX paradigm, voice & tone, and a "departure" (something you invented that isn't in any reference).
- **Phase 4**: Anti-convergence audit — no Inter, no purple gradients, no tab bar with 5 generic icons, no "Submit", no "An error occurred".
- **Phase 5**: Human critique — would the user feel understood? Is there a moment of delight? Is the creative tension actually resolved? If anything is flat — iterate.

**Audit Mode** (new) — review and fix existing interfaces:

- Paste your code or describe your current UI
- The agent documents what exists, then runs the full convergence scan: UI (fonts, colors, layout), UX (navigation, feedback, empty states), and Human (empathy, voice, memorability)
- Scores the design 1–5 (Generic → Safe → Adequate → Distinctive → Human)
- Produces a targeted Improvement Brief: top 3 high-impact changes, specific UI/UX/voice fixes, and one "Departure" — an original idea that elevates the design beyond "fixed" to "distinctive"
- If you ask it to execute, it rebuilds using the brief

The result isn't just "different from the default" — it's design that feels like a human made it.

It works with Claude Code (native .skill), Cursor (.cursorrules), and OpenAI Codex (AGENTS.md). Drop the files in your project and the agent picks it up automatically.

Covers Web (React/Next.js), iOS (SwiftUI), Android (Jetpack Compose), React Native, and dashboards. MIT licensed.

**GitHub**: https://github.com/rgranet/designlint

Would love feedback — especially from anyone who's tried the Audit Mode on their existing projects.
