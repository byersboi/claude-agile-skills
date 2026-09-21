# Metrics Visualisation Guide

How to build and read the four charts that carry most of the useful signal: burn-up, cumulative flow diagram, cycle time scatterplot, and the control-style run chart. For which metrics to use and why, see the `agile-metrics` skill.

## Principles

- **Show variation, not averages.** An average cycle time of 6 days hides a distribution running from 1 to 40; the tail is where your customers live
- **Percentiles, not means.** Report the 85th percentile. It answers the question people are actually asking: "how long will this probably take?"
- **Same chart, same interval, every time.** Trend requires consistency
- **Annotate events** — team changes, holidays, incidents, scope changes. An unexplained step change gets explained by whoever has the loudest theory
- **No chart without a decision it informs.** If nobody would act differently, stop drawing it

---

## 1. Burn-up chart

**What it shows:** work completed against total scope, over time. Two lines: cumulative done, and total scope.

```
items
  80 |                                    ___________  ← scope line
  70 |                    ________________
  60 |      ______________
  50 |                                        ....••  ← done line
  40 |                                 ...•••
  30 |                          ...•••
  20 |                  ...•••
  10 |          ...•••
   0 |___•••_________________________________________
      S1   S2   S3   S4   S5   S6   S7   S8   S9
```

**Why burn-up beats burn-down:** the scope line is visible. A burn-down that flatlines looks like a team problem; the burn-up shows scope rose by 20 items in Sprint 3. Never show a stakeholder a burn-down when scope is moving.

**How to read it:**
- Gap between the lines at any point = work remaining
- Extend both lines to see where they'd converge — that's your naive forecast
- Scope line rising steadily = uncontrolled scope growth, or discovery working as intended. The chart doesn't tell you which; the conversation does
- Done line flattening = an impediment, not a motivation problem

**Build it from:** completed item count per Sprint (or per week) and total item count, cumulative. Story points work too; items are more honest.

---

## 2. Cumulative flow diagram (CFD)

**What it shows:** the number of items in each workflow state over time, stacked.

```
items
      |                                    ████████  Done
      |                              ██████████████
      |                        ████████▒▒▒▒▒▒▒▒▒▒▒▒  Test
      |                  ██████████▒▒▒▒▒░░░░░░░░░░░  In progress
      |            ██████████▒▒▒▒░░░░░░▓▓▓▓▓▓▓▓▓▓▓▓  To do
      |______________________________________________
       week 1                                week 12
```

**How to read it:**
- **Band width (vertical)** = WIP in that state. A widening band is a queue forming
- **Band width (horizontal)** = approximate cycle time through that state
- **Top line slope** = throughput. Flattening means delivery has stopped
- **Any band widening steadily** = the bottleneck. It is almost always testing, review or a wait-for-someone-else state
- **Bands running parallel** = a healthy, stable system

**Most common reading error:** treating a widening "in progress" band as productivity. It's the opposite — more started, not more finished.

**Build it from:** a daily snapshot of item counts per column. Most tools generate it; if yours doesn't, a daily count into a spreadsheet takes two minutes.

---

## 3. Cycle time scatterplot

The most useful chart in this file, and the least used.

**What it shows:** one dot per completed item — completion date on the x-axis, days taken on the y-axis — with percentile lines drawn across.

```
days
  40 |                    •
  30 |        •                          •
  25 |----------------------------------------- 95th
  15 |----•-------•---------•---------•-------- 85th
  10 |--•---•---•---•---•-----•---•---•-------- 70th
   5 |•••••••••••••••••••••••••••••••••••••••••
   0 |_________________________________________
      Jan        Feb        Mar        Apr
```

**How to read it:**
- **85th percentile line** = your service level expectation. "85% of items finish within 15 days" is a sentence a stakeholder can use
- **Dots above the line** = the exceptions. Go and look at each one; they usually share a cause — an external dependency, a particular work type, a hand-off
- **Line drifting up** = the system is degrading, usually because WIP has crept up
- **Vertical clusters** = batch releases. Work finishing together means it was waiting together
- **Widening spread over time** = increasing unpredictability, which matters more to stakeholders than the average

**Build it from:** start date and end date for each completed item. That's all. If your tool won't export it, two columns in a spreadsheet will do.

**Use it for:** setting an SLE, answering "how long does something like this usually take?", and spotting the difference between a slow system and an unpredictable one.

---

## 4. Throughput run chart

**What it shows:** items completed per week or per Sprint, as a line, with a median line drawn.

**How to read it:**
- **Median line** = your typical delivery rate; use it for forecasting, not the mean
- **Sustained runs above or below the median** (seven or more consecutive points) = a real change in the system, not noise
- **A single spike** = usually a batch of small items or a release, not a productivity gain
- **High variability** = forecasting will be wide; reduce WIP and item size before trying to speed up

Throughput is the input to Monte Carlo forecasting — see `references/forecasting-with-throughput.md`.

---

## What to show which audience

| Audience | Show | Don't show |
|---|---|---|
| The team | CFD, scatterplot, throughput run chart | Anything comparing them to another team |
| Product Owner | Burn-up, throughput, forecast ranges | Velocity in isolation |
| Sponsor / steering | Burn-up, forecast range with confidence, milestone confidence | CFD (too much detail), velocity, individual metrics |
| Wider organisation | Outcome metrics and delivery frequency | Team-level flow metrics |

---

## Visualisation anti-patterns

| Anti-pattern | Why it misleads | Instead |
|---|---|---|
| Burn-down shown when scope is changing | Makes discovery look like failure | Burn-up with the scope line visible |
| Average cycle time reported | Hides the tail that customers experience | 85th percentile |
| Velocity chart to stakeholders | Invites cross-team comparison and gaming | Throughput and forecast ranges |
| Single-date forecast from a trend line | Implies a certainty that doesn't exist | A range with a confidence level |
| Traffic lights with no text | Amber becomes a place to hide | Always a sentence with the colour |
| Charts nobody discusses | Reporting theatre | Bring one chart to the retro and ask what it's telling you |
| Individual-level metrics | Destroys collaboration instantly | Team-level only, always |
