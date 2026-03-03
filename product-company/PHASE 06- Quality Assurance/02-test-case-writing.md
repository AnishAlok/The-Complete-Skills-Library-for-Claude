# test-case-writing.md

> **Skill:** Produces well-structured test cases with clear preconditions, numbered steps, an expected result per step, and traceability to requirements for manual or automated execution.

---

## TLDR

A test case is a specific scenario verifying a defined behavior of the software. This skill produces test cases that are complete, unambiguous, and reproducible: anyone who reads it can execute it and determine pass or fail. Used by QA engineers writing cases for manual execution or as specifications for automation engineers.

---

## Topic Explanation

### What Makes a Test Case Good

**Atomicity.** One test case tests one behavior. A case checking five things is five tests combined. When it fails, you cannot tell which behavior broke.

**Reproducibility.** Same preconditions and steps always produce the same result. A test that sometimes passes and sometimes fails is unreliable and erodes trust.

**Independence.** Test cases must not depend on each other. Test B should not require Test A to have run first. Dependent tests fail in chains and make root cause diagnosis difficult.

**Traceability.** Every test case should trace to a requirement, user story, or acceptance criterion. This makes coverage measurable against requirements.

**Clear pass/fail criteria.** "The page loads correctly" cannot be evaluated. "The dashboard loads within 3 seconds and displays the user name and three most recent reports" can be.

### Positive vs. Negative Test Cases

Positive cases verify the system behaves correctly when used as intended. Happy path.

Negative cases verify the system handles incorrect, unexpected, or boundary inputs gracefully: required fields left empty, negative numbers where positive are required, unauthorized actions attempted.

A complete suite requires both. Teams commonly write extensive positive tests and few negative tests. Negative cases find a disproportionate share of defects.

### Boundary Value Analysis

For any input accepting values 1 to 100: test 0 (just below minimum), 1 (lower boundary), 100 (upper boundary), 101 (just above maximum), and a mid-range value. Errors concentrate at boundaries, not in the middle of valid ranges.

---

## Output Format

```
TEST CASE

ID: [TC-XXX]
Title: [Brief descriptive title]
Feature: [module or feature being tested]
Author: [QA engineer] | Date: [YYYY-MM-DD]
Type: [Positive / Negative / Boundary / Edge case]
Priority: [P1 Critical / P2 High / P3 Medium / P4 Low]
Requirement: [linked requirement, story ID, or acceptance criterion]

PRECONDITIONS:
[Exact system state before Step 1. User role, data that must exist, features enabled.]

TEST STEPS:
Step 1: [Exact action] -> Expected: [what should happen after this step]
Step 2: [Exact action] -> Expected: [what should happen]
Step N: [Final action] -> Expected: [final expected result]

OVERALL EXPECTED RESULT:
[The outcome that constitutes a pass. Specific and observable.]

ACTUAL RESULT: [Filled in during execution]
STATUS: Pass / Fail / Blocked / Not Run

POSTCONDITIONS:
[System state after execution. Any cleanup required.]

TEST DATA:
[Specific accounts, field values, or files required to execute this test]

NOTES:
[Known related issues, environmental requirements, related test IDs]
```

---

## Example: Positive and Negative Cases for the Same Feature

```
TC-101: Admin exports compliance report as PDF [Positive]
Preconditions: Logged in as Admin role. One or more compliance reports exist. On Reports > Compliance page.
Step 1: Click Export on any report row -> Expected: Export modal opens with format options
Step 2: Select PDF from Format dropdown -> Expected: PDF option highlighted and selected
Step 3: Select Last 30 days -> Expected: Date range shows as selected
Step 4: Click Export in the modal -> Expected: Modal closes, loading indicator appears in nav
Step 5: Wait up to 30 seconds -> Expected: Toast notification: "Your report is ready to download"
Step 6: Click the download link in the toast -> Expected: PDF file downloads to local machine
Step 7: Open the downloaded PDF -> Expected: PDF shows report title, correct date range, all data rows
Overall expected: PDF file is named [AccountName]-compliance-[date].pdf and contains complete data.

TC-102: Export button disabled when no reports exist [Negative]
Preconditions: Logged in as Admin. Zero compliance reports exist in this account.
Step 1: Navigate to Reports > Compliance -> Expected: Page loads with empty state message
Step 2: Observe Export button state -> Expected: Export button is disabled or not present
Overall expected: User cannot initiate export with no data. No error state or crash occurs.
```

---

## Starter Prompt

```
You are a QA engineer writing test cases.

Feature: [what is being tested]
Acceptance criteria: [the behaviors to verify]
User roles involved: [which user types interact with this feature]
Positive scenarios: [happy path flows to cover]
Negative scenarios: [error states and invalid inputs to test]
Boundary conditions: [any min/max values or range limits]
Test data available: [test accounts and data that exist]

Produce complete test cases covering all scenarios.
Each must include preconditions reproducible by any tester,
steps with an expected result per step, and a specific measurable overall expected result.
Cover positive, negative, and boundary cases.
Flag any expected result that cannot produce a clear pass/fail determination.
```

---

## Related Skills

| Use This Next | Why |
|---|---|
| `regression-test-suite.md` | Test cases are organized into regression suite tiers |
| `defect-report.md` | Failed test cases generate formal defect reports |
| `automation-test-plan.md` | Manual test cases become automation candidates |

*Skill file version: 1.0 | Phase: 07 - Quality Assurance | Company type: Product*
