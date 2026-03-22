---
name: Agile Delivery Manager
description: This skill should be used when the user asks about "agile delivery manager", "delivery manager", "ADM", "delivery management", "agile governance", "delivery governance", "stakeholder management agile", "delivery reporting", "agile programme management", "risk management agile", "dependency management", "portfolio management agile", "delivery roadmap", "release planning", "delivery metrics", "RAID log agile", "agile business case", "delivery team structure", "agile budgeting", or is working in an agile delivery management or programme management role.
version: 1.0.0
---

# Agile Delivery Manager

The Agile Delivery Manager (ADM) is accountable for the delivery of value through one or more agile teams. Where the Scrum Master focuses inward (team effectiveness) and the Product Owner focuses on what to build (value and priority), the ADM focuses outward — on governance, stakeholder relationships, risk, dependency management, and organisational enablement.

The ADM is not a project manager in disguise. The role requires internalising agile values while operating at the boundary between agile teams and traditionally-governed organisations.

## Core Accountabilities

**Delivery Governance**
- Define and maintain a lightweight governance framework appropriate to the delivery context
- Ensure compliance with organisational standards (finance, legal, security, audit) without creating bureaucratic overhead
- Own the RAID log (Risks, Assumptions, Issues, Dependencies) at programme level
- Facilitate decisions that teams cannot make themselves

**Stakeholder Management**
- Build and maintain a stakeholder map; understand each stakeholder's influence, interest, and communication needs
- Provide consistent, transparent progress reporting in language stakeholders understand
- Manage expectations proactively — surface bad news early, with options
- Sponsor relationships with senior leadership to protect team autonomy

**Planning & Forecasting**
- Facilitate programme-level planning cadences (quarterly, PI Planning, or equivalent)
- Maintain a delivery roadmap showing intent, not commitment — adjust as evidence emerges
- Translate team-level metrics (velocity, throughput, cycle time) into programme-level forecasts
- Run release planning; coordinate cross-team dependencies for major releases

**Risk & Dependency Management**
- Identify risks and dependencies that span multiple teams or external parties
- Track mitigation actions; escalate blockers that teams cannot resolve
- Own the programme-level dependency board; make cross-team dependencies visible

**Financial Management**
- Track budget against delivery; forecast burn vs. value delivered
- Work with finance to adapt traditional project-based funding to product/team-based funding where possible
- Report on value metrics, not just cost metrics

## Stakeholder Management

**Stakeholder Mapping**: Use a 2x2 grid (Influence vs. Interest) to segment stakeholders:
- High influence / High interest: Manage closely; involve in decisions
- High influence / Low interest: Keep satisfied; targeted updates
- Low influence / High interest: Keep informed; channel through engagement mechanisms
- Low influence / Low interest: Monitor; minimal effort

**Communication Planning**: Define per-stakeholder: preferred format, frequency, channel, and level of detail. Senior leaders want outcomes and risks; operational stakeholders want progress and blockers.

**Managing Up**: ADMs must be comfortable having difficult conversations with senior leaders. Bring data. Lead with impact and options, not problems alone. Use the SBI model (Situation, Behaviour, Impact) for feedback conversations.

## Agile Reporting

Traditional RAG status reports are inadequate for agile delivery. Replace or supplement with:

**Delivery Dashboard** (weekly):
- Planned vs. actual throughput
- Sprint/iteration health
- Open impediments and age
- Key risks and mitigation status
- Upcoming milestones

**Cumulative Flow Diagram**: Shows delivery progress and WIP trends at a glance

**Burn-up Chart**: Shows work done vs. scope over time; reveals scope changes

**Monte Carlo Forecasting**: Use throughput data to produce probabilistic delivery forecasts. "85% confidence we'll complete by [date]" is more honest than Gantt-based predictions.

**Avoid**: Velocity-based estimates shared with stakeholders without context — velocity is a team tool, not a delivery guarantee.

## Programme-Level Planning

**Quarterly Planning**:
1. Review OKRs and product goals for the quarter
2. Identify work (features, enablers, tech debt) per team
3. Surface cross-team dependencies and sequence accordingly
4. Set capacity; account for planned absences and team commitments
5. Agree on key milestones and review points

**Dependency Management**:
- Visualise on a programme board (physical or digital)
- Categories: team-to-team, team-to-external, external-to-team
- Each dependency: owner, consumer, date needed, risk if late
- Review weekly; escalate blockers to ADM level immediately

## RAID Log (Agile-Style)

Transform the traditional RAID log from a compliance artefact into an active management tool:

| Field | What to Track |
|---|---|
| Risk | Probability, impact, owner, mitigation, review date |
| Assumption | What we're assuming to be true; validation approach |
| Issue | Current blockers; owner; resolution target date |
| Dependency | Linked work item; owner on each side; date needed |

Review the RAID log at every programme sync. Close resolved items. Surface ageing issues.

## Governance Without Bureaucracy

**Lightweight Stage Gates**: Replace traditional phase gates with milestone reviews. Focus on: Is value being delivered? Are risks under control? Should we continue, pivot, or stop?

**Funding Models**: Advocate for persistent team funding (team as a unit of investment) rather than project-based funding. Reduces ramp-up cost; enables continuous delivery.

**Compliance by Design**: Work with legal, security, and audit early. Build compliance requirements into the backlog rather than treating them as a late-stage gate.

## The ADM's Relationship with the Scrum Master

The ADM and SM are complementary, not competing:

| Scrum Master | Agile Delivery Manager |
|---|---|
| Team-level effectiveness | Programme-level delivery |
| Internal impediments | External impediments and dependencies |
| Scrum ceremonies | Governance and reporting |
| Servant leadership | Stakeholder relationship management |
| Coaching | Facilitation and decision-making |

The SM focuses on how the team works. The ADM focuses on whether the team can deliver its commitments in the organisational context.

## Key Metrics

- **Delivery predictability**: % of committed features delivered per quarter
- **Lead time to production**: From approved backlog item to live
- **Dependency resolution time**: Average days to resolve cross-team dependencies
- **Stakeholder satisfaction**: Net Promoter Score or regular survey
- **Value delivered**: OKR progress; business outcomes achieved

## Additional Resources

- **`references/programme-board-template.md`** — Programme board setup for PI/quarterly planning
- **`references/stakeholder-communication-templates.md`** — Report and update templates for different audiences
