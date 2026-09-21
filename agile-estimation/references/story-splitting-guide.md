# Story Splitting Guide

Patterns for breaking large backlog items into small, independently valuable slices, with worked examples. For estimation technique and INVEST see the `agile-estimation` skill.

## Why split

A story that takes most of a Sprint hides risk until it's too late to act. Small stories give faster feedback, smoother flow, more accurate forecasting, and the option to stop early when you've learned enough.

**Rule of thumb:** nothing larger than half a Sprint's capacity for one pair. If a team of five can't get six to ten items done in a Sprint, the items are too big.

**The test that matters:** each slice, on its own, is worth something to someone. If a slice only has value once its siblings land, you have made tasks, not stories.

---

## The nine patterns

Try them roughly in this order — the first few produce the best slices most often.

### 1. Workflow steps
Split by the steps a user moves through. Deliver the skeleton end to end first, then enrich.

> **Before:** "As a claimant I can submit a claim."
> **After:** Submit claim with core details · Attach supporting evidence · Save and return to a draft · Receive confirmation notification · Track claim status

### 2. Business rule variations
Each rule or eligibility case is a slice. Ship the common case first.

> **Before:** "Calculate entitlement."
> **After:** Standard rate for a single applicant · Joint applicants · Reduced rate for part-year residency · Backdating rules

### 3. Happy path / unhappy paths
Build the success case. Handle each failure case as its own slice.

> **Before:** "Process a payment."
> **After:** Payment succeeds · Card declined · Timeout and retry · Partial refund

Use with care: some unhappy paths are not optional for a live release. Split them out to sequence the work, not to skip it.

### 4. Data variations
One data type, format or source at a time.

> **Before:** "Import supplier data."
> **After:** Import from CSV · Import from the supplier API · Handle legacy fixed-width files · Handle multi-currency values

### 5. Interface variations
Simplest interface first; richer versions later.

> **Before:** "Users can filter the report."
> **After:** Filter by date range (basic form) · Add saved filter presets · Add typeahead search · Mobile-optimised filter panel

### 6. Operations (CRUD)
Create, read, update, delete are four stories, and usually not equal in value.

> **Before:** "Manage team members."
> **After:** View team members · Add a member · Edit a member · Deactivate a member

### 7. Defer performance
Make it work, then make it fast — when a slow version is genuinely usable.

> **Before:** "Search returns results in under a second."
> **After:** Search returns correct results · Search returns results in under a second for 10k records

### 8. Break out the spike
When the team genuinely cannot size the work, timebox the learning separately and size the rest afterwards.

> **Before:** "Integrate with the legacy billing system."
> **After:** Spike: establish how the billing API handles partial records (2 days) · then the real stories

Spikes are a last resort, not a warm-up. Two in a row on the same topic is a signal to talk to someone who knows the system.

### 9. Major effort first
When the first instance carries all the cost and subsequent ones are cheap.

> **Before:** "Accept Visa, Mastercard and Amex."
> **After:** Accept one card type (builds the payment infrastructure) · Add Mastercard · Add Amex

---

## The splitting conversation

1. **What's the user outcome?** If nobody can say it, the story isn't ready to split — it's ready to be refined
2. **Where's the uncertainty?** Split so the risky part is its own slice, delivered early
3. **What's the smallest thing that would teach us something?** Often a better first slice than the most valuable one
4. **Which pattern fits?** Walk the list above; workflow steps and business rules cover most cases
5. **Check each slice against INVEST** — independent, negotiable, valuable, estimable, small, testable
6. **Re-order.** Splitting is wasted if you then do all the slices in the same Sprint anyway

---

## Splitting smells

| Smell | What it means | What to do |
|---|---|---|
| Slices named "backend" / "frontend" / "testing" | Split by component, not by value | Re-split by user outcome; the layers come along inside each slice |
| "Part 1 of 3" | Tasks in story clothing | Ask what each part is worth on its own; if nothing, merge and split differently |
| Every slice needs all the others to ship | Not independent | Look for a thinner end-to-end path through all of them |
| The slice can't be demoed | Not testable or not valuable | Ask what a user could do after it that they couldn't before |
| Splitting produced 14 slices | Over-split; coordination cost now exceeds the benefit | Recombine to 4–6 |
| Team can't agree on a split | Usually a shared-understanding gap, not a splitting problem | Go back to the problem and the user |

---

## Worked example

**Original:** "As a service manager I can report on team performance so that I can identify where support is needed." — sized XL, nobody confident.

**The conversation:**
- *Outcome?* Managers spot struggling teams before it becomes a crisis
- *Uncertainty?* Whether the data in the source system is complete enough to be trustworthy
- *Smallest learning?* Put last quarter's data in front of three managers and see if they'd act on it

**Split (ordered):**
1. Spike: assess completeness of throughput data in the source system (2 days)
2. Single-team throughput report, last 30 days, on screen — *the risky, valuable core*
3. Multi-team view with a team selector
4. Cycle time added alongside throughput
5. CSV export
6. Scheduled email digest
7. Configurable thresholds and alerting

Slices 1–2 answer whether the whole thing is worth building. Items 5–7 may never be needed — which is the real benefit of splitting, and the reason to resist doing them "while we're in there".
