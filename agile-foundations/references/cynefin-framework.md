# Cynefin — choosing an approach that fits the problem

Cynefin (Dave Snowden) is a sense-making framework, not a categorisation model. Its value to an agile practitioner is simple: it explains *why* agile works for some problems and is wasteful for others, and it gives you language for the conversation with a sponsor who wants a plan for something nobody understands yet.

## The five domains

| Domain | Relationship between cause and effect | Approach | Practice |
|---|---|---|---|
| **Clear** (simple/obvious) | Obvious to everyone | Sense → Categorise → Respond | Best practice |
| **Complicated** | Knowable with analysis or expertise | Sense → Analyse → Respond | Good practice |
| **Complex** | Only visible in hindsight | Probe → Sense → Respond | Emergent practice |
| **Chaotic** | No discernible relationship | Act → Sense → Respond | Novel practice |
| **Confused** (aporetic) | You don't know which domain you're in | Break the problem down until you do | — |

### Clear
Known solutions, repeatable. Payroll processing, password resets, a standard onboarding. **Do:** standardise, automate, write the runbook. **Don't:** hold a workshop about it.

**The trap:** complacency. Clear problems drift into chaotic when conditions change and nobody notices the procedure has stopped fitting. The boundary between clear and chaotic is the only cliff edge in the model.

### Complicated
Hard but knowable — bring in expertise. Performance tuning, a database migration, a tax calculation engine. **Do:** analyse, design, get an expert view, then execute. Up-front design earns its keep here.

**The trap:** expert entrainment — the specialist sees the problem they know how to solve. Get more than one expert opinion on anything expensive.

### Complex
Most product development. You cannot know the answer in advance; you find it by running safe-to-fail experiments and amplifying what works. **Do:** small bets, fast feedback, short cycles, tolerate failure. This is the domain agile is designed for.

**The trap:** demanding certainty. Asking for a detailed twelve-month plan for a complex problem doesn't reduce the uncertainty — it just moves the discovery of it to the end.

### Chaotic
Crisis. A live outage, a security breach, a service failing in public. **Do:** act to stabilise, then sense what you've got, then respond. Command and control is correct here and only here.

**The trap:** staying too long. Crisis mode is addictive for some organisations and some leaders. Move back to complex as soon as the bleeding stops.

### Confused
The most common starting position and the least acknowledged. The honest move is to say "we don't know what kind of problem this is yet" and break it into parts you can place.

---

## Using it in practice

**With a sponsor asking for a fixed plan:**
> "Some of this is complicated — the integration work, where we have the expertise to design it up front. Some of it is complex — we genuinely don't know yet how people will use this. I can give you a plan for the first and a set of experiments with decision points for the second. What I can't give you is a confident plan for the complex part, and neither can anyone else."

**Sorting a programme's work.** Run it as a workshop: every significant workstream gets placed in a domain, with the group arguing the placement. The argument is the value. Outputs:
- Clear work → standardise and automate it; stop spending planning time on it
- Complicated work → get the right expertise involved early; design up front
- Complex work → fund experiments, not deliverables; set decision points, not deadlines
- Chaotic work → stop planning and stabilise

**Choosing a delivery approach:**

| Domain | Fits |
|---|---|
| Clear | Standard operating procedure, automation, Kanban with tight SLEs |
| Complicated | Staged delivery with expert design, or Scrum with strong technical spikes |
| Complex | Scrum, Kanban with frequent feedback, continuous discovery, set-based design |
| Chaotic | Incident command; no framework |

**Estimation follows the domain.** Complicated work can be estimated by people who have done it before. Complex work cannot be estimated with confidence at all — use probabilistic forecasting from throughput instead, and say so honestly. See `monte-carlo-forecasting`.

---

## Safe-to-fail experiments (the complex-domain tool)

For complex problems, design experiments rather than solutions. Each one needs:

- **A hypothesis** — what we believe, stated so it could be wrong
- **What we'll observe** — the signal that tells us either way
- **Amplify condition** — what we do more of if it works
- **Dampen condition** — what we stop if it doesn't
- **A safe-to-fail boundary** — time, spend or blast radius, agreed up front

Run several small experiments in parallel rather than one big pilot. Parallel experiments in a complex domain beat sequential ones, because you're not just testing a solution — you're learning the shape of the problem.

---

## Misuses to avoid

- **Treating it as a 2x2 maturity model.** Domains are not levels. Complex is not "better" than clear
- **Placing people or teams in domains.** It describes problems, not competence
- **Using it to avoid planning.** "It's complex" is not an excuse for not knowing what you'll do next week; it's a reason to plan in shorter loops
- **Forcing everything into complex** because that's where agile lives. Plenty of delivery work is genuinely complicated, and up-front design is the right answer for it
