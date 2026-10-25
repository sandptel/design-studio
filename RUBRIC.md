# Rubric and screenshots

## Taking screenshots

Use `claude-in-chrome` if it's connected. Otherwise use headless Chrome:

```bash
google-chrome-stable --headless=new --hide-scrollbars --window-size=1440,900 --screenshot="$OUT/desk.png" "$URL"
google-chrome-stable --headless=new --hide-scrollbars --window-size=390,844  --screenshot="$OUT/mob.png"  "$URL"
```

Then Read the PNGs. You must actually look at them. Judging from the code alone doesn't count.

## Score each item from 0 to 2 (fix the lowest first)

| # | Check | 2 = pass |
|---|---|---|
| 1 | **3-second test** | The primary action is the most obvious thing on the screen |
| 2 | **Brief fit** | It looks like *this* product, not any SaaS. The metaphor shows. |
| 3 | **Hierarchy** | Size, weight and position follow how much each element matters, and nothing has equal weight by accident |
| 4 | **Not default** | No banned defaults (below), and it doesn't land in one of frontend-design's three AI-cluster looks unless the brief chose it |
| 5 | **Taste** | No rule in taste.md or DESIGN.md is violated |
| 6 | **States** | Every relevant state is designed, not just the happy path |
| 7 | **Craft** | Spacing follows one scale; alignment is consistent; type follows one scale; no orphans or widows in headlines; images aren't stretched |
| 8 | **Interaction** | Hover, focus and active states exist; transitions take 150–250ms with an ease-out curve; there's no layout shift |
| 9 | **Accessibility** | Contrast meets AA, focus is visible, targets are at least 44px on mobile, and reduced motion is respected |
| 10 | **Responsive** | Mobile is designed, not just squeezed: no horizontal scroll, and the primary action is within thumb reach |
| 11 | **Restraint** | Remove one accessory. Is there anything to cut without hurting the job? |

## Banned defaults (use one only if the brief justifies it)

- A purple or blue gradient hero with a centered headline and two buttons
- A row of three icon feature cards
- Glassmorphism or gradient blobs with no reason
- Emoji as icons, or decorative stock illustrations
- A dashboard made only of identical stat tiles
- Inter, Roboto or system-ui used as the *display* face without the concept justifying it
- Numbered `01 / 02 / 03` markers on content that isn't a sequence
- The CTA copy "Get Started", "Submit" or "Learn More"

## Polish checklist (last task of every build)

Custom focus rings in the accent colour · `text-wrap: balance` on headings · tabular numbers for data · consistent corner radius family · a shadow and elevation scale with no more than 3 levels · selection colour · favicon/title · skeleton loaders shaped like the real content · empty states with a clear next action · `prefers-color-scheme` if the concept allows it.
