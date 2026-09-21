# SAFe Configuration Decision Guide

Which SAFe configuration — if any — fits, and what each one costs. For the comparison with LeSS, Nexus and Scrum of Scrums, see the `agile-scaling` skill.

## First: should you adopt SAFe at all?

Answer honestly before choosing a configuration.

| Question | If no... |
|---|---|
| Do teams already do team-level agile competently? | Fix that first. SAFe on top of weak teams produces ceremony without delivery |
| Are there genuine dependencies you cannot design away? | Reorganise instead. Scaling to manage self-inflicted dependencies is expensive theatre |
| Do multiple teams need to deliver one coherent thing? | Independent teams don't need a train |
| Will leadership change how it funds and governs work? | SAFe without lean budgeting is a new set of meetings attached to the old governance |
| Can you commit to it for 18 months? | Partial SAFe is the worst of both worlds |

**The honest position:** SAFe adds real coordination value at scale and real bureaucratic overhead at team level. It is most defensible in large, regulated organisations with genuine cross-team dependencies and governance obligations. It is least defensible as a way of making an existing programme structure feel agile.

---

## The four configurations

### Essential SAFe
The minimum viable configuration and the only one most organisations need. One Agile Release Train (ART): 5–12 teams, 50–125 people, delivering one solution.

**You get:** ART, PI Planning, System Demo, Inspect & Adapt, Scrum Masters, Product Owners, Product Management, Release Train Engineer, System Architect, Business Owners, Iterations and the PI cadence.

**Choose it when:** you have one product or value stream, multiple teams, and dependencies that need a shared cadence.

### Large Solution SAFe
Adds a Solution Train above multiple ARTs — Solution Management, Solution Architect, Solution Train Engineer, pre- and post-PI planning.

**Choose it when:** the solution genuinely cannot be delivered by one ART — typically hundreds of people, hardware and software together, or regulated systems-of-systems (defence, aerospace, medical devices, large-scale infrastructure).

**Do not choose it because** you have two ARTs and it feels tidy. The coordination overhead is substantial and each extra layer moves decisions further from the work.

### Portfolio SAFe
Adds portfolio-level concerns above the ARTs: Lean Portfolio Management, strategic themes, portfolio Kanban, lean budgets, epics with guardrails, Value Stream Coordination.

**Choose it when:** funding and prioritisation are the actual constraint — money is allocated annually to projects and cannot follow evidence. This layer is where SAFe's most valuable ideas live (persistent funding of value streams, guardrails instead of gates).

See `lean-portfolio-management` — you can adopt these practices without adopting SAFe.

### Full SAFe
All layers. Genuinely appropriate for a small number of very large enterprises. If you are considering it, the question to answer first is whether the organisation needs to be this big to deliver this thing.

---

## Decision path

```
Multiple teams on one product, real dependencies?
  └─ No  → don't scale; fix team-level practice or reorganise
  └─ Yes → Is one train (5–12 teams) enough?
        └─ Yes → ESSENTIAL SAFe
        └─ No  → Is it truly one solution needing multiple trains?
              └─ Yes → LARGE SOLUTION SAFe
              └─ No  → separate trains, coordinate lightly

Separately: is funding/prioritisation the real constraint?
  └─ Yes → add the PORTFOLIO layer (or adopt LPM practices alone)
```

---

## What each layer costs

| Layer | Recurring cost | Watch for |
|---|---|---|
| Essential | PI Planning every 8–12 weeks (2 days, everyone); RTE role; ART sync cadence | PI Planning becoming a status event; teams losing the ability to change scope mid-PI |
| Large Solution | Pre/post-PI planning; Solution Train roles; extra integration cadence | Decisions drifting two layers away from the teams doing the work |
| Portfolio | Portfolio Kanban, epic governance, LPM cadence | Epic approval becoming the stage gate SAFe was meant to replace |

**Budget honestly:** Essential SAFe costs roughly 5–8% of team capacity in ceremony, plus the RTE role, plus two days per PI for everyone. That is defensible when it removes more waiting than it creates, and indefensible when it doesn't.

---

## Adoption sequence that works

1. **Team-level competence first.** Scrum or Kanban working properly in each team
2. **Technical practices.** Continuous integration and test automation before you add cadence — a train that cannot integrate is just a queue
3. **One train, one value stream.** Launch a single ART and run three PIs before considering anything else
4. **Inspect and adapt for real.** If the I&A workshop produces no change to how the ART works, the adoption is decorative
5. **Portfolio layer only when funding is the constraint** — and only if leadership will actually change how money moves

---

## Tailoring — what you can safely drop

SAFe is presented as a system, but in practice:

- **Keep:** PI Planning (the single highest-value practice), the System Demo, the dependency board, Inspect & Adapt, lean budgeting
- **Question:** the full role set — many organisations don't need a distinct Solution Architect or Business Owner per train
- **Drop without regret:** story points normalised across teams (breaks the metric), PI commitment treated as a contract, the full SAFe glossary imposed on everyone

Tailoring is normal and SAFe's own guidance allows it. The failure mode is tailoring away the hard parts — the cross-team conversation and the funding change — while keeping the ceremonies.

---

## SAFe anti-patterns

| Anti-pattern | What it looks like |
|---|---|
| **SAFe as a rebadge** | Programme managers become RTEs, projects become epics, nothing else changes |
| **Velocity normalisation** | Points made comparable across teams so they can be compared. Guaranteed gaming |
| **PI commitment as contract** | Teams punished for missing PI objectives; sandbagging follows within one PI |
| **Big-room planning theatre** | Two days of presentations, plan already decided |
| **Train without technical practices** | Cadence imposed on teams who can't integrate; the increment never exists |
| **Portfolio without funding change** | Portfolio Kanban on top of annual project budgets |
| **Certification as adoption** | Everyone trained, nothing different |
