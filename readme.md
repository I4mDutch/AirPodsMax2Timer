# Timer until Airpods Max 2!

This simple application shows how many days have passed since last Tuesday. As I write this on Monday, October 5, it indicates the number of days it took my dad to get me the AirPods Max 2 early. It also includes a second timer counting down to my birthday, showing the actual time remaining. When November 12, 2026 arrives, the application stops working.

## How the page flows

After the "Who are you?" menu (My dad / My mom / Both of us / Custom), the page reads like a story, one numbered step at a time:

1. **Why I need them**: the reasons (collapsible).
2. **What it changes**: right now vs. with AirPods Max 2.
3. **How long it's been**: days since I asked, birthday countdown, and Key Dates.
4. **The cost**: The Math. Type the price and Q1 money to get cost per day/hour.
5. **Your questions**: Excuse Busters, 14 objections answered.
6. **Gut check**: the "Would You?" quiz.
7. **My side of the deal**: my promises and a contract the parent can sign.
8. **The ask**: the Convinced-o-meter and **"Please buy me them. 🙏"** with YES / (runaway) No.

Also on the page:
- **Persuasion bubbles** with a pop sound, tailored to who's viewing. The 🔔 button (top-right) turns bubbles and sound off (🔕) or back on. Edit them in the `BUBBLES` list in `index.html`.
- A floating **🛒 Compare sellers** button opens the retailers spreadsheet (`RETAILERS_URL` in `config.js`).
- Dark mode toggle, animated background, and a reading-progress bar at the top.
- **Party mode** once a completion date is set: confetti, "Party, woo! It's all done. We got it!", and only the timers and Key Dates stay.

## Marking it as completed

Open **`config.js`** (not `index.html`) and put the date between the quotes:

```js
const COMPLETED_ON = "10/20/2026";
```

`"10/20/2026"`, `"2026-10-20"` and `"October 20, 2026"` all work. Save, then commit/push if hosted. On GitHub you can edit it right in the browser: open `config.js`, click the pencil icon, change the date, and commit.

The page switches to party mode: it shows **"Hey, it's done on [date]."**, stops the count at the number of days it took, hides the reasons banner, and fills in "Completed on". The birthday countdown keeps running until November 12. To go back, set it to `""`.

**Preview without editing anything:** add `?done=10/20/2026` to the end of the page URL.
