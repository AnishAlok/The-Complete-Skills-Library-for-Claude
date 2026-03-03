# bug-report.md

> **Skill:** Produces a structured bug report with reproduction steps, environment details, expected vs. actual behavior, severity assessment, and relevant diagnostic information.

---

## TLDR

A well-formed bug report gives engineers everything they need to reproduce, understand, and fix a defect without a back-and-forth of clarifying questions. This skill produces structured bug reports that reduce triage time and eliminate the most common reasons engineers cannot reproduce reported bugs.

---

## Topic Explanation

### The Anatomy of an Effective Bug Report

**Reproduction steps:** The single most important section. Precise, numbered steps starting from a known state. If the bug cannot be reproduced, it usually cannot be fixed. If reproduction requires guessing, engineering time is wasted.

**Expected vs. actual behavior:** Many bugs are reported as "X is broken" without stating what correct behavior looks like. Explicitly stating both eliminates ambiguity about whether the behavior is truly a defect or a design misunderstanding.

**Environment:** The specific context in which the bug was observed. OS, browser version, user account, feature flags enabled, data state. Many bugs are environment-specific.

**Frequency:** Does this always happen, sometimes happen, or did it happen once? Intermittent bugs require different investigation approaches.

### Severity vs. Priority

**Severity:** The technical impact of the bug. How badly does it break things?
- Critical: Data loss, security vulnerability, system down
- High: Core functionality broken, no workaround
- Medium: Feature degraded, workaround exists
- Low: Minor cosmetic issue, negligible user impact

**Priority:** The urgency of fixing it relative to other work. A low-severity bug in a high-visibility area may be high priority. A high-severity bug in a rarely-used feature may be low priority. Severity is a QA judgment. Priority is a product judgment.

Both must be assigned separately.

---

## Output Format

```
BUG REPORT

Title: [Short descriptive title: [Component] - [What is wrong]]
Reporter: [Name]
Date reported: [YYYY-MM-DD]
Severity: [Critical / High / Medium / Low]
Priority: [P1 / P2 / P3 / P4]
Status: [New / Triaged / In progress / Fixed / Closed / Won't fix]
Assignee: [if known]

ENVIRONMENT
- Product version / build:
- Browser / OS / device:
- User account / role:
- Feature flags enabled:
- Relevant data state:

DESCRIPTION
[One paragraph clearly describing what is broken.]

REPRODUCTION STEPS
Starting state: [Describe the exact state before step 1]
1. [Step 1]
2. [Step 2]
3. [Step n]

EXPECTED BEHAVIOR
[What should happen when the steps above are followed.]

ACTUAL BEHAVIOR
[What actually happens. Be specific.]

FREQUENCY
[ ] Always reproducible
[ ] Intermittent (~__% of the time)
[ ] Happened once, could not reproduce

SCREENSHOTS / RECORDINGS
[Attach or link]

LOGS / ERROR MESSAGES
[Paste relevant console errors, server logs, or network responses]

WORKAROUND
[If one exists, describe it]

ADDITIONAL CONTEXT
[Any other relevant information: related bugs, recent changes, affected user count]
```

---

## Starter Prompt

```
You are a QA engineer or developer writing a bug report.

What is broken: [description of the defect]
Environment: [where it was observed]
Reproduction steps: [how to reproduce it]
Expected behavior: [what should happen]
Actual behavior: [what actually happens]
Frequency: [always / intermittent / once]
Severity: [critical / high / medium / low]
Available logs or screenshots: [any diagnostic data]

Produce a complete structured bug report using the standard template.
Make reproduction steps precise and numbered, starting from a known state.
Distinguish expected vs. actual behavior explicitly.
```

---

*Skill file version: 1.0 | Phase: 05 - Engineering | Company type: Product*
