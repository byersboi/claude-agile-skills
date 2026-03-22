---
name: Agile Scaling
description: This skill should be used when the user asks about "scaling agile", "SAFe", "scaled agile framework", "LeSS", "large scale scrum", "Nexus", "Spotify model", "PI planning", "program increment", "ART", "agile release train", "value stream", "multiple teams", "multi-team scrum", "scaling scrum", "enterprise agile", "agile at scale", "DevOps at scale", "agile transformation large organisation", "squads tribes chapters guilds", or is choosing or implementing a scaling framework.
version: 1.0.0
---

# Agile Scaling

Scaling agile means applying agile principles across multiple teams working on a shared product or programme. The core challenge: maintaining the benefits of small-team agility (speed, autonomy, feedback) while achieving the coordination needed for large, interdependent work.

**First principle**: Don't scale until team-level agility is working. Scaling amplifies both strengths and weaknesses.

## Choosing a Scaling Approach

| Framework | Scale | Complexity | Best For |
|---|---|---|---|
| Nexus | 3–9 teams | Low | Scrum teams on one product |
| LeSS | 2–8 teams (LeSS); 8+ (LeSS Huge) | Medium | Feature teams; product focus |
| SAFe | 50–1000+ people | High | Enterprise; portfolio alignment |
| Spotify Model | 100–1000 people | Medium | Engineering culture; autonomy |
| Scrum of Scrums | 2–10 teams | Low | Lightweight; no framework change |

No framework is universally best. Choose based on: current team maturity, organisational context, regulatory environment, and leadership appetite for change.

---

## SAFe (Scaled Agile Framework)

SAFe is the most widely adopted enterprise agile framework. It provides four configurations (Essential, Large Solution, Portfolio, Full) for different scales and complexities.

### Core Concepts

**Agile Release Train (ART)**
- The primary value delivery vehicle in SAFe
- 5–12 teams (50–125 people) aligned to a common mission
- Delivers features on a shared cadence (Program Increment)
- Includes SM, PO, Release Train Engineer (RTE), System Architect

**Program Increment (PI)**
- Fixed cadence of 8–12 weeks containing 4–5 sprints + Innovation & Planning (IP) sprint
- Each PI begins with PI Planning — the most important SAFe event
- Teams align to PI Objectives: business value + stretch objectives

**Value Streams**
- End-to-end flow of value to the customer
- Operational: directly delivers products/services to customers
- Development: builds and supports systems used by operational value streams

### PI Planning

PI Planning is a two-day face-to-face event for the entire ART. It is the heartbeat of SAFe.

**Day 1**:
- Business context from leaders
- Product/Solution Vision
- Architectural vision
- Team breakouts: draft PI Objectives and identify risks

**Day 2**:
- Team breakouts continue: finalise plans, resolve dependencies
- Risk review and ROAM (Resolved, Owned, Accepted, Mitigated)
- Final plan review and confidence vote (Fist of Five)
- Management review and problem solving

**Outputs**: PI Objectives per team, programme board showing dependencies, preliminary iteration plans, ROAM risks

**Why it matters**: PI Planning achieves alignment and trust that no amount of asynchronous communication can replicate. In distributed settings, invest heavily in tooling and pre-work to preserve its value.

### SAFe Roles

| Role | Scope | Description |
|---|---|---|
| RTE (Release Train Engineer) | ART | Senior SM; facilitates ART events; removes systemic impediments |
| Product Manager | ART | Owns Programme Backlog; defines Features; interface to business |
| System Architect | ART | Technical vision and enabler backlog; non-functional requirements |
| Business Owners | ART | Senior stakeholders; participate in PI Planning; assign business value |
| Scrum Master | Team | Standard SM accountabilities |
| Product Owner | Team | Manages Team Backlog; owns team-level priorities |

---

## LeSS (Large-Scale Scrum)

LeSS is deliberately minimal — it is Scrum, not a new framework layered on top. Created by Craig Larman and Bas Vodde.

**Core principle**: Descale. Remove organisational complexity rather than adding coordination frameworks.

### LeSS Structure

**LeSS (2–8 teams)**:
- One Product Owner for all teams
- One Product Backlog for all teams
- Each team has its own Sprint Backlog
- Sprint Planning 1: all teams + PO, select items
- Sprint Planning 2: each team plans how
- Sprint Review: all teams present integrated Increment
- Overall Retrospective: cross-team improvement

**LeSS Huge (8+ teams)**:
- Requirement Areas: logical groupings of the backlog
- Area Product Owner per Requirement Area
- One overall Product Owner maintains product-level priority

### LeSS Key Practices

- **Feature teams over component teams**: Teams take full responsibility for end-to-end features, not layers
- **No additional roles**: No equivalent of RTE or SAFe Programme layer
- **Multi-team Sprint events**: Sprint Reviews and Retrospectives include all teams together
- **Communities of Practice**: Cross-team learning groups replace formal Chapter/Guild structures

**When to choose LeSS**: When the organisation can commit to feature teams and is willing to remove management layers rather than add coordination overhead.

---

## Nexus

Developed by Ken Schwaber (co-creator of Scrum) and Scrum.org. Extends Scrum for 3–9 teams delivering a single integrated product.

### Nexus Additions to Scrum

**Nexus Integration Team (NIT)**:
- Scrum Master (also NIT SM), Product Owner, and cross-functional members
- Accountable for integration; resolves cross-team technical and process issues
- Not a management team — a coordination and quality mechanism

**Nexus Events**:
- **Nexus Sprint Planning**: Before individual team planning; NIT and teams identify dependencies and integration work
- **Nexus Daily Scrum**: Selected representatives (≤15 min) inspect integration issues; feeds team Daily Scrums
- **Nexus Sprint Review**: Single review of the integrated Increment
- **Nexus Sprint Retrospective**: Three phases — overall, then team-level, then back to overall with team actions

**Nexus Sprint Backlog**: Shared visibility of cross-team work and dependencies

**When to choose Nexus**: When already using Scrum well at team level and need the lightest possible scaling layer.

---

## Spotify Model

Not a prescriptive framework — Spotify's 2012 organisational design became a model for autonomy-with-alignment.

### Structural Elements

**Squad**: Cross-functional team (like a Scrum team); owns an area of the product; maximum autonomy on how to work

**Tribe**: Collection of squads working in related areas; typically ≤100 people; Led by a Tribe Lead

**Chapter**: Group of people with the same skill (e.g., all backend engineers across squads in a tribe); career home; Chapter Lead is line manager

**Guild**: Informal, cross-tribe community of practice (e.g., all data engineers across the company)

### Key Principles

- **Loosely coupled, tightly aligned**: Squads should be able to release independently; aligned to company strategy through OKRs
- **Failure-friendly**: Experiments expected to fail; learn fast
- **Trust over control**: Autonomy requires trust; earned through transparency

**Important caveat**: The Spotify model as described was an approximation of reality at one company at one point in time. Spotify itself has moved on. Adopt principles, not structures wholesale.

---

## Scrum of Scrums (SoS)

The simplest multi-team coordination mechanism. Representatives from each Scrum team meet regularly (usually daily or 3x per week) to:
- Surface cross-team impediments
- Identify and resolve dependencies
- Coordinate integration work

**Format**: 15–30 minutes; each team answers: What did we do that might affect other teams? What will we do? What are our impediments?

**Limitations**: Works well up to 4–5 teams. Beyond that, add another coordination layer (Meta-SoS) or adopt a proper scaling framework.

---

## Scaling Anti-Patterns

- **SAFe without Scrum maturity**: Adding SAFe overhead when individual teams aren't delivering reliably makes things worse
- **Cargo cult PI Planning**: Running PI Planning without genuine team autonomy produces fake plans
- **Feature teams in name only**: Calling teams "feature teams" but keeping component ownership siloes
- **Framework shopping**: Changing scaling frameworks when the real problem is leadership behaviour
- **Scaling too fast**: Moving to 10+ teams before demonstrating the approach with 2–3 works

## Additional Resources

- **`references/safe-configuration-guide.md`** — SAFe Essential vs Full configuration decision guide
- **`references/pi-planning-facilitation.md`** — Step-by-step PI Planning facilitation guide
