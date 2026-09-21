# Backlog Management Techniques

Prioritisation and ordering techniques with worked examples. For the PO accountabilities and backlog principles, see the `product-owner` skill.

## Ordering is not prioritisation

Prioritisation ranks by value. **Ordering** decides what to do next, and has to account for dependencies, risk, learning value and capacity. A backlog can be perfectly prioritised and badly ordered.

Order by: *what unblocks the most* → *what reduces the most risk* → *what delivers the most value soonest* → everything else.

---

## MoSCoW

**Must / Should / Could / Won't (this time)** — best for scoping a fixed-date release.

**How to run it:** agree the deadline and the definition of Must first — "without this, the release cannot happen at all, and we would rather slip than ship without it". Then classify.

**The rule that makes it work:** Musts must be less than 60% of capacity. If everything is a Must, nobody has prioritised anything — they've just recorded their preferences.

> **Worked example — regulatory release, 8 weeks, capacity ~40 items:**
> - **Must (22 items, 55%)**: the statutory reporting fields, the audit log, the data retention change
> - **Should (10)**: bulk export, the improved error messages
> - **Could (8)**: dashboard tidy-up, saved filters
> - **Won't this time (14)**: the API v2 work — explicitly named, so it stops being raised weekly
>
> When the inevitable slippage arrives, the Coulds go first, then the Shoulds, and the conversation is already had.

**Naming the Won'ts is the most valuable part** and the part most often skipped.

---

## WSJF (Weighted Shortest Job First)

> **WSJF = Cost of Delay ÷ Job Size**, where Cost of Delay = User/Business Value + Time Criticality + Risk Reduction/Opportunity Enablement

Best for portfolio or feature-level prioritisation where items compete for the same capacity.

**How to run it:** score each component 1–20 using a modified Fibonacci scale (1, 2, 3, 5, 8, 13, 20), relatively. Always anchor by giving the smallest item in each column a 1.

> | Feature | Value | Time crit. | Risk/Opp | CoD | Size | **WSJF** |
> |---|---|---|---|---|---|---|
> | Fraud detection rules | 13 | 20 | 8 | 41 | 5 | **8.2** |
> | Self-service password reset | 8 | 3 | 3 | 14 | 2 | **7.0** |
> | Reporting dashboard | 13 | 3 | 1 | 17 | 13 | **1.3** |
> | Platform upgrade | 3 | 8 | 20 | 31 | 13 | **2.4** |
>
> The dashboard is the second most valuable item and the second-lowest priority — because it's large and nothing gets worse by waiting. This is the conversation WSJF exists to produce.

**Watch for:** scoring inflation once people learn how the maths works, and job size estimates produced by the people who want the work done. Score value and size in separate sessions with different people if you can.

---

## Kano model

Classifies features by how satisfaction responds to them:

- **Basic (must-be)** — absence causes dissatisfaction; presence earns nothing. Security, uptime, accessibility
- **Performance** — more is linearly better. Speed, coverage, accuracy
- **Delighter** — unexpected; drives loyalty. Decays into Performance and then Basic over time

**How to use it:** cover every Basic before adding any Performance features. Delighters are worth roughly one per release — they're what people talk about, but they don't compensate for missing basics.

> A service with a delightful onboarding flow and a 6-second search will lose to one with plain onboarding and instant search. Search speed is a Basic in that category now; it wasn't five years ago.

**Practical test:** ask users two questions per feature — "how would you feel if it worked this way?" and "how would you feel if it didn't?" The pattern of answers classifies it.

---

## Cost of Delay and CD3

For a value conversation without a full WSJF exercise, ask one question: **"what does it cost us per week that this isn't live?"**

Four patterns worth recognising:

| Urgency profile | Shape | Implication |
|---|---|---|
| Fixed date | Value drops off a cliff after a date | Schedule backwards from the date |
| Expedite | Cost accruing now and rising | Do it now; everything else waits |
| Standard | Value lost steadily from now | Order by CD3 (cost of delay ÷ duration) |
| Intangible | No cost now; large later | The category where technical debt lives, and why it never gets done |

Naming the intangible ones explicitly is the only reliable way to get debt and enabler work prioritised.

---

## Impact Mapping

Connects features to outcomes, and cuts scope by making the assumption visible.

> **Why** (goal) → **Who** (actors) → **How** (impacts — behaviour changes) → **What** (deliverables)
>
> **Why:** reduce support calls about order status by 40%
> **Who:** customers · support agents · warehouse staff
> **How (customers):** check status themselves instead of calling · get notified before they wonder
> **What:** order tracking page · proactive SMS on dispatch · status in the confirmation email

**The value is in the pruning.** Each "What" is a bet on a "How". If nobody believes customers will use a tracking page, that branch dies before it's built.

---

## Story mapping

Two dimensions: the user's journey left to right, alternatives and detail top to bottom. Slice horizontally to define releases.

**Use it for:** finding a thin end-to-end slice, spotting gaps in a journey, and showing stakeholders what a smaller release actually looks like rather than arguing about it in the abstract.

**The move that wins arguments:** draw the line for release one across the map. Everyone can see what's in and what's out, and the conversation becomes concrete in about ninety seconds.

---

## Backlog hygiene

**Size:** roughly two to three Sprints of refined items at the top. Below that you can't plan; above it you're refining things that will change before you build them.

**The rest is a list of ideas, not a backlog.** Treat it as such — it doesn't need estimating, ordering or grooming.

**Quarterly cull.** Anything untouched for six months: delete it. It is not lost — if it mattered, it will come back, and it usually comes back better. A 900-item backlog is not an asset; it is a place where good ideas go to be un-findable.

**Refinement discipline:**
- Top 10 items: refined, sized, acceptance criteria agreed
- Next 10–20: understood, roughly sized, not detailed
- Everything else: a title and a sentence

---

## Handling the "everything is priority one" stakeholder

**The forced-rank move:** "I can do these in some order. Which of these three is first?" Nobody can defend three number ones when the question is which one waits.

**The trade move:** "Yes — what comes out to make room?" Prioritisation is only real when it costs something.

**The evidence move:** "What happens if this ships in March rather than January?" If the answer is nothing, it isn't urgent. If the answer is specific and expensive, you've just found your cost of delay.

**The transparency move:** publish the ordered backlog and the reasoning. Most escalations are about not being heard rather than about the decision.

---

## Anti-patterns

| Anti-pattern | Consequence | Fix |
|---|---|---|
| Backlog as a suggestion box | Thousands of items; nothing findable | Cull quarterly; ideas list separate from backlog |
| Prioritising by stakeholder seniority | Loudest voice wins; value ignored | Use a visible technique and publish the reasoning |
| Everything Must | MoSCoW becomes a list | Cap Musts at 60% of capacity |
| Refining fifty items deep | Waste — most will change | Two to three Sprints of depth, no more |
| Estimates used as value | Small things done because they're small | Value and size are separate axes; WSJF uses both |
| Technical work never prioritised | Debt compounds until delivery stops | Make it a class of service with allocated capacity |
| No "won't do" | The same items resurface every month | Name them explicitly and say why |
