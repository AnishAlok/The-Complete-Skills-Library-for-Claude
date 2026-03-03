# test-plan.md

> **Skill:** Produces a QA test plan covering test strategy, test cases, coverage requirements, environments, and execution schedule for a feature or release.

---

## TLDR

A test plan defines what will be tested, how, and by whom before a feature or release goes to production. It covers test strategy, test case inventory, coverage targets, environment requirements, and exit criteria. Used by QA engineers to structure their work and by the team to verify that quality gates are defined before implementation begins.

---

## Topic Explanation

### Test Pyramid

The test pyramid (Mike Cohn) is the foundational framework for test strategy:

**Unit tests (base):** Test individual functions or classes in isolation. Fast, numerous, cheap. Should make up the majority of the test suite.

**Integration tests (middle):** Test how components work together. Slower than unit tests. Cover service boundaries, database interactions, and API contracts.

**End-to-end tests (top):** Test the full user flow through the system. Slowest, most expensive, most fragile. Use sparingly for the most critical user journeys.

A healthy test suite has many unit tests, a moderate number of integration tests, and few carefully selected end-to-end tests.

### Test Coverage Targets

Line coverage and branch coverage metrics are useful proxies but imperfect measures of test quality. A test suite with 100% line coverage that only tests the happy path is not a good test suite.

Better coverage measure: coverage of scenarios, not lines. Does the test suite cover:
- The happy path
- Each error condition
- Boundary conditions (empty input, maximum input, single item)
- Race conditions (for concurrent code)
- Security-sensitive paths

### Testing Environments

**Local:** Developer machine. Unit and integration tests.
**Development (dev):** Shared environment. Integration testing with real services.
**Staging:** Production-like. End-to-end testing. Performance testing.
**Production:** Limited post-deployment smoke tests only.

---

## Output Format

```
1. TEST PLAN HEADER
   Feature/release, version, QA lead, PM, engineering lead.
   Test plan dates: written, reviewed, execution start, exit criteria target.

2. TEST SCOPE
   What is covered by this test plan.
   What is explicitly out of scope (tested elsewhere or not testable).
   Risk-based prioritization: highest-risk areas that need most coverage.

3. TEST STRATEGY
   Test types to be used: unit / integration / E2E / performance / security.
   Test pyramid allocation: approximate distribution.
   Automation vs. manual: what is automated vs. manual and why.

4. TEST ENVIRONMENT REQUIREMENTS
   Environments needed.
   Test data requirements.
   External system mocks or stubs needed.
   Setup and teardown requirements.

5. TEST CASES

   For each test area:
   Test ID | Description | Type | Priority | Preconditions | Steps | Expected result | Pass/Fail

   Coverage by category:
   - Happy path tests
   - Error and exception tests
   - Boundary and edge case tests
   - Security tests
   - Performance tests (if applicable)

6. REGRESSION TEST SCOPE
   Existing functionality that must be verified not broken.
   Regression test suite reference.

7. DEFECT MANAGEMENT
   Defect severity definitions.
   Blocking defects vs. non-blocking.
   Escalation process for critical defects.

8. EXIT CRITERIA
   Conditions that must be met before QA sign-off.
   - All P1 test cases passing.
   - Zero open P1 defects.
   - Zero open P2 defects (or documented acceptance with PM sign-off).
   - Performance targets met.
   - Security review passed.

9. TEST EXECUTION SCHEDULE
   Timeline for test execution by phase.
   Dependencies on build availability.
```

---

## Starter Prompt

```
You are a QA engineer writing a test plan.

Feature/release: [what is being tested]
Technical spec reference: [link to technical or feature spec]
Test types needed: [unit / integration / E2E / performance / security]
Risk areas: [functionality with highest risk or complexity]
Environment requirements: [what environments and test data are needed]
Exit criteria: [what must be true before QA sign-off]
Timeline: [testing window]

Produce a complete test plan including test strategy, test cases by category
(happy path, error cases, edge cases, security), environment requirements,
exit criteria, and execution schedule.
```

---

*Skill file version: 1.0 | Phase: 05 - Engineering | Company type: Product*
