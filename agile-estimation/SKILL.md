---
name: Agile Estimation
description: This skill should be used when the user asks about "agile estimation", "story points", "planning poker", "t-shirt sizing", "estimation techniques", "relative estimation", "dot voting estimation", "affinity estimation", "three-point estimation", "#noestimates", "right-sizing stories", "splitting user stories", "breaking down epics", "acceptance criteria", "user story writing", "INVEST criteria", "definition of ready", "backlog refinement estimation", "velocity based estimation", "throughput forecasting", or needs help with backlog refinement, story writing, or estimation practices.
version: 1.0.0
---

# Agile Estimation

Estimation in agile serves planning and forecasting — not performance management or commitment. The goal is to create a shared understanding of relative size and complexity, enabling teams to make informed decisions about what to take into a sprint and how to forecast delivery.

## Core Principle: Relative, Not Absolute

Agile estimation is relative: "This story is twice as complex as that one." It is not an effort-hour estimate pretending to be story points. Teams that translate story points to hours undermine the benefits of relative sizing.

Story points capture a combination of:
- **Complexity**: How hard is this to understand and implement?
- **Effort**: How much work is involved?
- **Uncertainty**: How much do we not know yet?

---

## Estimation Techniques

### Planning Poker

The most widely used agile estimation technique. Produces consensus through structured discussion.

**How it works**:
1. PO reads and clarifies a backlog item
2. Each team member privately selects a card (modified Fibonacci: 0, 1, 2, 3, 5, 8, 13, 20, 40, 100, ?, ∞)
3. All cards revealed simultaneously (prevents anchoring)
4. Discuss divergence — the extremes explain their reasoning
5. Repeat until convergence; team agrees on estimate

**Why simultaneous reveal matters**: If one person reveals first, others anchor to their number. The whole point is independent estimation followed by discussion.

**Handling divergence**: Don't average — discuss. The person with the highest estimate often sees complexity others missed. The person with the lowest may have a simpler approach. Both views are valuable.

**When to use**: Sprint refinement sessions with 5–12 items. Works best for 10 or fewer items per session. Take your time on the first few items to calibrate the team's scale.

**Modified Fibonacci sequence**: 1, 2, 3, 5, 8, 13, 20, 40, 100 (some teams add ½ and ∞). The gaps between large numbers reflect that our estimates are increasingly imprecise as size grows.

### T-Shirt Sizing

Faster than planning poker. Useful for large backlogs, epics, or when a rough scale is sufficient.

**Sizes**: XS, S, M, L, XL, XXL

**How it works**:
1. Establish reference items for each size using known stories
2. For each new item, team agrees (by discussion or dot vote) on a size
3. Can be mapped to story points later if needed (e.g., S=3, M=5, L=8, XL=13)

**When to use**: Initial backlog sizing, Epic-level estimation, new teams still calibrating, large backlogs needing quick triage.

### Affinity Estimation

Fastest technique for large volumes. Silent, then discuss outliers.

**How it works**:
1. Write each item on a card
2. Silently arrange cards on a spectrum from smallest to largest
3. Cluster into size groups (or Fibonacci values)
4. Discuss only where placement is disputed

**When to use**: Sizing 20+ items quickly; backlog grooming sessions with a large unestimated backlog.

### Dot Voting (for Priority, not Size)

Dot voting is a prioritisation technique, not a size estimation technique. Teams sometimes confuse these.

**Use for**: Deciding which items to focus on this sprint, which topics to discuss in a retro, which risks to address first.

**Not for**: Estimating complexity or effort.

### Three-Point Estimation (PERT)

Used when uncertainty is high or when converting to time estimates is required (some governance contexts demand it).

**Formula**: `(Optimistic + 4×Most Likely + Pessimistic) / 6`

Example: O=2 days, M=5 days, P=12 days → (2 + 20 + 12) / 6 = 5.67 days

**When to use**: Fixed-scope contracts, regulatory delivery contexts, when probability ranges are needed for risk management.

---

## Choosing an Estimation Technique

| Need | Technique |
|---|---|
| High precision, shared understanding | Planning Poker |
| Speed with reasonable accuracy | T-Shirt Sizing |
| Large backlog, quick triage | Affinity Estimation |
| Avoid estimation entirely | #NoEstimates (use throughput) |
| Time-based governance requirements | Three-Point / PERT |

---

## #NoEstimates

A pragmatic alternative: skip story-point estimation entirely and use **throughput** for forecasting.

**How it works**:
1. Right-size all stories to approximately the same size (≤ 1 day of work)
2. Count completed stories per sprint (throughput)
3. Use historical throughput + Monte Carlo simulation to forecast delivery dates

**Advantages**: Eliminates estimation overhead; forecasts are based on actual delivery data, not guesses; no velocity gaming.

**Requirements**: Stories must be consistently small. Teams need discipline in story splitting.

---

## Writing Good User Stories

User stories are placeholders for conversations, not requirement specifications. The INVEST criteria help teams write better stories.

### INVEST Criteria

- **Independent**: Can be developed and delivered separately from other stories
- **Negotiable**: Not a fixed contract — details are discussed with the PO
- **Valuable**: Delivers value to an identified user or stakeholder
- **Estimable**: The team can estimate the size
- **Small**: Fits within a Sprint
- **Testable**: Acceptance criteria are clear enough to test

### Story Format

`As a [user type], I want [action/goal], so that [benefit/reason]`

- **User type**: Be specific — not "user" but "returning customer" or "operations analyst"
- **Action**: What they want to do, not what the system should do
- **Benefit**: The "so that" is the most important part; it guides implementation decisions

### Acceptance Criteria

Use **Given / When / Then** (BDD) format:
- **Given** [a context or precondition]
- **When** [an action is taken]
- **Then** [an expected outcome occurs]

Example:
- Given a customer has items in their basket
- When they click "Proceed to checkout"
- Then they are taken to the delivery address page with their saved addresses pre-populated

Write acceptance criteria before estimating. If the team can't write them, the story needs more analysis.

---

## Story Splitting Patterns

Large stories (Epics or L/XL items) must be split before they can be pulled into a Sprint. Common patterns:

| Pattern | Example Split |
|---|---|
| **By workflow step** | "User registers" → split into: capture details / validate / confirm / notify |
| **By user type** | "User manages account" → admin user / standard user / guest user |
| **By data variation** | "Search products" → by name / by category / by price range |
| **By operation** | CRUD → Create / Read / Update / Delete as separate stories |
| **Happy path first** | Basic flow without edge cases; add edge cases as separate stories |
| **Spike first** | Create a time-boxed investigation story when there's too much uncertainty to estimate |

**Avoid**: Splitting by architecture layer ("frontend for story X" + "backend for story X"). These are tasks, not user stories, and they don't deliver independent value.

---

## Definition of Ready

Some teams use a Definition of Ready (DoR) to gate items before they enter Sprint Planning. A story is ready when:

- Acceptance criteria are written and agreed
- Dependencies are identified and resolved (or acceptance criteria updated to reflect what's possible)
- The team can estimate it
- It fits within a Sprint (or can be split further)
- Any necessary designs or technical spikes are complete

**Caution**: A DoR can create a mini-waterfall if applied rigidly. Use it as a conversation guide, not a hard gate.

## Additional Resources

- **`references/story-splitting-guide.md`** — Detailed patterns and examples for splitting large stories
- **`references/acceptance-criteria-templates.md`** — Given/When/Then templates for common story types
