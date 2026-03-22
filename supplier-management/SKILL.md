---
name: Supplier & Vendor Management
description: This skill should be used when the user asks about "supplier management", "vendor management", "agile contracting", "third-party dependencies", "supplier integration", "SLA agile", "T&M contract", "fixed price agile", "supplier ceremonies", "managing suppliers", "vendor relationships", "offshore supplier", "distributed supplier", "supplier dependency", "commercial change control", "agile procurement", "supplier performance", "supplier retrospective", "joint planning supplier", "supplier escalation", "managing third parties", "outsourcing agile", "contract management agile", "supplier communication", or is working with external suppliers or vendors in an agile delivery context.
version: 1.0.0
---

# Supplier & Vendor Management

Organisations rarely deliver complex agile programmes entirely with internal capability. Suppliers, vendors, and outsourced partners are a reality of modern delivery — but traditional supplier management approaches are built around fixed requirements, output-based contracts, and arm's-length relationships. These assumptions are fundamentally at odds with agile.

Effective agile supplier management is not about eliminating contracts or accountability; it is about designing commercial relationships, working practices, and governance that allow the agile team as a whole — including supplier resources — to respond to change without being trapped by the terms under which they operate.

## Agile Contracting Principles

The Agile Manifesto principle on contracts is explicit: "Customer collaboration over contract negotiation." This does not mean contracts are unimportant; it means the contract should enable the working relationship rather than substitute for it.

**The Problem with Fixed-Scope Contracts**

Traditional fixed-price, fixed-scope contracts are built on the assumption that requirements can be fully defined upfront, and that cost is most predictable when scope is locked. In practice, this produces:
- Change control processes that penalise discovery and learning
- Suppliers optimising for contract compliance rather than customer outcomes
- Adversarial relationships when the inevitable changes arise
- Delivery of the wrong thing, on time, within budget

**Common Contract Models**

| Contract Type | Description | Agile Fit |
|---|---|---|
| Fixed price, fixed scope | Agreed deliverables at agreed cost | Poor — punishes change; creates adversarial dynamics |
| Time & Materials (T&M) | Supplier charges for time and materials consumed | Good agility, but requires active client-side governance to manage spend |
| Capped T&M | T&M with an upper cost limit | Balanced — agility within financial guardrails |
| Outcome-based / value-based | Payment linked to agreed outcomes or value delivered | High alignment; requires well-defined and measurable outcomes |
| Managed service | Supplier owns delivery of a defined service | Appropriate for stable, commodity capabilities |

**Lean Contract Approaches**

Several approaches have emerged to make contracts more agile-friendly:

- **DSDM Agile Project Framework contracts**: Built around timeboxes, iterations, and the MoSCoW prioritisation model. Scope is variable; time and cost are fixed.
- **Agile Alliance Contractual Framework**: Template clauses designed to support iterative delivery, continuous feedback, and collaborative governance.
- **Minimum viable scope with options**: Contract a core scope with pre-agreed option-exercising mechanisms for extensions, reducing renegotiation overhead.
- **Sprint-based milestones**: Break the contract into iteration-level milestones. Each sprint or timebox constitutes a payment trigger based on working software demonstrated, not documentation produced.

The guiding principle is that the contract should reflect what the parties actually intend: collaborative, iterative delivery with shared accountability for outcomes.

## Selecting Suppliers

Supplier selection in an agile context goes beyond cost and technical capability. Cultural fit, agile maturity, and collaborative mindset are as important as delivery track record.

**Evaluating Supplier Agile Maturity**

Do not take supplier claims of "we do agile" at face value. Probe:
- How do they structure their delivery teams? (Cross-functional? Self-organising?)
- How do they handle changing requirements mid-engagement?
- What ceremonies do they run, and who attends?
- How do they surface bad news? Can they share examples?
- What does their Definition of Done look like?
- Have they ever worked embedded with a client's agile team, rather than in a separate delivery unit?

**Adapting the RFP/RFI for Agile**

Traditional RFPs ask suppliers to propose fixed solutions to fully specified problems. An agile-aligned RFP instead:
- Shares the problem context and strategic intent rather than a detailed specification
- Asks suppliers to propose how they would discover and shape the solution collaboratively
- Requests evidence of iterative delivery: case studies showing adaptation to change
- Invites suppliers to a workshop or working session as part of evaluation — observed collaboration is more revealing than written proposals

**Assessing Cultural Fit**

A capable supplier with the wrong mindset will undermine agile working more than a less capable supplier that embraces it. Indicators of good cultural fit:
- Willingness to share failures and lessons learned
- Comfort with ambiguity and evolving requirements
- Proactive communication rather than gate-keeping information
- Collaborative approach to problem-solving in interviews and workshops

**Supplier Capability Frameworks**

For large or strategic supplier relationships, consider a structured capability assessment across dimensions such as:
- Agile delivery methods and practices
- Quality engineering and test automation capability
- DevOps and CI/CD maturity
- Communication and transparency behaviours
- Commercial flexibility and relationship management

Score suppliers consistently across these dimensions to support objective comparison and to create a baseline for ongoing relationship management.

## Integrating Suppliers into Agile Teams

The greatest risk in supplier integration is creating a two-speed team: an internal agile core and a separate supplier delivery unit operating on a different cadence with different artefacts and communication channels. This reliably produces delays, misalignment, and friction.

**Embedding Supplier Resources**

Where possible, integrate supplier resources into the team as if they were internal. This means:
- Supplier team members attend all standard Scrum or Kanban ceremonies
- They take work items directly from the shared backlog, not from a separate specification document
- They participate in retrospectives — including giving feedback on the client organisation
- They have access to the same tooling (Jira, Confluence, Slack, etc.) as internal team members

**Supplier Involvement in Ceremonies**

| Ceremony | Supplier Involvement |
|---|---|
| Sprint Planning | Participate in full; take on sprint commitments alongside internal team |
| Daily Stand-up | Attend and report blockers; included in impediment resolution |
| Sprint Review | Demonstrate their own work; receive stakeholder feedback directly |
| Retrospective | Participate fully; psychological safety must extend to supplier staff |
| Backlog Refinement | Contribute to estimation and acceptance criteria; domain knowledge is valuable |
| PI / Quarterly Planning | Participate in planning their work and dependencies alongside internal teams |

**Defining Interfaces Clearly**

When full embedding is not feasible (e.g., offshore suppliers with significant time zone difference, or specialist sub-suppliers with narrow scope), define the interface explicitly:
- What artefacts does the supplier consume as input?
- What artefacts do they produce as output?
- What are the handoff points, and who is accountable for each?
- How are questions and blockers raised and resolved?
- What is the agreed response time for queries?

Unclear interfaces are the most common cause of supplier delivery failure. Document them, agree them with the supplier, and review them regularly.

**Dedicated vs. Shared Supplier Teams**

A dedicated supplier team — assigned exclusively to your delivery — is almost always preferable to a shared team split across multiple client engagements. Shared teams introduce context-switching overhead, competing priorities, and inconsistent availability. When engaging suppliers, negotiate for dedicated allocation wherever possible, even if it costs marginally more.

## Managing Supplier Dependencies

Supplier work creates dependencies on the programme, and unmanaged supplier dependencies are a leading cause of programme delays.

**Representing Supplier Dependencies on the Programme Board**

Treat supplier dependencies the same as cross-team dependencies on the programme board:
- Each dependency has an owner on the client side and a named counterpart on the supplier side
- Record what is needed, from whom, and by when
- Flag dependencies that are at risk early — do not wait until the date passes
- Review supplier dependencies at every programme sync or ART sync

**Tracking Supplier Deliverables in the RAID Log**

Supplier commitments belong in the RAID log as dependencies and, where there is risk to delivery, as risks:

| RAID Category | Supplier Application |
|---|---|
| Risk | Supplier capacity risk, key person risk, financial stability of supplier |
| Assumption | Assumptions about supplier availability, capability, or responsiveness |
| Issue | Active blockers caused by or affecting the supplier |
| Dependency | Specific supplier deliverables needed by a date; bi-directional |

**Escalation Paths**

Define escalation paths before they are needed:
- Who is the day-to-day supplier contact?
- Who is the supplier delivery manager or account manager?
- Who is the senior sponsor on each side?
- What is the agreed SLA for responding to escalated issues?
- At what point does an issue escalate automatically to senior sponsor level?

Escalation should feel routine, not adversarial. Frequent, low-friction escalation is healthier than rare, crisis-driven escalation.

## SLAs vs Agile Delivery

Service Level Agreements originated in managed service and IT operations contexts. When applied uncritically to agile software delivery, they can drive the wrong behaviours.

**The Tension**

Traditional SLAs measure outputs (delivered features, response times, defect volumes) on fixed cycles that may not align with sprint cadences. This creates reporting overhead and can incentivise suppliers to optimise for metric compliance rather than genuine delivery quality.

**Adapting SLAs to Agile Cadences**

Where SLAs are contractually required, align them to agile rhythms:
- Measure per sprint or per timebox rather than per calendar month where possible
- Use throughput, cycle time, and defect escape rate rather than activity-based metrics
- Include leading indicators (e.g., days in review, blocked items) not just lagging ones

**Service-Level Thinking vs. Output-Level Thinking**

Service-level thinking asks: "Is the supplier providing a service of the quality we need?" Output-level thinking asks: "Did the supplier produce the specified deliverables?" In agile, service-level thinking is more appropriate:
- Is the supplier team responsive and collaborative?
- Is the quality of work enabling or impeding downstream activities?
- Is the supplier raising risks and issues proactively?
- Is the supplier adapting when requirements change?

**Measuring Supplier Performance in Agile**

| Metric | What It Tells You |
|---|---|
| Sprint commitment vs. delivery | Predictability; planning accuracy |
| Defect escape rate | Quality of supplier output before handoff |
| Cycle time for supplier work items | Efficiency; flow of work through supplier team |
| Blocked items age | How long supplier blockers remain unresolved |
| Retrospective actions closed | Engagement with continuous improvement |
| Stakeholder satisfaction rating | Qualitative relationship health |

## Supplier Communication Cadences

Communication structure is the single most important factor in supplier relationship health. Without deliberate cadences, communication becomes reactive and problems surface too late.

**Recommended Cadence**

| Frequency | Forum | Purpose |
|---|---|---|
| Daily | Stand-up (embedded suppliers) | Progress, blockers, collaboration |
| Weekly | Supplier operational sync | Delivery progress, issue resolution, near-term planning |
| Fortnightly / per sprint | Sprint review and retrospective | Inspect output; improve ways of working |
| Monthly | Commercial and relationship review | Budget tracking, SLA review, relationship health |
| Quarterly | Strategic supplier review | Roadmap alignment, contract review, strategic priorities |

**Joint Planning Sessions**

Include key suppliers in programme or PI planning sessions. Suppliers who only see their slice of the backlog — without understanding the broader programme context — make worse decisions and surface problems later than they should.

**Shared Reporting**

Establish shared dashboards or reporting artefacts that both client and supplier contribute to and can see. Avoid a dynamic where the client asks for status and the supplier produces a separate report. Shared visibility creates shared accountability.

**Transparency Expectations**

Set explicit expectations with suppliers from the outset:
- Bad news should travel fast — the client will not penalise transparency
- Blockers should be raised the day they are identified, not at the next formal review
- Capacity changes (team member departure, unplanned leave) should be communicated immediately
- The supplier should proactively flag risks to scope, quality, or timeline

## Commercials & Change Control

Even in agile-aligned contracts, commercial and change control processes must be managed carefully. The goal is commercial flexibility without commercial chaos.

**Managing Scope Changes with Suppliers**

Changes in agile are expected and welcome — but they must be managed commercially. An effective approach:
1. Maintain a rolling backlog visible to both parties
2. Agree the scope for each sprint or iteration in advance
3. Changes to in-flight sprint scope trigger a conversation; changes to future backlog are fluid
4. Formal change requests are reserved for changes that affect the commercial baseline (total budget, key milestone dates, agreed outcomes)

**Commercial Flexibility Mechanisms**

Build flexibility into the contract rather than relying on formal change requests for every discovery:
- **Flexible scope pool**: A proportion of the contracted budget (e.g., 15–20%) is reserved for emerging priorities, drawable without a formal change request
- **Sprint-level options**: Pre-agreed optional work packages that can be activated or deactivated per sprint based on progress
- **Review and extend clauses**: Short initial contract with structured review points at which scope and budget can be recalibrated

**Change Request Process That Doesn't Kill Agility**

When a formal change request is genuinely required:
- Keep the process lightweight — one-page commercial change note is usually sufficient
- Define a turnaround SLA for approval (e.g., 5 business days)
- Empower a named client authority to approve changes below a defined threshold without escalation to procurement or the board
- Do not allow unapproved scope to be carried out "on goodwill" — this creates commercial disputes and erodes the relationship

## Vendor Relationship Management

Supplier relationships exist on a spectrum from purely transactional (commodity supplier, easily switched) to genuinely strategic (embedded partner, high mutual dependency). The management approach should match the relationship type.

**Strategic vs. Tactical Supplier Relationships**

| Dimension | Tactical | Strategic |
|---|---|---|
| Switching cost | Low | High |
| Integration depth | Arm's length | Deeply embedded |
| Communication frequency | Formal and periodic | Continuous and informal |
| Commercial flexibility | Standard terms | Jointly negotiated |
| Governance | Contract compliance | Shared outcomes |
| Investment in relationship | Minimal | Significant |

Most organisations have too many suppliers in the strategic category and too few governance mechanisms for genuinely strategic ones. Rationalise the portfolio; invest deeply in the relationships that matter.

**Joint Retrospectives**

For any significant supplier relationship, run joint retrospectives on a regular basis — at least quarterly. Effective joint retrospectives:
- Include representatives from both organisations with authority to change ways of working
- Cover the working relationship, not just delivery outputs
- Are psychologically safe — the supplier must feel able to critique the client organisation
- Produce agreed actions with owners and dates on both sides

**Supplier Satisfaction**

Measure supplier satisfaction, not just your satisfaction with the supplier. A supplier that is frustrated, under-resourced, or commercially stressed will underperform. Simple periodic surveys or structured conversations with supplier delivery leads can surface relationship issues early.

**Managing Underperforming Suppliers**

When supplier performance deteriorates:
1. Diagnose before acting — is the root cause within the supplier's control?
2. Raise the concern formally but constructively; share specific evidence
3. Agree a performance improvement plan with measurable targets and a review date
4. Escalate to senior sponsors on both sides if improvement is not achieved
5. If performance remains unacceptable, invoke contractual remedies — but have a transition plan ready before doing so
6. Never rely solely on a supplier who is on a performance improvement plan for critical path delivery

Switching suppliers mid-programme is expensive and disruptive. The goal is always to recover the relationship where possible.

## Offshore & Distributed Suppliers

Offshore and nearshore suppliers offer cost advantages and access to specialist capability, but introduce communication and quality management challenges that require deliberate mitigation.

**Time Zone Challenges**

- Establish a minimum overlap window (e.g., two hours per day) during which both sides are available simultaneously
- Use this window for stand-ups, collaborative working sessions, and issue resolution — not status updates
- Record key decisions and design discussions for asynchronous review
- Avoid a pattern where the offshore team is blocked overnight waiting for a response — resolve blockers before the working day ends where possible

**Communication Tools**

- Use a shared messaging platform (Slack, Teams) for informal, rapid communication rather than relying on email
- Maintain a shared backlog tool (Jira, Azure DevOps) with real-time visibility for both sides
- Use video for ceremonies wherever possible — audio-only calls are significantly less effective for nuanced conversations
- Document decisions immediately after collaborative sessions; do not rely on verbal agreements

**Cultural Considerations**

Cultural differences affect communication styles, hierarchy expectations, and the willingness to surface problems. Common patterns with offshore suppliers:
- High-context cultures may communicate blockers or concerns indirectly — create explicit channels and norms for raising issues
- Hierarchical cultures may expect the client to provide more prescriptive direction than an agile approach implies; invest in educating the team on self-organisation
- Saving face may prevent team members from admitting they do not understand requirements; create a psychologically safe environment and encourage questions

**Managing Quality Across Distributed Supplier Teams**

- Agree and document a shared Definition of Done that applies equally to onshore and offshore work
- Build automated quality gates (unit tests, code coverage, static analysis) into the delivery pipeline — do not rely on manual review across time zones
- Conduct regular code or output reviews jointly — this builds shared standards and trust
- Address quality issues in retrospectives, not just in formal supplier reviews

## Anti-patterns

**Treating Suppliers as Output Factories**

Suppliers given a specification and left to deliver it will optimise for specification compliance, not for customer outcomes. They lack context, cannot adapt to change, and surface problems late. Treat suppliers as collaborative partners who need context, feedback, and involvement.

**No Shared Definition of Done**

When the client has one Definition of Done and the supplier team has another (or none), quality mismatches are inevitable. "Done" must mean the same thing across the whole team, regardless of who employs the individual.

**Separate Ceremonies Creating Silos**

Running a separate supplier stand-up, a separate supplier review, and a separate supplier retrospective — rather than integrating suppliers into team ceremonies — creates two parallel delivery realities that drift apart over time. Ceremonies should be shared wherever feasible.

**Hiding Bad News from Suppliers**

Clients who hide strategic uncertainty, budget pressure, or programme difficulties from their suppliers create a dysfunctional dynamic. Suppliers cannot plan, adapt, or support effectively without context. Treat strategic suppliers as partners who need to understand the environment they are operating in.

**Confusing Activity with Delivery**

Measuring supplier performance by hours logged, documents produced, or meetings attended rather than working software demonstrated and outcomes progressed creates perverse incentives. Measure what matters.

**Assuming Agile Maturity**

Accepting a supplier's claim that they are agile without evidencing it leads to painful misalignment once delivery is underway. Probe, evidence, and test cultural fit before contracting.

**No Escalation Path**

A supplier delivery failure with no pre-agreed escalation path becomes a crisis. Define escalation routes at contract inception. The best time to agree what happens when things go wrong is before things go wrong.

**Over-relying on a Single Supplier**

Strategic dependency on a single supplier without a transition plan or competitive tension creates leverage imbalance. Maintain market awareness; periodically test the market; build internal capability in critical domains.
