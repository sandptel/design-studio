# Evolve

This mode runs only when the user asks for it ("evolve", "improve it", "what next", "suggest features"). It proposes changes first and builds only what the user picks.

## 1. Audit

- Read `DESIGN.md` (brief, decisions, tasks) and `taste.md`.
- Take screenshots of the main screens and score them with RUBRIC.md.
- Look for: rubric items below 2, decisions that were never applied everywhere, states still missing, friction on the primary action, and features the brief's user would plausibly need next.

## 2. Propose (3–5 items, ranked by impact on the success signal)

Write each one as a single line:

```
[polish|feature] <title>: <why it moves the success signal> · tier S/M · <experts it needs>
```

Mix polish items and new features. At least one item should be a new feature idea that comes from the user's job, not from a generic feature list.

## 3. Pick and build

Ask the user with AskUserQuestion (multiSelect) which ones to build. Each picked item goes through its tier's normal flow (S: build directly; M: one feature round, then BUILD.md). Afterwards, apply SKILL.md §4 (Learn), including from the rejected proposals: a rejection is taste signal too.
