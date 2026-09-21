# Product Discovery Methods

Continuous discovery practices — how to find out what's worth building before building it. For PO accountabilities and backlog work see the `product-owner` skill; for prioritisation once you have candidates, see `references/backlog-management-techniques.md`.

## The premise

Most features don't work. Industry studies of tested product ideas consistently find that only a minority produce the intended effect, and a meaningful proportion make things worse. Discovery isn't a phase before delivery — it's the habit of finding out which minority you're in before you spend a quarter on it.

**Continuous discovery, in one sentence:** the team talks to users every week, and decisions trace back to something a real person said or did.

---

## The Opportunity Solution Tree

Teresa Torres's structure, and the single most useful discovery artefact.

```
                    OUTCOME
         "Reduce order-status support calls by 40%"
                       │
        ┌──────────────┼──────────────┐
   OPPORTUNITY    OPPORTUNITY    OPPORTUNITY
   "I don't know  "I don't trust "I want to change
   where my       the estimated  the delivery slot"
   order is"      date"
        │
   ┌────┴────┬──────────┐
 SOLUTION  SOLUTION   SOLUTION
 Tracking  Proactive  Status in
 page      SMS        confirmation email
        │
   EXPERIMENT: fake-door test on the tracking link
```

**How to use it:**
1. **One outcome at the top.** A behaviour change or business result, not a feature
2. **Opportunities are needs, pains and desires** expressed in the user's words, gathered from interviews. Not solutions with a question mark
3. **Compare solutions within an opportunity**, never across the whole tree. Three ways to solve one problem is a real choice; three unrelated features is a wish list
4. **Experiments test the riskiest assumption** behind a solution, not the solution itself

**Why it beats a backlog for discovery:** it makes visible which opportunity a feature is meant to address, so you can kill a feature without losing the problem.

---

## Continuous interviewing

**The practice:** one user conversation a week, minimum, with the team present — not a quarterly research project delivered as a report.

**Interview for stories, not opinions.** Opinions about hypothetical features are worthless; specific past behaviour is data.

| Ask this | Not this |
|---|---|
| "Tell me about the last time you needed to check an order." | "Would you use an order tracking page?" |
| "Walk me through what you did." | "How often do you check orders?" |
| "What happened next?" | "Would that be useful?" |
| "What did you do when that didn't work?" | "What features would you like?" |

**Mining for opportunities:** as they tell the story, note every point of friction, workaround or emotion. Those are opportunities. A user describing a spreadsheet they maintain to work around your product has just handed you a roadmap.

**Keep it cheap:** 20–30 minutes, two people from the team, recruited from existing users. The barrier is always process, never willingness — people will talk to you.

---

## Assumption mapping

Before building anything, list what must be true for it to work, then sort by *how certain are we* against *how damaging if wrong*.

```
  high risk │  TEST THESE         TEST THESE
   if wrong │  FIRST              (research)
            │  (experiment)
            ├─────────────────────────────────
   low risk │  Just build it      Note it, move on
            │
            └─────────────────────────────────
              low certainty       high certainty
```

**Four assumption types to check for each idea:**
- **Desirability** — do people want it?
- **Viability** — does it work for the business?
- **Feasibility** — can we build it?
- **Usability** — can people work out how to use it?

Teams over-test feasibility (comfortable, technical) and under-test desirability (uncomfortable, requires talking to people). The unknown that sinks products is almost always desirability.

---

## Experiment types, cheapest first

| Method | Tests | Cost | Good for |
|---|---|---|---|
| **Customer interview** | Desirability, problem existence | Hours | Everything; start here |
| **Fake door / smoke test** | Demand | Days | "Would anyone click this?" |
| **Concierge** | Desirability, value | Days | Deliver the outcome manually for five users |
| **Wizard of Oz** | Desirability, usability | Days | Front end real, back end human |
| **Prototype test** | Usability, comprehension | Days | Before any code |
| **A/B test** | Effect size | Weeks | Comparing real alternatives at scale |
| **Beta / limited release** | All four | Weeks | Final validation before full rollout |

**The concierge test is underrated.** Doing the thing manually for a handful of users teaches you more about whether it's valuable — and what the edge cases are — than any amount of prototype testing.

**Rule:** the cost of the experiment should be proportionate to the cost of being wrong. A two-week build needs a conversation; a two-quarter build needs an experiment with a number attached.

---

## Defining the outcome

Discovery without a clear outcome becomes interesting research nobody acts on.

> **Weak:** "Improve the ordering experience"
> **Better:** "Reduce order-status support calls by 40% within two quarters"
> **Better still:** "…by 40%, without reducing customer satisfaction below its current level"

The guardrail in the third version is what stops the team achieving the metric by removing the phone number.

See `okr-management` for outcome framing at team and organisation level.

---

## Making discovery continuous

**What it looks like when it's working:**
- A weekly interview slot in the diary that doesn't get cancelled
- The whole team joins some interviews — not just the PO. A developer who has watched a user struggle builds differently
- Opportunities visible alongside the delivery board
- A standing agenda item: "what did we learn about users this Sprint?"
- Some features get killed before they're built, and this is treated as a success

**What blocks it, and the usual answer:**

| Blocker | Response |
|---|---|
| "We don't have access to users" | Start with internal proxies — support, sales, account teams — while you fix access. Then fix access; it's a real impediment to escalate |
| "No time for discovery" | Discovery time is cheaper than the wrong feature. Start with one 30-minute conversation a week |
| "We already know what to build" | Then the interview will confirm it cheaply. If it doesn't, you just saved a quarter |
| "Research is someone else's job" | A report delivered to a team is not discovery; it's a document |
| "Stakeholders decide what we build" | Bring them one interview recording. It changes the conversation more than any argument |

---

## Discovery anti-patterns

| Anti-pattern | Consequence |
|---|---|
| Discovery as a phase | Learning stops once build starts, which is when the real questions arrive |
| Solution validation only | Asking "do you like this?" about something already decided; confirms what you hoped |
| Leading questions | Users are polite and will agree with you |
| Research handed over as a report | Nobody reads it; nothing changes |
| One big study, annually | Out of date within a quarter |
| Discovery without an outcome | Interesting insight, no decisions |
| Never killing anything | If discovery has never stopped a feature, it isn't functioning |
