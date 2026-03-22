---
name: Scrum
description: This skill should be used when the user asks about "scrum", "sprint planning", "daily standup", "daily scrum", "sprint review", "sprint retrospective", "product backlog", "sprint backlog", "definition of done", "definition of ready", "sprint goal", "scrum ceremonies", "scrum events", "scrum artifacts", "scrum roles", "story points", "velocity", "increment", "product owner", "development team", "scrum team", "backlog refinement", or wants help facilitating or improving any Scrum practice.
version: 1.0.0
---

# Scrum

The Scrum framework is a lightweight empirical process control framework for developing and sustaining complex products. It is built on three pillars—transparency, inspection, and adaptation—and guided by five values: Commitment, Courage, Focus, Openness, and Respect.

## Core Structure: 3-5-3

**3 Accountabilities**
- **Product Owner** — Maximizes value; owns and orders the Product Backlog; accountable for product outcomes
- **Scrum Master** — Ensures Scrum is understood and enacted; serves team, PO, and organization; removes impediments
- **Developers** — Cross-functional; self-managing; accountable for creating a usable Increment each Sprint

**5 Events**
- **Sprint** — Container for all other events; fixed length (≤ 1 month); never cancelled except in extreme circumstances
- **Sprint Planning** — Defines Sprint Goal, selects backlog items, creates Sprint Backlog; ≤ 8 hours for 1-month Sprint
- **Daily Scrum** — 15-minute daily event for Developers to inspect progress toward Sprint Goal and adapt the plan
- **Sprint Review** — Inspect the Increment and adapt the Product Backlog; collaborative with stakeholders; ≤ 4 hours
- **Sprint Retrospective** — Inspect team effectiveness; create actionable improvement plan; ≤ 3 hours; last event of Sprint

**3 Artifacts (each with Commitment)**
- **Product Backlog** → commitment: Product Goal
- **Sprint Backlog** → commitment: Sprint Goal
- **Increment** → commitment: Definition of Done

## Sprint Planning

Sprint Planning addresses three topics:
1. **Why** is this Sprint valuable? → Sprint Goal
2. **What** can be Done this Sprint? → Developers forecast items from Product Backlog
3. **How** will chosen work get done? → Developers decompose items into tasks ≤ 1 day

Effective Sprint Planning requires a refined Product Backlog. Facilitate by surfacing the Sprint Goal first — this gives selection criteria for backlog items rather than just pulling a list.

## Daily Scrum

The purpose is to inspect progress toward the Sprint Goal and adapt the Sprint Backlog as necessary. Developers run it — not the Scrum Master. The three classic questions are a pattern, not a rule. Encourage focus on the Sprint Goal, not individual status reporting. If conversations emerge, take them offline.

Common anti-patterns to address:
- Status reporting to Scrum Master rather than peer coordination
- Attendance by non-Developers turning it into a status meeting
- No follow-through on identified blockers

## Sprint Review

A working session, not a demo. The team and stakeholders collaborate on what was done, what changed in the environment, and what to do next. Update the Product Backlog based on insights. Avoid treating this as a formal gate or sign-off event.

## Sprint Retrospective

The team inspects itself — processes, interactions, tools, Definition of Done. Focus on the most impactful improvement and add it to the next Sprint Backlog as an actionable item with a clear owner.

See `references/retrospective-formats.md` for facilitation formats.

## Artifacts & Commitments

**Product Backlog**
- Single source of work for the Scrum Team
- Product Owner is accountable; Developers collaborate on ordering and estimation
- Refined continuously — at least 10% of each Sprint
- Items near top should be small enough to complete in ≤ 1 Sprint

**Sprint Backlog**
- Owned by Developers; visible plan for achieving Sprint Goal
- Updated throughout Sprint; never assigned top-down
- If work emerges that jeopardizes the Sprint Goal, negotiate with Product Owner

**Definition of Done (DoD)**
- Quality standard for the Increment; agreed by Scrum Team (or organization if it sets one)
- If DoD is not met, work cannot be released or counted as Done
- Review and tighten DoD in retrospectives as capability matures

**Definition of Ready (DoR)**
- Not a Scrum Guide artefact, but a widely used team practice for ensuring backlog items are fit for Sprint Planning
- A backlog item is Ready when the team has enough information to commit to it and complete it within the Sprint
- Owned by the team (what they need to start work); the Product Owner is accountable for ensuring items meet it before planning
- Typical DoR criteria:
  - User story or equivalent written and understood
  - Acceptance criteria agreed between PO and team
  - Dependencies identified and either resolved or reflected in scope
  - Team can estimate it (no "we need to investigate first" blockers remaining)
  - Small enough to complete within the Sprint (or can be split further)
- **Caution**: Apply as a conversation guide, not a bureaucratic gate. Items stalled in "not ready" are an impediment — not a system feature. If too many items fail the DoR, the refinement process needs attention, not the gate.

## Velocity & Forecasting

Velocity = average story points (or items) completed per Sprint over a rolling window (typically 3–5 Sprints). Use it for forecasting, not as a performance target. Velocity is not comparable across teams. Common mistakes to avoid:
- Using velocity to pressure teams
- Comparing team velocities
- Treating velocity as a commitment rather than a forecast

## Common Impediments & Responses

| Impediment | Response |
|---|---|
| Sprint Goal not defined or ignored | Establish Sprint Goal as planning prerequisite |
| Daily Scrum is a status meeting | Redirect to Sprint Goal progress; coach Developers to self-manage |
| Sprint Review is a rubber-stamp | Invite active stakeholder participation; turn it into a conversation |
| DoD is weak or absent | Facilitate team agreement; link quality issues back to DoD gaps |
| Velocity gaming | Educate on purpose; shift conversation to outcomes |

## Additional Resources

- **`references/retrospective-formats.md`** — Facilitation formats for Sprint Retrospectives
- **`references/scrum-guide-essentials.md`** — Key quotes and nuances from the 2020 Scrum Guide
