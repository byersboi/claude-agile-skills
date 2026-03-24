---
name: Release Management
description: This skill should be used when the user asks about "release management", "release planning", "go/no-go decision", "release readiness", "hotfix process", "feature flags", "dark launch", "deployment coordination", "release notes", "DORA metrics", "deployment frequency", "change failure rate", "release checklist", "release communication", "rollback planning", "release train", "continuous delivery", "release cadence", "release governance", "release retrospective", "release owner", "release sign-off", "progressive delivery", "canary release", "release pipeline", "production incident", "incident classification", "incident priority", "P0", "P1", "P2", "incident triage", "incident severity", "post-incident review", or is managing or coordinating software releases in an agile context.
version: 1.0.0
---

# Release Management

Release management in agile contexts is the discipline of coordinating, governing, and communicating the movement of working software from development to production. It is not a gate at the end of a project — it is a recurring, repeatable capability that improves with each iteration.

The goal is not to control releases — it is to make releasing safe, predictable, and frequent enough that it becomes unremarkable.

## Release Cadence & Planning

**Establishing a release cadence**: Choose a cadence based on organisational risk tolerance, technical capability, and customer need. Common patterns:

| Cadence | Typical context |
|---|---|
| Continuous / on-demand | High-maturity CI/CD, small changes, feature flags in use |
| Weekly | Teams with stable pipelines but manual approvals |
| Fortnightly / sprint-aligned | Releases tied to sprint boundaries |
| Monthly / quarterly | Regulated industries, large-scale coordinated releases |

**Release scope definition**: Before each release, confirm:
- What features/stories are included (release scope)
- What is explicitly excluded and why
- What dependencies must be resolved before release
- Who has sign-off authority

**Release planning session** (for coordinated multi-team releases):
1. Identify all work targeting this release across teams
2. Surface cross-team dependencies and confirm readiness
3. Agree on a release window and freeze date
4. Assign a release owner — one person accountable for the release succeeding
5. Confirm rollback plan exists before proceeding

## Release Readiness

A release is ready when it meets the agreed Definition of Done at release level — not just at story or sprint level.

**Release Definition of Done** (adapt to context):
- All acceptance criteria met and signed off by Product Owner
- Automated test suite passes (unit, integration, regression, performance)
- Security scan completed; critical findings resolved
- Release notes drafted and reviewed
- Runbook written and tested in staging
- Monitoring and alerting configured for new functionality
- Data migration scripts tested against production-like data
- Compliance and legal sign-offs obtained (where required)
- Rollback procedure documented and rehearsed

**Go/No-Go Decision**: Hold a brief go/no-go meeting prior to release. Attendees: release owner, product owner, lead engineer, operations representative, and any required approvers.

| Check | Owner | Status |
|---|---|---|
| Tests passing | Engineering | Go / No-Go |
| Security sign-off | Security | Go / No-Go |
| PO acceptance | Product Owner | Go / No-Go |
| Ops readiness | Operations | Go / No-Go |
| Rollback plan confirmed | Release Owner | Go / No-Go |

A single No-Go blocks the release. The release owner facilitates the decision but does not override it.

## Deployment Coordination

For releases involving multiple teams or systems:

**Sequencing**: Map the deployment order. Identify what must go first (shared services, APIs, databases) before dependent components are deployed. Visualise as a dependency chain, not a Gantt chart.

**Coordination mechanisms**:
- Shared release Slack channel / war room (virtual or physical)
- Step-by-step runbook with owner for each step
- Agreed checkpoints between steps (confirm each stage before proceeding)
- Single release commander during the deployment window

**Communication during deployment**: Notify internal stakeholders at start, at key milestones, and on completion. For customer-facing releases, co-ordinate with support teams and prepare response to queries.

## Feature Flags & Progressive Delivery

Feature flags decouple deployment from release — code ships to production but is not yet visible to users. This is the single most effective technique for reducing release risk.

**Types of feature flags**:

| Type | Purpose | Lifespan |
|---|---|---|
| Release flag | Hide incomplete feature | Short — remove after full rollout |
| Experiment flag | A/B test or multivariate test | Short to medium |
| Ops flag | Kill switch for problematic feature | Medium — keep until confident |
| Permission flag | Feature for specific user segments | Long-lived |

**Progressive delivery techniques**:
- **Canary release**: Release to a small % of users; monitor; expand if healthy
- **Dark launch**: Deploy and exercise code in production without exposing to users
- **Blue/Green deployment**: Run two identical environments; switch traffic atomically
- **Ring-based rollout**: Internal users → early adopters → general availability

**Feature flag hygiene**: Flags accumulate technical debt. Track all active flags. Set expiry dates. Remove flags once rollout is complete — stale flags are a source of bugs and confusion.

## Release Communication

**Internal communication plan**:
- Who needs to know about the release, and when
- What level of detail each audience needs (executives want outcomes; support needs functionality changes; operations needs infrastructure impact)
- Who is the point of contact for questions

**Release notes**: Write for the reader, not the developer. Include:
- What changed and why it matters to the user
- Known limitations or issues
- What to do if something goes wrong
- Link to full technical changelog for those who need it

**External / customer communication**: Co-ordinate with product marketing for significant releases. Avoid technical jargon. Focus on benefit delivered, not feature shipped.

## Production Incident Classification

Before a hotfix can be scoped and deployed, the incident must be classified. Severity determines response urgency, who is involved, and what the deployment path looks like. Without a shared classification framework, every incident feels like a P0 and teams burn out.

**Priority levels**:

| Priority | Name | Definition |
|---|---|---|
| **P0** | Critical Outage | Full system or core functionality down; no workaround; all users affected |
| **P1** | Major Degradation | Core functionality severely impaired for a significant portion of users; limited workaround |
| **P2** | Minor Degradation | Core functionality impaired for a small number of users, OR non-core functionality down for many users |
| **P3** | Normal Bug | Minor defect or cosmetic issue; no immediate business risk; workaround available |
| **P4** | Inquiry / No Issue | False alarm, known issue already tracked, documentation question |

**Triage questions** — answer these to assign the correct priority:

| Question | P0 | P1 | P2 | P3/P4 |
|---|---|---|---|---|
| Scope of user impact | All users | Significant % | Small % or non-core | Individual / negligible |
| Workaround available? | No | Limited | Yes | Yes |
| System integrity at risk? | Yes | Possibly | No | No |
| Revenue/SLA exposure? | Immediate and severe | Significant | Moderate | Low or none |

**Response windows by priority**:

| Priority | Response target | Deployment path |
|---|---|---|
| P0 | Immediate — all hands | Emergency hotfix; bypass normal cadence |
| P1 | Within 1–2 hours | Hotfix; expedited review and approval |
| P2 | Same business day | Expedited or next scheduled release |
| P3 | Next sprint | Normal sprint cycle |
| P4 | Backlog / no action | Add to backlog or close as no-issue |

**Escalation**: P0 and P1 incidents require immediate notification to the release owner, engineering lead, and relevant stakeholders. Do not wait for the next standup.

**Post-incident**: Every P0 and P1 requires a written post-incident review within 24–48 hours. Cover: what happened, timeline, root cause, immediate fix, and longer-term remediation to prevent recurrence. Blameless — focus on the system, not individuals.

## Hotfix & Emergency Release Process

Hotfixes are expedited releases addressing critical production issues (security vulnerabilities, data loss, severe outages). They bypass normal release cadence but must not bypass safety.

**Hotfix criteria** — use the expedited path when:
- Production is down or severely degraded
- Data integrity is at risk
- Security vulnerability is actively being exploited or is critically exposed
- Contractual SLA breach is imminent

**Expedited process**:
1. Confirm the issue and its severity (avoid false alarms)
2. Assign a single engineer to the fix — no parallel competing fixes
3. Minimum viable testing: automated tests must pass; targeted manual test of the affected area
4. Two-person review (no solo hotfixes)
5. Expedited go/no-go: release owner + one approver
6. Deploy with enhanced monitoring
7. Write up a post-release review within 24 hours

**What not to skip**: Even under pressure, do not skip code review, automated tests, or the rollback plan. These take minutes and prevent catastrophic follow-on incidents.

## Rollback Planning

Every release must have a rollback plan agreed before deployment begins.

**Rollback criteria** — define in advance:
- Error rate above X% for Y minutes
- Latency exceeding Z ms at the Pth percentile
- Critical business function returning errors
- Specific monitoring alert firing

**Decision authority**: Who can call a rollback? Establish in advance. Do not require a committee decision mid-incident.

**Rollback mechanisms**:
- Feature flag off (fastest; zero downtime)
- Revert deployment to previous version (minutes)
- Database rollback (complex; plan carefully — forward-only migrations preferred)
- DNS or load balancer switch (blue/green)

**Document and test** the rollback procedure in staging before every production release. An untested rollback plan is not a rollback plan.

## DORA Metrics

The DevOps Research and Assessment (DORA) metrics are the industry standard for measuring release and delivery health:

| Metric | What it measures | Elite benchmark |
|---|---|---|
| **Deployment Frequency** | How often you release to production | On-demand (multiple per day) |
| **Lead Time for Changes** | Commit to production time | Less than one hour |
| **Change Failure Rate** | % of releases causing incidents | 0–15% |
| **Time to Restore Service** | Mean time to recover from incident | Less than one hour |

Use DORA metrics to have honest conversations about release capability — not to blame teams, but to identify systemic improvements. A high change failure rate is a process problem, not a people problem.

## Release Retrospective

After every significant release (or at regular cadence for frequent releases):

- What went smoothly? What should we repeat?
- What caused friction or delay? What should we improve?
- Were any surprises? How do we prevent them?
- Did the rollback plan hold up under scrutiny?
- What would make the next release safer or faster?

Capture improvements as backlog items. Assign owners. Review progress at the next release retro.

## Release Anti-patterns

| Anti-pattern | Problem | Better approach |
|---|---|---|
| Big-bang releases | Concentrated risk; hard to diagnose failures | Smaller, more frequent releases |
| Release as a gate | Delays value; treats release as exception not norm | Continuous delivery mindset |
| No release owner | Accountability diffused; decisions slow | Named release owner per release |
| Untested rollback | Rollback fails under pressure | Test rollback in staging every time |
| Feature freeze too late | Insufficient testing time; rushed decisions | Define freeze date at release planning |
| Skipping release retro | Same problems recur | Retro is mandatory, not optional |
| Manual release steps without runbook | Steps missed; errors introduced | Everything in a runbook; automate where possible |
