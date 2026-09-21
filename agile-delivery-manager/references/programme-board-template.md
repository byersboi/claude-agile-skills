# Programme Board Template

A programme board makes cross-team work, dependencies and risk visible in one place. It is not a scaled-up team board — teams keep their own. This board carries only what spans teams.

## Setting it up

**Physical or digital?** Digital (Miro, Jira Plans, Azure DevOps) if any team is remote — which is nearly always. Physical boards work when everyone is co-located and only then; a board half the programme can't see is worse than no board.

**One board, one programme.** If you need two boards, you probably have two programmes. Say so.

**Who owns it:** the ADM owns the board's health. Teams own their own rows. If the ADM is the only person who ever moves a card, the board has become a reporting artefact and has stopped being a planning tool.

## Board structure

### Swimlanes — one per team, plus two

```
┌──────────────┬───────────┬──────────────┬─────────┬──────────┬──────────┐
│              │ Committed │ In progress  │ Blocked │ In test  │ Done     │
├──────────────┼───────────┼──────────────┼─────────┼──────────┼──────────┤
│ Team A       │           │              │         │          │          │
├──────────────┼───────────┼──────────────┼─────────┼──────────┼──────────┤
│ Team B       │           │              │         │          │          │
├──────────────┼───────────┼──────────────┼─────────┼──────────┼──────────┤
│ Team C       │           │              │         │          │          │
├──────────────┼───────────┼──────────────┼─────────┼──────────┼──────────┤
│ Cross-team   │  work no single team owns — integration, migration, cut-over│
├──────────────┼───────────┼──────────────┼─────────┼──────────┼──────────┤
│ External     │  work owned outside the programme that we depend on        │
└──────────────┴───────────┴──────────────┴─────────┴──────────┴──────────┘
```

The **Cross-team** lane is the one most programmes omit, and it is where delivery usually fails. Integration, data migration, cut-over and environment work belong to nobody by default. Give them a lane and an owner.

The **External** lane holds work you cannot move but must track — supplier deliverables, another department's API, a regulatory approval. A card with no owner inside the programme still needs a date and a named contact outside it.

**Card granularity:** features or epics, not stories. If a card moves more than once a fortnight, it is too small for this board. Aim for 5–15 cards per team per quarter.

### Card format

```
┌────────────────────────────────────┐
│ [FEATURE] Payments reconciliation  │
│ Team: B          Owner: <name>     │
│ Target: Sprint 14 (w/c 12 Jan)     │
│ Outcome: finance can close month-  │
│   end without manual matching      │
│ Depends on: #47 (Team A), Supplier │
│   X API v2                         │
│ Confidence: ●●○ (medium)           │
└────────────────────────────────────┘
```

**Confidence, not percentage complete.** High / medium / low, set by the team, reviewed weekly. "60% done" tells a stakeholder nothing useful; "low confidence, because the supplier hasn't confirmed the API date" tells them everything.

## Dependency visualisation

Three notations, in order of preference:

**1. Linked cards (digital boards).** A line between the producing card and the consuming card. Best option — it survives cards moving.

**2. Dependency register alongside the board.** Where linking isn't available:

| ID | Producer | Consumer | What's needed | Needed by | Confirmed? | Risk if late | Owner |
|---|---|---|---|---|---|---|---|
| D-012 | Team A | Team B | Auth token service in test env | Sprint 12 | Yes | Team B idle ~1 sprint | <name> |
| D-013 | Supplier X | Team C | API v2 sandbox | Sprint 13 | No | Blocks cut-over | <name> |

**"Confirmed?" is the only column that matters.** An unconfirmed dependency is a wish. Chase confirmation from the *producing* side in writing before treating a date as real.

**3. Dependency matrix** for programmes with 5+ teams — teams on both axes, count of open dependencies in each cell. Reveals the team everyone is waiting on, which is usually a structural problem rather than a delivery one.

## Quarterly / PI planning use

**Before the session:**
- Board reflects reality, not aspiration — close finished work, be honest about carry-over
- Each team has draft candidate features from the PO
- Known external dates are on the board (regulatory deadlines, supplier releases, freeze periods)

**During:**
1. Teams draft their lane for the quarter
2. **Dependency walk** — each team reads out what it needs from others and what others need from it. Every dependency gets a card or a register row, with both names on it
3. Sequence: move cards until dependency arrows point forwards in time, not backwards
4. Capacity check: holidays, on-call, planned attrition, support load
5. **Risk round** — what would have to be true for this plan to hold? Capture as ROAM (Resolved / Owned / Accepted / Mitigated)
6. Confidence vote on the plan as a whole (fist-to-five). Below 3 average, replan — don't proceed and hope

**After:** photograph or export the board. When the plan changes in week six — it will — you want the original to compare against, not to enforce.

## Running cadence

| Rhythm | Session | What happens at the board |
|---|---|---|
| Weekly | Programme sync (30 min) | Walk the board right to left; blocked cards only; confirm dependency dates |
| Fortnightly | Dependency review | Register reviewed line by line; unconfirmed dates chased |
| Monthly | Risk and milestone review | ROAM status; milestone confidence re-set |
| Quarterly | Replanning | Rebuild the board for the next quarter |

**Walk the board right to left.** Starting at "Committed" makes the meeting about what's starting; starting at "Done" and moving backwards makes it about what's finishing. Finishing is the thing you want.

## Anti-patterns

| Anti-pattern | What it looks like | Fix |
|---|---|---|
| **Board as status report** | Only the ADM updates it; teams learn about it from the weekly pack | Teams move their own cards, live, in the sync |
| **Story-level cards** | Hundreds of cards; nobody can see the shape of the quarter | Roll up to feature level; teams keep story detail on their own boards |
| **Dependencies as arrows only** | Pretty lines, no owner, no date | Every dependency has two names and a date needed |
| **Blocked column as parking** | Cards sit blocked for weeks | Age blocked cards; anything over a sprint escalates automatically |
| **No cross-team lane** | Integration and cut-over appear in week 11 | Create the lane at planning; give it a named owner |
| **Plan enforcement** | The quarterly board is treated as a commitment register | Board shows intent; replan openly when evidence changes |
| **Confidence never changes** | Everything is green until it is red | Ask the team, not the lead; make low confidence safe to declare |
