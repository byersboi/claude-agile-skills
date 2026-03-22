---
name: Kanban
description: This skill should be used when the user asks about "kanban", "kanban board", "WIP limits", "work in progress limits", "flow metrics", "cumulative flow diagram", "CFD", "lead time", "cycle time", "throughput", "kanban system", "pull system", "flow efficiency", "classes of service", "service level expectation", "SLE", "kanban cadences", "replenishment meeting", "service delivery review", "operations review", or wants help implementing or improving a Kanban system.
version: 1.0.0
---

# Kanban

Kanban is a method for managing and improving the flow of knowledge work. It is not a framework with prescribed roles or ceremonies — it is a strategy applied on top of existing workflows. The core idea: visualise work, limit work-in-progress, and actively manage flow.

## Core Practices (Kanban Method)

1. **Visualise** — Make work, workflow, and risks visible on a board
2. **Limit WIP** — Constrain the amount of work active at any stage
3. **Manage Flow** — Monitor and optimise the movement of work through the system
4. **Make Policies Explicit** — Define entry/exit criteria, priorities, escalation rules
5. **Implement Feedback Loops** — Use cadences to inspect and adapt
6. **Improve Collaboratively** — Use models and the scientific method for incremental, evolutionary change

## Kanban Board Design

A board should reflect the **actual workflow**, not an idealised one. Start with what you do now.

**Typical columns**: Options → Analysis → Development → Review → Test → Done

**Key design decisions**:
- Add **buffer columns** between stages to visualise queue vs. active work (e.g., "Dev Ready" vs. "In Dev")
- Use **swimlanes** for classes of service or customer segments
- Make policies visible on the board (WIP limits, SLEs, escalation criteria)

## WIP Limits

Limiting WIP is the single most impactful Kanban practice. WIP limits:
- Expose bottlenecks rather than hiding them
- Create pull pressure that improves collaboration
- Reduce context switching
- Shorten cycle times (Little's Law: CT = WIP / Throughput)

**Setting WIP limits**: Start with (number of people × 1.5) per stage as a heuristic. Observe; adjust based on flow data. The right limit is the one that creates healthy tension without paralysis.

**When WIP limit is breached**: Swarm the blocked work rather than starting new work. A breached WIP limit is a signal, not a failure.

## Flow Metrics

### Cycle Time
Time from when work **starts** (first active column) to when it is **done**. The primary delivery metric. Use percentiles (50th, 85th, 95th) rather than averages.

### Lead Time
Time from when work is **requested** (enters the system) to when it is **done**. Includes wait time. What the customer experiences.

### Throughput
Number of work items completed per unit time (per week is common). More stable than velocity; useful for forecasting without estimation.

### Flow Efficiency
`Active Time / Lead Time × 100%`. Most knowledge work systems run at 5–15% flow efficiency. Improving flow efficiency means reducing wait time, not working faster.

### Work Item Age
How long a currently-in-progress item has been active. Items ageing beyond the 85th percentile SLE need intervention.

## Service Level Expectation (SLE)

An SLE states: "X% of work items will be completed within Y days." Derived from historical cycle time data. Not a commitment — a probabilistic forecast.

Example: "85% of standard features complete within 12 days."

Use SLEs to:
- Set customer expectations
- Trigger escalation for ageing items
- Guide prioritisation

## Cumulative Flow Diagram (CFD)

A stacked area chart showing the count of items in each workflow stage over time.

**How to read**:
- **Width of a band** at a point in time = WIP in that stage
- **Slope of the Done line** = throughput
- **Horizontal distance between entry and exit** = approximate lead time
- **Bands widening** = increasing WIP / bottleneck forming
- **Flat Done line** = work stopped flowing

Use the CFD weekly to spot systemic problems before they become crises.

## Classes of Service

Different work items have different risk profiles and should be handled differently. Common classes:

| Class | Description | Policy |
|---|---|---|
| Expedite | Critical, time-sensitive | WIP limit: 1; drops all other limits |
| Fixed Date | External deadline | Flag early; track to date |
| Standard | Normal business value | FIFO within WIP limits |
| Intangible | Debt, enablers, improvements | Pull when capacity exists |

Make class policies visible on the board. Teams should not debate class on a case-by-case basis.

## Kanban Cadences

Kanban replaces prescribed ceremonies with **cadences** — regular meetings with specific purposes:

| Cadence | Frequency | Purpose |
|---|---|---|
| Daily Standup | Daily | Coordinate; flag blockers; review board |
| Replenishment / Commitment | Weekly | Pull new work into the system |
| Service Delivery Review | Bi-weekly | Review SLE performance; improve flow |
| Operations Review | Monthly | Process health; metrics trends |
| Risk Review | As needed | Surface and address systemic risks |

## Kanban vs Scrum

| Aspect | Scrum | Kanban |
|---|---|---|
| Cadence | Fixed Sprints | Continuous flow |
| Roles | Prescribed (PO, SM, Devs) | No prescribed roles |
| WIP Control | Sprint boundary | Explicit WIP limits |
| Change | Only between Sprints | Anytime (within policies) |
| Estimation | Required (story points) | Optional |
| Best for | Product development, feature teams | Operations, support, mixed work |

Neither is superior. Many teams use Scrumban — Scrum's cadence with Kanban's flow discipline.

## Getting Started

1. Map the actual current workflow — interview the team; avoid the idealised version
2. Create a physical or digital board reflecting that workflow
3. Agree on start/done definitions for each column
4. Set initial WIP limits (can be loose at first)
5. Start tracking cycle time immediately
6. Hold a weekly replenishment meeting and daily standup
7. Review the CFD every two weeks; adjust WIP limits based on data

## Additional Resources

- **`references/flow-metrics-guide.md`** — Detailed guide to calculating and interpreting flow metrics
- **`references/kanban-board-patterns.md`** — Board design patterns for different team types
