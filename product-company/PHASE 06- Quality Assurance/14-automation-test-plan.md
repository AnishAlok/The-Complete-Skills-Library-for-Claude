# automation-test-plan.md

> **Skill:** Produces a test automation strategy and coverage plan defining what to automate, framework selection rationale, coverage targets by layer, CI/CD integration, maintenance approach, and implementation roadmap.

---

## TLDR

A test automation plan defines the strategy for building and maintaining automated tests: which tests to automate, what frameworks to use, coverage targets by pyramid layer, CI/CD integration, and the roadmap for building coverage over time. It answers: where should we invest in automation to get the most reliable, fastest-running, lowest-maintenance test suite possible?

---

## Topic Explanation

### What to Automate (and What Not To)

**Good automation candidates:** high-frequency regression tests that run every sprint, tests that are tedious and error-prone when executed manually, API and service integration tests with well-defined contracts, and data-driven tests with many parameter combinations.

**Poor automation candidates:** features currently in active development that change every sprint, visual design verification that requires human aesthetic judgment, exploratory testing (which requires adaptive human judgment by definition), one-time investigation tests, and features with very low change risk that rarely cause regressions.

The automation selection should be driven by the test pyramid: maximize unit test automation, strong integration test automation, and selective E2E automation for critical paths only.

### The E2E Automation Fragility Problem

End-to-end automated tests are notoriously fragile. They break frequently due to UI changes, test environment instability, timing issues, and test data state problems. A large suite of E2E tests that fails 20% of the time for reasons unrelated to the product erodes trust in the entire test infrastructure.

Common mitigations: page object model to centralize and isolate UI selectors, explicit waits rather than fixed sleep statements, complete test data isolation to prevent inter-test dependencies, and a ruthless policy of retiring or fixing chronically flaky tests rather than tolerating them.

### Calculating Automation ROI

Investment in automation is justified when the time saved exceeds the time invested:

ROI = (Manual test execution time x number of runs) minus (Automation development time + Ongoing maintenance time)

Example: A test taking 10 minutes manually, running every sprint for 50 sprints, saves 500 minutes. If automation development takes 60 minutes and maintenance averages 5 minutes per sprint (250 minutes over 50 sprints), the net saving is 190 minutes. Positive ROI; automate it.

Documenting ROI rationale for each automation candidate helps prioritize where to invest limited automation engineering time.

---

## Dos

- **Do start with unit and integration layers before E2E.** The highest ROI automation is at the base of the pyramid, not the top.
- **Do define flaky test retirement criteria before beginning.** "If a test fails more than X% of runs for non-product reasons over Y sprints, it is retired."
- **Do allocate sprint capacity explicitly for automation maintenance.** Without a maintenance budget, the suite degrades faster than it grows.

---

## Donts

- **Dont automate features under active development.** The maintenance cost of constantly updating tests for in-progress features is higher than the value.
- **Dont count flaky tests as "passing" in coverage metrics.** A test that sometimes passes is not providing reliable coverage.

---

## Output Format

```
1. AUTOMATION PLAN HEADER
   Product, date, QA lead. Current automation state.
   Target state and overall timeline.

2. AUTOMATION OBJECTIVES
   What this investment achieves.
   Target metrics: coverage %, regression run time, manual QA hours saved per sprint.

3. SCOPE
   In scope: test types and feature areas targeted for automation.
   Out of scope: areas explicitly not being automated, with rationale.

4. TECHNOLOGY SELECTION
   Unit testing: [framework and rationale]
   Integration testing: [framework and rationale]
   E2E / UI testing: [framework, e.g., Playwright / Cypress, and rationale]
   API testing: [framework, e.g., Postman/Newman / REST-assured, and rationale]
   Performance testing: [tool if in scope]
   Visual regression: [tool if in scope]

5. COVERAGE TARGETS BY PYRAMID LAYER
   Unit tests: [target code coverage %]
   Integration tests: [API contract coverage target, service integration coverage]
   E2E tests: [number of critical user journeys to be covered]
   Overall regression automation: [target % of regression suite automated]

6. AUTOMATION CANDIDATES
   Test or area | Type | Priority | Dev effort estimate | Run time | ROI rationale | E2E flakiness risk

7. IMPLEMENTATION ROADMAP
   Phase 1 (Sprints N to M): [highest ROI items first]
   Coverage target at end of Phase 1: X%

   Phase 2 (Sprints M to P): [next priority tier]
   Coverage target at end of Phase 2: Y%

   Phase 3 (Sprints P to Q): [remaining items]
   Coverage target at end of Phase 3: Z%

8. CI/CD INTEGRATION
   Where each test layer runs in the pipeline.
   Trigger conditions: on every commit / PR only / nightly / pre-release.
   Pass/fail gates: what causes a pipeline failure.
   Parallel execution approach to minimize total run time.

9. MAINTENANCE APPROACH
   Ownership: who owns automated tests for each feature area.
   Flaky test policy: investigation trigger criteria and retirement criteria.
   Sprint capacity allocated to automation maintenance: [% of QA sprint capacity].
   Quarterly coverage review process.

10. REPORTING
    How automation results are surfaced: dashboard, CI notifications, sprint reports.
    Pass rate trend. Flakiness rate trend. Coverage trend over time.
```

---

## Starter Prompt

```
You are a QA lead writing a test automation plan.

Product: [name and tech stack]
Current automation state: [what is already automated, if anything]
Test pyramid gaps: [where the current coverage is weakest]
CI/CD platform: [pipeline tool]
Development cadence: [sprint length, release frequency]
QA team capacity: [engineers available for automation work]
Priority features or journeys to automate: [the highest-value targets]

Produce a complete automation plan covering:
- Framework selection with rationale for each layer
- Coverage targets by pyramid layer
- Prioritized automation candidates with ROI rationale
- Implementation roadmap with coverage milestones
- CI/CD integration and pass/fail gates
- Maintenance approach and sprint capacity allocation

Every E2E automation candidate must include a flakiness risk assessment.
```

---

## Related Skills

| Use This Before | Why |
|---|---|
| `qa-test-strategy.md` | Strategy defines the automation goals this plan executes |
| `test-case-writing.md` | Manual test cases become the specification for automation |

| Use This Alongside | Why |
|---|---|
| `regression-test-suite.md` | Automation plan determines which tests can achieve Tier 1 status |

*Skill file version: 1.0 | Phase: 07 - Quality Assurance | Company type: Product*
