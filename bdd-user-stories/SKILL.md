---
name: BDD User Stories
description: This skill should be used when the user asks about "BDD", "behaviour-driven development", "behavior-driven development", "Gherkin", "Cucumber", "Given When Then", "acceptance criteria as tests", "executable specifications", "feature files", "writing scenarios", "three amigos", "discovery workshops", "user stories for QA", "linking user stories to tests", "acceptance test-driven development", "ATDD", "scenario outlines", "writing testable stories", or wants to write user stories and acceptance criteria in a way that connects directly to automated testing.
version: 1.0.0
---

# BDD User Stories

Behaviour-Driven Development (BDD) is a practice that closes the gap between business requirements and automated tests by writing acceptance criteria in a structured, plain-language format that both humans and computers can understand. It ensures that what is built matches what was agreed — and that this agreement is verified automatically, every time.

The key insight of BDD is that the conversation about what a story means is more valuable than the story itself. The Gherkin scenarios that come out of that conversation serve as living documentation, acceptance criteria, and automated tests simultaneously.

---

## The Three Practices

BDD follows an iterative cycle of three practices:

### 1. Discovery
Structured conversations around concrete examples to build shared understanding before any code is written. The goal is to surface misunderstandings, edge cases, and low-priority requirements early — when they are cheap to deal with.

### 2. Formulation
Documenting the examples from discovery as executable specifications. These are written in Gherkin — a plain-language format that is human-readable and machine-executable.

### 3. Automation
Using the formulated specifications to guide implementation through automated tests. These tests act as a continuous safety net: if the behaviour changes, the tests fail.

---

## The Three Amigos

Before writing scenarios, the right people need to be in the conversation. The "Three Amigos" are:

- **Product Owner / Business Analyst** — defines what the system should do and why
- **Developer** — understands what is technically feasible and how it might be built
- **Tester / QA** — thinks about edge cases, failure paths, and what could go wrong

The three amigos meet before a story is played to walk through it using concrete examples. This conversation surfaces ambiguity that would otherwise be discovered during development or, worse, after release.

**Discovery workshop format:**
1. Present a user story
2. Ask: "Can you give me a concrete example of this working correctly?"
3. Ask: "What would cause this to fail? What are the edge cases?"
4. Capture examples in Given/When/Then format
5. Agree on which examples will become automated scenarios

---

## Gherkin Syntax

Gherkin is the language used to write BDD scenarios. It is structured, but readable as plain English.

### Basic structure

```gherkin
Feature: Withdrawing cash
  As a bank customer
  I want to withdraw cash from an ATM
  So that I can access my money without visiting a branch

  Scenario: Successful withdrawal
    Given Alice has 234.56 in her account
    When Alice tries to withdraw 200.00
    Then the withdrawal is successful
    And Alice's balance is 34.56

  Scenario: Insufficient funds
    Given Alice has 50.00 in her account
    When Alice tries to withdraw 200.00
    Then the withdrawal is declined
    And Alice's balance remains 50.00
```

### Keywords

| Keyword | Purpose |
|---|---|
| `Feature` | Groups related scenarios; describes the capability being tested |
| `Scenario` | A single concrete example of behaviour |
| `Given` | The initial context — the state of the world before the action |
| `When` | The action or event being tested |
| `Then` | The expected outcome — what should be true after the action |
| `And` / `But` | Continue the previous step type for readability |
| `Background` | Steps that run before every scenario in the file — use for common setup |
| `Rule` | Groups scenarios that illustrate the same business rule |
| `Scenario Outline` | A template scenario run multiple times with different data |
| `Examples` | The data table used with a Scenario Outline |

### Scenario Outline (data-driven testing)

```gherkin
Scenario Outline: Withdrawal limits
  Given <name> has <balance> in their account
  When <name> tries to withdraw <amount>
  Then the result is <outcome>

  Examples:
    | name  | balance | amount | outcome   |
    | Alice | 500.00  | 200.00 | success   |
    | Bob   | 100.00  | 200.00 | declined  |
    | Carol | 200.00  | 200.00 | success   |
```

### Background (shared setup)

```gherkin
Feature: Account management

  Background:
    Given the banking system is online
    And the ATM has sufficient cash

  Scenario: ...
  Scenario: ...
```

---

## Writing Good Scenarios

### Do

- **Write in business language** — scenarios should be readable by anyone, not just developers. Avoid technical terms, method names, or implementation details.
- **Use concrete values** — "Alice has 234.56 in her account" is better than "a user has sufficient funds". Specific values make failures easier to diagnose.
- **Keep scenarios short** — aim for 3–5 steps. Long scenarios are usually testing multiple things at once.
- **Test one thing per scenario** — each scenario should have a single `When` step. Multiple actions mean multiple scenarios.
- **Name scenarios precisely** — the name should describe the specific situation, not just "happy path" or "error case".
- **Cover the edges** — happy path scenarios are easy. The value is in the scenarios that cover failures, boundary conditions, and unexpected inputs.

### Avoid

- **Imperative style** — don't describe clicks and form fills. Describe intent.
  - ❌ `When the user clicks the "Submit" button`
  - ✅ `When the user submits their application`
- **UI details** — scenarios should survive a redesign of the interface
- **Duplicating step text** — if the same step appears in multiple scenarios, use `Background` or refactor
- **Testing implementation** — scenarios test what the system does, not how it does it

---

## Connecting User Stories to Scenarios

A user story and its BDD scenarios should tell the same story at different levels of detail.

**User story:**
> As a bank customer, I want to withdraw cash from an ATM, so that I can access my money without visiting a branch.

**Acceptance criteria (traditional):**
> - Customer can withdraw if they have sufficient funds
> - Withdrawal is declined if funds are insufficient
> - Balance is updated after a successful withdrawal

**BDD scenarios:**
```gherkin
Scenario: Successful withdrawal within available balance
  Given Alice has 234.56 in her account
  When Alice withdraws 200.00
  Then the withdrawal is successful
  And Alice's balance is 34.56

Scenario: Withdrawal declined when funds are insufficient
  Given Alice has 50.00 in her account
  When Alice tries to withdraw 200.00
  Then the withdrawal is declined
  And Alice's balance remains 50.00
```

The scenarios are the acceptance criteria — not a separate document, but the same information in an executable form.

---

## Definition of Done and BDD

In a BDD approach, a story is not done until its scenarios pass. This makes the definition of done concrete and unambiguous:

- All agreed scenarios are written in Gherkin
- All scenarios are automated and passing
- No existing scenarios have been broken

This replaces the vague "QA sign-off" step with a specific, automated check that can be run at any time.

---

## Tags

Tags allow scenarios to be grouped and run selectively:

```gherkin
@smoke @payments
Scenario: Successful withdrawal
  ...

@regression
Scenario: Withdrawal declined when funds are insufficient
  ...
```

Common tagging strategies:
- `@smoke` — critical path scenarios run on every build
- `@regression` — full suite run before releases
- `@wip` — work in progress, excluded from CI until complete
- `@manual` — scenarios that document behaviour not yet automated

---

## Level Guidance

**Junior:** Focus on writing clear, readable scenarios that a non-technical stakeholder could understand. The most common mistake at this level is writing scenarios that describe the UI rather than the behaviour. Ask yourself: "Would this scenario still make sense if the interface changed completely?" Also practise running the three amigos conversation — the discussion is where most of the value is created.

**Mid-weight:** Focus on scenario design — knowing which scenarios to write, not just how to write them. A comprehensive set of scenarios covers the happy path, the common failure paths, and the boundary conditions. Work with testers to identify the edge cases that are most likely to be missed. Ensure scenarios stay in sync with the product as it evolves — stale scenarios are worse than no scenarios.

**Senior / Lead:** The hardest work at this level is embedding BDD as a team practice rather than a documentation exercise. BDD fails when scenarios are written after the code, when they are maintained only by testers, or when the three amigos conversation is skipped. Focus on the process: are the right people in the room before stories are played? Are scenarios being used to drive development, or just to verify it afterwards? Connect BDD to the team's definition of done and make passing scenarios a non-negotiable release gate.

---

## Additional Resources

- **Cucumber documentation** — [cucumber.io/docs](https://cucumber.io/docs) — full Gherkin reference and BDD guides
- **`skills/scrum/SKILL.md`** — for connecting BDD to sprint planning and definition of done
- **`skills/agile-estimation/SKILL.md`** — scenarios written upfront make stories easier to estimate accurately
- **`references/scenario-writing-checklist.md`** — quick checklist for reviewing scenarios before they are automated
