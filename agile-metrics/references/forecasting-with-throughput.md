# Forecasting with Throughput — step by step

A procedure you can run in a spreadsheet in twenty minutes. For the reasoning — why probabilistic forecasting beats estimation, how to choose confidence levels, what to do when the forecast is unwelcome — see the **`monte-carlo-forecasting`** skill. This file is the mechanics and a worked example.

## What you need

Just one thing: **how many items your team completed in each of the last 8–12 weeks** (or Sprints). No story points, no estimates, no velocity.

**Data quality rules:**
- Count *completed* items, at the same definition of done each week
- Use the last 8–12 periods — long enough to capture variation, recent enough to reflect the current team
- Don't clean out the bad weeks. The week with an incident and the week half the team was away are exactly the variation you're forecasting
- Exclude a period only if the team was materially different (a reorganisation, not a holiday)

---

## Method A: the two-minute forecast (no simulation)

Good enough for a corridor conversation.

Take your historical throughput per week. Your forecast range for *N* weeks is the low and high of that history:

> Last 10 weeks: 7, 4, 9, 6, 5, 8, 3, 7, 6, 5 items
> Median = 6 items/week · Low = 3 · High = 9
>
> **45 items remaining:** 45 ÷ 9 = 5 weeks (optimistic) · 45 ÷ 6 = 7.5 weeks (typical) · 45 ÷ 3 = 15 weeks (pessimistic)

Report the middle and the pessimistic figure, never the optimistic one alone. This method overstates the extremes — a team doesn't hit its worst week ten times running — which is exactly what Monte Carlo fixes.

---

## Method B: Monte Carlo — "when will these N items be done?"

**The idea:** simulate the next few weeks hundreds of times by drawing at random from your actual history, and count how often each answer comes up.

### Step by step in a spreadsheet

1. **Column A — history.** Put your 10 weekly throughput figures in A1:A10
2. **One trial:** in B1, draw a random past week:
   `=INDEX($A$1:$A$10, RANDBETWEEN(1, 10))`
   Fill down 30 rows — that's 30 simulated weeks
3. **Cumulative:** in C1 `=B1`; in C2 `=C1+B2`; fill down
4. **Weeks to finish:** find the first row where the cumulative total reaches your backlog size:
   `=MATCH(TRUE, INDEX($C$1:$C$30 >= $F$1, 0), 0)` where F1 holds the number of items remaining
5. **Repeat 500–1000 times.** Either copy the trial block across 500 columns, or press recalculate repeatedly and record the answer — a data table is cleaner
6. **Sort the 500 results** and read off the percentiles:
   - 50th percentile = the coin-flip date
   - **85th percentile = the date you commit to**
   - 95th percentile = the date you'd defend to an auditor

### Worked example

> **Backlog remaining:** 45 items
> **History (items/week):** 7, 4, 9, 6, 5, 8, 3, 7, 6, 5
> **1,000 simulated runs → weeks to complete:**
>
> | Percentile | Weeks | Date (from 21 September) |
> |---|---|---|
> | 50% | 7 | 9 November |
> | 70% | 8 | 16 November |
> | **85%** | **9** | **23 November** |
> | 95% | 11 | 7 December |

**How to say it:** "We're 85% confident of finishing by 23 November. There's a coin-flip chance of 9 November, and if things go badly it's early December. If you need 9 November, we need to cut roughly 12 items."

Notice what the spread does for the conversation: it turns "when will it be done?" into "how much certainty do you want, and what will you trade for it?"

---

## Method C: "how much will be done by a fixed date?"

The same simulation, run the other way — useful for a regulatory deadline or a go-live you can't move.

1. Fix the number of weeks available (say 8)
2. Each trial: sum 8 randomly drawn weeks from history
3. Run 1,000 trials, sort the totals, read the percentiles

> **8 weeks available. 1,000 trials:**
> 50% chance of completing 48 items or more · **85% chance of completing 40 or more** · 95% chance of 36 or more
>
> "We can commit to 40 items by the deadline with high confidence. The scope is currently 55. Which 15 would you like to drop?"

This is the single most useful version of the technique, because it converts a date argument into a scope conversation.

---

## Adjustments that are worth making

- **Split by work type** if cycle times differ wildly — features and incidents behave differently. Forecast them separately or the distribution is meaningless
- **Account for known absences** by scaling the drawn weeks (e.g. multiply by 0.6 for a week with 40% of the team away). Do this transparently, not silently
- **Add a scope growth factor** when discovery is ongoing: if the backlog has historically grown 15% during delivery, simulate 45 × 1.15 items. Ignoring this is the most common reason honest forecasts still come in late
- **Re-run weekly.** A forecast is a living output, not a one-off. The range should narrow as you approach

## Adjustments that are not worth making

- Weighting recent weeks more heavily, unless the team genuinely changed — it usually just imports optimism
- Excluding "unrepresentative" bad weeks — they're representative; that's the point
- Forecasting from fewer than six data points; say "not enough history yet" instead

---

## Common objections and answers

| Objection | Answer |
|---|---|
| "Our items aren't the same size" | Over 20+ items, size variation averages out. Check with a cycle time scatterplot — if the spread is enormous, split items rather than abandoning the method |
| "We don't have historical data" | You have completion dates in your tool. That's all this needs |
| "Management want one date" | Give them the 85th percentile as the date and say what confidence it carries. One number, honestly qualified |
| "This ignores dependencies" | Correct. Model known blockers separately; the simulation forecasts the team's own flow |
| "Last quarter was unusual" | Every quarter is unusual. That's why we sample the variation instead of assuming it away |

---

## Reporting it

Say the confidence level out loud, every time. "23 November at 85% confidence" is a professional statement; "23 November" is a hostage.

Track your own accuracy: record the forecast range each month and what actually happened. After two quarters you can say "our 85% forecasts have landed inside the range every time", which is worth more than any single forecast.
