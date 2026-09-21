# PI Planning Facilitation Guide

A step-by-step guide to running a two-day planning event for 5–12 teams. Applies to SAFe PI Planning and to any equivalent big-room quarterly planning. For whether to scale at all, see the `agile-scaling` skill.

## What it's for

One purpose: **teams plan together, in the same space, so dependencies surface now rather than in week six.** Everything else — the vision briefing, the confidence vote, the retrospective — serves that. If teams leave with a plan they didn't build, the event has failed regardless of how well it ran.

---

## Preparation (the four weeks before)

Preparation is 80% of the outcome. An unprepared PI Planning is two days of expensive confusion.

**Four weeks out**
- Confirm dates, venue and attendance. Everyone who will do the work attends — not their representatives
- Product Management drafts the top ten features, ordered, with clear outcomes
- Architecture drafts any enablers and constraints

**Two weeks out**
- Features refined enough that teams can size and sequence them; not decomposed for them
- Known external dates on the calendar: supplier releases, regulatory dates, freeze periods, holidays
- Capacity drafted per team, including on-call, support and leave

**One week out**
- Send the pre-read: vision, top features, known constraints, agenda. People read it if it's short
- Brief the Business Owners on what they'll be asked to do (value scoring, being available)
- Walk the room or the board; test the tooling with remote attendees

**Facilitator's readiness check:** if you cannot answer "what are the top five features and what outcomes do they serve?" a week before, postpone. A delayed event beats a wasted one.

---

## Day one

| Time | Session | Notes |
|---|---|---|
| 09:00 | Business context | A senior leader, 20 minutes, on where the organisation is and why this matters. Not a deck read aloud |
| 09:30 | Product vision | Product Management: top features and the outcomes behind them. 45 min including questions |
| 10:15 | Architecture and practices | Constraints, enablers, and anything changing technically. Keep it to 20 minutes |
| 10:45 | Planning context and agenda | The facilitator: how the two days run, what "done" looks like |
| 11:00 | **Team breakouts 1** | Teams draft objectives, sequence work into iterations, identify dependencies and risks |
| 13:00 | Lunch | |
| 14:00 | **Team breakouts continue** | Facilitators circulate; dependency board fills |
| 16:00 | **Draft plan review** | Each team, 5 minutes: objectives, dependencies, risks. Strictly timed |
| 17:00 | Management review and problem-solving | Leadership adjusts scope, resolves conflicts, decides on the problems teams surfaced |

**Facilitating breakouts:** circulate, don't hover. The three questions worth asking a team: *What are you depending on that isn't on the board? Who's depending on you? What would make this plan fail?*

**The dependency board is the artefact that matters.** Every dependency gets a card with both teams named and the iteration it's needed by. A dependency without a name on both sides is a wish.

---

## Day two

| Time | Session | Notes |
|---|---|---|
| 09:00 | Planning adjustments | Leadership explains overnight decisions — scope changes, priority calls. Be explicit about what changed and why |
| 09:15 | **Team breakouts 2** | Teams rework plans against the adjustments; finalise objectives |
| 11:00 | **Final plan review** | Each team presents final objectives, dependencies, risks |
| 13:00 | Lunch | |
| 14:00 | **Risk ROAMing** | Every risk: Resolved / Owned / Accepted / Mitigated. Each one named and dispositioned in the room |
| 15:00 | **Confidence vote** | Fist-of-five, per team then across the train |
| 15:30 | Plan rework if needed | Only if confidence is low — and actually do it |
| 16:00 | Planning retrospective and next steps | What to change for next time; where the plan lives; when the first sync is |

**The confidence vote is the event's integrity test.** Average below three means replan — not "note the concern and proceed". If a facilitator has never seen a train replan after a low vote, the vote is decorative and everyone knows it.

**ROAM properly.** "Accepted" is a legitimate answer given consciously by someone with the authority to accept it. What isn't legitimate is a risk list nobody dispositions.

---

## Remote and hybrid

Two days on video is brutal. Adjust rather than transplant:

- **Three shorter days** beat two long ones. Four hours of plenary per day, maximum
- **One digital board**, built and tested in advance, with a clear area per team and a dependency zone
- **Breakout rooms pre-configured** with the right people in each
- **A co-facilitator per breakout** whose job is chat, timekeeping and dragging in the people a team needs
- **Dependency negotiation needs a channel** — a named room where two teams can talk without leaving the event
- **Remote speaks first** in hybrid. Always

---

## Common failure modes

| Failure | Cause | Fix |
|---|---|---|
| Teams presented a plan rather than making one | Features decomposed in advance by architects or leads | Bring features, not tasks; let teams break them down |
| Dependencies discovered in week six | Breakouts too short; no dependency walk | Protect breakout time; make the dependency board mandatory |
| Confidence vote always high | Voting isn't safe | Anonymous voting; visibly act on a low vote once and the problem disappears |
| Objectives are feature lists | Nobody asked for outcomes | "What will be true afterwards that isn't true now?" |
| Plan treated as a commitment | Leadership frames it as a contract | State explicitly at the open: this is intent, revisited every iteration |
| Two days, no decisions | Business Owners absent or without authority | Get decision-makers in the room, or don't run the event |
| Same problems every PI | No planning retrospective, or nothing acted on | Close with the retro; act on one thing before the next PI |

---

## After the event

- Publish the plan and dependency board within 24 hours, in a place teams actually use
- Diarise the cross-team sync cadence immediately — the dependency board needs a weekly walk or it goes stale within a fortnight
- Capture the ROAMed risks somewhere with owners and review dates
- Revisit objectives at each iteration boundary. A PI plan that hasn't changed by week four wasn't a plan; it was a prediction nobody checked
