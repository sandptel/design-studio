# Demos

Show real, clickable options early, so the user's eye decides instead of their imagination. Variants must differ in **concept** (layout, hierarchy, interaction model, density), never just in colour.

## Concept round (tier L): 3 archetypes as one Artifact

Spawn **3 parallel subagents** (Agent tool, general-purpose) in one message. Each one gets the full brief, taste.md, the content to use, and one archetype:

| Archetype | Direction | ui-ux-pro-max dials |
|---|---|---|
| **Minimal** | Quiet and typographic, with a lot of whitespace. Precision is the luxury. | `--variance 2 --motion 2 --density 3` (adjust density to the brief) |
| **Expressive** | A bold concept from the metaphor, with signature motion and a type-led hero | `--variance 7 --motion 8` |
| **Unconventional** | Breaks the pattern expected for this product type, e.g. a spatial, conversational, timeline or canvas interaction model | `--variance 9` |

Prompt each subagent to:
1. Load `frontend-design` and follow its two-pass process: write a token plan (4–6 named hex values, display/body/utility type, layout as ASCII, one signature), then critique the plan against the generic AI defaults and revise it before writing code.
2. Run the ui-ux-pro-max `--design-system` search with its dials and adapt the result. Don't copy it verbatim.
3. Build the **primary screen** as one self-contained `variant-<archetype>.html` in the scratchpad, using real content and covering the main action plus one key state (empty or error). Include hover and focus states and its signature moment.
4. Take a screenshot (see RUBRIC.md), fix anything broken, and return a 3-line summary: the concept sentence, the tokens and the signature.

Then the main thread loads `artifact-design` and publishes one Artifact: an `index.html` with a fixed bottom tab bar switching between three iframes of the variant files (passed via `files`). Below the frame, show each variant's 3-line summary.

**Ask for verdicts with AskUserQuestion**, one question per variant (multiSelect where it fits):
- Keep / Discard / Keep parts of it
- If they keep parts: which parts (type, palette, layout, signature, interaction model)?

Finish with: "Mix the kept parts into one direction?" Show the merged concept sentence and the tokens. Lock them into `DESIGN.md` → Concept and Tokens, then apply SKILL.md §4 (Learn).

## Feature rounds (tiers M and L): 2–3 variants per feature, on localhost

Run these only for **ambiguous or hero features**: the primary action, the key data view, the signature moment, and anything where you can't confidently pick a variant. List the features you plan to run rounds for and the ones you'll build directly, so the user can add to the list or remove from it.

For each round:
1. If there's a codebase, use the `prototype` skill's UI pattern: a variant switcher using a `?variant=` query string, shown as a floating bar, on a throwaway route. If there isn't one yet, use an Artifact as in the concept round.
2. Build 2–3 variants **inside the locked concept**. Use subagents when the variants differ a lot. For small variations, build them inline.
3. Ask for one verdict per variant:
   - **Keep**: this is the one.
   - **Discard**
   - **Merge into <other>**: say which parts of it carry over.
   - **Coexist**: then ask how they should coexist:
     - a user setting (a toggle or preference)
     - responsive (one variant per breakpoint)
     - mode (beginner/expert, compact/comfortable)
     - context (a different state or entry point decides which one shows)
4. Record the verdict and how the variants coexist in `DESIGN.md` → Decisions, then learn (SKILL.md §4).
5. Delete the throwaway route once the decision is recorded.

After the last round, go to BUILD.md.
