# Interview

The goal is a brief confident enough to design from, not a questionnaire. Before each question, think hard: what would this product look like under each plausible answer? Ask only the questions whose answer changes the design.

## Rules

- **One question at a time**, using AskUserQuestion. Put your recommended answer first and label it "(Recommended)".
- **Answer from context first.** Don't ask what the request, the codebase, DESIGN.md or taste.md already answers.
- **Show, don't describe.** For any question about layout, density or hierarchy, attach an ASCII wireframe `preview` to each option so the user picks by eye.
- **Caps.** Tier M allows at most 3 questions. Tier L allows at most about 8. Stop earlier once the brief is confident. Anything still unknown becomes a stated assumption that the demos will test.

## Question order (skip the ones already answered)

**Product (what it has to do)**
1. **Who**: the specific user and their context (device, time pressure, expertise). Offer 2–3 concrete personas.
2. **Job and main action**: the one thing the screen must make effortless. Offer candidates.
3. **Success signal**: how we'll know it works (time to task, conversion, a return visit, the right decision made).
4. **Scope cut**: what v1 deliberately leaves out.

**Feel (what it is like to use)**
5. **Mood and metaphor**: "if this product were a physical object or place, what would it be?" Offer 3 metaphors that fit the brief, e.g. a pilot's checklist, a gallery wall card or a field notebook.
6. **Density and pace**: calm and spacious, balanced, or dense and expert. Show ASCII previews.
7. **References**: products or sites they love or hate for this, and why. If they have none, offer famous examples.
8. **Signature moment**: the one thing people should remember. Offer 3 candidates tied to the main action.

## Output

Write the brief into `DESIGN.md` (Brief section) and show it in 5–7 lines:

```
Who:        <persona + context>
Job:        <in the user's words>
Primary:    <the one action>
Success:    <signal>
Feel:       <metaphor> · <density> · refs: <...>
Signature:  <moment>
Assumed:    <open items the demos will test>
```

Then go to DEMOS.md.
