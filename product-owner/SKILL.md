---
name: Product Owner
description: This skill should be used when the user asks about "product owner", "PO role", "product owner responsibilities", "product backlog management", "backlog prioritisation", "product vision", "product goal", "product owner anti-patterns", "product owner and scrum master", "product owner and stakeholders", "product owner coaching", "value maximisation", "product roadmap agile", "MoSCoW prioritisation", "WSJF", "cost of delay", "impact mapping", "opportunity solution tree", "user research agile", "product discovery", "product owner vs product manager", "empowered product team", or is working with, coaching, or acting as a Product Owner.
version: 1.0.0
---

# Product Owner

The Product Owner is accountable for maximising the value of the product resulting from the work of the Scrum Team. They are the single person accountable for the Product Backlog — its content, ordering, and transparency.

The PO is not a requirements clerk, a proxy for stakeholders, or a sprint traffic manager. They are the product's strategic owner: making the call on what gets built, in what order, and why.

This skill links to:
- **`scrum`** — Scrum framework, events, and artifacts the PO participates in
- **`agile-estimation`** — Story writing, acceptance criteria, and backlog refinement
- **`agile-ceremonies`** — Backlog Refinement, Sprint Planning, Sprint Review facilitation
- **`agile-delivery-manager`** — PO / ADM boundary; stakeholder management at programme level

---

## Core Accountabilities

The 2020 Scrum Guide defines the PO's accountabilities clearly:

1. **Developing and explicitly communicating the Product Goal** — The strategic destination for the product
2. **Creating and clearly communicating Product Backlog items** — Backlog items must be understood by the team
3. **Ordering the Product Backlog** — Priority is the PO's decision, informed by stakeholders and the team
4. **Ensuring the Product Backlog is transparent, visible, and understood** — The team should never be surprised by what's at the top

The PO may delegate these activities, but remains accountable. If the Scrum Team does not respect PO decisions, those decisions will not be implemented — a failure mode to address with the Scrum Master.

---

## Product Vision and Product Goal

**Product Vision**: The long-term destination — why this product exists and what it will become. Timeframe: 3–5 years. Stable. The "north star" for all decision-making.

**Product Goal**: The medium-term objective — the next significant outcome the team is working toward. One Product Goal at a time. When achieved, it's retired and a new one set. Timeframe: typically one quarter.

**Backlog items should serve the Product Goal**. If a backlog item cannot be connected to the current Product Goal, question whether it should be prioritised.

### Communicating Vision

Techniques for communicating product vision to teams and stakeholders:

- **Product Vision Board** (Roman Pichler): Market, Needs, Product, Business Goal on one page
- **Elevator pitch**: "For [target user] who [has need], [product] is a [category] that [key benefit]. Unlike [alternative], our product [differentiator]."
- **Product Box**: Teams imagine the physical box the product would be sold in — forces benefit-first thinking

---

## Backlog Management

### Ordering the Backlog

The Product Backlog is ordered, not just prioritised. One item is always next. The PO's ordering decisions should be explicit and explainable.

**Factors that drive ordering**:
- **Business value**: Which item delivers the most value to users or the business?
- **Risk**: Which item, if not done soon, puts the product goal at risk?
- **Dependencies**: What must be done first to unblock other work?
- **Learning**: What do we need to build to validate our assumptions?
- **Cost of Delay**: What is the opportunity cost of not doing this item now?

### Prioritisation Techniques

**MoSCoW**:
- Must Have — non-negotiable; without these the product fails
- Should Have — important but not critical; workarounds exist
- Could Have — nice to have; only if capacity exists
- Won't Have (this time) — explicitly out of scope for now

**WSJF (Weighted Shortest Job First)** — SAFe technique; useful for comparing features:
`WSJF = Cost of Delay / Job Duration`
Higher WSJF = do first. Cost of Delay includes: user/business value, time criticality, risk reduction/opportunity enablement.

**Kano Model**: Categorise features by their impact on customer satisfaction:
- **Basic** (must-be): Expected; absence causes dissatisfaction
- **Performance** (linear): More = more satisfaction; less = less
- **Delighters** (attractive): Unexpected; presence creates delight; absence is not noticed

Use Kano to identify which features are differentiators vs. table stakes.

### Backlog Refinement

The PO leads refinement — it is not the Scrum Master's meeting. Typical cadence: 1–2 sessions per sprint, covering ~10% of sprint capacity.

**PO responsibilities in refinement**:
- Present upcoming items and explain the user need behind them
- Clarify acceptance criteria with the team
- Adjust items based on team feedback (split, merge, reorder)
- Decide when an item is ready for Sprint Planning

**Definition of Ready (DoR)**: A lightweight checklist to ensure items are ready before entering Sprint Planning. The PO owns ensuring items meet it; the team owns defining it.

A typical DoR:
- [ ] User story written in agreed format (or equivalent)
- [ ] Acceptance criteria written and agreed with the team
- [ ] Dependencies identified and either resolved or reflected in criteria
- [ ] Team can estimate it (no open "we need to investigate" blockers)
- [ ] Sized small enough to complete within the Sprint

**Caution**: Apply the DoR as a conversation guide, not a bureaucratic gate. If items are stalled in "not ready", that's an impediment to investigate — not a feature of the system.

---

## Stakeholder Management

The PO represents stakeholders to the team and the team to stakeholders. Neither direction should be a passive relay.

**Represent stakeholders to the team**: Translate business needs into backlog items. Filter out requests that don't serve the Product Goal. Bring market context, user research, and business strategy into the team's understanding.

**Represent the team to stakeholders**: Explain why things are ordered the way they are. Push back on requests that would compromise value or quality. Set realistic expectations on delivery.

**Stakeholder engagement model**:
- Identify: Who has a stake in this product? (users, buyers, internal sponsors, regulators)
- Understand: What do they need? What do they fear? What does success look like for them?
- Engage: How often and in what format does each stakeholder need to hear from the PO?
- Sprint Review: Primary stakeholder touchpoint — invite, prepare, and facilitate genuine dialogue

**PO cannot be a "yes" person**: Saying yes to every stakeholder request is abdication, not service. The PO's job is to make the hard trade-offs and explain the reasoning.

---

## Product Discovery

The PO should continuously validate that the backlog reflects real user needs, not assumptions.

**Opportunity Solution Tree** (Teresa Torres): Visualises the path from business outcome → user opportunities → solutions → experiments. Prevents jumping to solutions before understanding the opportunity.

**Impact Mapping** (Gojko Adzic): Connects business goals → actors → impacts → deliverables. Keeps the backlog anchored to outcomes, not features.

**Continuous Discovery Habits**:
- Talk to customers weekly (even brief interviews)
- Observe users using the product (not just gathering feedback)
- Track product usage data; connect to backlog items
- Run small experiments before committing to full features

---

## PO Participation in Scrum Events

| Event | PO Role |
|---|---|
| **Sprint Planning** | Proposes Sprint Goal; clarifies backlog items; negotiates scope |
| **Daily Scrum** | Optional; available for questions; not a participant unless also a Developer |
| **Backlog Refinement** | Leads the session; presents and clarifies items |
| **Sprint Review** | Hosts/presents; collects stakeholder feedback; updates backlog based on outcomes |
| **Sprint Retrospective** | Full participant; reflects on how PO collaboration can improve |

---

## Product Owner vs. Product Manager

These roles are often confused and sometimes combined:

| Dimension | Product Owner (Scrum) | Product Manager |
|---|---|---|
| Focus | Team-level; backlog; sprint | Strategic; market; business model |
| Scope | One product/value stream | May span multiple products |
| Framework | Scrum-specific accountability | Framework-agnostic |
| Horizon | Current + next sprint | 6–18 months |
| Primary output | Ordered Product Backlog | Strategy, roadmap, go-to-market |

In many organisations, one person holds both roles. In larger organisations, the PM sets strategy and the PO translates it into a backlog. Neither is a proxy for a requirements committee.

---

## Product Owner Anti-Patterns

| Anti-Pattern | Description | Impact | Remedy |
|---|---|---|---|
| Absent PO | Unavailable for questions; rarely attends events | Team builds the wrong thing; blocked in refinement | Negotiate protected time; clarify accountability with management |
| Proxy PO | Forwards requests from "the business" without filtering or deciding | No prioritisation; team receives conflicting signals | PO must have authority to say no; coach the true decision-maker |
| Story Factory | Writes stories continuously; backlog grows faster than team can deliver | Team loses sight of Product Goal; no strategic clarity | Focus on Product Goal; prune backlog ruthlessly |
| Scope Creep Enabler | Accepts all requests; never says no | Sprint goals missed; team overloaded | Coach on trade-offs; use WSJF or MoSCoW explicitly |
| Micromanager | Specifies implementation, not outcome | Undermines team autonomy; technical debt | Reframe to outcomes: "what problem are we solving?" not "how should this work?" |
| Part-time PO | Holds the role alongside another full-time role | Backlog unrefined; sprint planning chaotic | Advocate for dedicated PO time; minimum 50% |

---

## Coaching the Product Owner

When coaching a PO (as SM or Agile Coach):

**Common growth areas**:
- Saying no: Most new POs find this hardest. Practise giving reasons; connect no to the Product Goal
- Writing outcomes not features: "Users can track their delivery" not "Add tracking page"
- Being available: PO presence in refinement and at team questions is irreplaceable
- Backlog hygiene: Regular pruning; items older than 6 months without prioritisation are probably waste

**Useful coaching questions**:
- "What user problem does this solve?"
- "If you could only ship one thing this sprint, what would it be and why?"
- "What would we stop building if this item goes to the top?"
- "How will you know when this feature has delivered its value?"

## Additional Resources

- **`references/backlog-management-techniques.md`** — Detailed prioritisation and ordering techniques with worked examples
- **`references/product-discovery-methods.md`** — Continuous discovery practices, Opportunity Solution Tree, Impact Mapping
