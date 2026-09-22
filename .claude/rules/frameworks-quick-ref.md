# Frameworks quick reference

## Scrum in brief

**Three accountabilities:** Product Owner (what), Developers (how), Scrum Master (effectiveness)
**Five events:** Sprint, Sprint Planning, Daily Scrum, Sprint Review, Sprint Retrospective
**Three artifacts:** Product Backlog (+ Product Goal), Sprint Backlog (+ Sprint Goal), Increment (+ Definition of Done)
**Five values:** Commitment, Focus, Openness, Respect, Courage

**Sprint length:** 1–4 weeks (consistent). Shorter = faster feedback loops. Most teams: 2 weeks.

**Definition of Done vs Acceptance Criteria:**
- DoD = quality standard applied to every Increment (owned by the team / org)
- AC = specific conditions for a single backlog item (owned by the PO)

## Kanban in brief

**Core practices:** Visualise workflow, limit WIP, manage flow, make policies explicit, implement feedback loops, improve collaboratively
**Key metrics:** Cycle time (work started → done), Lead time (requested → done), Throughput (items completed per period), WIP
**CFD (Cumulative Flow Diagram):** Width = cycle time, slope = throughput, flat band = blockage

**WIP limits:** Set per workflow stage. Too high = no benefit. Too low = starvation. Start with team size minus one.

## Framework selection guide

| Context | Consider |
|---------|---------|
| Single team, iterative product dev | Scrum |
| Operational/support work, variable flow | Kanban |
| Multiple interdependent teams | SAFe / LeSS / Nexus |
| Lightweight scaling, strong engineering culture | LeSS |
| Enterprise with governance/compliance needs | SAFe |
| Small teams, autonomous squads | Spotify model (not a framework — a culture pattern) |
| Mixed (product teams + ops) | Scrum for product, Kanban for ops |

**The honest answer on SAFe:** It adds coordination value at scale but bureaucratic overhead at the team level. Only adopt it if you genuinely need cross-team alignment at programme cadence. LeSS is leaner but requires more organisational courage.

## Key metrics explained

| Metric | What it measures | Watch for |
|--------|-----------------|-----------|
| **Velocity** | Story points completed per sprint | Gaming (inflating estimates); only meaningful for same team over time |
| **Throughput** | Items completed per sprint/week | More honest than velocity; doesn't require estimation |
| **Cycle time** | Work started → done | Long tail = blockages; benchmark 85th percentile |
| **Lead time** | Requested → done | Customer-facing; includes queue time |
| **WIP** | Items in progress | Inversely related to flow efficiency; lower = faster |
| **Flow efficiency** | Active time / (active + wait time) | Most teams: 15–30%. Target >40% |
| **DORA metrics** | Deployment freq, lead time for changes, MTTR, change failure rate | Engineering team health; see release-management skill |

**On velocity:** Velocity is a planning tool for the team, not a performance metric for management. Never compare velocity across teams. Never set velocity targets. Doing either breaks the system.

## Prioritisation techniques

**MoSCoW:** Must / Should / Could / Won't — good for release scope decisions; watch out for "everything is Must"

**WSJF (Weighted Shortest Job First):** (CoD + ToE + RR&OE) / Job Size — used in SAFe; favours small, high-value items; good for portfolio prioritisation

**Kano model:** Basic needs (must-haves), Performance needs (more = better), Delighters (unexpected value) — good for product discovery and feature decisions

**Impact mapping:** Why → Who → How → What — connects features to business outcomes; cuts scope creep

## Sprint events: time boxes

| Event | 1-week sprint | 2-week sprint | 4-week sprint |
|-------|-------------|---------------|---------------|
| Sprint Planning | 2h | 4h | 8h |
| Daily Scrum | 15 min | 15 min | 15 min |
| Sprint Review | 1h | 2h | 4h |
| Retrospective | 45 min | 1.5h | 3h |

These are maximums, not targets. A 2-week team with strong refinement practices may run Sprint Planning in 90 minutes.

## Scaling: key decisions

**When to scale:**
- You have genuine inter-team dependencies that cannot be eliminated
- Teams need shared cadence to deliver coherent value
- Governance requires cross-team visibility

**When not to scale (yet):**
- Teams are not yet doing basic Scrum well
- Dependencies could be removed by reorganising
- The "scaling" is actually a way to avoid fixing team-level problems

**Nexus vs LeSS vs SAFe:**
- **Nexus** — lightweight, 3–9 Scrum teams, minimal new roles, integration Scrum Team, Scaled Daily Scrum
- **LeSS** — 2–8 teams, one PO, one Product Backlog, multi-team Sprint events; organisational restructuring required
- **LeSS Huge** — 8+ teams, Area POs, Area Product Backlogs
- **SAFe** — full enterprise framework, Agile Release Train, PI Planning, many new roles; high adoption overhead

## OKRs quick structure

```
Objective: Inspirational, qualitative, direction-setting — "What do we want to achieve?"
  Key Result 1: Measurable, outcome-focused — "How will we know we got there?"
  Key Result 2: 2–5 KRs per Objective
  Key Result 3: Target 70% achievement = healthy stretch (100% = not ambitious enough)
```

**OKR pitfalls:** KRs that are outputs (features shipped) not outcomes (behaviour changed); too many OKRs dilutes focus; cascading OKRs top-down undermines team ownership — co-create them instead.
