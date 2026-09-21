# Improvement Metrics Templates

Templates for tracking whether improvements actually improved anything. For the tools themselves see `references/improvement-tools-reference.md`; for metric definitions and interpretation see the `agile-metrics` skill.

## The rule this file exists to enforce

**An improvement without a measure is an opinion.** Not every change needs a chart — but every change needs an agreed way of knowing whether it worked, decided *before* the change, not argued about afterwards.

Three things to agree up front:
1. **The measure** — what will move if this works
2. **The current value** — the baseline, taken before the change
3. **When you'll look** — a date, in the diary

---

## 1. Improvement experiment card

One per retro action. Keep it on the board, next to the delivery work.

```
IMPROVEMENT: Limit WIP to 4 items in progress
Owner: <name>            Started: 21 Sep      Review: 19 Oct

PROBLEM
Items sit in progress for weeks; we finish in a rush at the end
of the Sprint.

HYPOTHESIS
If we limit WIP to 4, we'll finish items sooner and more evenly.

MEASURE          BASELINE        TARGET        ACTUAL
85th %ile
cycle time       14 days         < 10 days     ___
Items finished
in last 3 days
of Sprint        60%             < 30%         ___

WHAT WE'LL DO IF IT WORKS: keep the limit; try 3
WHAT WE'LL DO IF IT DOESN'T: revert, and look at hand-offs instead
```

**The two bottom lines matter most.** Agreeing the abandon condition in advance is what stops a failed improvement becoming a permanent process nobody admits didn't work.

---

## 2. Retro action tracker

The minimum viable version, and the one most teams need. First item on every retro agenda.

| Action | Owner | Agreed | Due | Status | Did it work? |
|---|---|---|---|---|---|
| Limit WIP to 4 | <name> | 7 Sep | 21 Sep | Done | Cycle time 14 → 11 days. Keep |
| Automate the release checklist | <name> | 7 Sep | 21 Sep | Not started | Blocked — no capacity. Re-agree or drop |
| Invite ops to the review | <name> | 24 Aug | 7 Sep | Done | They came, found two issues early. Keep |

**Read it as a metric in itself:** the proportion of retro actions actually completed. Below half, and the problem isn't the actions — it's that improvement work isn't real work in this team. Fix that before generating more actions.

---

## 3. Improvement themes tracker (for the SM or coach)

Individual actions are the team's. Recurring themes are yours.

| Theme | Sprints raised | Team-fixable? | What I'm doing |
|---|---|---|---|
| Waiting on external approvals | 6, 7, 9, 10, 11 | No — organisational | Raised with <role>; gathering wait-time data for the case |
| Unclear acceptance criteria | 8, 9, 10 | Partly | Refinement format changed; watching |
| Environment instability | 4, 6, 7, 9, 11 | No — shared infrastructure | Escalated; on the programme risk log |

**The signal:** a theme raised three Sprints running that the team cannot fix is not a retrospective item. It is an impediment you own, and continuing to "discuss it in the retro" teaches the team that raising things is pointless.

---

## 4. Sprint-over-sprint improvement dashboard

Four measures, reviewed quarterly rather than every Sprint — improvement signal is slow and Sprint-level noise will mislead you.

| Measure | How to get it | What good movement looks like |
|---|---|---|
| **85th percentile cycle time** | Scatterplot of completed items | Falling, and the spread narrowing |
| **Throughput** | Items completed per Sprint | Stable or rising, with lower variability |
| **Retro actions completed** | Action tracker | Above 70% |
| **Escaped defects** | Defects found after release | Falling, or flat while throughput rises |

**Add one outcome measure** relevant to your product — adoption, support volume, task success rate. Process improvement that doesn't eventually move an outcome is motion, not progress.

**How to present it:** movement over four quarters, with annotations for what changed. Never as a target to hit; the moment any of these becomes a target, it stops measuring what you think it measures.

---

## 5. Flow efficiency baseline

The single most persuasive number for leadership, because it's usually shocking.

> **Flow efficiency = process time ÷ lead time**
>
> Pick ten recently completed items. For each: total elapsed days, and days where someone was actively working on it.
>
> | Item | Lead time | Process time | Efficiency |
> |---|---|---|---|
> | 1 | 22 days | 3 days | 14% |
> | 2 | 9 days | 2 days | 22% |
> | … | | | |
> | **Median** | **15 days** | **2.5 days** | **17%** |

**The conversation this enables:** "The team isn't slow. Work spends 83% of its life waiting — for review, for environments, for approvals. Making the team faster addresses 17% of the problem."

Re-baseline every six months. Most teams start between 15% and 30%; above 40% is genuinely good.

---

## Anti-patterns

| Anti-pattern | Consequence | Fix |
|---|---|---|
| Measure chosen after the change | Whatever moved becomes the justification | Agree the measure and baseline first |
| Improvement measured by activity | "We ran 12 retros" says nothing | Measure outcomes, not ceremonies |
| Targets set on improvement metrics | Gaming; cycle time falls because items get split smaller | Track as signal; never as a target |
| Everything measured | Nobody reads any of it | Four measures, quarterly |
| No abandon condition | Failed experiments become permanent process | Write the abandon condition on the card |
| Actions tracked, themes ignored | The same systemic problem recurs for a year | Keep a themes tracker; own the systemic ones yourself |
