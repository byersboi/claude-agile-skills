---
name: Monte Carlo Forecasting
description: This skill should be used when the user asks about "Monte Carlo forecasting", "Monte Carlo simulation", "probabilistic forecasting", "delivery forecast", "when will we finish", "forecast completion date", "confidence interval delivery", "how many sprints", "story point forecast", "velocity forecasting", "throughput forecasting", "forecasting with uncertainty", "delivery probability", "sprint forecast", "agile forecasting", "forecast range", "forecasting without estimates", "simulation forecasting", "delivery confidence", "forecasting techniques agile", or wants to produce or interpret a probabilistic delivery forecast.
version: 1.0.0
---

# Monte Carlo Forecasting

Monte Carlo forecasting is a simulation technique that uses a team's real historical delivery data to produce probabilistic answers to questions like "When will we finish?" or "How much can we deliver by a given date?"

Rather than producing a single-point estimate ("we'll finish in sprint 12"), Monte Carlo produces a range of outcomes with associated confidence levels ("there's an 85% chance we'll finish by sprint 12, and a 95% chance by sprint 13"). This is more honest, more useful, and more defensible than any deterministic forecast.

The method is named after the Monaco casino because it relies on random sampling — the same principle as rolling dice thousands of times to understand the probability distribution of outcomes.

## Why Monte Carlo Over Velocity-Based Estimation

The traditional approach to forecasting — divide remaining story points by average velocity — has a fatal flaw: it ignores variability. A team with an average velocity of 40 points might deliver anywhere from 25 to 60 in any given sprint. Dividing by 40 gives false precision.

**Average velocity forecast**: "300 points ÷ 40 average velocity = 7.5 sprints." States this as fact. Ignores that the team has never delivered exactly 40 points.

**Monte Carlo forecast**: "Based on 1,000 simulations drawing from your actual velocity history, there is a 50% chance you finish in 7 sprints, an 85% chance in 8 sprints, and a 95% chance in 9 sprints." Expresses the uncertainty that actually exists.

The second conversation is harder to have — stakeholders often want a date, not a range. But a range that is honest is more useful than a date that is wrong.

| Approach | Accounts for variability | Communicates uncertainty | Defensible |
|---|---|---|---|
| Average velocity ÷ remaining points | No | No | Weakly |
| Best/worst/likely case | Partially | Partially | Moderately |
| Monte Carlo simulation | Yes | Yes | Strongly |

## What You Need

**Historical velocity data**: Ideally 8–12 sprints of actual velocity. Fewer sprints mean the simulation is less reliable — the sample is too small to represent the team's true range. More than 20 sprints risks including data from a very different team composition or context.

**Use recent, representative data**: If the team has grown, lost a key member, or significantly changed its way of working in the last few months, older data may not reflect current capability. Use your judgement — include data that reflects how the team works now.

**Remaining scope**: A reasonably stable estimate of remaining story points (or items, if using throughput). Monte Carlo cannot compensate for a wildly uncertain backlog — it models delivery variability, not scope uncertainty.

**A target**: Either a number of sprints ("can we finish 300 points in 6 sprints?") or a date ("what can we deliver by the end of Q3?").

## How It Works

At its core, a Monte Carlo simulation for sprint forecasting works like this:

1. Collect the team's historical velocity for N sprints (e.g. 38, 52, 44, 61, 49, 55, 47, 60)
2. Run thousands of simulated "futures": for each simulation, randomly sample from that history sprint by sprint, accumulating points until the target scope is reached
3. Record how many sprints each simulation required
4. Count the distribution — out of 1,000 simulations, how many finished in 5 sprints? 6? 7? 8?
5. Express as cumulative confidence: "X% of simulations completed within N sprints"

The random sampling means that high-velocity and low-velocity sprints both appear in proportion to how often they appeared historically. The simulation respects the team's actual pattern of variability, not an idealised average.

**Example output** (illustrative):

| Sprints to complete | % of simulations | Cumulative confidence |
|---|---|---|
| 5 | 8% | 8% |
| 6 | 34% | 42% |
| 7 | 31% | 73% |
| 8 | 18% | 91% |
| 9 | 7% | 98% |
| 10+ | 2% | 100% |

Reading this: there is a 42% chance of finishing within 6 sprints, an 73% chance within 7, and a 91% chance within 8. If the team needs to commit to a date, 8 sprints gives reasonable confidence; 9 sprints gives very high confidence.

## Choosing a Confidence Threshold

Different decisions warrant different confidence levels:

| Situation | Suggested threshold | Rationale |
|---|---|---|
| Internal planning target | 50% | Equally likely to hit or miss; good for planning purposes |
| Team commitment to stakeholders | 70–80% | Accepting some risk; appropriate when consequences of missing are moderate |
| External commitment or contractual | 85–90% | High confidence; accounts for most plausible bad scenarios |
| Regulatory or critical deadline | 95%+ | Near-certain; may require scope reduction or capacity increase |

Choosing a threshold is a risk conversation, not a technical one. Help stakeholders understand what 85% confidence means: "In roughly 1 in 6 scenarios based on our history, something unexpected happens and we don't make it. What's our plan if that occurs?"

## Simulations: How Many?

**1,000 simulations** is the standard minimum. It provides stable, reproducible results for typical sprint forecasting.

**10,000 simulations** gives marginally more precision at the tail ends of the distribution (very low or very high confidence percentiles). For most conversations, the difference is not meaningful.

Fewer than 500 simulations produces noisy results — run the same simulation twice and you may get noticeably different confidence numbers.

## Building a Simple Monte Carlo in a Spreadsheet

A basic Monte Carlo simulator does not require specialist software. A spreadsheet can run hundreds of simulations in seconds using random sampling functions.

**Structure**:
1. **Input table**: List historical velocity values in a column (one per sprint)
2. **Simulation grid**: A grid of rows (one per simulation) and columns (one per sprint). Each cell randomly samples from the historical velocity list using `INDEX` and `RANDBETWEEN`
3. **Cumulative sum**: Running total of simulated velocity across sprints
4. **Sprints to complete**: For each simulation row, the number of sprints until cumulative velocity exceeds the target
5. **Results**: Count of simulations completing in N sprints; express as % and cumulative %

**Key formula pattern** (illustrative, adapt to your layout):
- Sample a random historical velocity: `=INDEX($B$2:$B$9, RANDBETWEEN(1, COUNT($B$2:$B$9)))`
- Count simulations completing within N sprints: `=COUNTIF(results_column, "<="&N) / total_simulations`

**Recalculation**: Spreadsheet simulations recalculate on every change. To lock in a result, paste values before sharing. Or use a dedicated tool (see below).

## Tools

**Spreadsheet (Excel / Google Sheets)**: Sufficient for teams getting started. Manual setup required; results recalculate on every change (use paste-as-values to stabilise).

**ActionableAgile**: Purpose-built agile analytics tool with built-in Monte Carlo. Integrates with Jira and Azure DevOps. Strong visualisations; designed for practitioners.

**Jira plugins** (e.g. Nave, LinearB): Some Jira-connected tools offer Monte Carlo forecasting directly from your board data.

**Python / R**: For teams with analytical capability, a script can run more sophisticated simulations, handle larger datasets, and produce repeatable outputs. Libraries: `numpy` for random sampling, `matplotlib` for visualisation.

**Choosing a tool**: For a team new to Monte Carlo, a spreadsheet is a good starting point — building it manually builds understanding. Once the team trusts the method, a dedicated tool saves time and reduces error.

## Communicating Results to Stakeholders

This is where Monte Carlo forecasting most often fails — not in the maths, but in the conversation.

**Lead with the answer, then the confidence**: "We're 85% confident we'll complete the remaining scope within 8 sprints. That's our recommended commitment date. If you need higher certainty, we'd need to either extend by one sprint or reduce scope."

**Avoid the probability lecture**: Most stakeholders do not need to understand Monte Carlo to use the result. "Based on our delivery history, this is where the data puts us" is usually enough.

**Show the range, not just one number**: Share the 50%, 85%, and 95% dates. This makes the uncertainty visible without being overwhelming. "Most likely around sprint 7, very likely by sprint 9."

**Use it to reframe scope conversations**: Monte Carlo is a powerful tool for honest scope negotiation. "If you need 85% confidence by sprint 8, we can commit to 260 points. To reach 300 points at the same confidence, we need sprint 9." Scope, date, and confidence are a triangle — you can fix two, but not three.

**Re-run it regularly**: A Monte Carlo forecast made at the start of a quarter becomes stale as scope changes and new velocity data accumulates. Re-run it at least fortnightly, or after any significant scope change.

## Limitations and Honest Caveats

**Monte Carlo is only as good as the input data**: If the historical velocity is unrepresentative (team was understaffed, or working on unusually complex work), the forecast will be wrong. Garbage in, garbage out.

**It does not model unknown unknowns**: A simulation based on past sprints cannot account for a team member leaving, a major architectural discovery, or a stakeholder suddenly doubling the scope. It models the variability the team has experienced — not events outside that range.

**Scope must be reasonably stable**: If the backlog is growing as fast as the team is delivering, Monte Carlo cannot give a meaningful completion forecast. Stabilise scope before forecasting completion.

**Story points must be consistent**: If point inflation has occurred (the team has gradually calibrated points higher over time), mixing old and new velocity data distorts the simulation. Use throughput (items per sprint) as an alternative if points are inconsistent.

**It is a forecast, not a commitment**: A Monte Carlo result is the output of a model. It should inform decisions, not replace judgement. Use it as a prompt for honest conversations, not as a mechanism to hand a date to a stakeholder and walk away.

## Throughput-Based Monte Carlo

Story points are not required. For teams that do not estimate, or where point consistency is uncertain, use **throughput** (number of items completed per sprint) instead of velocity.

The method is identical — replace velocity figures with item counts per sprint, and replace "remaining story points" with "remaining backlog items." The simulation produces the same confidence distribution: "85% of simulations completed within N sprints."

Throughput-based forecasting is increasingly preferred because it removes the overhead of estimation and avoids debates about point consistency. It works best when backlog items are reasonably similar in size (use story splitting to achieve this).
