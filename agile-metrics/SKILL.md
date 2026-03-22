---
name: Agile Metrics
description: This skill should be used when the user asks about "agile metrics", "scrum metrics", "kanban metrics", "velocity", "throughput", "cycle time", "lead time", "burn down chart", "burn up chart", "cumulative flow", "sprint metrics", "delivery metrics", "flow metrics", "team metrics", "OKRs agile", "NPS agile", "predictability", "forecasting agile", "Monte Carlo", "story points metrics", "measuring agile", "agile KPIs", "team performance metrics", "health metrics", or needs help choosing, measuring, or interpreting agile metrics.
version: 1.0.0
---

# Agile Metrics

Metrics in agile serve inspection and adaptation, not performance management. The goal is to create shared understanding of how the system is working — and to make improvements based on evidence. When metrics become targets (Goodhart's Law), they lose their value and incentivise gaming.

## Metric Categories

| Category | Purpose | Primary Users |
|---|---|---|
| Flow Metrics | How work moves through the system | Team, SM, ADM |
| Sprint Metrics | Sprint health and predictability | Team, SM |
| Quality Metrics | Product and code health | Team, PO |
| Business Metrics | Value delivery and outcomes | PO, stakeholders |
| Team Health Metrics | People and culture | SM, coach |

---

## Flow Metrics (Kanban and Continuous Delivery)

### Cycle Time

**Definition**: Time from when work **starts** (first active state) to when it is **done**.

**How to measure**: Track state transitions with timestamps. Calculate per item. Report as percentiles (50th = median, 85th, 95th), not averages. Averages hide bimodal distributions.

**What it tells you**: How long it typically takes to deliver something once started. Shorter and more consistent = better.

**Red flags**: High variability (large spread between 50th and 95th percentile); upward trend over time.

### Lead Time

**Definition**: Time from when work is **requested** (enters the intake queue) to when it is **done**.

**Difference from cycle time**: Includes wait time before work begins. Lead time is what the customer experiences.

**Use**: Setting Service Level Expectations (SLEs); customer promise-making.

### Throughput

**Definition**: Number of work items completed per unit time (typically per week).

**Why it matters**: More stable than velocity; does not depend on estimation accuracy. Use for forecasting: "At our current throughput of 6 items/week, 30 remaining items will take approximately 5 weeks."

**Monte Carlo forecasting**: Run simulations using historical throughput to produce probabilistic forecasts. Example: "At 80% confidence, 30 items will complete within 6 weeks." More honest than Gantt-based estimates.

### Flow Efficiency

**Definition**: `(Active time / Total lead time) × 100%`

**Benchmark**: Most knowledge work systems run at 5–15% flow efficiency. Above 40% is high.

**Implication**: The biggest lever for delivery speed is usually reducing wait time, not working faster.

### Work Item Age

**Definition**: How long a currently-in-progress item has been in the active state.

**Use**: Items ageing beyond the 85th percentile SLE should be escalated. Track on the board.

---

## Sprint Metrics (Scrum)

### Velocity

**Definition**: Average story points (or PBIs) completed per sprint, typically over a rolling 3–5 sprint window.

**Appropriate use**:
- Forecasting: "At current velocity of 35 points, 200-point backlog will take approximately 6 sprints"
- Capacity planning for sprint selection
- Spotting trends (declining velocity may signal technical debt or team health issues)

**Inappropriate use**:
- Comparing teams (different estimation scales, different work types)
- As a performance target (creates pressure to inflate estimates)
- As a commitment (it's a forecast input, not a promise)

### Sprint Burn-Down Chart

Shows remaining work (points or tasks) against time within a sprint. Useful for the team to self-manage daily. Not a stakeholder reporting tool — it's a tactical board.

**Flat lines**: Work not being completed or updated. Prompt a conversation, not a sanction.
**Late vertical drops**: Work being marked done at the end without incremental progress. Challenge the Definition of Done.

### Sprint Burn-Up Chart

Shows work completed vs. total scope over time across multiple sprints. Better than burn-down for visualising scope changes. Recommended for stakeholder communication.

### Sprint Goal Achievement Rate

**Definition**: % of sprints where the Sprint Goal was achieved over the last 10 sprints.

**Why it matters**: More meaningful than velocity. A team consistently meeting Sprint Goals is predictable and focused.

**Target**: 80–90% is healthy. 100% may indicate Sprint Goals are too safe; 50% indicates planning or impediment problems.

---

## Quality Metrics

**Escaped defects**: Bugs found in production vs. bugs found in testing. Ratio indicates testing effectiveness.

**Technical debt ratio**: Proportion of sprint capacity consumed by tech debt remediation. Rising ratio signals a quality problem.

**Definition of Done compliance**: % of items meeting all DoD criteria. Anything below 100% requires attention.

**Test coverage trends**: Track over time, not as an absolute number.

---

## Business / Outcome Metrics

### OKRs (Objectives and Key Results)

**Structure**: Qualitative Objective + 2–5 quantitative Key Results.

Example:
- **Objective**: Improve the onboarding experience for new customers
- **KR1**: Reduce time-to-first-value from 14 days to 7 days
- **KR2**: Increase 30-day activation rate from 45% to 65%
- **KR3**: NPS for new users ≥ 50 by Q3 end

**Agile integration**: OKRs inform Product Goal and backlog priority. Sprint Reviews should reference progress toward KRs, not just feature delivery.

**Key rule**: Key Results measure outcomes, not outputs. "Ship feature X" is an output. "Increase activation rate by 20%" is an outcome.

### Net Promoter Score (NPS)

**Definition**: "How likely are you to recommend us to a friend?" (0–10 scale). Score = % Promoters (9–10) − % Detractors (0–6).

**Agile use**: Track NPS trend (not just point-in-time) as a lagging indicator of product value. Include in quarterly retrospectives.

### Time to Market

Measure from idea to production deployment. Tracks the full pipeline, not just development time.

---

## Choosing the Right Metrics

**For a Scrum team**: Velocity (forecasting), Sprint Goal achievement rate, escaped defects

**For a Kanban team**: Cycle time (percentiles), throughput, flow efficiency, WIP levels

**For a programme/portfolio**: Delivery predictability, lead time to production, dependency resolution time

**For team health**: Retrospective action completion rate, psychological safety scores, team stability

**Avoid vanity metrics**: Lines of code, number of meetings held, number of story points "in flight"

## Reporting Principles

1. **Show trends, not point-in-time data** — a single data point has no meaning; patterns over 6–12 weeks do
2. **Use visualisations** — CFDs, burn-ups, and scatter plots reveal patterns that tables hide
3. **Separate team metrics from management reporting** — team metrics are for the team's improvement; different metrics serve stakeholder communication
4. **Make metrics visible to the team first** — teams that own their metrics improve them; teams that have metrics imposed on them game them
5. **Pair metrics with conversations** — a metric that doesn't trigger a question or an action is noise

## Additional Resources

- **`references/metrics-visualisation-guide.md`** — How to create and interpret burn-up charts, CFDs, and cycle time scatterplots
- **`references/forecasting-with-throughput.md`** — Step-by-step Monte Carlo forecasting using historical throughput data
