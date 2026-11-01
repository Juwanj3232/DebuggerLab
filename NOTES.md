# Debugger notes

Name: Juwan J

## Part 1 — Countdown

| Pass | `play` | `gain` | `yardsToGo` after the pass |
|---|--------|---|---|
| 1 | 1      | 2 | 8 |
| 2 | 2      | 4 | 4 |
| 3 | 3      | 6 | -2 |

My guess before running: The loop would run 3 times (gains of 2, 4, and 6 add up to 12, which is more than 10), so it would print "First down after 3 plays." and the yards to go would end up below 0, at -2.

What it really printed: "First down after 3 plays." and "Yards to go at the end: -2". When the loop ended, `yardsToGo` was -2, which matches my guess. The loop condition is `yardsToGo > 0`, so it only stops once the gains overshoot the 10 yards.

## Bug 1 — totalYards

- **Where:** `totalYards`, the `for` line (`for (int i = 1; i < yards.length; i++)`).
- **What the debugger showed:** On the first pass through the loop, `i` was already 1, so `yards[0]` (12 yards) was never added to `total`. The method returned 140 instead of 152.
- **The fix:** I changed `int i = 1` to `int i = 0`. The total is now 152.

## Bug 2 — averageYards

- **Where:**
- **What the debugger showed:**
- **The fix:**

## Bug 3 — bestGame

- **Where:**
- **What the debugger showed:**
- **The fix:**

## Bug 4 — countBigGames

- **Where:**
- **What the debugger showed:**
- **The fix:**
