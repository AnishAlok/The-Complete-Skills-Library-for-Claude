# defect-report.md

> **Skill:** Produces a structured QA defect report with complete reproduction steps, justified severity and priority ratings, full environment details, and supporting evidence for efficient developer investigation and resolution.

---

## TLDR

A defect report gives developers everything needed to reproduce, understand, and fix a defect without follow-up questions. This skill produces QA-quality reports that minimize triage time through precise reproduction steps, justified severity/priority ratings, complete environment context, and supporting evidence. Distinct from an informal bug report in rigor, completeness, and traceability.

---

## Topic Explanation

### Severity vs. Priority

These are separate assessments with different owners.

**Severity** (technical impact, assigned by QA):
- S1 Critical: system crash, data loss, security vulnerability, complete feature failure with no workaround
- S2 High: major feature broken, significant user impact, workaround is difficult or unavailable
- S3 Medium: feature degraded, workaround exists, moderate impact
- S4 Low: minor cosmetic issue, negligible user impact

**Priority** (business urgency, assigned by product):
- P1: must fix before release
- P2: must fix in the next sprint
- P3: fix when capacity allows
- P4: log and monitor

These are independent. An S1 defect in a rarely-used admin function might be P2. An S4 cosmetic defect on the login screen visible to every user might be P1. Both dimensions must be assessed separately.

### Reproduction Rate

Always document reproduction rate: always reproducible (100%), frequent (greater than 50% of attempts), intermittent (less than 50%), or occurred once. Intermittent defects require different investigation approaches and should be logged with all available diagnostic data even when exact reproduction steps cannot be confirmed.

### The Reproduction Steps Standard

The most common defect report failure is vague reproduction steps. "Go to the export page and click export" is not sufficient. The standard: start from a precisely defined system state, number every action, and include the exact data used. Any QA engineer or developer who has never seen the defect should be able to reproduce it from the steps alone.

---

## Output Format

```
DEFECT REPORT

ID: [DEF-XXXX]
Title: [Component / Feature] - [What is wrong, specifically]
Reported by: [QA engineer]
Date: [YYYY-MM-DD]
Version / Build: [exact build identifier]

SEVERITY: [S1 Critical / S2 High / S3 Medium / S4 Low]
Severity justification: [why this rating applies based on S1-S4 definitions]
PRIORITY: [P1 / P2 / P3 / P4] (QA initial recommendation)
Status: [New / Triaged / In progress / Fixed / Verified / Closed / Won't fix]
Assigned to: [developer, if known at time of logging]

ENVIRONMENT
Browser: [name and exact version]
OS: [name and version]
Device: [if mobile or device-specific]
User role and account: [role used and test account identifier]
Feature flags enabled: [any relevant feature flags]
Data state: [relevant data conditions that may affect reproduction]

DESCRIPTION
[One clear paragraph describing what is happening that should not happen.
Written so a developer reading only this paragraph understands the problem.]

PRECONDITIONS
[The exact system state required immediately before Step 1.
Be specific: logged in as which role, which page, what data exists.]

REPRODUCTION STEPS
1. [Exact action]
2. [Exact action]
3. [The step that triggers the defective behavior]

EXPECTED BEHAVIOR
[What the system should do. Reference the specific acceptance criterion or
requirement that defines the correct behavior.]

ACTUAL BEHAVIOR
[What the system actually does. Precise and specific. Match this to what
is visible in the attached screenshots or recording.]

REPRODUCTION RATE
[ ] Always reproducible (100%)
[ ] Frequent (greater than 50% of attempts)
[ ] Intermittent (less than 50% of attempts)
[ ] Occurred once, not yet reproduced

EVIDENCE
Screenshots: [attached / linked]
Screen recording: [attached / linked]
Console errors: [paste or attach]
Network requests: [paste or attach if relevant]
Logs: [paste or attach if relevant]

WORKAROUND
[Description of any available workaround, or: No workaround available.]

RELATED ITEMS
Test case that found this: [TC-ID]
Related defects: [DEF-IDs]
Requirement reference: [story or spec link]
```

---

## Starter Prompt

```
You are a QA engineer writing a defect report.

What is broken: [description of the defect]
Environment: [browser, OS, device, exact version, user role]
Reproduction steps: [numbered steps to reproduce from a known starting state]
Expected behavior: [what should happen, from the spec or acceptance criteria]
Actual behavior: [what actually happens]
Reproduction rate: [always / frequent / intermittent / occurred once]
Severity: [S1-S4 with justification]
Evidence available: [screenshots, logs, console errors, recording]
Workaround: [if any exists]

Produce a complete defect report.
Reproduction steps must be numbered and start from a precisely defined precondition.
Expected behavior must reference the specification or acceptance criterion.
Severity must be justified against the S1-S4 definitions.
```

---

## Related Skills

| Use This Before | Why |
|---|---|
| `test-case-writing.md` | Test cases identify the defects that get reported here |

| Use This Alongside | Why |
|---|---|
| `qa-metrics-report.md` | Defect data from reports feeds QA metrics |

*Skill file version: 1.0 | Phase: 07 - Quality Assurance | Company type: Product*
