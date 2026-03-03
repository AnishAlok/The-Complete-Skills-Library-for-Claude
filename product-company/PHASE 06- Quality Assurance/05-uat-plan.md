# uat-plan.md

> **Skill:** Produces a User Acceptance Testing plan defining scope, participants, test scenarios, acceptance criteria, environment setup, and schedule for formal stakeholder validation before release.

---

## TLDR

A UAT plan defines how end users or business stakeholders formally validate that a system meets their requirements before production release. It answers: who tests, what they test, in what environment, over what timeline, and what must be true to accept the system for deployment.

---

## Topic Explanation

### UAT vs. QA Testing

QA testing verifies technical correctness: does the software behave as specified?

UAT verifies business fitness: does the software meet the actual needs of the people who will use it?

These are different questions. A system can correctly implement its specification while the specification missed what users actually needed. UAT is the final verification gate, focused on real-world usability and business process fit rather than technical correctness.

### Who Conducts UAT

UAT participants should be representative end users or business stakeholders, not QA engineers or developers. The value of UAT comes from the perspective of people who will actually use the system in production. QA engineers executing UAT scenarios produce QA testing, not UAT.

Good UAT participants: business process owners, representative end users from key roles, subject matter experts for domain-specific functionality, compliance or regulatory stakeholders if applicable.

### UAT Scenarios vs. Test Cases

UAT scenarios are written from a business process perspective, not a technical testing perspective.

QA test case: "Verify that clicking the Export button opens the export modal with format options."

UAT scenario: "Complete the end-of-month compliance reporting process. Generate the compliance report, confirm the data matches the prior-period report for unchanged accounts, export as PDF, and confirm it is formatted correctly for regulatory submission."

UAT scenarios are longer, less granular, and focused on business outcomes.

---

## Dos

- **Do write scenarios in business language, not technical language.** Business users should be able to read and execute them without QA help.
- **Do define explicit acceptance criteria for each scenario.** "Looks good" is not acceptance criteria.
- **Do provision the UAT environment with realistic data.** UAT with no data or obviously fake data produces false confidence.

---

## Output Format

```
1. UAT PLAN HEADER
   Project, release version, UAT lead, planned UAT dates, sign-off authority.

2. UAT OBJECTIVES
   Business processes and requirements being validated.
   Definition of successful UAT completion.

3. SCOPE
   In scope: features and business processes included.
   Out of scope: excluded features and rationale.

4. UAT PARTICIPANTS
   Name | Role | Business area | Scenarios assigned | Time commitment

5. UAT SCENARIOS
   For each scenario:
   - ID and title
   - Business process being validated
   - Assigned to: [participant name]
   - Preconditions: [starting state]
   - Steps: [business task in user language, not technical steps]
   - Acceptance criteria: [specific, observable pass conditions]
   - Business data to use

6. ACCEPTANCE CRITERIA (summary)
   Functional: all scenarios pass.
   Non-functional: performance acceptable to users, no critical defects open.
   Defect deferral criteria vs. blocking criteria.

7. UAT ENVIRONMENT
   Environment to use. Data setup requirements.
   Access provisioning: who sets up tester accounts and when.
   Support during UAT: who handles questions and triage.

8. UAT SCHEDULE
   Day-by-day schedule. Checkpoint reviews.
   Defect triage cadence. Sign-off meeting date.

9. DEFECT MANAGEMENT
   How UAT defects are reported. Severity classification.
   Resolution SLA during UAT. Who decides if a defect blocks sign-off.

10. EXIT CRITERIA AND SIGN-OFF PROCESS
    Specific conditions that must be true for sign-off.
    Contingency plan if exit criteria are not met by the planned date.
    Reference to UAT sign-off document.
```

---

## Starter Prompt

```
You are a QA lead or project manager writing a UAT plan.

Project: [what is being accepted]
Release scope: [features or system being validated]
UAT participants: [names, roles, and business areas]
Business processes to validate: [key workflows to cover]
UAT environment: [where testing will happen]
Timeline: [UAT start and end dates]
Sign-off authority: [who has authority to accept the system]

Produce a complete UAT plan with scenarios written in business language,
acceptance criteria, environment requirements, schedule, and exit criteria.
Every scenario must describe a real business task, not a software behavior.
Every scenario must have specific, observable acceptance criteria.
```

---

## Related Skills

| Use This Next | Why |
|---|---|
| `uat-sign-off.md` | UAT plan defines the test; sign-off records the outcome |

*Skill file version: 1.0 | Phase: 07 - Quality Assurance | Company type: Product*
