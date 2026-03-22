---
name: Continuous Improvement
description: This skill should be used when the user asks about "continuous improvement", "kaizen", "inspect and adapt", "team improvement", "process improvement", "improvement culture", "improvement backlog", "improvement kata", "improvement cycle", "PDCA", "plan do check act", "root cause analysis", "5 whys", "fishbone diagram", "Ishikawa", "lean thinking", "waste elimination", "value stream mapping", "improvement metrics", "retrospective improvement", "sustainable improvement", "improvement anti-patterns", "making improvements stick", "organisational improvement", "systems thinking", "bottleneck analysis", "constraint theory", "theory of constraints", or is trying to sustain or deepen a continuous improvement culture.
version: 1.0.0
---

# Continuous Improvement

Continuous improvement is the sustained practice of making small, frequent, evidence-based changes to how a team or organisation works. It is not a project with an end date — it is a permanent operating mode.

In agile contexts, the Retrospective is the primary continuous improvement ceremony. But retrospectives alone are insufficient. Improvement culture requires feedback loops, measurement, psychological safety, and systems thinking embedded in how the team operates every day.

This skill links to:
- **`scrum`** — Sprint Retrospective as the core improvement event
- **`kanban`** — Flow metrics and bottleneck identification
- **`agile-coach`** — Coaching teams toward self-improvement
- **`agile-metrics`** — Measuring whether improvements are working
- **`facilitation`** — Running improvement workshops effectively

---

## The Improvement Mindset

Three foundational beliefs distinguish genuinely improving teams from teams that perform improvement:

1. **Current state is a hypothesis, not a standard** — How we work today is our best current answer, not the right answer. Everything is subject to experimentation.

2. **Problems are treasures** — Surfacing a problem is a gift. The system that hides problems cannot improve. Leaders must visibly reward those who surface issues, not just those who hit targets.

3. **Small and frequent beats big and occasional** — A 1% improvement each sprint compounds. A large improvement initiative once a year creates change fatigue and rarely sticks.

---

## PDCA: The Improvement Cycle

Plan–Do–Check–Act (Deming Cycle) is the foundation of all structured improvement work.

**Plan**: Identify the problem; hypothesise a cause; design a small experiment (the improvement)

**Do**: Implement the experiment in a constrained way — one team, one sprint, one workflow

**Check**: Measure the outcome. Did it improve the metric we targeted? What else changed?

**Act**: If it worked — standardise and spread. If it didn't — learn and try again. If results are mixed — investigate.

**Key insight**: Most improvement efforts skip Check. They implement a change and assume it worked. Without measurement, improvement is guesswork.

---

## Retrospective as Improvement Engine

The Sprint Retrospective is the team's structured PDCA cycle. For it to drive real improvement:

**Make improvements to the Sprint Backlog**: Improvement actions must compete with other work for capacity. If they're not in the Sprint Backlog, they won't get done.

**One or two improvements, not ten**: Teams that list ten retrospective actions complete zero. Ruthlessly select the highest-impact one or two.

**Review last retro's action first**: Before generating new improvement ideas, review what was committed last time. If it wasn't done — that itself is worth understanding.

**Track improvement metrics**: If cycle time is the target metric, track it sprint-over-sprint. If the improvement isn't visible in the data, either the measurement is wrong or the intervention isn't working.

See **`scrum`** skill → `references/retrospective-formats.md` for facilitation formats.

---

## Root Cause Analysis

Retrospectives surface symptoms. Root cause analysis finds the causes worth addressing.

### Five Whys

**How**: Ask "Why did this happen?" five times (or until you reach a cause you can actually address).

**Example**:
1. *The deployment failed.* → Why? *The test suite didn't catch the regression.*
2. → Why? *The test coverage for that module is <40%.*
3. → Why? *We agreed to write tests but deprioritised it when the sprint got tight.*
4. → Why? *We don't have a DoD item that mandates test coverage.*
5. → Why? *We haven't agreed what "done" means for technical quality.* ← **Root cause**

**Common mistake**: Stopping at the first technical cause (step 1 or 2). The real root cause is almost always a process, agreement, or culture issue.

### Fishbone Diagram (Ishikawa / Cause-and-Effect)

**When to use**: When a problem has multiple potential contributing causes across different categories.

**How**:
1. Write the problem at the head of the fish (right side)
2. Draw the spine and branches representing cause categories: People / Process / Tools / Environment / Materials / Management (choose relevant ones)
3. Brainstorm causes in each category; attach to branches
4. Identify which causes are most probable or most actionable
5. Investigate those causes with Five Whys

**Use in agile teams**: After a serious incident, a missed sprint goal repeatedly, or a quality failure.

---

## Kaizen: Small, Continuous Improvement

Kaizen (Japanese: "good change") is the philosophy of small, daily improvements by everyone, not large transformations by a few.

**Kaizen principles**:
- Improvement is everyone's job, not just the SM's or coach's
- Small improvements today are better than perfect improvements someday
- Never blame people — fix systems
- Standardise what works; improve the standard continuously

**Team Kaizen practices**:
- **Improvement backlog**: A visible, prioritised list of improvement ideas — separate from the product backlog but reviewed at refinement
- **5-minute improvements**: If it takes less than 5 minutes to fix, fix it now rather than adding it to a backlog
- **Kaizen board**: A physical or digital board showing: To Try → In Progress → Done (for improvements specifically)

---

## Lean Thinking and Waste Elimination

Lean provides a vocabulary for identifying what to improve. The seven wastes of software development (Mary and Tom Poppendieck, adapted from Toyota):

| Waste | Description | Agile Manifestation |
|---|---|---|
| **Partially done work** | Incomplete items consuming capacity | Unfinished sprint items, long-lived branches |
| **Extra features** | Building more than needed | Gold-plating, features nobody uses |
| **Relearning** | Rediscovering what was already known | No knowledge sharing; tribal knowledge |
| **Handoffs** | Passing work between people/teams | Component teams; sequential approval chains |
| **Delays** | Waiting for decisions, reviews, dependencies | Sprint items blocked for days; PRs waiting |
| **Task switching** | Context switching between unrelated work | Too much WIP; too many priorities |
| **Defects** | Work that doesn't meet quality standards | Bugs found in review, test, or production |

Use this list in retrospectives to categorise and name what's slowing the team down.

---

## Value Stream Mapping

Value Stream Mapping (VSM) traces how work flows from request to delivery. Used to identify delays, handoffs, and improvement opportunities at a system level.

**How to run a VSM session (abbreviated)**:
1. Agree on a representative work type (e.g., "new feature", "bug fix")
2. Map each step from customer request to production deployment (left to right)
3. For each step, capture: average time active, average wait time before/after
4. Identify the step with the longest wait time — that's the primary improvement target
5. Understand the cause of that wait; design an experiment to reduce it

**Output**: A shared understanding of where time is actually spent vs. where teams assume it's spent. The two are almost always different.

---

## Theory of Constraints

Eliyahu Goldratt's insight: every system has one primary constraint that limits its throughput. Improving anything other than the constraint doesn't improve the system.

**Five focusing steps**:
1. **Identify** the constraint (what is limiting throughput?)
2. **Exploit** the constraint (maximise its output without major investment)
3. **Subordinate** everything else to the constraint (align other activities to feed the constraint optimally)
4. **Elevate** the constraint (invest to increase its capacity if needed)
5. **Repeat** (once the constraint is resolved, a new one will emerge)

**In software teams**: Common constraints are: code review throughput, deployment pipeline capacity, Product Owner availability, test environment capacity, and stakeholder decision speed.

**Practical application**: Use cycle time data and CFD analysis (see **`kanban`** skill) to identify where work accumulates — that's your constraint.

---

## Making Improvements Stick

The most common failure mode: improvements are identified in retrospectives but never implemented. Causes and remedies:

| Cause | Remedy |
|---|---|
| No capacity reserved for improvement | Treat improvement items as first-class Sprint Backlog items; reserve 10–20% capacity |
| No accountability | Named owner per improvement item; reviewed at start of next retro |
| Too many at once | Maximum 2 improvement items per sprint |
| No measurement | Define the metric that will confirm the improvement worked |
| Improvement misses the root cause | Use Five Whys before selecting the improvement |
| Management removes improvement capacity | Coach leadership on the ROI of improvement work |

---

## Improvement Culture Indicators

**Healthy**:
- Retrospectives produce different improvement items each sprint (team finds new things to improve)
- Team members raise problems without fear
- Failed experiments are discussed openly and treated as learning
- Improvement items are regularly completed
- Metrics trend in the right direction over 2–3 month windows

**Unhealthy**:
- Same issues appear in every retrospective
- Retrospective outputs are always aspirational but never actioned
- "We don't have time for improvements" is accepted as a valid position
- Problems are attributed to people, not systems
- Improvement work is the first thing cut when sprint gets tight

---

## Systems Thinking

Individual interventions in complex systems often produce unexpected results. Systems thinking helps improvement practitioners anticipate second-order effects.

**Useful mental models**:
- **Feedback loops**: Changes create effects that feed back to the change (reinforcing loops amplify; balancing loops constrain)
- **Delays**: The effect of a change is often not visible immediately; teams abandon improvements too soon
- **Local vs. global optimisation**: Improving one team's throughput can create a bottleneck elsewhere in the system
- **Emergent behaviour**: Team behaviour emerges from structure, incentives, and culture — not from individual personalities

**Practical implication**: Before implementing an improvement, ask: "What else might change as a result? Who else is affected? What are the second-order effects?"

## Additional Resources

- **`references/improvement-tools-reference.md`** — Quick reference for PDCA, Five Whys, Fishbone, VSM, and Theory of Constraints
- **`references/improvement-metrics-templates.md`** — Metric templates for tracking improvement outcomes sprint-over-sprint
