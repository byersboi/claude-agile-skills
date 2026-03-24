---
name: Engineering Standards & Governance
description: This skill should be used when the user asks about "engineering standards", "software development standards", "code quality", "good standing", "dependency management", "third-party libraries", "branch strategy", "branching strategy", "code review standards", "PR review", "pull request standards", "security scanning", "vulnerability scanning", "code coverage", "SonarCloud", "Dependabot", "technical governance", "engineering governance", "version pinning", "repository management", "pipeline security", "code maintainability", "engineering best practices", "software quality standards", "technical standards", or is establishing or reviewing engineering quality standards for an agile team.
version: 1.0.0
---

# Engineering Standards & Governance

Engineering standards define the baseline quality bar for software produced by an agile team. They are not bureaucracy — they are the agreed-upon conditions under which the team can move fast safely.

Without explicit standards, quality degrades gradually and invisibly. Each individual decision seems reasonable; the cumulative effect is a codebase that becomes expensive to maintain, risky to change, and slow to deliver. Standards make the implicit explicit, and create shared accountability for technical health.

The Scrum Master and Delivery Manager do not own engineering standards — engineers do. But SMs and ADMs must understand them well enough to protect the space for technical quality work, include standards-compliance in the Definition of Done, and escalate when pressure to deliver is causing standards to erode.

## Third-Party Dependencies

Third-party libraries and frameworks extend team capability but introduce risk — security vulnerabilities, breaking changes, abandoned projects, and licensing issues. Managing dependencies is ongoing, not a one-time decision.

**Criteria for adopting a third-party dependency**:
- Active maintenance: last commit within the last 6 months
- Community health: multiple active contributors (5 or more is a reasonable baseline)
- PR review culture: evidence of code review on contributions, not single-committer acceptance
- Security posture: no known unresolved critical vulnerabilities
- Licence compatibility: licence is compatible with your product's distribution model

**Version management**:
- Pin to exact versions in production dependencies (e.g. `"library": "2.4.1"` not `"^2.4.1"`)
- Exact pinning prevents silent upgrades introducing breaking changes or vulnerabilities
- Review and update dependencies on a regular cadence — do not let them drift years behind current
- Use a dependency management bot (e.g. Dependabot, Renovate) to surface available updates and security patches automatically

**Repository ownership**: Download and host third-party dependencies through your organisation's own package registry or repository where possible. Relying directly on public registries introduces supply chain risk — packages can be removed, modified, or hijacked.

**Security scanning**: Before integrating any new third-party library, run it through a security scanner. Integrate automated vulnerability scanning into the CI/CD pipeline so newly disclosed vulnerabilities are caught as part of the normal build process, not discovered in production.

## Branch Strategy

A clear, team-agreed branch strategy reduces merge conflicts, integration failures, and deployment confusion. The specific strategy matters less than its consistent application.

**Minimum viable branch structure**:

| Branch | Purpose |
|---|---|
| `main` | Production-ready code at all times; only merged into via PR |
| `develop` | Integration branch; all feature branches merge here first |
| Feature branches | Short-lived; cut from `develop`; merged back via PR |

**Rules**:
- All branches are cut from `develop` (never from `main` except hotfixes)
- No direct commits to `main` — ever
- Hotfix branches are the only exception: cut from `main`, merged to both `main` and `develop`
- Delete feature branches after merge — stale branches are noise and confusion

**Branch naming conventions** (agree as a team, then apply consistently):
- `feature/description-of-work`
- `bugfix/ticket-id-description`
- `hotfix/ticket-id-description`
- `spike/description`

**Trunk-based development** (alternative for high-maturity teams): Very short-lived branches (hours, not days) merged directly to `main` multiple times per day, protected by feature flags. Requires high test automation coverage and disciplined use of feature flags. Not suitable for teams with low CI/CD maturity.

## Code Review Standards

Code review is not a quality gate managed by a senior engineer — it is a shared team practice that improves code quality, spreads knowledge, and builds collective ownership.

**Minimum standards**:
- Every pull request requires at least one reviewer before merging
- No self-merging — the author cannot approve their own PR
- Reviewers check for: correctness, readability, test coverage, security implications, and alignment with architectural decisions
- PR size: keep PRs small enough to review meaningfully (a 2,000-line PR is not reviewable — it will be rubber-stamped)

**What good code review looks like**:
- Comments are specific, actionable, and kind — not vague ("this is wrong") or personal
- Distinguish between blocking feedback (must fix before merge) and suggestions (nice to have)
- Reviewers ask questions rather than assuming bad intent: "I'm not sure I follow the intent here — can you help me understand why this approach was chosen?"
- Authors respond to every comment — either with a change or a clear explanation
- Average review turnaround: same business day wherever possible; long wait times on reviews create flow problems

**Automated checks before human review**: Linting, formatting, and unit tests should pass automatically before a human reviews. Humans should review logic, not style.

## Code Quality & Coverage

**Code quality tooling**: Integrate static analysis into the pipeline. Tools like SonarCloud, SonarQube, or CodeClimate flag:
- Code smells (overly complex methods, duplicated logic, long parameter lists)
- Security hotspots (potential vulnerabilities requiring human review)
- Technical debt accumulation over time
- Test coverage trends

**Test coverage**: Coverage percentage is a lagging indicator, not a target. A codebase with 90% coverage but no assertions testing meaningful behaviour is not well-tested. Use coverage to find gaps, not to hit a number.

Practical guidance:
- Track coverage trends over time — declining coverage is a warning sign
- Prioritise coverage for business-critical paths and complex logic
- Don't write tests purely to hit a coverage target — they provide false confidence

**Code maintainability**:
- Methods and functions should do one thing
- Complex logic should be commented to explain *why*, not just *what*
- No magic numbers — use named constants
- Consistent naming conventions agreed and applied across the codebase
- Public APIs and shared modules documented

## Security Standards

Security is not a final gate before release — it is a continuous practice embedded in how the team builds.

**Shift left**: Introduce security checks early in the development process, not after code is complete. This means:
- Security requirements in the Definition of Ready (e.g. data classification, compliance impact)
- Threat modelling for features that handle sensitive data
- Security-aware code review (input validation, output encoding, authentication/authorisation checks)
- Automated vulnerability scanning in the CI/CD pipeline

**Pipeline security requirements**:
- Automated dependency vulnerability scanning on every build (e.g. OWASP Dependency-Check, Snyk, Dependabot alerts)
- Static Application Security Testing (SAST) integrated into the pipeline
- Secrets scanning — ensure credentials, API keys, and tokens are never committed to source control
- Container image scanning if deploying containerised applications

**Incident response readiness**: Security vulnerabilities in production are a subset of production incidents. Apply the P0–P1 incident framework — a critical security vulnerability being actively exploited is a P0; a high-severity vulnerability with no known exploitation is typically P1. Response should be immediate and follow the hotfix process.

## Repository Management

**Version control hygiene**:
- All production code lives in version control — no exceptions
- Repository access is controlled and reviewed periodically
- Sensitive configuration (credentials, secrets, API keys) is never stored in the repository — use environment variables or a secrets manager
- `.gitignore` files prevent accidental commits of build artefacts, local configs, and credentials

**Organisation-level repository hosting**: Store repositories in a shared organisation account, not individual developer accounts. This ensures continuity when team members leave and enables consistent access control.

**Repository documentation**:
- Every repository has a README covering: purpose, how to run locally, how to deploy, and how to contribute
- Architecture decisions recorded (Architecture Decision Records / ADRs) for significant choices
- Runbooks maintained for operational procedures

## Embedding Standards in Agile Practice

Engineering standards only hold if they are part of the team's daily practice, not a separate document nobody reads.

**Definition of Done**: Include key standards in the DoD. If peer code review, passing automated security scan, and test coverage are not in the DoD, they will be skipped under pressure.

**Sprint retrospectives**: Periodically review standards compliance. Is technical debt growing? Are PRs getting rubber-stamped? Is the pipeline catching issues before production? Use retros to raise standards as the team matures.

**Backlog items for standards work**: Dependency updates, security remediations, and tooling improvements are legitimate backlog items. They compete with features for capacity and should be prioritised accordingly — not deferred indefinitely. A team that never updates dependencies is accruing hidden risk.

**The SM's role**: The Scrum Master does not own engineering standards — that is the team's accountability. But the SM should:
- Protect time for technical debt and standards work in sprint planning
- Escalate when external pressure is causing the team to skip DoD criteria
- Surface the relationship between declining standards and declining delivery speed in retrospectives
- Ensure new team members understand and adopt the team's standards
