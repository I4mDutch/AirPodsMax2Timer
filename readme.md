# Timer until Airpods Max 2!

This simple application shows how many days have passed since last Tuesday. As I write this on Monday, October 5, it indicates the number of days it took my dad to get me the AirPods Max 2 early. It also includes a second timer counting down to my birthday, showing the actual time remaining. When November 12, 2026 arrives, the application stops working.

## Features

- **"Who are you?" menu** every time the page opens: *My dad*, *My mom*, or *Custom* (someone who is neither). Dad and Mom each get a short message; Custom goes straight to the timer.
- **Days Since I Asked** and **Days Until My Birthday** shown side by side (stacked on phones).
- Animated background, and a dark mode toggle in the top-right corner (remembers your choice).

## Marking it as completed

When the AirPods Max 2 arrive:

1. Open `index.html`.
2. Near the top of the `<script>` section, find:
   ```js
   const COMPLETED_ON = null;
   ```
3. Change it to the date they arrived, in `"YYYY-MM-DD"` format:
   ```js
   const COMPLETED_ON = "2026-10-20";
   ```
4. Save (and commit/push if hosted).

The page will then show **"Hey, it's done on [date]."** at the top, freeze the "Days Since I Asked" count at the number of days it took, and fill in "Completed on" in the Key Dates list. The birthday countdown keeps running until November 12.
