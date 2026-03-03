# wcag-compliance-report.md

> **Skill:** Produces a WCAG accessibility compliance documentation report for a product or product area, documenting conformance level, known issues, remediation status, and accessibility statement content.

---

## TLDR

A WCAG compliance report documents the current accessibility conformance status of a product: what level of WCAG 2.1 compliance has been achieved, what issues exist, what is being remediated, and what the publicly stated accessibility position is. Used for legal compliance documentation, procurement requirements, accessibility statements, and internal accessibility governance.

---

## Topic Explanation

### WCAG Compliance Report vs. Accessibility Audit

**Accessibility audit** (`accessibility-audit.md`): The evaluation activity. Finding issues through manual testing, automated tools, and AT testing.

**WCAG compliance report** (this skill): The governance document. Documenting the current conformance status, issue inventory, remediation roadmap, and accessibility statement. Often produced from the findings of an audit.

An organization that has conducted an audit and not produced a compliance report has findings but no governance. The compliance report is what turns audit findings into an organizational commitment.

### The Accessibility Statement

Many jurisdictions (EU, UK, US federal) require organizations to publish an accessibility statement. The Web Accessibility Initiative (WAI) provides a standard structure. A compliance report should include the content needed to produce this statement.

The accessibility statement typically includes:
- The standard the organization is targeting (WCAG 2.1 AA)
- The date of the last assessment
- Current conformance status (fully conformant / partially conformant / non-conformant)
- Known issues with a timeline for resolution
- How to report accessibility issues
- Contact information for accessibility questions

### Conformance Levels and How to Claim Them

"WCAG 2.1 AA conformant" is a specific legal claim that means all Level A and AA success criteria are met with no exceptions. Most products cannot claim full conformance. The more honest claims:

**Fully conformant:** No failures. Rare.
**Partially conformant:** Failures exist but in limited areas. The specific failures must be listed.
**Non-conformant:** Significant failures. Should include a timeline for improvement.

---

## Output Format

```
1. REPORT HEADER
   Product name and version, report date, assessment scope, assessment method,
   assessors, WCAG version and target level.

2. EXECUTIVE SUMMARY
   Current conformance status: Fully conformant / Partially conformant / Non-conformant.
   Total issues by severity (A vs. AA vs. AAA vs. best practice).
   Assessment scope (what was and was not assessed).
   Next assessment scheduled.

3. CONFORMANCE STATUS BY PRINCIPLE

   For each WCAG principle (Perceivable / Operable / Understandable / Robust):
   - Overall status for this principle
   - Passing criteria list
   - Failing criteria with issue reference

4. ISSUE INVENTORY
   Full list of accessibility issues with:
   - Issue ID
   - WCAG criterion (number and name)
   - Level (A / AA)
   - Description
   - Affected pages or components
   - Severity: Critical / Serious / Moderate
   - Status: Open / In progress / Fixed / Deferred
   - Target resolution date

5. REMEDIATION ROADMAP
   Phase 1 (Critical): Must-fix issues with timeline.
   Phase 2 (Serious): Should-fix issues with timeline.
   Phase 3 (Moderate): Consider-fixing issues with timeline.

6. ACCESSIBILITY STATEMENT CONTENT
   Conformance claim.
   Assessment date.
   Known limitations with descriptions and alternatives.
   How to report accessibility issues (contact method).
   Enforcement procedure (if public sector or regulated).

7. TESTING METHODOLOGY
   Tools used (automated scanners).
   Manual testing scope.
   Assistive technologies tested (screen readers, keyboard, voice control).
   Testing dates.

8. AUDIT HISTORY
   Previous assessments with dates and summary findings.
   Trend: improving / stable / declining.
```

---

## Starter Prompt

```
You are an accessibility compliance specialist producing a WCAG compliance report.

Product: [what is being documented]
Assessment scope: [what was assessed]
Assessment findings: [results from an accessibility audit]
WCAG version and level: [2.1 AA or other]
Current conformance status: [fully / partially / non-conformant]
Known issues: [list of identified issues]
Remediation commitments: [what is being fixed and when]
Public statement requirements: [whether an accessibility statement is needed]

Produce a complete WCAG compliance report including conformance status,
issue inventory with severity and status, remediation roadmap,
and accessibility statement content.
```

---

## Related Skills

| Use This Before | Why |
|---|---|
| `accessibility-audit.md` | The audit produces the findings this report documents |
| `design-qa-checklist.md` | QA checklist includes accessibility checks |

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
