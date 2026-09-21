# Improvement Tools — quick reference

One page per tool: what it's for, how to run it, and how it fails. For the improvement mindset and how these fit together, see the `continuous-improvement` skill. Value Stream Mapping has its own skill — **`value-stream-mapping`** — which covers current/future state mapping properly; the summary here is for choosing between tools, not for running a mapping workshop.

## Choosing a tool

| You have… | Use |
|---|---|
| A change you want to test safely | PDCA |
| A specific failure and no idea why | Five Whys |
| A problem with many possible causes | Fishbone (Ishikawa) |
| A slow end-to-end process | Value Stream Mapping |
| A system where one stage limits everything | Theory of Constraints |
| Lots of small friction and no single big problem | Kaizen |
| A recurring problem that keeps coming back | Five Whys, then check for a systemic cause |

---

## PDCA (Plan–Do–Check–Act)

**For:** running an improvement as an experiment rather than a decree.

**How to run it:**
1. **Plan** — state the problem, the hypothesis, the change, and what you'll measure. Write the prediction down: "if we limit WIP to 4, cycle time drops below 8 days"
2. **Do** — make the change, small and time-boxed. One change at a time or you won't know what worked
3. **Check** — compare against the prediction, with the measure you chose in advance
4. **Act** — adopt, adapt or abandon. Then start again

**Fails when:** the prediction isn't written down (everyone remembers being right), the change is too big to attribute, or there's no Check — most teams run Plan-Do-Plan-Do.

**Sprint-sized version:** one retro action = one PDCA cycle, checked at the next retro. "What did we agree, what happened, do we keep it?" as the first item on every retro agenda.

---

## Five Whys

**For:** getting past the symptom on a specific, concrete failure.

**How to run it:**
Start with a factual statement of what happened, then ask why, five times, following the causal chain.

> **Problem:** The release was rolled back on Friday night.
> 1. *Why?* A config change broke authentication in production.
> 2. *Why?* The config differs between staging and production.
> 3. *Why?* Production config is maintained by hand.
> 4. *Why?* The automation work was descoped twice to make feature dates.
> 5. *Why?* We have no way of getting infrastructure work prioritised against features.
>
> **Root cause:** prioritisation, not configuration. Fixing the config file fixes Friday; fixing the prioritisation fixes the next six months.

**Rules:**
- Facts, not blame. If an answer names a person, ask why the system allowed it
- Five is a guide — stop when you reach something you can actually change
- Follow one chain; if there are genuinely several, use Fishbone instead
- Validate the chain backwards: "if we fixed that, would this have happened?"

**Fails when:** it's done in a group where someone is defending their decisions, or when it stops at the first technical cause because that's the comfortable one.

---

## Fishbone / Ishikawa diagram

**For:** a problem with multiple contributing causes, where you don't know which matters most.

**How to run it (45 min):**
1. Write the problem at the head of the fish
2. Draw bones for categories. For delivery work: **People, Process, Tools, Environment, Information, Dependencies**
3. Silent writing — everyone adds causes to each bone
4. Group and discuss; ask "why" on the biggest ones
5. **Dot vote** on which cause, if removed, would most reduce the problem
6. Take the top two into PDCA cycles

**Fails when:** it becomes a complete inventory of everything wrong, with no prioritisation and no action. The vote is not optional.

---

## Value Stream Mapping (summary)

**For:** seeing where time actually goes across an end-to-end flow — usually to discover that most of it is waiting.

**The core idea:** map each step with its *process time* (work actually happening) and *lead time* (elapsed including waiting). Flow efficiency = process time ÷ lead time. Most delivery systems run at 15–30%; the improvement is nearly always in the queues between steps, not in the steps themselves.

**Run it properly using the `value-stream-mapping` skill** — current state, future state, improvement backlog. Don't attempt it from this summary.

**Fails when:** teams map the process they wish they had, or map only their own steps and miss the four-day wait at the approval gate.

---

## Theory of Constraints

**For:** systems where one stage limits the throughput of everything else.

**The five focusing steps:**
1. **Identify** the constraint — where work queues up. The CFD shows it; so does asking "what are we always waiting for?"
2. **Exploit** it — make sure the constraint is never idle or doing work it shouldn't. Free it from anything someone else could do
3. **Subordinate** everything else to it — stop other stages producing faster than the constraint can absorb. This is the counter-intuitive step and the one teams resist
4. **Elevate** it — add capacity, automate, train, hire
5. **Repeat** — when the constraint moves, start again. It always moves

**Common constraints in delivery:** a single person who reviews everything; a shared test environment; an external approval; one specialist skill.

**Fails when:** teams optimise a non-constraint and wonder why nothing changed. Local improvements away from the constraint produce more WIP, not more delivery.

---

## Kaizen

**For:** steady accumulation of small improvements, where no single big problem exists.

**How to run it:**
- Every retrospective produces one small change that can be completed before the next one
- Make improvement work visible on the board alongside delivery work
- Explicit capacity: roughly 10% of a Sprint. Unprotected improvement time is the first thing cut
- Celebrate the small ones publicly — it's how the habit forms

**Fails when:** improvement items live on a separate list nobody looks at, or when a "big bang" improvement initiative replaces the small steady ones.

---

## A3 problem solving

**For:** a substantial problem that needs to be thought through and communicated on one page.

One side of A3, seven boxes: **Background · Current state · Goal · Root cause analysis · Countermeasures · Plan · Follow-up.**

The constraint is the point — if it doesn't fit on one page, the thinking isn't finished. Useful for taking a systemic impediment to leadership, because it forces evidence before proposal.

---

## Choosing well: the practitioner's shortcut

Most teams reach for Five Whys because it's familiar, and use it on problems that aren't specific enough for it. The honest sequence:

1. Is there **one specific failure**? → Five Whys
2. Is it **slow rather than broken**? → VSM or Theory of Constraints
3. Are there **many contributing causes**? → Fishbone
4. Do you have a **candidate fix**? → PDCA it rather than mandating it
5. Is it **lots of small friction**? → Kaizen, and stop looking for a root cause that isn't there
