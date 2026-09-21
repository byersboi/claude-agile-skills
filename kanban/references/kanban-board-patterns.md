# Kanban Board Design Patterns

Board designs for different kinds of team, with the policies that make each work. For the Kanban method itself, see the `kanban` skill.

## Design principles

1. **The board shows reality, not the org chart.** Map how work actually flows, including the waiting
2. **Make queues visible.** A "waiting for review" column is uncomfortable and therefore valuable
3. **Every column has an explicit policy** — what it means for an item to be in it, and what must be true to leave
4. **WIP limits on columns, not just in total** — a limit only on "in progress" hides the queue in front of testing
5. **Start with the board you have, then evolve it.** A perfect board designed in a workshop rarely survives a week

**Diagnostic question when designing:** where does work wait? Those places need columns, not the activities people perform.

---

## Pattern 1: Basic development flow

The default for a product team.

```
┌─────────┬─────────────┬─────────────┬────────────┬──────┐
│ Backlog │ In progress │   Review    │    Test    │ Done │
│         │    (4)      │    (2)      │    (3)     │      │
│         ├──────┬──────┼──────┬──────┼─────┬──────┤      │
│         │ Doing│ Done │ Doing│ Done │Doing│ Done │      │
└─────────┴──────┴──────┴──────┴──────┴─────┴──────┴──────┘
```

**Split "doing" and "done" within each stage.** The "done" sub-column is the queue — it shows work finished at one stage and waiting for the next, which is where most of your cycle time lives.

**Policies:** to enter Review, the item has tests and a description of what changed. To leave Test, acceptance criteria are demonstrably met.

**WIP limits:** start at team size minus one for the main stage. Tighter on review and test — those are where queues form.

---

## Pattern 2: Support and operational work

Variable arrival, variable urgency, no Sprint boundary.

```
┌─────────────┬─────────┬─────────────┬────────────┬──────┐
│   Triage    │  Ready  │ In progress │  Verify    │ Done │
│             │   (6)   │    (3)      │    (2)     │      │
├─────────────┼─────────┼─────────────┼────────────┼──────┤
│ Expedite    │ ▓▓▓ swimlane — WIP limit 1, drops everything│
├─────────────┼─────────┼─────────────┼────────────┼──────┤
│ Standard    │         │             │            │      │
├─────────────┼─────────┼─────────────┼────────────┼──────┤
│ Maintenance │         │             │            │      │
└─────────────┴─────────┴─────────────┴────────────┴──────┘
```

**Classes of service as swimlanes.** Expedite has a WIP limit of one and an explicit policy: it pre-empts other work, and using it has a cost someone has to own.

**Key policies:** triage within 4 hours; an SLE per class ("standard items complete within 5 days, 85% of the time"); expedite requires named authorisation.

**Why it works:** it makes the cost of interruption visible. Teams that skip the expedite limit end up with every item expedited.

---

## Pattern 3: Mixed team — product work plus support

The most common real-world situation and the one that breaks naive boards.

```
┌─────────┬─────────────┬────────────┬──────┐
│ Backlog │ In progress │   Verify   │ Done │
├─────────┼─────────────┼────────────┼──────┤
│ Support │  (2)  ▓▓▓▓▓▓│            │      │  ← capacity allocation: 30%
├─────────┼─────────────┼────────────┼──────┤
│ Product │  (3)  ░░░░░░│            │      │  ← 70%
└─────────┴─────────────┴────────────┴──────┘
```

**Capacity allocation, not just WIP limits.** Decide the split in advance — "30% of our capacity goes to support" — and enforce it through the per-swimlane WIP limits. Without it, support consumes everything and product work never finishes.

**Review the allocation monthly** against what actually happened. If the team is permanently at 50% support against a 30% allocation, the problem is upstream of the board.

---

## Pattern 4: Discovery and delivery (dual track)

For teams doing continuous discovery alongside delivery.

```
DISCOVERY   ┌──────────┬───────────┬────────────┬──────────┐
            │ Ideas    │ Research  │ Validating │ Ready    │
            │          │   (2)     │    (2)     │ to build │
            └──────────┴───────────┴────────────┴──────────┘
                                                      ↓
DELIVERY    ┌──────────┬───────────┬────────────┬──────────┐
            │ Ready    │ Building  │  Verify    │ Released │
            │          │   (3)     │    (2)     │          │
            └──────────┴───────────┴────────────┴──────────┘
                                                      ↓
                                            ┌──────────────┐
                                            │ Measuring    │  ← did it work?
                                            └──────────────┘
```

**The "Measuring" column is the one everyone leaves off,** and it's the only one that tells you whether the work was worth doing. Items sit there for a defined period with a named owner and an agreed measure.

**Policy for "Ready to build":** validated with real users, sized, and with a stated success measure. Without the last of these, the measuring column stays empty.

---

## Pattern 5: Multi-team / programme board

Not a scaled team board. It carries only what spans teams — see `agile-delivery-manager/references/programme-board-template.md` for the full treatment.

**In short:** swimlane per team, plus a cross-team lane for integration and cut-over work that belongs to nobody, plus an external lane for what you depend on but don't control. Feature-level cards, not stories.

---

## Pattern 6: Personal / Scrum Master board

For your own work, which otherwise lives in your head.

```
┌────────┬──────────┬─────────────┬────────┬──────┐
│ This   │ Waiting  │ In progress │ Blocked│ Done │
│ quarter│ on others│    (3)      │        │      │
└────────┴──────────┴─────────────┴────────┴──────┘
```

**"Waiting on others" is the important column** — it's most of a Scrum Master's or delivery manager's work, and it's invisible until you make a column for it. Age the cards in it; anything over a fortnight needs chasing or dropping.

---

## Common board smells

| Smell | What it means | Fix |
|---|---|---|
| Everything in "In progress" | Board doesn't reflect real stages | Add the stages where work actually waits |
| No WIP limits | Not doing Kanban, just visualising | Start loose (team size), tighten as flow improves |
| WIP limits routinely breached | Limits are decoration | Agree what happens when the limit is hit — swarm, or don't start |
| Cards sit for weeks with no discussion | The board isn't being walked | Walk it daily, right to left, calling out item age |
| No blocked marker | Blockers invisible, so nothing gets escalated | Flag blocked items and record the *reason* and *since when* |
| Columns per person | Optimising for utilisation, not flow | Columns are stages of work, never people |
| Endless "ready" column | Upstream over-producing | Limit the ready queue too |
| Board doesn't match how work happens | People stop using it | Redesign it with the team in 30 minutes; it's meant to change |

---

## Evolving a board

Review the design quarterly, or whenever the team says the board is annoying — that's a signal, not a complaint.

Three questions:
1. **Where does work sit longest?** Does that place have its own column and limit?
2. **What do we track outside the board?** Anything in a side spreadsheet belongs on the board or shouldn't exist
3. **Which policies do we routinely ignore?** Fix them or delete them — an ignored policy teaches everyone that policies are optional
