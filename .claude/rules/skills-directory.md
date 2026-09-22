# Skills Directory

Each skill lives at `<skill-name>/SKILL.md`. Skills auto-trigger on matching queries in Claude Code.

## Skills map

| Skill | Trigger scenarios |
|-------|------------------|
| `agile-foundations` | Agile Manifesto, 12 principles, empiricism, agile vs waterfall, framework selection, agile culture/mindset |
| `scrum` | Sprint events, artifacts, DoD, DoR, velocity, sprint goal, sprint cancellation |
| `scrum-master` | SM role, stances, servant leadership, impediment management, joining a new team, SM backlog, anti-patterns, self-assessment |
| `product-owner` | PO accountabilities, backlog management, prioritisation (MoSCoW, WSJF, Kano), product discovery, PO anti-patterns |
| `kanban` | Kanban boards, WIP limits, flow metrics, CFD, cycle time, lead time, classes of service, Kanban cadences |
| `agile-coach` | Coaching stances, GROW model, Tuckman's model, psychological safety, organisational coaching, coaching vs mentoring |
| `agile-delivery-manager` | Governance, stakeholder management, programme planning, RAID, delivery reporting, dependency management |
| `head-of-delivery` | Head of delivery management, delivery capability, DDaT capability framework, delivery manager job family and progression, hiring/assessing delivery managers, delivery community of practice |
| `agile-scaling` | SAFe, LeSS, Nexus, Spotify model, Scrum of Scrums — when and how to scale |
| `agile-metrics` | Velocity, throughput, cycle time, lead time, OKRs, NPS, Monte Carlo forecasting |
| `agile-ceremonies` | Sprint Planning, Daily Scrum, Backlog Refinement, Retrospective, Story Mapping |
| `agile-estimation` | Planning Poker, T-shirt sizing, affinity estimation, INVEST, story splitting |
| `facilitation` | Session design, PODA framework, diverge-converge, Liberating Structures, remote facilitation |
| `conflict-management` | Thomas-Kilmann modes, escalation ladder, SBI feedback, agile conflict scenarios |
| `continuous-improvement` | PDCA, Kaizen, Five Whys, Value Stream Mapping, Theory of Constraints |
| `release-management` | Release cadence, go/no-go, feature flags, deployment coordination, rollback, DORA metrics |
| `lean-portfolio-management` | Portfolio Kanban, lean budgeting, WSJF, value streams, portfolio governance |
| `okr-management` | Writing OKRs, cadence, scoring, OKR hierarchy, connecting to delivery |
| `change-management` | ADKAR, Kotter, change curve, resistance, agile transformation, sustaining change |
| `value-stream-mapping` | Current/future state mapping, lean waste, flow efficiency, improvement backlog |
| `supplier-management` | Agile contracting, SLAs, integrating suppliers, offshore teams, vendor relationships |
| `sm-mentoring` | SM maturity model, mentoring conversations, observing & feedback, SM career paths |
| `sm-one-to-ones` | 1:1 purpose and structure, coaching vs pastoral care, confidentiality, agenda ownership |
| `team-health` | Health check formats, reading trends, acting on data, triangulating signals |
| `monte-carlo-forecasting` | Probabilistic forecasting, simulation mechanics, confidence thresholds, throughput-based forecasting |
| `engineering-standards` | Dependency governance, branch strategy, code review, security scanning, code quality |
| `bdd-user-stories` | BDD, Gherkin, scenario writing, user stories, acceptance criteria |
| `ai-in-agile` | Using AI in agile delivery, AI in ceremonies, AI-assisted estimation and retrospectives |

## Skill file structure

Each `SKILL.md` uses this frontmatter:

```yaml
---
name: <Human-readable name>
description: <Comma-separated trigger phrases for Claude Code auto-invocation>
version: 1.0.0
---
```

Followed by the skill content as markdown. Skills should be:
- Deep enough to be genuinely useful (not just definitions)
- Practical — include real-world examples, anti-patterns, and decision frameworks
- Structured with headers so Claude can navigate them efficiently
- Self-contained — don't assume the user has read other skills

## Reference files

Some skills have a `references/` subdirectory for supporting material (e.g., checklists, templates, format libraries) that would bloat the main SKILL.md. Example: `scrum/references/retrospective-formats.md`.
