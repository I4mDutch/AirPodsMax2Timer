# Timer until Airpods Max 2!

This simple application makes my case for the AirPods Max 2 and counts down to my birthday, showing the actual time remaining. When November 12, 2026 arrives, the application stops working.

## How the page flows (v1.1)

The page opens in a plain black-and-white look with the "Who are you?" menu:

1. **Who are you?** My mom.
2. **The message**: a personal message for that person.
3. **Pick a theme**: **Standard** (the original blue look), **Classic** (old parchment, like the U.S. Constitution) or **Apple** (built from Apple's design language: San Francisco type, one blue tint, rounded cards, Liquid Glass controls, light and dark). An animation reveals the chosen theme.
4. **The intro**: "Hey, [name], let me run a few things to show why this site exists," followed by quick answers to *What is it?*, *What is it for?*, *Why not just ask again?* and *How does it work?*
5. **Start the story**, which leads into the page, one numbered step at a time:

1. **Why I need them**: the reasons (collapsible).
2. **What it changes**: right now vs. with AirPods Max 2.
3. **How long it's been**: birthday countdown and Key Dates.
4. **The cost**: The Math. The price starts at **$549, Apple's max price** for AirPods Max 2 (change `DEFAULT_PRICE` in `index.html`). Type a cheaper price and Q1 money to get cost per day/hour.
5. **Your questions**: Doubt Busters, 12 questions answered.
6. **Gut check**: the "Would You?" quiz.
7. **My side of the deal**: my promises and a contract Mom can sign.
8. **The ask**: **"Will you get me the AirPods Max 2? 💙"** with YES / "Let me think about it".

**Returning visitors** see "Welcome back, [name]" with one button that skips straight to the story in their last theme, or "Start over" to pick again.

Also on the page:
- **🎨 Theme button** (top-right): switch between Standard, Classic and Apple at any time.
- **Step navigator** (right edge, wide screens only): numbered dots for the 8 steps. Hover to see each step's name, click to jump, and the current step is highlighted.
- **Persuasion bubbles** with a pop sound. The 🔔 button (top-right) turns them on (🔔) or off (🔕); they start off by default. Edit them in the `BUBBLES` list in `index.html`.
- A floating **🛒 Compare sellers** button opens the retailers spreadsheet (`RETAILERS_URL` in `config.js`).
- Dark mode toggle, animated background, and a reading-progress bar at the top.
- **Party mode** once a completion date is set: confetti, "Party, woo! It's all done. We got it!", and only the timers and Key Dates stay.

## Marking it as completed

Open **`config.js`** (not `index.html`) and put the date between the quotes:

```js
const COMPLETED_ON = "10/20/2026";
```

`"10/20/2026"`, `"2026-10-20"` and `"October 20, 2026"` all work. Save, then commit/push if hosted. On GitHub you can edit it right in the browser: open `config.js`, click the pencil icon, change the date, and commit.

The page switches to party mode: it shows **"Hey, it's done on [date]."**, hides the reasons banner, and fills in "Completed on". The birthday countdown keeps running until November 12. To go back, set it to `""`.

**Preview without editing anything:** add `?done=10/20/2026` to the end of the page URL.
