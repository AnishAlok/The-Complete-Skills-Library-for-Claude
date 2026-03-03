# regression-test-suite.md

> **Skill:** Produces regression test suite documentation that organizes test cases into a maintainable tiered suite covering the critical paths that must continue to work after every change.

---

## TLDR

A regression test suite is the curated set of test cases that runs after every significant change to verify existing functionality has not broken. This skill produces the documentation: test selection rationale, execution tiers, coverage map, and maintenance process. Used to establish and sustain a regression testing practice that scales with the product.

---

## Topic Explanation

### Why Suites Must Be Curated

The naive approach is to run all tests. This fails at scale: thousands of tests take hours, and under delivery pressure the suite gets skipped entirely. Regression suites must be curated: a deliberate selection that most efficiently verifies nothing critical broke.

### Risk-Based Selection

**High-risk (always in regression):** core user journeys, payment and billing flows, authentication and authorization, data integrity operations, external integrations.

**Medium-risk (include for changes to related areas):** secondary features, administrative functions, edge cases for common flows.

**Low-risk (periodic or pre-release only):** rarely-used features, cosmetic-only areas, features with no recent changes.

### Tiered Execution

**Tier 1 (Smoke):** 5 to 15 minutes. Runs on every commit or PR. Critical paths only. Must be 100% automated or it will not run consistently.

**Tier 2 (Core Regression):** 30 to 60 minutes. Runs on every merge to main or daily. Core feature coverage.

**Tier 3 (Full Regression):** 2 to 4 hours. Runs pre-release or weekly. Comprehensive coverage including lower-risk areas.

---

## Dos

- **Do define tier boundaries by execution time, not by test count.** A Tier 1 that takes 45 minutes will not get run on every commit.
- **Do make Tier 1 100% automated.** Manual Tier 1 tests create a human bottleneck in CI/CD.
- **Do document the rationale for each Tier 1 inclusion.** Future maintainers need this context when reorganizing.
- **Do prune the suite quarterly.** Suites only grow if not actively maintained. Tests that never fail or never run should be reviewed for removal.

---

## Donts

- **Dont add every new test case to the regression suite automatically.** Evaluate each for tier placement based on risk criteria.
- **Dont include Tier 1 tests that require manual setup or teardown.** They become a bottleneck in automated pipelines.

---

## Output Format

```
1. SUITE HEADER
   Product, suite version, QA lead, last updated.
   Stats: total tests by tier, overall automation percentage.

2. TIER DEFINITIONS
   For each tier:
   - Name and number
   - Target execution duration
   - Coverage focus
   - Current test count
   - Automation requirement
   - CI/CD trigger: when it runs

3. TEST INVENTORY BY AREA
   Area | Total tests | Tier 1 | Tier 2 | Tier 3 | Automation status

4. CRITICAL PATH COVERAGE
   The user journeys covered in Tier 1 with rationale for each inclusion.
   Known coverage gaps and documented risk acceptance.

5. COVERAGE MAP
   Requirements or user stories with at least one regression test.
   Requirements with no regression coverage: intentional vs. unintentional gaps.

6. MAINTENANCE PROCESS
   When to add: new features, defects fixed, requirements changed.
   When to remove: features removed, duplicate tests, obsolete flows.
   Ownership and quarterly review cadence.

7. EXECUTION RESULTS TRACKING
   How pass/fail results are tracked over time.
   Flaky test policy: what triggers investigation and retirement.
   Failure triage: who investigates and within what timeframe.
```

---

## Starter Prompt

```
You are a QA lead building regression test suite documentation.

Product: [name and key feature areas]
Critical user journeys: [paths that absolutely must work]
Automation maturity: [current automation percentage]
CI/CD integration: [where regression runs in the pipeline]
Team capacity: [QA engineers available for maintenance]
Existing tests: [count and organization if known]

Produce complete regression suite documentation with tier definitions,
critical path coverage with rationale, coverage map, and maintenance process.
Flag any critical user journey not covered by Tier 1.
Flag any Tier 1 test that requires manual execution.
```

---

## Related Skills

| Use This Before | Why |
|---|---|
| `test-case-writing.md` | Test cases must exist before organizing into a suite |

| Use This Alongside | Why |
|---|---|
| `automation-test-plan.md` | Automation plan determines what can achieve Tier 1 status |
| `qa-metrics-report.md` | Suite coverage is a key tracked metric |

*Skill file version: 1.0 | Phase: 07 - Quality Assurance | Company type: Product*
