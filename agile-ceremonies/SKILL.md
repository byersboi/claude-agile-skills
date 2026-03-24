---
name: Agile Ceremonies
description: This skill should be used when the user asks about "agile ceremonies", "agile meetings", "facilitating ceremonies", "sprint planning facilitation", "retrospective facilitation", "daily standup facilitation", "sprint review facilitation", "backlog refinement", "backlog grooming", "story mapping", "user story workshop", "definition of ready", "definition of done", "DoR", "DoD", "acceptance criteria", "Gherkin", "Given When Then", "working agreements", "team charter", "inception workshop", "kickoff workshop", "release planning", "PI planning facilitation", "facilitation techniques agile", "diverge converge", "liberating structures", "async standup", "walking standup", "consolidated demo", "cross-team demo", "capacity planning sprint", or needs help planning or running any agile ceremony or workshop.
version: 1.0.0
---

# Agile Ceremonies

Ceremonies (also called events or meetings) are the primary inspection-and-adaptation mechanisms in agile frameworks. Effective ceremonies create shared understanding, surface impediments, and produce actionable outputs. Ineffective ceremonies are compliance theatre that erode team morale and trust.

## Principles for Effective Facilitation

1. **Clear purpose before structure**: Every ceremony should have a stated purpose, desired outcomes, and agenda shared in advance
2. **Silence before discussion**: Individual reflection before group discussion prevents anchoring and groupthink
3. **Visible outputs**: Use a physical or digital board — not just conversation — to capture discussion
4. **Timeboxing**: Set and honour time limits for each segment; use a visible timer
5. **Psychological safety first**: Open with connection; close with commitment
6. **Close with actions**: Every ceremony ends with ≥1 named, owned, time-bound action item

---

## Sprint Planning

**Purpose**: Create a shared plan for the Sprint, including Sprint Goal and Sprint Backlog.

**Timebox**: ≤ 8 hours for 1-month Sprint (scale proportionally)

**Agenda**:
1. **Why** (30 min): PO presents Sprint Goal proposal; team discusses and refines it
2. **What** (60–90 min): Team selects items from Product Backlog based on capacity and Sprint Goal; PO clarifies
3. **How** (remaining time): Developers decompose selected items into tasks ≤ 1 day; create Sprint Backlog

**Capacity Planning**:

Before selecting backlog items, establish the team's actual available capacity for the sprint. Do not assume everyone is 100% available.

**Step 1 — Calculate normal capacity per person**:
Start with working hours per day, minus time lost to meetings, ceremonies, and non-sprint activities. A common baseline is 6 productive hours per day for a full-time team member in a typical sprint.

**Step 2 — Apply a focus factor**:
Not all productive hours are available for sprint work. Interruptions, context switching, ad-hoc requests, and general overhead mean the realistic figure is lower. An 80% focus factor is a common starting point — giving 4.8 usable hours per person per day, or approximately 48 hours over a 10-day sprint.

Adjust the focus factor to reflect your team's actual context. A team working in a noisy, interrupt-heavy environment may need 70% or lower. A mature, well-protected team may sustain 85–90%.

**Step 3 — Deduct known capacity draws**:

| Deduction type | Description |
|---|---|
| **Spikes** | Technical investigation or research tasks not estimated as story points — deduct the estimated hours directly |
| **Planned absence** | Leave, training, travel, bank holidays — deduct the actual hours unavailable |
| **Unplanned absence** | Track retrospectively; use to inform capacity planning in future sprints |

**Step 4 — Express as actual capacity and percentage**:
Sum each person's remaining hours after deductions. Express as a percentage of normal capacity for easy communication at sprint planning. A team running at 60% capacity should select significantly less work than a team at 90%.

**Example** (illustrative, generic):

| Team member | Normal (hrs) | Spikes | Planned absence | Actual capacity | Capacity % |
|---|---|---|---|---|---|
| Person A | 48 | 5 | 8 | 35 | 73% |
| Person B | 48 | 0 | 16 | 32 | 67% |
| Person C | 48 | 0 | 0 | 48 | 100% |
| **Total** | **144** | **5** | **24** | **115** | **80%** |

**Using capacity at sprint planning**: Compare total available hours against the estimated effort for candidate backlog items. If the team uses story points, capacity provides a sanity check — does the total estimated effort feel proportionate to available hours? If the team uses hour-based estimates, map directly.

**Facilitation tips**:
- Calculate capacity before the planning session, not during it — it slows the meeting
- Share the capacity summary at the start of the What section so the team has a shared anchor
- Start with the Sprint Goal, not the backlog list — items should serve the goal
- Use capacity as a guide, not a hard ceiling — the team's judgement about what is achievable matters
- If items can't be broken down sufficiently, they need refinement — don't plan unrefined items

---

## Daily Scrum

**Purpose**: Inspect progress toward Sprint Goal; adapt the Sprint Backlog plan.

**Timebox**: 15 minutes maximum

**Format options**:
- Classic 3 questions: Yesterday / Today / Blockers (team-centric, not SM-centric)
- Walk the board: Review each in-progress item on the Sprint Backlog; discuss blockers
- Sprint Goal focus: "What did we do yesterday to advance the Sprint Goal? What will we do today?"

**Structure** (total 15 mins):

| Segment | Time | Purpose |
|---|---|---|
| Kickoff | 2–3 mins | Brief focus check; surface energy or context needed |
| Team updates | ~10 mins | Each person: 60–90 seconds maximum |
| Blockers | 2–3 mins | Name blockers; assign owner; take offline immediately |
| Close | 1 min | Any quick announcements; confirm follow-ups |

**Standup variations** — rotate based on team context:

| Variation | How it works | Best for |
|---|---|---|
| **Walking standup** | Team walks between locations while talking | Co-located teams; breaks up desk-bound routine |
| **Kanban board style** | Talk through each in-progress card left to right | Teams with high WIP visibility needs |
| **Async standup** | Written updates in Slack/Teams using a bot (e.g. Geekbot, Standuply) before the standup time | Remote teams across time zones; reduces meeting fatigue |

**Blocker handling**: When a blocker is named, immediately assign an owner and take it offline. Do not try to solve blockers during the standup — it derails the timebox and excludes uninvolved team members.

**Facilitation tips**:
- Developers run this event — SM facilitates only when needed
- Start at the same time and place daily
- If discussions emerge, capture them and take offline ("let's park that and pick it up after the standup")
- Track impediments visibly — if they're not on the board, they don't exist

---

## Backlog Refinement

**Purpose**: Ensure the Product Backlog is ready for upcoming Sprint Planning.

**Timebox**: Typically 5–10% of Sprint capacity; often one or two sessions per sprint.

**Target output**: Top of backlog items are small enough (≤ half a sprint day's work), well-understood, and meet a Definition of Ready (if the team uses one).

**Agenda**:
1. Review existing items: clarifications, re-estimation if needed
2. Break down large items (Epics → Features → Stories)
3. Add acceptance criteria
4. Estimate using team's chosen technique

**Facilitation tips**:
- PO sets agenda and orders items; team shapes them
- Use time limits per item to prevent rabbit holes
- Items that need significant investigation should trigger a spike, not unbounded discussion
- Aim to keep 2–3 sprints of refined items at the top of the backlog

---

## Sprint Review

**Purpose**: Inspect the Increment and adapt the Product Backlog based on feedback.

**Timebox**: ≤ 4 hours for 1-month Sprint

**Agenda**:
1. **Context** (10 min): SM or PO: Sprint Goal, what was completed, what wasn't
2. **Demo** (30–60 min): Team demonstrates working product; stakeholders interact — not just watch
3. **Feedback** (20–30 min): What's working? What's missing? What changed in the environment?
4. **Backlog adaptation** (20 min): PO adjusts backlog based on feedback; team forecasts next sprint

**Facilitation tips**:
- Frame it as a collaboration, not a show — invite stakeholders to try the product
- Prepare a clear demo flow; assign demonstrators; test everything beforehand
- Celebrate completed work before diving into feedback
- Capture feedback visibly; make clear what will be added to the backlog
- If nothing was completed, still run the review — transparency about scope and impediments is valuable

**Consolidated cross-team sprint demo** (for scaled contexts with multiple squads):

When multiple teams are delivering related products, individual team reviews can create silos — teams don't know what others have shipped, and stakeholders attend multiple disconnected sessions. A consolidated sprint demo addresses this.

**Format**:
- Single session every sprint featuring customer-impacting features from all squads
- Broadcast style — presenters demo, audience observes; questions via chat or follow-up (not interruptions)
- Scope limited to completed, release-ready features only — no technical debt, no work-in-progress
- Demos run on deployed environments; no slides or mockups
- Rotating chair (different team leads the session each sprint)

**Pre-demo preparation**: Each squad's PO or lead confirms their demo content in advance with the session chair. Only features that are complete and can be demonstrated on a live environment are included.

**Who benefits**: Marketing (understand what's shipping), Customer Success (prepare for customer questions), other squads (awareness of cross-team dependencies and progress), leadership (real visibility without status reports).

**What to include**: Completed features, before/after comparisons where relevant, key metrics if available. Optionally: note any significant sprint disruptions (urgent requests that changed scope) so the audience understands what was deprioritised and why.

---

## Sprint Retrospective

See **`references/retrospective-formats.md`** in the `scrum` skill for detailed formats.

**Purpose**: Inspect how the team worked and create an improvement plan.

**Timebox**: ≤ 3 hours for 1-month Sprint

**Core structure** (regardless of format):
1. **Set the stage** (5–10 min): Check-in; prime directive
2. **Gather data** (10–15 min): Silent individual writing
3. **Generate insights** (15–20 min): Discussion; pattern identification
4. **Decide on actions** (15–20 min): Select ≤3 improvements; make them specific and owned
5. **Close** (5 min): Retro on the retro; appreciation

---

## Definition of Ready & Definition of Done

### Definition of Ready (DoR)

The DoR is a checklist that ensures a backlog item is genuinely ready to enter Sprint Planning. The team defines it; the PO ensures items meet it before refinement is complete.

**DoR checklist** (adapt to your context):

- [ ] Written as a user story or equivalent (clear who benefits and why)
- [ ] Acceptance criteria defined — ideally in Given/When/Then (Gherkin) format
- [ ] Story is small enough to complete within the sprint (no item larger than half the sprint)
- [ ] Dependencies identified and either resolved or explicitly accepted
- [ ] Business value is understood and can be articulated
- [ ] Team has estimated it (no outstanding "we need to investigate first" blockers)
- [ ] UI/UX designs attached or confirmed not required
- [ ] Technical feasibility confirmed — no open architectural unknowns
- [ ] Data, API, or integration requirements identified
- [ ] Test cases or test approach defined

**Gherkin format for acceptance criteria**:
```
Given [a context or precondition]
When [an action is taken]
Then [an expected outcome occurs]
```

Example:
```
Given a user is logged in and viewing their order history
When they click on a completed order
Then they see the order details including items, date, and total cost
```

**Caution**: Apply the DoR as a conversation guide, not a bureaucratic gate. If items repeatedly fail it, that points to an upstream problem — refinement not happening early enough, or PO not engaging with the team before planning.

---

### Definition of Done (DoD)

The DoD is the team's shared commitment to quality. An item is only Done when every criterion is met. It applies to every item, every sprint — no exceptions without explicit team agreement.

**DoD checklist** (adapt to your context):

- [ ] Code complete and merged to the agreed branch
- [ ] Peer code review completed (at least one reviewer)
- [ ] Unit tests written and passing
- [ ] Functional testing completed against acceptance criteria
- [ ] No critical or high-severity bugs introduced
- [ ] UI/UX validated against designs (where applicable)
- [ ] API contracts met and tested (where applicable)
- [ ] Performance benchmarks met (where applicable)
- [ ] Security requirements addressed (where applicable)
- [ ] Documentation updated (user-facing and/or technical)
- [ ] Demonstrated to or accepted by the Product Owner
- [ ] Deployed to staging (or production, depending on team's release cadence)

**Team confidence check**: Before marking an item Done, the team should be able to say with confidence: "We would be comfortable releasing this to users right now." If not, it is not Done.

**DoD vs. acceptance criteria**: Acceptance criteria are specific to one story (does this feature work as specified?). The DoD applies to every story (does every story meet our quality bar?). Both must be met.

**Evolving the DoD**: Review the DoD in retrospectives. As the team matures, the bar should rise — adding automated tests, performance gates, accessibility checks. The DoD should reflect where the team wants to be, not just where they are.

---

## Backlog / Story Mapping

**User Story Mapping** (Jeff Patton's technique): A visual approach to understanding user journeys and creating a structured backlog.

**How to run**:
1. **Identify users and goals**: Who are we building for? What are they trying to achieve?
2. **Map activities** (top row, left to right): High-level activities in sequence (the user journey backbone)
3. **Map tasks** (below activities): Specific tasks within each activity
4. **Slice for releases** (horizontal cuts): Group tasks into releases by value, not completion

**Output**: A map showing the full user journey, with releases as horizontal slices across the map. Enables scope conversations grounded in user value.

---

## Working Agreements / Team Charter

Run at team formation or when norms need resetting.

**Facilitation format**:
1. **Individual brainstorm** (10 min): What do you need from this team to do your best work?
2. **Share and cluster** (15 min): Group similar ideas
3. **Discuss and agree** (20 min): For each cluster, agree on a norm (specific, observable behaviour)
4. **Document and display** (5 min): Make agreements visible on the team wall/space

**Topics to cover**: Core hours / availability, communication channels, meeting norms, definition of done, how decisions are made, how conflicts are resolved, quality standards.

**Review periodically**: Revisit working agreements in retrospectives, especially after team changes.

---

## Inception / Kickoff Workshop

Use at the start of a new product, programme, or major initiative.

**Purpose**: Align the team on vision, scope, users, risks, and ways of working before the first sprint.

**Typical agenda (1–2 days)**:
1. Vision and product goal
2. User identification and empathy mapping
3. User story mapping or impact mapping
4. High-level backlog creation and prioritisation
5. Risk identification
6. Team working agreements
7. Technical architecture overview
8. Definition of Done and Definition of Ready
9. First sprint planning

---

## Facilitation Techniques (Quick Reference)

| Technique | Purpose | How |
|---|---|---|
| 1-2-4-All | Inclusive discussion | Think alone → pair → group of 4 → all |
| Dot voting | Prioritisation | Each person gets N dots to place on options |
| Fist of Five | Consent | Rate agreement 0–5 simultaneously |
| Round Robin | Equal voice | Each person speaks once before anyone speaks twice |
| Parking Lot | Manage scope | Visible list of important-but-off-topic items |
| Timebox | Pace control | Visible timer; honour when it expires |
| Paired affinity | Clustering | Silently group similar stickies together |

## Additional Resources

- **`references/retrospective-formats.md`** — Full set of retrospective formats (see `scrum` skill)
- **`references/facilitation-tools.md`** — Digital tools for remote ceremony facilitation
