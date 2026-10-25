# design-studio

A Claude Code skill that runs UI work like a small product-design studio. It works like this:

1. Thinks like a product manager and interviews you, one question at a time.
2. Shows 3 concept demos (Minimal, Expressive, Unconventional) as an Artifact, then shows variants of the key features on localhost.
3. You keep, discard, merge or combine them.
4. It builds on its own, routing each task to specialist skills: `frontend-design`, `ui-ux-pro-max`, `motion-design`, `dataviz`. It checks its work with screenshots against a scoring rubric.
5. It learns your taste (`taste.md`, kept local) and each product's decisions (`DESIGN.md` in the repo).
6. When you ask it to `evolve`, it proposes the next improvements.

The size of the request decides the flow: tweak → feature → product.

## Install

```bash
git clone https://github.com/sandptel/design-studio ~/.claude/skills/design-studio
```

Recommended companions: [frontend-design](https://github.com/anthropics/claude-plugins-official), [ui-ux-pro-max](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill), plus the `motion-design`, `dataviz` and `prototype` skills. Each one is used if it's installed and skipped if it isn't.

Use it with `/design-studio <idea>`, or simply ask for any UI.
