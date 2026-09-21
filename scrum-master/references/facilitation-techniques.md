# Facilitation Techniques for Each Scrum Event

Event-by-event facilitation craft for Scrum Masters. For general session design (PODA, Liberating Structures, workshop planning) see the `facilitation` skill; for the events themselves see `agile-ceremonies`. This file is about what you actually do in the room.

## The default posture

Facilitate the *process*, stay out of the *content*. The moment you start answering technical questions or arbitrating priority, you have stopped facilitating and the team has lost its neutral party.

Four moves you'll use constantly:

| Move | When | What it sounds like |
|---|---|---|
| **Redirect** | A question is aimed at you that belongs to the team | "Good question — who in the team knows?" |
| **Make visible** | The same point has been made three times | "Let me write that up so we don't lose it." |
| **Name the pattern** | The dynamic is the problem, not the topic | "I notice we've come back to this three times. What's going on?" |
| **Timebox out loud** | Discussion is expanding without converging | "Five minutes on this, then we decide or park it." |

---

## Sprint Planning

**Before:** confirm the PO has ordered items and that top items were refined. If they weren't, say so before the session starts, not during it — planning that turns into refinement is a predictable failure you can head off.

**Part 1 — the Sprint Goal.** The most common failure is the goal being announced rather than agreed.

- Have the PO frame the *outcome* they want, not the items they want done
- Ask the team: "If we achieved that but only delivered half these items, would it be a good Sprint?" A yes means the goal is real
- Draft the goal on the board and leave it visible for the rest of the session
- Test it: is it valuable on its own, testable, and achievable in one Sprint?

**Part 2 — the plan.** Hand the pen over. The team decomposes, sizes and self-selects.

- If one person is doing all the decomposing, split into pairs for ten minutes and have them report back
- Watch capacity honestly: holidays, on-call, support rota, the person who is half on another team
- Silent-write the risks before discussing them — verbal rounds surface only the comfortable ones

**Closing move:** fist-to-five on "is this a plan we believe in?" Below three, do not proceed on hope — find out what the objection is.

**Anti-patterns to intervene on:** the PO answering sizing questions; the loudest engineer setting every estimate; over-commitment driven by a stakeholder in the room.

---

## Daily Scrum

Your goal is to become unnecessary here within a few Sprints.

**If you facilitate at all,** facilitate the format, not the content:
- Walk the board right to left — finishing beats starting
- Ask about the *work*, not the people: "what's this item waiting on?" rather than "what did you do yesterday?"
- Close with "does anything about that change our plan for the Sprint Goal?"

**Fading out, deliberately:**
1. Sprints 1–2: you run it, explaining why the structure exists
2. Sprints 3–4: the team rotates facilitation; you attend and stay silent
3. Sprint 5 onward: you attend occasionally; the team notices your absence only in that nothing changes

**Common failures and the intervention:**

| Failure | Intervention |
|---|---|
| Status report to the SM | Stand outside the circle; stop making eye contact with the speaker |
| Problem-solving swallows the timebox | "Who needs to be in that conversation? Straight after, fifteen minutes." |
| Silent members | Ask about an item on the board, not about the person |
| Always overruns | Timer visible; end at fifteen minutes even mid-sentence, once. It only takes once |

---

## Backlog Refinement

Not an event in the Guide — which means you have licence to design it. Keep it under 10% of capacity.

- **Pre-read.** Send the items 24 hours ahead. Refinement is where preparation shows
- **Three questions per item:** what problem, for whom, how would we know it worked
- **Size last.** Sizing before understanding produces numbers, not shared understanding
- **Split aggressively** — see `agile-estimation/references/story-splitting-guide.md`. If an item is too big to discuss in ten minutes, it is too big to plan
- **Park the rabbit holes.** Technical design debates belong in a separate session with the three people who care

**Facilitation tell:** if the same two people talk for the whole session, the format is wrong. Try silent reading followed by written questions.

---

## Sprint Review

The hardest event to facilitate because the audience is not yours to control.

**Set it up so feedback is possible:**
- Give stakeholders the context in the first five minutes — where we are against the Product Goal
- Have the *team* walk through the Increment, not you and not a slide deck
- Include what was not done and why. Leaving it out is what teaches stakeholders that reviews are theatre

**Get real feedback instead of "looks great":**
- Ask specific, structured questions rather than "any questions?": "What would stop you using this tomorrow?" / "What's missing for your team?" / "What would you have prioritised instead?"
- Silent-write first for larger groups — three minutes, then collect
- Have people use it live where you can. Watching someone struggle beats any opinion

**Close by adapting the backlog in the room** so stakeholders see their input land. That is what brings them back.

---

## Sprint Retrospective

Format choices are in `scrum/references/retrospective-formats.md`. What matters more than format:

**Vary it.** The same format five Sprints running produces the same conversation five times.

**Structure every retro in five phases** (Derby and Larsen): set the stage → gather data → generate insight → decide what to do → close. Teams that skip "set the stage" get shallow data; teams that skip "generate insight" jump from symptom to action.

**Depth techniques when it stays superficial:**
- Silent writing first, always
- Anonymous input for teams with low safety — digital board, no names
- Five Whys on one item rather than surface treatment of eight
- A timeline of the Sprint on the wall — events jog memory that categories don't
- Ask directly: "what's the thing we're not talking about?" then wait

**Leave with one action, owned, sized to finish before the next retro.** A retro that produces "discuss further" has failed. If the same theme recurs three Sprints running, it is probably systemic — stop asking the team to fix it and take it outside the team yourself.

**When you are part of the problem:** have someone else facilitate. An SM facilitating a retro about their own behaviour gets a polite retro.

---

## Cross-cutting techniques

**Working agreements.** Agree them once, revisit them when broken. Reference them neutrally in the moment: "we agreed one conversation at a time."

**Conflict in the room.** Don't smooth it. Name it and slow it down: "You two see this differently — say more about what's behind that." See `conflict-management`.

**The dominant voice.** Structural fixes work better than confrontation: round-robin, silent writing, 1-2-4-All, or simply "let's hear from someone who hasn't spoken."

**Remote specifics.** Cameras on where possible but never mandated; a co-facilitator watching chat; break every 45 minutes; a shared board everyone edits rather than one screen everyone watches. See `facilitation` for tooling.

**Your own review.** After every event you facilitate, ask yourself one question: what did I do that the team could have done? That answer is your fade-out plan.
