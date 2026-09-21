# Team Health Check Templates

Ready-to-run formats. For the reasoning — how to read trends, triangulate signals, and act on what health checks tell you — see the **`team-health`** skill. This file gives you the dimensions, statements and facilitation steps to run one on Thursday.

## Choosing a format

| Format | Best for | Time | Cadence |
|---|---|---|---|
| Squad Health Check (traffic light) | Established teams, trend tracking | 45–60 min | Quarterly |
| Team Barometer | Quick pulse between full checks | 20 min | Monthly |
| Safety check (1–5) | Before a difficult retro; new teams | 5 min | As needed |
| Team Canvas | New or re-formed teams | 90–120 min | On formation |
| Agile maturity self-assessment | Teams wanting a practice-level view | 60 min | Twice yearly |

**Rules that apply to all of them:**
- The team owns the data. If a manager sees individual responses, you get the answers people think are safe
- Never compare teams. The moment scores are compared, they become performance data and stop being honest
- Trend beats absolute value. A team at amber and improving is healthier than a team at green and sliding
- No action, no more health checks. Two rounds with nothing changing and participation collapses

---

## 1. Squad Health Check (traffic light)

Each dimension is voted green / amber / red, plus an arrow for direction of travel (improving / stable / worsening). The arrow is the more valuable data.

**Dimensions and the statement people vote on:**

| Dimension | Green looks like |
|---|---|
| **Delivering value** | "We deliver something useful to our users regularly." |
| **Easy to release** | "Releasing is simple, safe and boring." |
| **Fun** | "I enjoy working in this team." |
| **Health of codebase** | "We're proud of the code; changing it is straightforward." |
| **Learning** | "We're learning something useful all the time." |
| **Mission** | "We know why we're here and we're excited about it." |
| **Pawns or players** | "We control our own destiny and decide what to build and how." |
| **Speed** | "We get things done quickly, without waiting or delays." |
| **Suitable process** | "Our way of working fits us; we improve it when it doesn't." |
| **Support** | "We get help and support when we ask for it." |
| **Teamwork** | "We're one team, pulling in the same direction." |
| **Psychological safety** | "I can raise problems and admit mistakes without fear." |

**How to run it (55 minutes):**
1. **Set up (5 min)** — restate that this is the team's data, and what will and won't be shared
2. **Individual voting (10 min)** — everyone votes on all dimensions privately, before discussion
3. **Reveal (5 min)** — show the spread, dimension by dimension. Don't average it away; the spread is the interesting part
4. **Discuss the divergent ones (20 min)** — where the team disagrees most, not where it scores lowest. Disagreement means people are experiencing different realities
5. **Pick two (10 min)** — the two dimensions worth working on, and one concrete action each
6. **Close (5 min)** — record the scores for next time; agree who does what

**Facilitation note:** if everything is green, ask "which of these would our users/stakeholders score differently?"

---

## 2. Team Barometer (quick pulse)

Eight statements, scored 1–5, run monthly in ten minutes. Use between full checks to spot movement early.

1. We have a clear, shared purpose
2. I know what's expected of me
3. We trust each other
4. We can disagree openly and resolve it
5. Our workload is sustainable
6. We learn from our mistakes
7. We get the support we need from outside the team
8. I'd recommend this team to someone I like

Run as a poll; look only at movement since last month. Anything that drops by a point gets five minutes of discussion at the next retro.

---

## 3. Safety check

Five seconds each, anonymous, before a retro you expect to be difficult.

> On a scale of 1–5, how safe do you feel to say what you really think in this session?
> 5 = I'll say anything · 1 = I'll smile and say nothing

**Reading it:** average of 4+, proceed normally. 3s and below present, switch to written and anonymous formats, and consider whether the right people are in the room. If anyone scores 1, the retro's topic is the safety, not the Sprint. Never ask who gave which score.

---

## 4. Team Canvas (new or re-formed teams)

Ninety minutes, one large shared canvas, nine areas. Work through them in this order:

1. **People and roles** — who we are, what each of us brings
2. **Purpose** — why this team exists
3. **Goals** — what we intend to achieve, by when
4. **Values** — what matters to us as a team
5. **Strengths and assets** — what we're good at, what we have
6. **Weaknesses and risks** — what we lack, what could go wrong
7. **Needs and expectations** — what each person needs from the others
8. **Rules and activities** — how we'll work together, decide, and handle conflict
9. **Working agreement** — the short list we'll actually hold each other to

**Facilitation:** silent writing first in every section. Give the "needs and expectations" section twice the time you think it deserves — it's where the real contracting happens, and it prevents half the conflict you'd otherwise mediate in month three.

Revisit on any significant change of membership, leadership or goal. See Tuckman in the `agile-coach` skill: those changes reset the team to forming whether anyone acknowledges it or not.

---

## 5. Agile maturity self-assessment

For teams who want a practice-level view rather than a feelings-level one. Score each 1–4: 1 not doing it, 2 doing it inconsistently, 3 doing it well, 4 doing it well and improving it.

**Delivery**
- We deliver a usable increment every Sprint
- Our Definition of Done is meaningful and we hold to it
- We release without drama

**Product**
- Every item traces to a user need or a business outcome
- We know whether what we shipped worked
- The backlog is ordered and refined enough to plan from

**Technical**
- Automated tests give us confidence to change things
- We integrate continuously
- Technical debt is visible and actively managed

**Team**
- We plan our own work and manage our own dependencies
- We surface problems early
- We improve something real every Sprint

**Use the spread, not the total.** A team at 3 across delivery and 1 across technical has a specific, actionable problem; a "total maturity score" has none.

---

## Anti-patterns

| Anti-pattern | Consequence | Fix |
|---|---|---|
| Scores reported upward | Teams score for the audience | Team keeps the data; share themes only, with consent |
| Comparing teams | Gaming; loss of honesty | Never produce a league table |
| Checking without acting | Participation collapses by round three | One visible action per check, completed |
| Manager facilitating | Answers shift towards the expected | Neutral facilitator; ideally from outside the team |
| Health check instead of retro | Measurement replaces improvement | The check informs the retro; it doesn't replace it |
| Too frequent | Survey fatigue; noise instead of trend | Quarterly full check; monthly pulse at most |
