# Flow Metrics — calculating and interpreting

How to compute each flow metric from data you already have, and what each one tells you. For Kanban practice generally see the `kanban` skill; for charting, `agile-metrics/references/metrics-visualisation-guide.md`.

## The data you need

Two timestamps per work item: **when it started** (entered the first active column) and **when it finished** (entered Done). That's it. Everything below comes from those two columns plus a daily count of items per state.

**Define "started" once and hold to it.** The commonest source of nonsense metrics is a team where half the items are dragged into "In progress" when work begins and half when they're created.

---

## The four core metrics

### Cycle time
**Definition:** elapsed working days from start to finish, for a single item.
**Calculate:** `finish date − start date`, counting working days.
**Report as:** the **85th percentile**, never the mean.

> 20 items, sorted by duration. The 85th percentile is the 17th value (0.85 × 20 = 17).
> 1,1,2,2,2,3,3,3,4,4,5,5,6,7,8,9,**12**,15,22,31 → **85th percentile = 12 days**
>
> "85% of our work finishes within 12 days." The mean here is 7.3 days, which describes almost nothing anyone experiences.

**What moves it:** WIP (most), item size, hand-offs, waiting on people outside the team. Rarely how hard people are working.

### Lead time
**Definition:** elapsed time from *request* to finish — includes the queue before work started.
**Calculate:** `finish date − request date`.

**Why both matter:** cycle time is your team's performance; lead time is the customer's experience. A team with a 5-day cycle time and a 60-day lead time has a prioritisation problem, not a delivery problem — and the customer cannot tell the difference.

### Throughput
**Definition:** number of items completed per period.
**Calculate:** count of items finished per week or Sprint. No estimation involved.
**Report as:** the median of the last 8–12 periods, with the range.

Throughput drives forecasting — see `agile-metrics/references/forecasting-with-throughput.md`.

### Work in progress (WIP)
**Definition:** items started but not finished, at a point in time.
**Calculate:** count them. Daily.

The one number to watch if you only watch one. WIP is the lever; cycle time is the outcome.

---

## Little's Law

> **Average cycle time = average WIP ÷ average throughput**

The most useful relationship in flow, because it's arithmetic rather than opinion.

> 20 items in progress, finishing 5 per week → average cycle time = 20 ÷ 5 = **4 weeks**
> Halve WIP to 10, throughput unchanged → cycle time = 10 ÷ 5 = **2 weeks**

**What it tells you:** you cannot reduce cycle time without either reducing WIP or increasing throughput — and increasing throughput by starting more work does the opposite. This is the sentence that wins the WIP-limit argument.

**Caveats:** it holds on averages over a stable period, with items entering and leaving at similar rates. Don't apply it to a single item or a fortnight of chaos.

---

## Flow efficiency

> **Flow efficiency = active time ÷ total elapsed time**

Take ten completed items; for each, count the days someone was actually working on it versus the total elapsed.

> Median: 2.5 active days out of 15 elapsed = **17%**

**Benchmark:** most teams sit between 15% and 30%. Above 40% is genuinely good.

**Why it's the most persuasive metric you have:** it reframes "the team is slow" as "work waits 83% of its life". The improvement is in the queues, not in the people.

**How to measure it cheaply:** you don't need tooling. Take ten items and walk them through with the team from memory — "how many days was anyone actually on this?" Rough is fine; the number is shocking at any precision.

---

## Work item age

**Definition:** for items *currently in progress*, how many days since they started.

The only flow metric that lets you act today rather than analyse yesterday. Everything else is a post-mortem.

**Use it in the daily:** walk the board and call out the age of each in-progress item. Anything approaching your 85th percentile cycle time gets attention now, before it becomes an exception.

> "This one's at 11 days. Our 85th percentile is 12. What does it need?"

**This single practice does more for cycle time than most process changes.**

---

## Service Level Expectation (SLE)

**Definition:** a forecast of how long an item should take, stated with a probability.

> "85% of items finish within 12 days."

Derived directly from your cycle time percentiles, not negotiated with stakeholders. Review quarterly.

**Use it to:** set expectations without promising dates per item, and to trigger action when an item breaches it.

---

## Reading the numbers together

| Pattern | What it means | What to do |
|---|---|---|
| High WIP, long cycle time | Too much started, not enough finished | Lower WIP limits; swarm on the oldest item |
| Stable cycle time, wide spread | Unpredictable system — worse for stakeholders than slow | Reduce item size variation; find the exception items' common cause |
| Throughput up, cycle time up | Items got smaller and more numerous, not faster | Check item sizes before celebrating |
| Cycle time fine, lead time terrible | Queue before work starts | Prioritisation and intake problem, not a team problem |
| Low flow efficiency | Waiting dominates | Attack the queues: hand-offs, approvals, environments, reviews |
| Throughput volatile | Interruptions, or highly variable item sizes | Separate work types; class-of-service them |
| Everything stable, nobody happy | Metrics may be measuring the wrong thing | Check outcomes, not just flow |

---

## Pitfalls

- **Averages.** Use percentiles. An average cycle time hides exactly the tail that damages trust
- **Comparing teams.** Different work, different item sizes, different definitions. Meaningless and corrosive
- **Targets.** Set a cycle time target and item size will shrink to meet it. Track as signal, never target
- **Counting blocked time out.** Tempting, and wrong — waiting is part of the customer's experience
- **Mixing work types.** Features and incidents have different distributions; forecast them separately
- **Measuring individuals.** Guarantees gaming and destroys collaboration. Team level only
- **Too little data.** Fewer than 20 completed items and percentiles mean little; say so rather than reporting them
