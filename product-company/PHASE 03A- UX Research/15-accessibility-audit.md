# accessibility-audit.md

> **Skill:** Produces a structured accessibility audit report evaluating an interface against WCAG 2.1 (AA) guidelines, documenting violations with severity ratings, WCAG criterion references, and remediation recommendations.

---

## TLDR

An accessibility audit systematically evaluates an interface against the Web Content Accessibility Guidelines (WCAG) 2.1 at Level AA. The audit identifies violations that prevent or impede use by people with disabilities, assigns severity ratings, and provides specific remediation guidance. Used to achieve WCAG compliance, reduce legal risk, and improve the experience for all users.

---

## Topic Explanation

### WCAG 2.1 Structure

WCAG 2.1 is organized around four principles (POUR):

**Perceivable:** Information and UI components must be presentable to users in ways they can perceive. Key guidelines: text alternatives for images, captions for video, content adaptable to different presentations, sufficient color contrast.

**Operable:** UI components and navigation must be operable. Key guidelines: all functionality keyboard accessible, users have enough time to read content, no content that causes seizures, navigation aids.

**Understandable:** Information and UI operation must be understandable. Key guidelines: readable text, predictable behavior, input assistance for errors.

**Robust:** Content must be robust enough to be interpreted by a wide variety of user agents including assistive technologies. Key guidelines: compatible with current and future AT.

### Conformance Levels

**Level A:** Minimum compliance. Failures at Level A create fundamental barriers for some users.
**Level AA:** The standard for most legal and procurement requirements. Covers the most significant barriers.
**Level AAA:** Highest level. Not required for full conformance; used for specialized services.

Most accessibility audits target WCAG 2.1 AA. This skill defaults to Level AA.

### Audit Methods

**Automated testing:** Tools like axe, WAVE, or Lighthouse catch approximately 30 to 40% of WCAG violations automatically. Fast but incomplete.

**Manual testing:** An expert evaluates the interface against each relevant WCAG criterion. Catches issues automated tools miss. Required for full compliance verification.

**Assistive technology testing:** Testing with screen readers (NVDA, VoiceOver, JAWS), keyboard-only navigation, and voice control software. Reveals real-world AT compatibility issues.

A complete accessibility audit uses all three methods.

### Most Common WCAG 2.1 AA Violations

Research from WebAIM's annual accessibility surveys consistently finds these as the most common:
- Insufficient color contrast (criterion 1.4.3)
- Missing alt text for images (criterion 1.1.1)
- Empty or missing form labels (criterion 1.3.1, 2.4.6)
- Missing skip navigation links (criterion 2.4.1)
- Keyboard traps (criterion 2.1.2)
- Unclear link text "click here" (criterion 2.4.4)
- Missing page language declaration (criterion 3.1.1)

---

## When to Use This Skill

Use when:
- Preparing for a product launch with accessibility compliance requirements
- Responding to an accessibility complaint or legal inquiry
- Conducting a periodic accessibility review
- Auditing a competitor or acquisition target

---

## Dos

- **Do reference specific WCAG 2.1 criteria by number and name.** Vague references ("this is not accessible") are not actionable. "Fails WCAG 2.1 criterion 1.4.3 Contrast (Minimum)" is.
- **Do include automated, manual, and AT testing.** Automated alone misses the majority of issues.
- **Do test with real assistive technology, not just automated tools.** Screen reader behavior often differs from what automated tools predict.
- **Do provide specific remediation guidance.** "Add alt text" is not sufficient. "Add descriptive alt text that describes the content and function of the image, e.g., 'Bar chart showing Q3 revenue by region'" is.

---

## Output Format

```
1. AUDIT HEADER
   Product/interface audited, WCAG version and level, audit methods used,
   tools used, evaluator(s), date, scope.

2. EXECUTIVE SUMMARY
   Overall compliance status (Pass/Fail/Partial).
   Total violations by severity.
   Top 3 most impactful issues.
   Estimated effort to reach compliance.

3. VIOLATIONS BY WCAG PRINCIPLE (POUR)

   For each violation:
   - WCAG criterion number and name (e.g., 1.4.3 Contrast Minimum)
   - Conformance level: A / AA / AAA
   - Severity: Critical / Serious / Moderate / Minor
   - Description of the violation with specific location(s)
   - Impact: which disability groups are affected and how
   - Remediation recommendation with code example if applicable
   - Priority: Must fix / Should fix / Recommended

4. AUTOMATED TEST SUMMARY
   Tool(s) used and date.
   Total automated violations found.
   Note on what automated tools cannot detect.

5. MANUAL TEST FINDINGS
   Issues found only through manual evaluation.

6. ASSISTIVE TECHNOLOGY TEST FINDINGS
   Screen reader test results (which SR, which browser).
   Keyboard-only navigation results.
   Voice control results (if tested).

7. REMEDIATION PRIORITY MATRIX
   All violations sorted by: impact (high/medium/low) x effort (high/medium/low).
   Quick wins: high impact, low effort.
   Strategic fixes: high impact, high effort.

8. COMPLIANCE ROADMAP
   Phased remediation plan to reach WCAG 2.1 AA compliance.
   Phase 1 (must-do), Phase 2 (should-do), Phase 3 (recommend).
```

---

## Starter Prompt

```
You are an accessibility specialist conducting a WCAG 2.1 AA audit.

Interface being audited: [describe the interface, flows, or paste relevant details]
Scope: [which pages or flows are included]
Known issues: [any accessibility problems already identified]
Legal or compliance context: [any specific requirements driving the audit]

Apply WCAG 2.1 AA criteria across the POUR principles.
Document each violation with criterion number and name, severity,
impact on disability groups, and specific remediation guidance.
Produce a prioritized remediation matrix and compliance roadmap.
```

---

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
