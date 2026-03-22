---
name: Value Stream Mapping
description: This skill should be used when the user asks about "value stream mapping", "VSM", "value stream", "current state map", "future state map", "lead time analysis", "wait time", "process efficiency", "lean waste", "muda", "seven wastes", "8 wastes", "handoffs", "flow efficiency", "value-added time", "value stream workshop", "development value stream", "operational value stream", "improvement backlog from VSM", "Theory of Constraints", "bottleneck analysis", "process mapping", "VSM facilitation", "value stream metrics", or wants to analyse end-to-end flow from request to delivery.
version: 1.0.0
---

# Value Stream Mapping

Value Stream Mapping (VSM) is a lean management technique for visualising the end-to-end flow of work from the moment a customer request enters a system to the moment value is delivered. It makes two things visible that are otherwise invisible: where time is actually spent, and how much of that time genuinely adds value to the customer.

VSM originated at Toyota as part of the Toyota Production System, where it was called "material and information flow mapping". It was popularised for Western practitioners by Mike Rother and John Shook in *Learning to See* (1998). Its application has since expanded from manufacturing into software development, IT operations, and knowledge work more broadly.

The central insight of VSM is that most lead time in any system is not working time — it is waiting time. Teams are often shocked to discover that a piece of work that takes three days of active effort spends three weeks sitting in queues. VSM makes that gap visible, undeniable, and actionable.

## What Is a Value Stream?

A value stream is the sequence of activities required to deliver a product, service, or feature to a customer. It includes every step — from the triggering request, through analysis, design, development, review, testing, and deployment, to live operation. It includes the work steps and the wait between them.

A value stream has a clear customer (internal or external), a clear trigger (what starts the flow), and a clear end point (when value is delivered to the customer). If any of these three are ambiguous, the first task is to agree on them before mapping begins.

**What a value stream is not**: A value stream is not a team's sprint backlog, a delivery pipeline, or a process diagram showing how things should work. It is a map of how things actually work — including the handoffs, delays, queues, and rework loops that process diagrams typically omit.

## Types of Value Streams

The SAFe (Scaled Agile Framework) distinction between operational and development value streams is useful even outside SAFe organisations.

**Operational Value Streams** describe the recurring flow of work that delivers ongoing products or services to end customers. Examples: processing a customer order, handling a support ticket, onboarding a new user, deploying a release. These are repeatable, relatively stable flows that run continuously.

**Development Value Streams** describe the flow of work that creates or enhances the systems, products, or capabilities that operational value streams depend on. In software organisations, this means the flow from a feature idea (or requirement) through development, testing, and deployment into production.

| Type | Focus | Typical Trigger | Typical End Point |
|---|---|---|---|
| Operational | Value delivery to end customer | Customer request or event | Customer receives service |
| Development | Capability creation or improvement | New feature, bug, or enabler | Feature live in production |

In practice, many organisations map their development value stream first (because it is more tractable for a cross-functional agile team) before tackling the operational value stream, which often involves more organisational complexity.

## VSM Workshop Setup

A VSM session is a facilitated workshop, not an analysis exercise conducted by one person in isolation. The map produced by a group of practitioners who do the work is orders of magnitude more accurate — and more credible — than one assembled from documentation or interviews alone.

**Who to involve**:
- Representatives from every step in the value stream: product, design, engineering, QA, security review, operations/platform, and any approval or compliance stages
- A facilitator (the Scrum Master, Agile Coach, or Delivery Manager) who understands the mapping technique and can keep the group objective
- A senior stakeholder sponsor for at least the opening session — their presence signals that this is real, not a box-ticking exercise
- Avoid: managers who will speak for the people doing the work. The people doing the work must be in the room.

**Duration**:
- Current state mapping: half a day to a full day depending on complexity
- Analysis and waste identification: two to three hours
- Future state design: half a day
- Planning and action: two hours

**Physical vs. digital**:
- Physical (sticky notes on a wall or paper roll) is superior for collaborative energy, real-time editing, and group sense-making. It is harder to preserve and share afterwards.
- Digital tools (Miro, Mural, LucidChart) work well for distributed teams and produce artefacts that are easier to circulate. They require more facilitation discipline to keep everyone engaged.

**Prerequisites**:
- Agree on the work type to map before the session (e.g., "standard new feature from approved concept to production") — trying to map everything in one session leads to an unusable composite
- Gather baseline data if available: average cycle times per stage, defect rates, rework rates. The map should be validated against data, not just drawn from memory.
- Book a dedicated room or virtual session block — interruptions destroy the collaborative state that VSM relies on

## Current State Mapping

The current state map is the honest picture of how work flows today. Its purpose is not to document what should happen — it is to surface what actually happens, including the informal steps, workarounds, and waiting periods that nobody has ever written down.

**Running the current state session**:

1. **Define the scope**: Agree on the customer, the trigger event, and the end point. Write these on the map before touching process steps.

2. **Walk the value stream**: Starting from the customer's request and working left to right, identify every step in the process. Each step should be something that consumes time or resource — not an ideal phase label.

3. **Capture process steps**: For each step, record:
   - Step name and who performs it
   - **Process Time (PT)**: How long this step takes when someone is actively working on it
   - **Wait Time (WT)**: How long work sits waiting before this step begins, or waiting after this step to move on
   - **WIP**: How many items are typically in-progress or queued at this step at any given time
   - **Rework/defect rate**: What percentage of items require rework at or after this step

4. **Map information flows**: Identify what information triggers work to move between steps (emails, tickets, alerts, meetings), and where information gaps or mismatches cause delays.

5. **Identify handoffs**: Mark every point where work is passed from one person, team, or system to another. Handoffs are high-risk points for delay, information loss, and quality degradation.

**VSM notation** (simplified for knowledge work):

| Symbol | Meaning |
|---|---|
| Process box | A step where active work occurs |
| Triangle / queue | Work waiting between steps |
| Arrow (push) | Work is pushed to the next step when done |
| Arrow (pull) | Work is pulled when the next step has capacity |
| Lightning bolt | Electronic information flow (e.g., ticket updated, alert fired) |
| Envelope | Manual information flow (e.g., email, meeting) |
| Data box | Metrics attached to a process or queue step |
| Timeline (bottom) | Alternating value-added and non-value-added time |

At the bottom of the map, draw a timeline: alternating bars showing the process time of each step and the wait time between each step. Sum these to calculate total lead time and total value-added time.

## Identifying Waste (Muda)

Muda is the Japanese term for waste — any activity that consumes time, resource, or effort without adding value from the customer's perspective. Toyota identified seven original wastes; a commonly accepted eighth was added for knowledge work.

In a software or knowledge-work context:

| Waste | Definition | Examples in Software/Knowledge Work |
|---|---|---|
| **Overproduction** | Producing more than is needed, sooner than needed | Features built before a business case is confirmed; documentation nobody reads; automated reports nobody reviews |
| **Waiting** | Idle time while work waits for the next step, a decision, an approval, or a dependency | PRs sitting unreviewed; tickets blocked on a Product Owner response; deployments waiting for a change approval board |
| **Transport** | Moving work or information from one place to another without adding value | Passing specifications through multiple layers; re-entering data between tools; status updates relayed through management chains |
| **Over-processing** | Doing more work on an item than the customer needs | Excessive documentation for low-risk changes; redundant review layers; gold-plating features beyond requirements |
| **Inventory** | Unfinished work accumulating in queues or backlogs | Large product backlogs; features built but not deployed; branches not merged; stories in "ready" for weeks |
| **Motion** | Unnecessary movement of people or effort to get work done | Chasing approvals across departments; attending meetings to get answers that could be written down; context switching between unrelated tasks |
| **Defects** | Work that does not meet quality requirements and must be reworked | Bugs found in UAT or production; requirements misunderstood and re-done; tests written after the fact that reveal design flaws |
| **Unused talent** | Failing to use the knowledge, skills, and creativity of the people doing the work | Teams not involved in requirement decisions; engineers excluded from architecture; testers only consulted at the end |

When reviewing the current state map, annotate each step and each queue with the primary waste type it represents. This transforms the map from a picture of how things work into a prioritised list of improvement targets.

**Categorising waste**: Not all waste is equal. Some waste is incidental (easy to remove with a simple change) and some is structural (requires organisational or process redesign). Mark each waste as:
- **Type 1 (incidental)**: Can be eliminated now, without changing fundamental process structure
- **Type 2 (structural)**: Requires deeper change — worth addressing, but needs planning

## Future State Mapping

The future state map is a design for how the value stream should work once identified wastes are addressed. It is not a utopian fantasy — it is the next achievable state, typically within a three-to-six month horizon.

**Designing the future state**:

Start with the longest queues and the biggest sources of waste. Apply lean flow principles:

**Continuous flow**: Where possible, eliminate queues between steps by enabling work to move directly from one step to the next without waiting. This often requires cross-functional teams where multiple skills are co-located, reducing handoffs.

**Pull systems**: Work should be pulled by a downstream step when it has capacity, rather than pushed by an upstream step when it finishes. Pull prevents upstream steps from producing faster than downstream steps can absorb, which is the root cause of inventory waste. Kanban WIP limits are a practical implementation of pull in knowledge work.

**Theory of Constraints application**: Every system has one primary constraint — the step that limits throughput most. Identify it (it is usually the step with the longest queue or highest WIP). The future state should be designed around exploiting that constraint:
- Ensure the constraint is never starved of work (buffer upstream)
- Ensure work does not pile up behind the constraint unnecessarily (buffer downstream)
- Remove non-constraint waste only after the constraint is addressed — improving a non-constraint step does not improve the system

**Questions to guide future state design**:
- What is the customer's required cadence (takt time)? Can the value stream deliver at that rate?
- Where is continuous flow achievable right now?
- Where must we still use push, and how do we control the queue?
- Which handoffs can be eliminated through team restructuring or skill development?
- Where should we implement pull signals (Kanban triggers, ready columns, replenishment cadences)?
- What is the target lead time? What process efficiency are we aiming for?

Draw the future state map using the same notation as the current state. Mark the key changes. The gap between the two maps is the improvement agenda.

## Metrics from VSM

VSM produces a small set of metrics that are directly calculable from the map and immediately meaningful.

**Total Lead Time (TLT)**: The sum of all process time and all wait time across the entire value stream. This is what the customer experiences from request to delivery.

```
TLT = Σ (Process Time) + Σ (Wait Time)
```

**Total Value-Added Time (VA Time)**: The sum of process time steps that directly transform the work into something the customer values. Excludes rework, approvals that add no quality signal, status reporting, and other non-value-adding activities.

**Process Efficiency (PE)**: The ratio of value-added time to total lead time, expressed as a percentage.

```
Process Efficiency = (VA Time / TLT) × 100%
```

Most knowledge work systems operate at 5–20% process efficiency. A well-optimised software delivery value stream can reach 30–40%. Values above 50% are rare and typically indicate either an unusually streamlined system or a mapping error.

**Average Queue Size**: The average number of items waiting at each step. High queue sizes at a particular step signal a bottleneck.

**Longest Wait Time**: The step with the greatest wait time is typically the primary improvement target. Reducing it has the greatest effect on total lead time.

| Metric | Formula | What It Tells You |
|---|---|---|
| Total Lead Time | Σ PT + Σ WT | End-to-end customer experience |
| Value-Added Time | Σ PT (value-adding steps only) | How much time actually creates value |
| Process Efficiency | VA / TLT × 100% | System health; improvement headroom |
| Longest Wait | Max (WT per step) | Primary improvement target |
| Defect Rate | Rework % per step | Quality waste in the system |

## Translating VSM to Action

The output of a VSM workshop is not the map — it is the improvement backlog that the map generates. Without an explicit translation from findings to actions, the map becomes a decorative artefact.

**Creating the improvement backlog**:

1. From the annotated current state map, list every identified waste item
2. For each waste item, formulate a hypothesis: "If we [change], then [metric] will improve by approximately [amount]"
3. Write an improvement backlog item for each hypothesis, with a description, owner, and target metric
4. Score and prioritise: use a simple impact vs. effort matrix (2x2) to sequence the backlog. High-impact, low-effort items go first.

**Prioritisation criteria**:
- Items that reduce the longest wait time (highest system-level impact)
- Items that reduce the primary constraint's load
- Items that eliminate structural waste (Type 2) before the team grows and the waste scales with it
- Items that can be measured — if you cannot tell whether the improvement worked, deprioritise it

**Measuring impact**:

Before implementing any improvement, define the baseline metric and the target. After implementing, measure the same metric at a consistent interval (sprint-over-sprint, or monthly). If the metric does not move, the improvement either did not address the root cause or was not fully implemented.

Track VSM metrics over time. A monthly review of lead time, process efficiency, and queue sizes tells you whether the improvement programme is working at a system level, not just locally.

## VSM in Agile Contexts

**VSM and Kanban**: VSM and Kanban are natural partners. Kanban boards visualise flow at a team level; VSM visualises flow across the entire value stream including upstream and downstream of the team. Use VSM to identify where WIP limits should be set and why — limits derived from VSM analysis are far more defensible than limits set by intuition. Flow efficiency, a core Kanban metric, is identical to process efficiency in VSM.

**VSM for DevOps pipeline analysis**: Deployment pipelines are a value stream in their own right. Map the pipeline as a VSM: code commit → automated build → test suite → static analysis → staging deployment → manual approval (if any) → production deployment. Measure wait time between pipeline stages (most CI/CD tools provide this data). Common findings: long-running test suites creating a bottleneck; manual approval steps adding hours or days of wait; flaky tests causing rework loops. The future state design typically includes parallelising test stages, eliminating unnecessary approval gates, and optimising slow build steps.

**Team-level vs. programme-level VSM**:

| Level | Scope | Who Maps | Primary Waste Found |
|---|---|---|---|
| Team-level | From backlog entry to production deployment | The delivery team | Handoffs within the team, rework loops, deployment friction |
| Programme-level | From business idea to customer outcome | Leads from multiple teams, product, and business | Cross-team dependencies, approval chains, portfolio queuing |

Start at team level if the organisation is new to VSM — the scope is manageable and the team can act on its own findings immediately. Move to programme level once team-level VSM is embedded, as the biggest delays are usually in the space between teams, not within them.

**VSM and Scrum**: VSM is not a Scrum ceremony, but it connects directly to the Sprint Retrospective. A VSM workshop every quarter provides the system-level perspective that sprint-level retrospectives cannot reach. Use VSM findings to set the theme for a sequence of retrospectives: "This quarter, our VSM showed that code review wait time is our biggest delay. Every retro this quarter will include a review of whether our improvement is working."

## Common VSM Anti-patterns

**Treating VSM as a one-time exercise**: VSM is most valuable as a regular practice — at minimum quarterly, ideally whenever significant process changes are made. A single mapping session produces a snapshot; regular mapping produces a trend. Organisations that map once and never return typically find that the gains from the initial improvement erode as the system reverts to old patterns.

**Mapping too narrow a slice**: Teams often map only the part of the value stream they control — for example, the development sprint, but not the upstream discovery and approval process, and not the downstream deployment and release process. The largest wait times are almost always in the parts of the value stream that fall between teams or between teams and the business. Narrow mapping produces locally optimised improvements that do not move total lead time.

**Not involving the people doing the work**: VSM workshops facilitated by managers, coaches, or analysts who then present findings to the team produce maps that are inaccurate, resented, and not actioned. The people who do the work know things that no interview or document can capture. Their involvement is not optional — it is the mechanism by which the map becomes accurate and the improvement becomes owned.

**Precision over insight**: Some teams spend excessive time arguing about whether the average wait time for a step is four days or four and a half days. VSM is not a measurement exercise — it is a sense-making exercise. Rough accuracy is sufficient to identify the right improvement targets. Perfect data collection can wait for after the first improvement cycle.

**Analysis paralysis**: A VSM workshop that produces a beautifully annotated map, a thorough waste catalogue, and a comprehensive future state design — and then generates no improvement actions within the next two weeks — has failed. The map is not the output. The improvement backlog, owned by named individuals, with a first action taken within the sprint after the workshop, is the output.

**Focusing only on process steps, ignoring information flows**: In knowledge work, information delays are as significant as process delays. A feature that sits for a week because the engineer cannot get a product decision is not captured by examining process steps alone. Map information flows explicitly — where do decisions need to be made, who makes them, and how fast does the answer reach the person who needs it?

**Confusing value-added with busy**: A step that keeps the team busy is not automatically value-added. Over-processing and rework keep people busy while consuming capacity that could be used for genuine value creation. The test for value-added is the customer's perspective: would the customer be willing to pay for this step if they knew about it? If not, it is waste.

## Additional Resources

- **`continuous-improvement`** skill — PDCA cycle, Kaizen, Five Whys, and making improvements stick
- **`kanban`** skill — Flow metrics, WIP limits, and Cumulative Flow Diagram interpretation
- **`agile-metrics`** skill — Measuring delivery performance and improvement outcomes over time
- **`facilitation`** skill — Running collaborative workshops effectively with cross-functional groups
