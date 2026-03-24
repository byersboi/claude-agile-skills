# Scenario Writing Checklist

Use this checklist to review BDD scenarios before they are handed to a developer for automation.

---

## The Scenario

- [ ] The scenario name describes a specific situation, not just "happy path" or "error"
- [ ] The scenario tests exactly one behaviour (one `When` step)
- [ ] The scenario is 3–5 steps long
- [ ] A non-technical stakeholder could read and understand it
- [ ] The scenario uses concrete values, not vague generalisations

## Given (Context)

- [ ] The context describes the state of the world, not how that state was set up
- [ ] All context needed to understand the scenario is present
- [ ] No unnecessary context is included (keep it to what's relevant)

## When (Action)

- [ ] There is only one `When` step
- [ ] The action is described in business terms, not UI terms
- [ ] The action is something a user or system would actually do

## Then (Outcome)

- [ ] The outcome is observable and verifiable
- [ ] The outcome is described from the user's perspective
- [ ] All significant outcomes are captured (not just the primary one)

## Coverage

- [ ] The happy path is covered
- [ ] The most likely failure path is covered
- [ ] Boundary conditions are covered (e.g. exactly at a limit, just over a limit)
- [ ] Any edge cases raised in the three amigos session are covered

## Quality

- [ ] No UI details (button names, field labels, page titles) appear in steps
- [ ] No technical implementation details appear in steps
- [ ] Steps do not duplicate each other across scenarios (use Background if needed)
- [ ] The scenario would still make sense if the interface changed

---

## Common Rewrites

| Instead of | Write |
|---|---|
| `When the user clicks the Submit button` | `When the user submits their application` |
| `Then the success message is displayed` | `Then the user is told their application was successful` |
| `Given the database contains a record for Alice` | `Given Alice has an active account` |
| `When the system calls the payment API` | `When Alice completes her purchase` |
| `Then the boolean flag is set to true` | `Then Alice's account is marked as verified` |
