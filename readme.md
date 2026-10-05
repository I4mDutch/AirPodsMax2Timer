# Timer until Airpods Max 2!

This simple application shows how many days have passed since last Tuesday. As I write this on Monday, October 5, it indicates the number of days it took my dad to get me the AirPods Max 2 early. It also includes a second timer counting down to my birthday, showing the actual time remaining. When November 12, 2026 arrives, the application stops working.

## Features

- **"Who are you?" menu** every time the page opens: *My dad*, *My mom*, or *Custom* (someone who is neither). Dad and Mom each get a short message plus a reminder to check the reasons banner; Custom goes straight to the timer.
- **Reasons banner** at the top with a soft glowing pulse: why the AirPods Max 2 are worth it. Click its title to collapse/expand (remembered).
- **Persuasion bubbles** pop up in the bottom-left corner every ~18 seconds, tailored to Dad, Mom, or anyone else. Edit them in the `BUBBLES` list in `index.html`.
- **Compare sellers**: a floating green button (bottom-right) plus buttons in the reasons banner and decision card open the retailers spreadsheet. Change the link in `config.js` (`RETAILERS_URL`).
- **The Math**: type the price and your Q1 money; it shows what your parents actually pay, per day over 2 years, and per hour of use.
- **My Promises**: what you commit to if you get them.
- **Decision Time**: "So... can we order them?" The YES button celebrates; the No button runs away.
- **Menu** also has *Both of us* for when Mom and Dad look together.
- **Key Dates** shown as tiles, including school days with one earbud; "Completed on" shows **???** until it's done.
- **Days Since I Asked** and **Days Until My Birthday** side by side (stacked on phones).
- Animated background, and a dark mode toggle in the top-right corner (remembers your choice).
- **Party mode** once a completion date is set: confetti, party colors, and "Party, woo! It's all done. We got it!"

## Marking it as completed

Open **`config.js`** (not `index.html`) and put the date between the quotes:

```js
const COMPLETED_ON = "10/20/2026";
```

`"10/20/2026"`, `"2026-10-20"` and `"October 20, 2026"` all work. Save, then commit/push if hosted. On GitHub you can edit it right in the browser: open `config.js`, click the pencil icon, change the date, and commit.

The page switches to party mode: it shows **"Hey, it's done on [date]."**, stops the count at the number of days it took, hides the reasons banner, and fills in "Completed on". The birthday countdown keeps running until November 12. To go back, set it to `""`.

**Preview without editing anything:** add `?done=10/20/2026` to the end of the page URL.
