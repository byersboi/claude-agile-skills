---
name: Team Health
description: This skill should be used when the user asks about "team health", "team health check", "team health survey", "sprint survey", "health check survey", "team morale", "team wellbeing", "measuring team health", "team health dimensions", "psychological safety survey", "team health radar", "Spotify health check", "squad health check", "team health trends", "team health data", "triangulating team signals", "reading team health", "team health indicators", "team health action", "acting on team health", "team health report", "sharing health data", "team health baseline", "team health over time", "team health intervention", or is an SM monitoring and responding to team health using surveys, retrospectives, and one-to-one conversations.
version: 1.0.0
---

# Team Health

Team health is the Scrum Master's primary diagnostic responsibility. Delivery metrics tell you what a team is producing; health metrics tell you whether the team is sustainable — whether it can keep producing, improve, and weather difficulty without breaking.

A healthy team is not a happy team in a superficial sense. It is a team that communicates honestly, challenges each other safely, recovers from setbacks, and continuously improves. Health is not a feeling — it is a set of observable, measurable conditions that either enable or undermine high performance.

The SM's job is not to make the team feel good. It is to maintain the conditions under which the team can do its best work.

## What Team Health Actually Is

Health is multi-dimensional. A team can score well on delivery confidence and poorly on psychological safety. A team can feel great about collaboration and be quietly burning out. Measuring only one dimension gives a false picture.

**Core dimensions of team health**:

| Dimension | What it measures |
|---|---|
| **Psychological safety** | Can people speak up, admit mistakes, and challenge without fear? |
| **Clarity** | Does the team understand its goals, priorities, and what good looks like? |
| **Collaboration** | Does the team work well together — sharing knowledge, helping each other, resolving friction? |
| **Morale & energy** | Is the team engaged and motivated, or drained and going through the motions? |
| **Quality** | Does the team take pride in the work? Is technical debt a source of stress? |
| **Delivery confidence** | Does the team feel it can meet its commitments? Is the pace sustainable? |
| **Learning & improvement** | Is the team getting better? Are retrospective actions actually happening? |
| **Relationships with stakeholders** | Does the team feel supported, trusted, and respected by those outside the team? |

Not every dimension needs a dedicated survey question — but every dimension should be in view. If you are only measuring delivery confidence, you will be surprised by a team that suddenly implodes.

## Sprint Health Surveys

A sprint-cadence survey (run at the end of every sprint, before or alongside the retrospective) is the most reliable mechanism for tracking team health over time. Done well, it provides a consistent signal that is harder to fake than retrospective participation and more structured than 1:1 conversations.

**Design principles**:

- **Short**: 5–8 questions maximum. Longer surveys get abandoned or answered carelessly. If the team completes it in under three minutes, that is right.
- **Consistent**: Use the same questions every sprint so you can track trends. Resist the urge to add questions each sprint — it breaks comparability.
- **Anonymous**: Responses must be anonymous or you will get socially acceptable answers, not honest ones. Make anonymity explicit and mean it — never attempt to identify respondents from response patterns.
- **Actionable**: Only include dimensions you are prepared to act on. Asking about something and never doing anything about it is worse than not asking.
- **Closed before the retro**: Circulate the survey on the last day of the sprint, close it before the retrospective starts. Use aggregated results to inform what you bring into the room.

**Question types**:

*Likert scale (1–5 or 1–10)*: Good for tracking trends over time.
- "I feel comfortable raising concerns or disagreements in this team." (1 = strongly disagree, 5 = strongly agree)
- "I feel confident we can meet our commitments at a sustainable pace."
- "I have the clarity I need about our goals and priorities."

*Traffic light / RAG*: Quick and visual. Good for health check formats.
- "How are you feeling about the team's collaboration this sprint?" (Green / Amber / Red)

*Net Promoter style (0–10)*: Useful for overall sentiment.
- "On a scale of 0–10, how much are you enjoying working in this team right now?"

*Open text (use sparingly)*: One optional free-text question per survey.
- "Is there anything on your mind that the survey hasn't captured?"

**Avoiding survey fatigue**: The biggest risk to survey quality is habituation — people stop reading the questions and click through. Mitigate by:
- Keeping it genuinely short
- Showing the team that results are used — share aggregates, refer to trends in retros
- Occasionally rotating one question to reflect a current theme
- Taking a break during quiet periods (e.g., between PI cycles) if the team signals fatigue

## Triangulating Signals

A sprint health survey is one input. The retro is another. 1:1 conversations are a third. The SM's job is to read across all three and build a picture that is more accurate than any single source.

Each source has a different character:

| Source | Strengths | Limitations |
|---|---|---|
| **Sprint survey** | Consistent, anonymous, quantitative, trackable over time | Surface-level; can miss nuance; anonymity means no follow-up |
| **Retrospective** | Rich qualitative data; surfaced in the group; leads to action | Social pressure shapes what gets said; loudest voices dominate; may not surface sensitive issues |
| **1:1 conversations** | Deep, individual, confidential; surfaces what people won't say publicly | Not anonymised (SM carries individual context); time-intensive; dependent on relationship quality |

**When signals align**: If the survey shows low psychological safety, the retro produces only surface-level topics, and 1:1s reveal that people are self-censoring — the picture is clear. The team does not feel safe. Act.

**When signals contradict**: If the survey shows high satisfaction but 1:1s reveal significant individual concerns, or if the retro is lively and productive but the survey trends down — investigate. The contradiction is itself a signal. Possible explanations:
- The survey is measuring the wrong things
- The team presents well collectively but individuals are struggling
- One or two people are driving retro energy while others disengage
- There is a lag between reality and survey scores

**The triangulation habit**: After each sprint, before the retro, spend ten minutes asking yourself:
- What did the survey tell me? What trends am I seeing?
- What themes emerged in 1:1s this sprint?
- What do I expect to surface in the retro — and what do I expect will *not* surface?
- What is the gap between what the team says publicly and what I hear privately?

That gap is where the most important SM work happens.

## Reading the Picture

**Signs of a healthy team**:
- Survey scores are stable or improving; variation is within a normal range
- The retro surfaces real issues, not just process tweaks
- 1:1s are easy — people bring genuine topics without prompting
- The team challenges each other constructively without the SM facilitating it
- Problems are raised early, not escalated at the last minute
- The team talks about improvement; retro actions get done

**Early warning signals** — act before these become crises:

| Signal | What it may indicate |
|---|---|
| Survey scores declining for 2+ sprints | Growing problem; do not wait for a third sprint |
| Retro generating only trivial topics | Low psychological safety or loss of faith in improvement |
| 1:1s becoming status updates with no depth | Disengagement or loss of trust in the relationship |
| One person's absence from survey or retro | Disengagement or something personal worth checking |
| High variance in survey scores (some 5s, some 1s) | Team is not a team — sub-groups or significant individual divergence |
| Survey scores high, 1:1s reveal stress | People are performing wellness; look harder |
| Sudden score drop after a specific event | That event caused damage; name it |

**Normal variation vs. signal**: Not every dip is a crisis. A hard sprint, a production incident, or a difficult stakeholder conversation will show up in the survey. The question is: does the team bounce back? A dip followed by recovery is healthy. A dip that does not recover, or a slow gradual decline, is a signal.

## Acting on Health Data

**Principle**: If you ask, you must act. Not always immediately, not always visibly — but if team members believe their survey responses lead to nothing, they stop being honest.

**Closing the loop**: After every sprint, share aggregated results with the team. Not a full analysis — a brief summary: "Here's what the survey showed this sprint. I want to flag two things..." This signals that you read it and it matters.

**Calibrating your response** to what the data shows:

| Picture | Response |
|---|---|
| Healthy, stable | Maintain; name what's working; protect it |
| One dimension dipping | Bring the theme into the retro (without attribution); monitor closely |
| Multiple dimensions dipping | Prioritise in the retro; have 1:1s with individuals you're most concerned about; consider a dedicated health retrospective |
| Sustained decline across dimensions | Escalate the systemic picture; this is beyond team-level; the SM may need support from an agile coach or the ADM |
| Crisis signals (safety, conflict, someone struggling) | Act immediately; do not wait for the retro cadence |

**The health retrospective**: When health data shows a pattern that normal retros are not addressing, run a dedicated health retrospective — a session where the explicit focus is the team's health rather than the sprint's output. Use a health check format (see below) to structure it. This resets the conversation and creates space for topics that get crowded out in regular retros.

## Tracking Over Time

A single sprint's data is a snapshot. Trends are what matter.

**Visualise**: Maintain a simple chart of survey scores by dimension over time. Share it with the team periodically (quarterly or at PI boundaries). Trends are more honest than any individual data point, and seeing a trend often prompts the team to reflect in ways that a single score does not.

**Baseline**: Establish a baseline in the first 2–3 sprints. This is your reference point. Is the team improving from their baseline? Declining? Flat?

**Seasonal patterns**: Some variation is predictable — scores often dip at the end of a quarter when pressure is high, or after a major release. Knowing your team's pattern helps you distinguish normal variation from genuine deterioration.

**Reviewing trends with the team**: Quarterly, share the trend data with the team. "Here's how we've tracked over the last three months. What do you notice? What should we do about it?" This models transparency, gives the team ownership of their health, and often surfaces insights the SM has not seen.

## Sharing Health Data

**What to share with the team**: Aggregated scores and trends. Not individual responses, not verbatim free-text (unless the team is small enough that it cannot be attributed). The team should see their own data — it belongs to them.

**What to share with leadership or management**: This requires care. Team health data is primarily a tool for the SM and the team. Sharing raw scores with leadership can create pressure that distorts future responses ("we need to score high or management will intervene").

If leadership asks for health data:
- Share trend direction, not raw scores: "The team's confidence in delivery has improved over the last quarter."
- Share themes, not specifics: "Psychological safety has been a focus area; we've been working on it in retrospectives."
- Never share anything that could identify an individual's response.
- Be explicit with the team about what you are and are not sharing upward.

## Observation-Based Health Assessment

Surveys measure what people are willing to report. Observation measures what is actually happening. An SM who only uses surveys will miss health signals that are visible in behaviour but not in self-reported data.

Use ceremony observation as a structured health diagnostic — not as surveillance, but as a professional reading of team dynamics that informs where to coach next.

### What to Observe in Ceremonies

**Professionalism and presence**:
- Do team members arrive on time and stay engaged, or drift in late and check phones?
- Is attention present in ceremonies, or are people half-attending?
- Do team members follow through on commitments made in planning and standups?

**Morale and energy**:
- What is the energy level in the room — engaged, flat, or visibly strained?
- Are there signs of humour, lightness, and enjoyment alongside the work?
- Are people protective of each other, or do small tensions surface in comments and reactions?

**Collaboration signals**:
- Do team members help each other without being asked?
- Is knowledge shared freely, or hoarded by individuals?
- When someone is stuck, does the team respond — or wait for the SM to act?
- Are retro action items genuinely collective, or always assigned to the same one or two people?

**Ownership and initiative**:
- Does the team self-organise in planning — or wait to be told what to pick up?
- Are impediments raised proactively, or only when they've already caused a delay?
- Does the team challenge the backlog — pushing back on unclear items, asking why?
- Do team members follow through without reminders?

**Communication quality**:
- Are standup updates meaningful and aimed at the team, or a rote recitation for the SM?
- Does the team have direct conversations with each other, or route everything through the SM or PO?
- In conflict, do team members engage constructively or go quiet?

### Reading the Observation Picture

Combine your observations with the survey data and 1:1 signals to get a rounded picture:

| What you observe | What it may indicate |
|---|---|
| Late arrivals, phones out, low eye contact | Disengagement or low respect for ceremonies — worth exploring |
| Team members talking over each other | High energy, possibly; or unresolved dominance dynamic |
| Silence in response to "any blockers?" | Low psychological safety or habituation — blockers exist but aren't raised |
| Strong peer-to-peer conversation without SM involvement | Self-organisation is healthy — reduce your facilitation footprint |
| Same person always answering for the team | Others are deferring — healthy deference or suppressed voices? |
| Laughter and banter alongside the work | Trust is present; use it |
| Post-ceremony energy flat, people leaving immediately | Low investment in the ceremony — review purpose and format |
| Team members helping each other unprompted | Collaboration is intrinsic, not SM-driven — a strong health signal |

**Observation vs. interpretation**: Describe what you see before drawing conclusions. "Three team members checked their phones during planning" is an observation. "The team is disengaged" is an interpretation. Both matter — but keep them separate. The interpretation is a hypothesis to test in a 1:1 or by creating a space in a retro, not a fact to act on directly.

---

## Health Check Formats

**Spotify Squad Health Check**: Teams RAG-rate a set of dimensions (Easy to Release, Suitable Process, Tech Quality, Value, Speed, Mission, Fun, Learning, Support). A visual output — green/amber/red across dimensions — makes trends immediately readable. Works well for periodic deep-dives (quarterly) alongside a lighter sprint survey.

**Custom sprint survey**: Bespoke questions tailored to the team's current context and the dimensions most relevant to them. More flexible than a fixed model; requires discipline to keep it short and consistent.

**NPS-style pulse**: A single question — "On a scale of 0–10, how much would you recommend this team as a great place to work right now?" — with one optional open question. Extremely lightweight; very easy to sustain; limited in diagnostic value but excellent as a leading indicator of trend.

**Team health radar**: Score each dimension on a radar chart. Provides a visual representation of relative strengths and weaknesses. Useful for sharing with the team and for retrospective facilitation — the shape of the radar often prompts useful conversation.

**Choosing a format**: The best format is the one the team will sustain. A sophisticated model that the team stops engaging with after three sprints is worse than a simple pulse they complete honestly every sprint. Start simple; add complexity only if the team asks for it.

## Example Sprint Survey

The following is an illustrative 6–8 question sprint health survey. All questions use a 1–5 Likert scale for consistency and trend tracking. Adapt to your team's context.

**Preamble** (shown at the top of the survey):
> This survey focuses on your well-being, collaboration, and agile effectiveness during the latest sprint. Responses are anonymous. Insights will help identify areas for improvement in future sprints.

**Core questions**:

| # | Question | Scale anchors |
|---|---|---|
| 1 | Overall, how happy were you during this sprint? | 1 = Very unhappy → 5 = Extremely happy |
| 2 | Did you feel heard and valued in team discussions? | 1 = No, never → 5 = Yes, always |
| 3 | How stressed did you feel during this sprint? | 1 = No stress → 5 = Extremely stressed |
| 4 | How manageable was your workload this sprint? | 1 = Not enough work → 5 = Overwhelming |
| 5 | How well did the team collaborate this sprint? | 1 = Very poorly → 5 = Extremely well |
| 6 | How effective was the sprint compared to what was planned? | 1 = Very poor → 5 = Extremely effective |

**Recommended additions** to close coverage gaps:

| # | Question | Scale anchors | Dimension covered |
|---|---|---|---|
| 7 | I had clarity on what the team needed to achieve this sprint. | 1 = No clarity → 5 = Completely clear | Clarity |
| 8 | I feel the team is improving how it works. | 1 = Not at all → 5 = Definitely | Learning & improvement |

**Dimensions covered by this survey**:

| Dimension | Covered by |
|---|---|
| Morale & energy | Q1 |
| Psychological safety | Q2 |
| Sustainability | Q3 |
| Workload balance | Q4 |
| Collaboration | Q5 |
| Delivery confidence | Q6 |
| Clarity | Q7 |
| Learning & improvement | Q8 |
| Quality | Not covered — add if technical health is a concern |
| Stakeholder relationships | Not covered — add for teams with high external dependency |

**Note on Q4 (workload)**: This question is bidirectional — both extremes (1 = not enough work, 5 = overwhelming) signal a problem. A score of 3 is the healthy midpoint. When reading results, a team average of 2 and a team average of 4 both warrant attention, unlike all other questions where higher is consistently better. Flag this interpretation when sharing results with the team.

**Keeping it sustainable**: 6 questions is the recommended minimum; 8 covers all core dimensions. Resist adding more — every additional question reduces completion quality. If a topic needs exploring in depth, use the retrospective rather than the survey.
