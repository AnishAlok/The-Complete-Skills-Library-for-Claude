# qa-test-strategy.md

> **Skill:** Produces an overall QA strategy document defining the testing approach, scope, methodology, tooling, team responsibilities, and quality standards for a product or release.

## TLDR

This skill answers: "How does this team ensure quality end to end?" A QA strategy is the governing document for all testing activity: what will be tested, at what levels, with what tools, by whom, and what quality gates must pass before release.

## Topic Explanation

### QA Strategy vs. Test Plan

QA strategy: the framework for quality. Relatively stable.
Test plan: execution plan for a specific release. Changes frequently.
The strategy guides every test plan.

### The Testing Pyramid

Unit tests (base): fastest, cheapest, most granular. Written by developers. Majority of all tests.
Integration tests (middle): test interactions between components and services.
End-to-end tests (top): test complete user journeys. Slowest and most fragile. Reserve for critical paths.

### Shift-Left Testing

Shift-left moves quality earlier in development. A bug found in requirements costs far less than one found in production. Practices: requirements review for testability, acceptance criteria before development, developer unit tests, CI on every commit.

### Risk-Based Testing

Prioritizes effort toward highest-risk areas: most complex, most frequently changed, most critical to business outcomes.

## Dos

- Define quality gates with measurable criteria, not aspirational statements
- Assign ownership at every test level
- Align the strategy with the actual development process
- Review and update the strategy annually

## Donts

- Do not write aspirational standards the team cannot currently meet
- Do not omit non-functional testing: performance, security, and accessibility are quality dimensions

## Output Format

```
1. STRATEGY HEADER
   Product, version, date, QA lead, review cadence.

2. QUALITY OBJECTIVES
   Quality goals, definition of done at each gate, metrics and targets.

3. SCOPE
   In scope: products, systems, test types.
   Out of scope: excluded areas and rationale.

4. TESTING APPROACH AND PRINCIPLES
   Core philosophy, shift-left commitments, risk-based criteria, pyramid target.

5. TEST LEVELS AND OWNERSHIP
   For each level (unit / integration / system / E2E / UAT):
   definition, owner, when it runs, tooling, coverage target.

6. TEST TYPES COVERED
   Functional, regression, performance, security, accessibility, compatibility, exploratory.

7. QUALITY GATES
   Merge gate: conditions before code merges to main.
   Release gate: conditions before production deployment.
   Gate waiver authority and circumstances.

8. DEFECT MANAGEMENT
   Severity definitions. Triage process. Resolution SLA. Release blocking criteria.

9. TEST ENVIRONMENTS
   Inventory, ownership, test data management, parity requirements.

10. TOOLING
    Test management, automation, CI/CD, defect tracking, performance, security tools.

11. TEAM RESPONSIBILITIES
    QA and developer obligations. Escalation path.

12. METRICS AND REPORTING
    Key metrics tracked, cadence, audience, how metrics drive decisions.
```

## Starter Prompt

```
You are a QA lead writing a test strategy document.

Product: [what is being tested]
Team: [developers, QA engineers, product managers]
Development methodology: [agile / continuous delivery / release train]
Current testing maturity: [what testing currently exists]
Key quality risks: [the most important concerns for this product]
Tooling: [existing tools and CI/CD platform]
Release cadence: [how often releases happen]

Produce a complete QA strategy covering all 12 sections.
Every quality gate must be measurable. Every test level must have a named owner.
Flag any quality risk with no proposed testing coverage.
```

## Related Skills

| Use This Before | Why |
|---|---|
| test-case-writing.md | Strategy defines standards that test cases implement |
| regression-test-suite.md | Strategy defines regression scope and tier targets |
| automation-test-plan.md | Strategy defines automation goals the plan executes |

*Skill file version: 1.0 | Phase: 07 - Quality Assurance | Company type: Product*
