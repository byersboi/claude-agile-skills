# Acceptance Criteria Templates

Given/When/Then patterns for common story types. For scenario-writing craft, Gherkin discipline and BDD practice, see the **`bdd-user-stories`** skill and its `references/scenario-writing-checklist.md`. This file is a pattern catalogue to copy from during refinement.

## The two formats

**Rule-based** — a checklist of conditions. Faster to write; fine for simple items.

> - Password must be at least 12 characters
> - Rejected passwords show the specific reason
> - The user is not locked out after a failed attempt

**Scenario-based (Given/When/Then)** — describes behaviour through examples. Slower, but surfaces the disagreements that rule lists hide.

> **Given** I am on the password reset page
> **When** I submit a password of fewer than 12 characters
> **Then** I see "Password must be at least 12 characters" and the field keeps focus

**Which to use:** scenarios when the behaviour is conditional, has edge cases, or when two people in refinement describe it differently. Rules for the rest. Don't write scenarios for everything — volume kills readability.

## Rules for writing them

- **Written during refinement, with the team.** AC written by the PO alone are a specification hand-off
- **Observable behaviour only.** No implementation ("the service calls the payments API")
- **One behaviour per scenario.** Multiple Whens usually means multiple scenarios
- **No conjunctions in the When.** "When I submit and confirm" hides a step
- **Cover the unhappy paths.** Most defects live where nobody wrote a Then
- **Concrete values beat descriptions** — "a balance of £0.00" not "an invalid balance"

---

## Pattern catalogue

### Form submission / validation

```
Scenario: Valid submission
  Given I have completed all required fields
  When I submit the form
  Then my details are saved
  And I see a confirmation with my reference number

Scenario: Missing required field
  Given I have left the email field empty
  When I submit the form
  Then I see "Enter your email address" next to the email field
  And the rest of my answers are retained

Scenario: Invalid format
  Given I have entered "not-an-email" in the email field
  When I submit the form
  Then I see "Enter an email address in the correct format, like name@example.com"
```

### Authentication and permissions

```
Scenario: Permitted role
  Given I am signed in as a team administrator
  When I open the member management page
  Then I can add and remove members

Scenario: Insufficient permission
  Given I am signed in as a standard user
  When I navigate directly to the member management URL
  Then I see a "you do not have access" page
  And no member data is returned

Scenario: Session expired
  Given my session has been idle for 30 minutes
  When I submit the form
  Then I am asked to sign in again
  And my unsaved answers are restored after signing in
```

### Search and filtering

```
Scenario: Results found
  Given there are 12 records matching "reconciliation"
  When I search for "reconciliation"
  Then I see 10 results on the first page
  And I see "12 results" above the list

Scenario: No results
  When I search for "zzzzz"
  Then I see "No results for 'zzzzz'"
  And I see suggestions for broadening my search

Scenario: Filters combine
  Given I have filtered to status "Open"
  When I add the filter date "last 7 days"
  Then only records that are both open and from the last 7 days are shown
  And both filters are shown as removable tags
```

### Payments and money

```
Scenario: Successful payment
  Given my basket total is £42.50
  When my card payment is authorised
  Then my order is confirmed
  And I receive a receipt showing £42.50

Scenario: Card declined
  Given my card will be declined
  When I submit payment
  Then I see "Your card was declined — try another card"
  And my basket is unchanged
  And no order is created

Scenario: Duplicate submission
  Given I have submitted payment
  When I press the browser back button and submit again
  Then only one payment of £42.50 is taken
```

Money, dates and time zones are where ambiguity costs most. Always write the concrete value.

### Notifications

```
Scenario: Notification sent on status change
  Given I have opted in to email updates
  When my application status changes to "approved"
  Then I receive an email within 5 minutes
  And the email contains my reference number and next steps

Scenario: Opted out
  Given I have opted out of email updates
  When my application status changes
  Then I receive no email
  And the status is still updated in my account
```

### Data import / integration

```
Scenario: Valid file
  Given a CSV with 500 valid rows
  When I upload it
  Then all 500 records are imported
  And I see "500 records imported"

Scenario: Partial failure
  Given a CSV with 500 rows of which 3 have an invalid date
  When I upload it
  Then 497 records are imported
  And I can download a file listing the 3 failed rows with the reason

Scenario: Upstream unavailable
  Given the supplier API is not responding
  When the scheduled import runs
  Then the import is retried after 15 minutes
  And the support team is alerted after the third failure
```

### Accessibility

Better as rules than scenarios, and they belong in the Definition of Done rather than repeated on every story:

> - Operable by keyboard alone, in a logical order
> - All form fields have associated labels; errors are announced to screen readers
> - Contrast meets WCAG 2.2 AA
> - No information conveyed by colour alone
> - Tested with a screen reader before Done

### Non-functional criteria

Attach only where the story genuinely carries the requirement:

> - The results page renders in under 2 seconds at the 95th percentile with 10,000 records
> - The endpoint handles 50 requests per second without error
> - Failed writes are retried three times, then logged and alerted

---

## Anti-patterns

| Anti-pattern | Why it hurts | Fix |
|---|---|---|
| AC written after development | Becomes a test plan for what was built | Write during refinement, before sizing |
| Implementation in the Then | Locks the solution; breaks when the design changes | State observable outcomes |
| "As expected" / "works correctly" | Untestable; means different things to each reader | Name the expected behaviour explicitly |
| Twenty scenarios per story | Nobody reads them; the story is too big | Split the story |
| Only happy paths | Defects arrive from the paths nobody wrote | Ask "what could go wrong here?" for every story |
| DoD items repeated on every story | Noise that hides the story-specific criteria | Keep cross-cutting quality in the DoD |
