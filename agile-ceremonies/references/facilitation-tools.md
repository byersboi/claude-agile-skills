# Digital Tools for Remote Ceremony Facilitation

Tool selection for running Scrum events remotely and hybrid. For workshop-level tool choice and virtual facilitation technique see `facilitation/references/remote-facilitation-tools.md`; this file is ceremony-specific.

## Choosing: three rules

1. **Fewest tools that do the job.** Every extra tool is a login, a licence and a five-minute delay at the start of a session
2. **Whatever the team already has.** A well-used shared document beats an unadopted specialist tool
3. **Check access before the session, not during it.** Contractors, suppliers and people in other departments are the ones who won't get in

---

## Tool categories

| Category | What it's for | Common options |
|---|---|---|
| Collaborative whiteboard | Retros, planning, mapping, workshops | Miro, Mural, FigJam, Excalidraw |
| Work management | Backlog, board, metrics | Jira, Azure DevOps, Trello, Linear, GitHub Projects |
| Video conferencing | Everything | Teams, Zoom, Meet |
| Async input | Pre-reads, written proposals, health checks | Shared docs, forms, wikis |
| Retro-specific | Retros with built-in voting, anonymity, action tracking | Retrium, EasyRetro, Parabol, TeamRetro |
| Estimation | Planning Poker | Built-in tools, or dice/cards on camera |
| Polling | Temperature checks, confidence votes, dot voting | Built into video tools, Slido, Mentimeter |

**On retro-specific tools:** worth it for teams with low psychological safety (genuine anonymity is hard to fake on a whiteboard) and for tracking whether actions actually get done. Otherwise a whiteboard is enough and more flexible.

---

## Per-ceremony setup

### Sprint Planning
- **Board plus whiteboard, side by side.** The backlog tool holds the items; the whiteboard holds the Sprint Goal, capacity, risks and the plan
- Sprint Goal pinned top-centre of the whiteboard, visible all session
- Capacity grid as a simple table — names down, working days, known absences, support rota
- Confidence vote at the end via poll or emoji reactions

### Daily Scrum
- The board is the only artefact needed. Share it, walk it right to left
- Persistent chat channel for the follow-up conversations the event spawns
- For distributed time zones: a written daily in a channel plus one synchronous session a week beats a 7am call nobody is awake for

### Backlog Refinement
- Items sent as a pre-read link 24 hours ahead
- Comment directly on items so questions are captured where the item lives, not in chat history that vanishes
- Whiteboard for the one item that needs drawing — usually there is one

### Sprint Review
- Screen share from the person who built it, not the SM
- **Structured feedback capture:** a whiteboard column per question, everyone writes for three minutes before anyone speaks
- Record it for stakeholders who couldn't attend — but never let recording become a substitute for attending
- Adapt the backlog live, on screen, so people see their input land

### Retrospective
- Whiteboard or retro tool with **private writing before reveal** — the single most important feature. Without it, the first person to write anchors everyone else
- Dot voting to converge
- Actions created in the work management tool during the session, with an owner, or they will not happen
- Timer visible to everyone

### Inception / bigger workshops
- Whiteboard with a pre-built template and clearly labelled areas
- Breakout rooms configured before the session starts
- A co-facilitator whose only job is chat, hands and timekeeping

---

## Making remote ceremonies work

**Structural participation.** Remote silence is not consent; it's disengagement, confusion or a muted microphone. Build in written input, polls and explicit turn-taking rather than asking "any thoughts?"

**Write before you speak.** Silent writing is more valuable remotely than in person — it removes the turn-taking problem entirely.

**Shorter, with breaks.** Attention drops hard after 45 minutes on video. A four-hour planning session is two two-hour sessions with a proper gap.

**Cameras:** encourage, don't mandate. Bandwidth, environment and neurodivergence are all legitimate reasons. Judge participation by contribution, not video.

**Async where the event allows.** Refinement questions, health checks, pre-reads and status all work better written and ahead of time. Reserve synchronous time for the conversations that genuinely need everyone.

---

## Hybrid — the hardest case

A hybrid ceremony defaults to two meetings: the room, and the people watching the room.

**What works:**
- **Everyone on their own device**, even those in the room. One shared laptop at the end of a table excludes remote attendees completely
- **Digital-first artefacts.** If the board is on a physical wall, remote people cannot use it. Move it
- **A remote advocate** — someone in the room whose job is to notice raised hands and unspoken remote attendees
- **Remote speaks first** on every round. In-room voices will otherwise fill every gap

**What doesn't:** a room camera and good intentions.

---

## Tooling anti-patterns

| Anti-pattern | Why it hurts | Fix |
|---|---|---|
| Tool sprawl | Five tools, five logins, ten minutes lost per session | Consolidate; make the board the single source of truth |
| Whiteboard graveyards | Dozens of abandoned boards, nobody can find last month's retro | One board per team per quarter, or a naming convention and an index |
| Actions in the whiteboard only | Never seen again after the session closes | Actions go into the work tool with an owner, during the session |
| Tool as the improvement | New retro tool instead of addressing why retros are flat | Fix the conversation first; the tool is never the blocker |
| Recording as attendance | Stakeholders stop turning up to the review | Keep recordings for genuine absence; get feedback live |
| Licences for some | Contractors and suppliers locked out of the board | Check access as part of preparing the session |
