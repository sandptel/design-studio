# Build (autonomous)

Once decisions are locked, build without asking the user anything. Only stop for a real blocker, meaning a decision the brief can't answer and a wrong guess would be costly.

## 1. Self-assign the plan

Write a task list into `DESIGN.md` → Tasks, and mirror it into the session's task tool if one is available. Order it like this:

1. **Foundation**: put the tokens into code (CSS variables or a theme file), set up fonts, and build base components (for tier L, load `design-system` and `ui-styling`).
2. **Primary flow**: build the main action end to end, including every state.
3. **Secondary screens and features**: follow the concept for features that didn't get a round.
4. **Signature moment**: load `motion-design`.
5. **States sweep**: empty, loading, error, first-run and heavy-data.
6. **Polish pass**: work through the polish checklist in RUBRIC.md.

Tag each task with the experts it needs from the SKILL.md routing table.

## 2. Loop for each task

```
load the task's experts → build → screenshot (desktop 1440 + mobile 390)
→ score with RUBRIC.md → fix the lowest-scoring item → re-screenshot
(up to 3 passes per screen) → tick the task → next
```

- Re-read `DESIGN.md` → Tokens before each screen, so you derive from the locked tokens instead of drifting.
- If a pass doesn't improve the score, stop iterating that screen and write the reason in the task notes.
- Don't invent new decisions that contradict DESIGN.md. If the build shows a decision was wrong, note it for the checkpoint.

## 3. Checkpoint (the one time the user is involved)

When every task is ticked, show:
- the URL (localhost) or Artifact link
- the desktop and mobile screenshots of the primary flow
- 3 lines: what was built, the things you're least sure of, and any decision you'd revisit

Ask for one verdict: **Ship it** / **Changes** (they list them; each change goes through tier S or M) / **Redo a feature** (run that feature's round again).

After that verdict, apply SKILL.md §4 (Learn) and mark the run as validated in DESIGN.md.
