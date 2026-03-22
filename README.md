# Claude Agile Skills

A collection of [Claude Code](https://claude.ai/code) skills for agile practitioners — Scrum Masters, Agile Coaches, Product Owners, Delivery Managers, and teams.

Created by [Michael Byers](https://www.linkedin.com/in/michaelbyers/) — [github.com/byersboi](https://github.com/byersboi), experienced Scrum Master.

## What are Claude Skills?

Skills extend Claude Code with specialised knowledge. When you ask Claude a question that matches a skill's trigger phrases, it automatically loads the relevant expertise into context — giving you answers grounded in deep, structured domain knowledge rather than generic responses.

## Skills Included

| Skill | What It Covers |
|---|---|
| `agile-foundations` | Agile Manifesto, 12 principles, empiricism, agile vs waterfall, framework selection |
| `scrum` | Sprint events, artifacts, DoD, DoR, velocity, impediments |
| `scrum-master` | SM stances, servant leadership, impediment management, facilitation, anti-patterns |
| `product-owner` | PO accountabilities, backlog management, prioritisation (MoSCoW, WSJF, Kano), product discovery |
| `kanban` | Boards, WIP limits, flow metrics, CFD, classes of service, Kanban cadences |
| `agile-coach` | Coaching stances, GROW model, Tuckman's model, psychological safety, organisational coaching |
| `agile-delivery-manager` | Governance, stakeholder management, programme planning, RAID, reporting |
| `agile-scaling` | SAFe, LeSS, Nexus, Spotify model, Scrum of Scrums — when and how to scale |
| `agile-metrics` | Velocity, throughput, cycle time, lead time, OKRs, NPS, Monte Carlo forecasting |
| `agile-ceremonies` | Sprint Planning, Daily Scrum, Backlog Refinement, Retrospective, Story Mapping |
| `agile-estimation` | Planning Poker, T-shirt sizing, affinity estimation, INVEST, story splitting |
| `facilitation` | Session design, PODA framework, diverge-converge, Liberating Structures, remote facilitation |
| `conflict-management` | Thomas-Kilmann modes, escalation ladder, SBI feedback, common agile conflict scenarios |
| `continuous-improvement` | PDCA, Kaizen, Five Whys, Value Stream Mapping, Theory of Constraints, making improvements stick |

## Installation

### Option 1 — Copy skills into your global Claude skills directory

```bash
# Clone this repository
git clone https://github.com/YOUR_USERNAME/claude-agile-skills.git

# Copy all skills to your Claude skills directory
cp -r claude-agile-skills/* ~/.claude/skills/
```

### Option 2 — Use as a plugin directory

Point Claude Code at this directory as a plugin:

```bash
cc --plugin-dir /path/to/claude-agile-skills
```

## Usage

Once installed, simply ask Claude naturally. Skills auto-trigger on matching queries:

- *"How should I facilitate a retrospective with a team that's lost trust?"* → `facilitation` + `conflict-management`
- *"What's the difference between cycle time and lead time?"* → `kanban` + `agile-metrics`
- *"How do I coach a Product Owner who keeps saying yes to everything?"* → `product-owner` + `agile-coach`
- *"We're scaling to 5 teams — should we use SAFe or LeSS?"* → `agile-scaling`
- *"How do I run a Sprint Retrospective for a remote team?"* → `scrum` + `facilitation`

## Contributing

Suggestions, corrections, and additions welcome. Open an issue or submit a pull request.

## Licence

MIT — free to use, adapt, and share.
