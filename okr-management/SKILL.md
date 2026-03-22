---
name: OKR Management
description: This skill should be used when the user asks about "OKRs", "objectives and key results", "OKR setting", "OKR cadence", "OKR grading", "OKR scoring", "OKR retrospective", "OKR check-in", "writing OKRs", "key results", "OKR alignment", "OKR anti-patterns", "team OKRs", "company OKRs", "OKR hierarchy", "OKR workshop", "OKR review", "OKRs vs KPIs", "connecting OKRs to delivery", "OKR facilitation", "quarterly goals", "goal setting agile", "outcome vs output", or is working on goal-setting, strategic alignment, or outcome-based planning in an agile context.
version: 1.0.0
---

# OKR Management

OKRs — Objectives and Key Results — are a goal-setting framework designed to align organisations around ambitious outcomes, create transparency at every level, and drive disciplined focus. Used well, OKRs shift teams from measuring what they do to measuring what they achieve. Used poorly, they become another reporting burden that nobody believes in.

This skill covers the full OKR lifecycle: writing, aligning, running cadences, scoring, and connecting OKRs to agile delivery.

---

## 1. What Are OKRs?

**Origin**: OKRs were developed at Intel by Andy Grove in the 1970s as a simplified version of Peter Drucker's Management by Objectives. John Doerr introduced the framework to Google in 1999, and its adoption there — alongside the publication of Doerr's book *Measure What Matters* (2018) — drove widespread uptake across the technology industry and beyond.

**The two components**:

| Component | What it is | Characteristics |
|---|---|---|
| **Objective (O)** | Where you want to go | Qualitative, inspirational, time-bound, memorable |
| **Key Result (KR)** | How you know you've arrived | Quantitative, outcome-based, measurable, 0–1 scored |

An Objective without Key Results is a wish. Key Results without an Objective are metrics in search of a purpose.

**OKRs vs KPIs**:

OKRs and KPIs serve different purposes and should coexist, not compete.

| | OKRs | KPIs |
|---|---|---|
| **Purpose** | Set direction; drive change | Monitor ongoing health |
| **Nature** | Stretch goals; temporary | Steady-state; continuous |
| **Frequency** | Quarterly or annual | Monthly or ongoing |
| **Failure** | Acceptable (0.7 target, not 1.0) | Failure signals a problem |
| **Example** | Increase trial-to-paid conversion by 20% | Monthly active users, churn rate |

A team might track NPS as a KPI (you should never let it fall below 40) and simultaneously run an OKR to improve it from 42 to 60 this quarter.

**OKRs vs output metrics**:

Output metrics measure what teams produce: features shipped, story points completed, releases deployed. OKRs measure outcomes — the change in user or business behaviour those outputs create. A team can ship ten features and move no OKR. That is a sign either the features were the wrong ones, or the OKR was poorly written.

---

## 2. Writing Good OKRs

### Strong Objectives

A good Objective is:

- **Inspirational**: It should motivate the team to get out of bed. "Improve system performance" is forgettable. "Make our platform the fastest in the market" is not.
- **Qualitative**: Objectives describe direction and ambition, not numbers. Numbers belong in Key Results.
- **Time-bound**: An Objective without a deadline is a dream. Quarterly OKRs are finite by definition; annual ones need mid-point reviews.
- **Achievable with effort**: Ambitious but not absurd. A genuinely stretch goal sits at the edge of what feels possible.
- **Memorable**: If the team cannot recall the Objective without looking it up, it is not doing its job.

**Weak vs strong Objectives**:

| Weak | Strong |
|---|---|
| Improve the product | Build the product our users love most |
| Reduce infrastructure costs | Operate with world-class efficiency and reliability |
| Work better as a team | Become the most trusted engineering team in the organisation |

### Strong Key Results

A good Key Result is:

- **Measurable**: There is no ambiguity about whether it has been achieved. A score from 0 to 1 can be calculated objectively.
- **Outcome-based**: It measures a change in state — user behaviour, business result, or system performance — not a task completed.
- **Independently verifiable**: Someone else can read the data and reach the same score.
- **Set at a stretch level**: A score of 1.0 should feel unlikely at the time of writing. If it feels certain, it is not a stretch KR.

**Weak vs strong Key Results**:

| Weak (output / task-based) | Strong (outcome-based) |
|---|---|
| Launch the new onboarding flow | Increase 7-day activation rate from 38% to 55% |
| Complete security audit | Reduce critical CVEs in production to zero |
| Run three customer interviews | Achieve Net Promoter Score of 50+ from new customer cohort |
| Write API documentation | 90% of integration partners successfully self-serve via docs within 30 days |

### How Many OKRs?

- No more than **3–5 Objectives** per level (company, team, individual)
- No more than **3–5 Key Results per Objective**
- Fewer is better. OKRs require genuine focus. Ten objectives signal that nothing is truly a priority.

### Common Writing Mistakes

- **Tasks disguised as KRs**: "Deliver feature X" is a task. "Reduce user time-to-first-value by 40%" is a Key Result.
- **Unmeasurable KRs**: "Improve team culture" cannot be scored. "Increase team eNPS from 20 to 45" can.
- **Objectives with numbers**: Objectives are qualitative. If your Objective contains a percentage, the number probably belongs in a KR.
- **Copying last quarter's OKRs**: OKRs should reflect current strategic priorities. Stale OKRs are a sign the process has become performative.
- **Guaranteed outcomes**: If every KR scores 1.0 every quarter, the targets are too conservative.

---

## 3. OKR Cadence

A healthy OKR practice runs on a layered cadence of planning, check-ins, reviews, and retrospectives.

### Annual vs Quarterly OKRs

| | Annual OKRs | Quarterly OKRs |
|---|---|---|
| **Typical level** | Company, sometimes department | Team and individual |
| **Purpose** | Set strategic direction | Translate strategy into near-term focus |
| **Review frequency** | Mid-year and end-of-year | Every week or fortnight |
| **Flexibility** | Low — change signals strategic drift | Moderate — can adapt to new information |

Most organisations run company OKRs annually and team OKRs quarterly. The quarterly team OKRs should contribute directly to the annual company OKRs.

### Check-ins (Weekly / Fortnightly)

Regular check-ins are the heartbeat of OKR execution. Without them, OKRs become a quarterly paperwork exercise.

A check-in should answer three questions:
1. What is the current score for each KR (0–1)?
2. What is the confidence level — has the forecast for end-of-quarter changed?
3. What are the blockers or risks to achieving the KR?

Check-ins are not a status report for leadership. They are a team discipline for staying honest about progress and adjusting effort accordingly. They should take no more than 30 minutes.

### Mid-Cycle Reviews

At the midpoint of a quarter (typically weeks 6–7 of a 13-week quarter), run a deeper review:
- Is each OKR still relevant, or has the strategy shifted?
- Are any OKRs already complete (a sign they were not stretching enough)?
- Are any OKRs clearly unachievable (a sign they need replanning or de-prioritisation)?
- Are resources allocated appropriately to the highest-priority OKRs?

The mid-cycle review is the right time to make hard calls — not to retroactively lower targets to protect scores.

### End-of-Quarter Grading

At the end of the quarter, each Key Result is scored 0–1 and the scores are published openly. The grading session should be honest and brief. It feeds directly into the OKR retrospective.

### OKR Retrospective

After grading, hold a retrospective focused on the OKR process as well as the outcomes:
- Which OKRs were achieved? What drove that?
- Which were missed? What would we do differently?
- Were the OKRs the right ones? Did they reflect true priorities?
- How did the OKR process itself work — cadence, check-ins, visibility?
- What carries forward into next quarter?

---

## 4. OKR Hierarchy

OKRs work at multiple levels simultaneously, and the connections between those levels are where most organisations struggle.

### The Four Levels

```
Company OKRs
    └── Department / Programme OKRs
            └── Team OKRs
                    └── Individual OKRs (optional)
```

**Company OKRs** set the strategic direction for the year. They are owned by the CEO and leadership team, made public to all employees, and typically contain 3–5 Objectives.

**Department / Programme OKRs** translate company OKRs into divisional priorities. A single company OKR may be supported by multiple department OKRs.

**Team OKRs** are where delivery happens. They should connect clearly to at least one department or company OKR and be owned by the team collectively, not assigned by management.

**Individual OKRs** are optional and controversial. Many practitioners recommend against individual OKRs because they can create unhealthy competition, undermine collaboration, and blur the line between OKRs and performance management. If used, they should be self-set and developmental in nature.

### Alignment vs Autonomy

The tension in OKR hierarchies is between top-down alignment (ensuring everyone pulls in the same direction) and bottom-up autonomy (allowing teams to determine how they contribute). The best OKR programmes do both:

- **Top-down**: Company OKRs set direction; teams are expected to connect their work to them.
- **Bottom-up**: Teams propose their own OKRs; leadership reviews for alignment, not dictates content.

A rule of thumb: approximately 40% of team OKRs should be self-generated (addressing team-level opportunities or improvements), with 60% aligned to company/department direction. Rigid top-down cascades produce compliance, not commitment.

### Bidirectional OKRs

In a mature OKR organisation, goal-setting flows in both directions:
- Leadership communicates strategic priorities (what matters and why)
- Teams propose OKRs in response, surfacing ground-level insights
- Leadership reviews for gaps and misalignments before finalising

This dialogue — rather than waterfall-style cascading — produces OKRs that teams genuinely own.

---

## 5. Connecting OKRs to Agile Delivery

OKRs and agile delivery are natural partners, but the connection requires deliberate design. Without it, agile teams run sprints that ship features disconnected from outcomes, and OKR reviews become an awkward quarterly exercise disconnected from how the team actually works.

### Linking the Product Backlog to OKRs

Every item in the product backlog should be traceable — directly or indirectly — to an OKR. A simple approach:

1. Label each backlog item with the OKR(s) it supports (using tags, a custom field, or a simple naming convention)
2. During backlog refinement, challenge items that cannot be linked to any active OKR
3. Use OKR alignment as one factor in prioritisation — items that directly move a Key Result score warrant higher priority

This does not mean every item needs a direct measurable link. Enabling work, technical debt reduction, and operational tasks support OKRs indirectly. The discipline is to be explicit about which OKR a piece of work serves and why.

### Sprint Goals and OKRs

The Scrum Guide requires a Sprint Goal for every Sprint. A well-crafted Sprint Goal aligns naturally with one or more Key Results:

- **Weak Sprint Goal**: "Complete the user stories in column A of the board"
- **Strong Sprint Goal**: "Enable users to complete checkout without assistance — moving our self-serve rate KR from 0.3 to 0.5"

The Sprint Goal becomes the team's short-horizon expression of its OKR commitment. Sprint Reviews should then explicitly address: what changed in our OKR scores as a result of this sprint?

### Avoiding Output Theatre

Output theatre is the agile anti-pattern where teams celebrate delivery of features whilst OKR scores remain static. It emerges when:
- Sprint reviews focus only on what was built, not what changed for users
- Velocity is the primary success metric
- Product Owners accept completed stories as "done" without evidence of outcome

To break the pattern:
- Make OKR score movement a standing agenda item in Sprint Reviews
- Instrument features before shipping so outcome data is available quickly
- Distinguish between delivery milestones ("we shipped X") and outcome milestones ("X moved KR Y from 0.4 to 0.6")

---

## 6. OKR Scoring and Grading

### The 0–1 Scale

Each Key Result is scored on a continuous scale from 0.0 (no progress) to 1.0 (fully achieved). Scores are not binary. A score of 0.6 represents meaningful progress and is not a failure.

| Score range | Interpretation |
|---|---|
| 0.0 – 0.3 | Little to no progress; root cause should be understood |
| 0.4 – 0.6 | Moderate progress; some value delivered, but fell short |
| 0.7 – 0.9 | Strong progress; this is the target zone for stretch goals |
| 1.0 | Fully achieved; consider whether the goal was ambitious enough |

### The 0.7 Target Zone

The most important counterintuitive principle in OKR grading: **a score of 0.7 is the goal, not a disappointment**. OKRs are designed to stretch. If a team scores 1.0 on every KR every quarter, their goals are not ambitious enough. Consistent 0.7–0.9 scoring indicates healthy stretch and honest self-assessment.

Google's original guidance: "If you're always getting 1.0, your OKRs aren't ambitious enough."

### Objective Scoring

An Objective score is typically the average of its Key Results scores, though teams may weight KRs by importance. The Objective score is indicative — the conversation about why each KR landed where it did is more valuable than the number itself.

### RAG Banding

For dashboards and programme-level visibility, scores can be expressed as RAG status:

| Colour | Score range | Meaning |
|---|---|---|
| Green | 0.7 – 1.0 | On track or achieved |
| Amber | 0.4 – 0.69 | At risk; intervention may be needed |
| Red | 0.0 – 0.39 | Off track; root cause review required |

### Avoiding Grade Inflation

Grade inflation — where teams consistently score themselves higher than performance warrants — destroys the credibility of the OKR process. Common causes:

- OKRs are tied to performance reviews, creating incentive to score high
- Leadership responds negatively to low scores, so teams sandbag targets or inflate grades
- Scoring is done in private rather than shared openly

Countermeasures: decouple OKRs from compensation decisions, celebrate honest low scores accompanied by learning, and publish all scores across the organisation.

---

## 7. OKR Anti-patterns

Understanding what OKRs are not is as important as understanding what they are.

**Sandbagging**
Teams set deliberately easy targets to guarantee high scores. Usually a symptom of OKRs being linked to performance management or of leadership over-reacting to missed targets. Address by celebrating learning from misses and by making the target-setting conversation visible.

**Too many OKRs**
Every team has 10 Objectives and 30 Key Results. Nothing is truly prioritised. The result is a reporting exercise, not a focus mechanism. Enforce a hard limit: 3–5 Objectives, 3–5 KRs each.

**Tasks as Key Results**
"Complete the API documentation" is not a Key Result — it is a task. Key Results measure the change that tasks create. If you cannot describe the outcome a task produces, you either don't understand its purpose or it should not be in the OKR.

**No connection to strategy**
Team OKRs that bear no relationship to company or department goals. Teams feel disconnected from organisational direction; leadership feels that delivery effort is not moving strategic needles. Fix with explicit alignment reviews before OKRs are finalised each quarter.

**OKRs as performance management**
Using OKR scores to evaluate individuals or set bonuses. This is the single most common way to destroy an OKR programme. When scores are tied to personal outcomes, teams sandbag, inflate grades, and stop taking risks. OKRs should inform conversations about performance, not mechanically determine them.

**Set and forget**
OKRs are written at the start of the quarter and not reviewed until the grading session. Without regular check-ins, the framework adds no value during the period it is meant to drive behaviour.

**Vanity OKRs**
OKRs that sound strategic but measure things the team can directly control regardless of external conditions (e.g., "publish 12 blog posts" rather than "grow organic inbound leads by 30%"). Vanity OKRs produce a false sense of progress.

**OKRs for everything**
Not all work should be captured in OKRs. Business-as-usual operations, mandatory compliance work, and ongoing maintenance are better tracked as KPIs or in a team's operational backlog. OKRs should reflect change and improvement, not the steady state.

---

## 8. Introducing OKRs to a Team or Organisation

### Common Rollout Mistakes

- **Big bang launch**: Introducing OKRs to the whole organisation simultaneously, without pilots. The first quarter is almost always rocky — better to absorb that learning in one team than across the business.
- **Importing someone else's OKRs**: Adopting OKRs verbatim from a case study or competitor without tailoring them to your context. OKRs must be written by the people who will execute against them.
- **Skipping the "why"**: Teams who do not understand the purpose of OKRs treat them as bureaucracy. Invest in education before implementation.
- **Linking to pay on day one**: The fastest way to destroy trust in the framework before it has had a chance to prove its value.

### Starting Small

Run a pilot with one team or one department for one quarter before scaling. Criteria for a good pilot team:
- Motivated to try something new
- Clear enough strategy to write meaningful OKRs
- Willing to share their scores openly, including misses

After the pilot, hold a public retrospective. Share what worked, what did not, and what the organisation is going to do differently. This demonstrates that the programme is learning, not just mandating.

### Building the Habit

OKRs become part of how a team thinks — rather than a quarterly task — when:
- Check-ins are integrated into existing meeting rhythms (sprint reviews, team syncs)
- OKR scores are visible on a shared dashboard or team wall
- Leaders reference OKRs in decision-making ("does this initiative support any of our current OKRs?")
- New work is evaluated against OKR alignment before being prioritised

### OKR Champions

Designate an OKR champion (or a small group) during the rollout phase. Their role is not to police the process but to:
- Support teams in writing better OKRs
- Facilitate check-ins until the habit is established
- Spot and surface systemic issues (too many OKRs, sandbagging, misaligned goals)
- Connect teams whose OKRs have dependencies or alignment opportunities

In an agile organisation, Scrum Masters and agile coaches are natural OKR champions.

---

## 9. OKR Facilitation

### OKR Writing Workshops

A well-facilitated OKR writing workshop turns a blank page into a draft set of OKRs in 90–120 minutes. A typical agenda:

1. **Context setting (10 min)**: Revisit company/department OKRs and strategic priorities for the period. What must the team focus on?
2. **Horizon scan (15 min)**: What did we learn last quarter? What opportunities or threats are most significant? What would we regret not addressing?
3. **Draft Objectives (20 min)**: Individually or in pairs, draft 3–5 candidate Objectives. Share and cluster. Vote if needed to narrow down.
4. **Draft Key Results (30 min)**: For each agreed Objective, draft KRs. Use the prompt: "What would we see in the world if this Objective were achieved?" Write 3–5 KRs per Objective.
5. **Stress-test (20 min)**: Challenge each KR against the quality criteria (see below).
6. **Alignment check (10 min)**: Map each team OKR to a company/department OKR. Any team OKR without a link is a candidate for removal or reframing.
7. **Confidence check (5 min)**: For each OKR, rate team confidence on a fist-to-five. Low confidence signals either an overly ambitious target or a missing dependency to surface.

### Facilitation Prompts

Use these prompts to draw out better OKRs from a team:

- "If we achieved this Objective perfectly, what would a customer or user notice?"
- "How would we know, from the data, that this Key Result had moved?"
- "If we did nothing this quarter, what would this metric do naturally?" (to check whether the KR represents genuine stretch)
- "Who outside this team would need to see this OKR and agree with it?"
- "Is this a KR or a task? Can we describe the outcome this task creates?"
- "What is the worst-case score if we deprioritise this OKR entirely?"

### Challenging Weak KRs

When a KR reads like a task or milestone, use the **"so that" technique**: ask the team to complete the sentence "We will do X *so that* Y". The Y is usually the real Key Result.

Example: "We will complete the API redesign" → "We will complete the API redesign *so that* partner integration time drops from 3 weeks to 3 days." The Key Result is the second part.

When a KR is unmeasurable, ask: "What data would tell us this had happened?" If the team cannot answer, the KR needs to be rewritten or replaced.

---

## 10. OKR Tools and Templates

### Simple OKR Template

Use this structure for recording and tracking OKRs:

| Field | Content |
|---|---|
| **Quarter** | e.g., Q2 2026 |
| **Team** | e.g., Platform Engineering |
| **Parent OKR** | Link to company/department OKR this supports |
| **Objective** | Qualitative, inspirational statement |
| **Key Result 1** | Measurable outcome with baseline and target |
| **KR1 Score** | 0.0 – 1.0 at check-in / end of quarter |
| **Key Result 2** | Measurable outcome with baseline and target |
| **KR2 Score** | 0.0 – 1.0 at check-in / end of quarter |
| **Key Result 3** | Measurable outcome with baseline and target |
| **KR3 Score** | 0.0 – 1.0 at check-in / end of quarter |
| **Objective Score** | Average of KR scores (or weighted) |
| **Owner** | Individual or team accountable |
| **Status** | On track / At risk / Off track |
| **Last updated** | Date of most recent check-in |

### Scoring Template

At each check-in, record:

| Key Result | Baseline | Target | Current | Score (0–1) | Confidence | Blocker / Note |
|---|---|---|---|---|---|---|
| 7-day activation rate | 38% | 55% | 44% | 0.35 | Medium | Onboarding redesign delayed to week 8 |
| Trial-to-paid conversion | 12% | 18% | 15% | 0.50 | High | A/B test running; results due week 7 |
| NPS (new customers) | 32 | 50 | 41 | 0.50 | Medium | Surveying cadence increased; trend positive |

**Score calculation**: (Current − Baseline) ÷ (Target − Baseline). Cap at 1.0.

Example: (44 − 38) ÷ (55 − 38) = 6 ÷ 17 = 0.35

### Example OKRs for a Software Delivery Team

**Objective 1: Make our platform the most reliable our customers have ever experienced**

| Key Result | Baseline | Target |
|---|---|---|
| Reduce P1 incident rate | 4 per month | 1 per month |
| Achieve 99.9% uptime across all production services | 99.4% | 99.9% |
| Reduce mean time to recovery (MTTR) | 45 min | 15 min |

**Objective 2: Accelerate the speed at which we deliver value to users**

| Key Result | Baseline | Target |
|---|---|---|
| Reduce lead time from commit to production | 8 days | 2 days |
| Increase deployment frequency | 3 per week | Daily |
| Reduce change failure rate | 18% | 5% |

**Objective 3: Earn the trust of our engineering organisation as a platform team**

| Key Result | Baseline | Target |
|---|---|---|
| Internal NPS from engineering teams using our platform | 22 | 50 |
| % of teams onboarded to CI/CD pipeline without external support | 40% | 85% |
| Reduce time for a new team to deploy their first service | 3 weeks | 3 days |

---

## Key Principles Summary

- OKRs measure **outcomes**, not outputs. If your KRs are tasks, rewrite them.
- **0.7 is success**. A 1.0 every quarter means your goals are not stretching you.
- OKRs and performance management **must stay separate**. Conflating them destroys the framework.
- Check-ins are **non-negotiable**. Without them, OKRs are quarterly paperwork.
- Start **small and visible**. Pilot with one team, share the learning, scale from evidence.
- The best OKRs are **written by the people who will deliver them**, informed by the direction set from above.
- Connect every sprint to an OKR. If a sprint cannot be linked to an outcome the organisation cares about, ask why the work is being done.
