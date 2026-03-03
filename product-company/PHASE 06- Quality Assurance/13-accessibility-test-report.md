# accessibility-test-report.md

> **Skill:** Produces an accessibility testing results report documenting WCAG compliance findings, assistive technology test results, remediation requirements, and the accessibility quality gate verdict for release sign-off.

---

## TLDR

An accessibility test report documents testing against WCAG and assistive technology requirements: which criteria pass and fail, the severity of failures, evidence, and required remediation before release. Used to demonstrate accessibility due diligence, support legal compliance requirements, and ensure the product is genuinely usable by people with disabilities.

---

## Topic Explanation

### WCAG and Target Conformance Level

WCAG (Web Content Accessibility Guidelines) defines accessibility requirements in three conformance levels:

**Level A:** Minimum accessibility. Removes the most significant barriers. The floor, not the target.

**Level AA:** Standard accessibility. Required by most accessibility laws worldwide: the ADA (US), Section 508 (US federal), and the EU Web Accessibility Directive. This is the standard target for commercial products.

**Level AAA:** Enhanced accessibility. Not required as a general target but appropriate for specific high-accessibility contexts.

WCAG 2.1 Level AA is the correct default target. The report should document compliance against this specific standard.

### The Four POUR Principles

WCAG 2.1 is organized around four principles. All accessibility failures belong to one of these categories:

**Perceivable:** Content must be available to at least one of the user's senses. Common failures: missing alt text, insufficient color contrast, videos without captions.

**Operable:** Users must be able to operate the interface. Common failures: keyboard-inaccessible interactive elements, focus traps, time limits without ability to extend.

**Understandable:** Content and operation must be understandable. Common failures: unlabeled form fields, unclear error messages, inconsistent navigation patterns.

**Robust:** Content must be interpreted correctly by a wide variety of assistive technologies. Common failures: invalid HTML structure, improper ARIA usage, broken semantic markup.

### Automated vs. Manual Testing Coverage

Automated tools (Axe, WAVE, Lighthouse) detect approximately 30 to 40% of WCAG failures. The remaining 60 to 70% require manual testing because they involve human judgment:
- Whether alt text is meaningful vs. merely present
- Whether the logical reading order makes sense when heard by a screen reader
- Whether keyboard navigation is usable in practice, not just technically possible
- Whether focus management works correctly in interactive components

Both automated scan results and manual testing results are required for a complete accessibility test report.

---

## Output Format

```
1. REPORT HEADER
   Product, release version, test date, tester(s).
   Target standard: WCAG 2.1 Level AA.
   Scope: pages and components included in this test.

2. EXECUTIVE SUMMARY
   Accessibility test result: PASS / FAIL / CONDITIONAL PASS.
   Level A failures: [N]. Level AA failures: [N].
   Overall compliance posture and release recommendation.

3. TESTING METHODOLOGY
   Automated tools used with version numbers.
   Manual testing performed.
   Assistive technologies tested:
   - NVDA with Chrome / Firefox (Windows)
   - JAWS with Chrome / Edge (Windows)
   - VoiceOver with Safari (macOS)
   - VoiceOver with Safari (iOS)
   - TalkBack with Chrome (Android)
   Pages and components in scope.

4. AUTOMATED SCAN RESULTS
   Tool, scan date, pages scanned.
   Finding count by severity.
   Most frequently occurring issue types.

5. FINDINGS
   For each finding:

   ID: [A11Y-XXX]
   WCAG Criterion: [number and name, e.g., 1.1.1 Non-text Content]
   Conformance Level: [A / AA / AAA]
   POUR Principle: [Perceivable / Operable / Understandable / Robust]
   Severity: [Critical / High / Medium / Low]
   Component / Page: [where the issue occurs]

   Description: [what the accessibility problem is in plain terms]
   Impact: [which disability groups are affected and how their experience is degraded]
   Evidence: [screenshot, ARIA tree capture, or automated tool reference]
   Remediation: [specific technical fix required]
   Status: [Open / Fixed / Accepted / Deferred]
   Owner: [developer or team]
   Due date: [based on severity]

6. ASSISTIVE TECHNOLOGY TEST RESULTS
   For each AT and browser combination tested:
   - Critical user journeys tested
   - Pass / Fail / Issues noted
   - Screen reader specific issues not captured by automated scanning

7. WCAG 2.1 AA CRITERIA SUMMARY
   Criterion | Level | Status
   1.1.1 Non-text Content | A | Pass
   1.3.1 Info and Relationships | A | Fail - see A11Y-003
   [Continue for all applicable criteria]

8. ACCESSIBILITY QUALITY GATE

   PASS: No Level A failures. Level AA failures are low severity with accepted mitigations.
   System is approved for release from an accessibility perspective.

   CONDITIONAL PASS: No Level A failures. Specific Level AA issues to be resolved by [date].
   Conditions: [list specific findings and resolution dates]

   FAIL: One or more Level A failures are open.
   Level A failures are minimum accessibility requirements.
   System is not minimally accessible. Release is blocked.

9. REMEDIATION TRACKING
   For each open finding: owner, specific fix approach, target date, retesting required.
```

---

## Starter Prompt

```
You are a QA engineer writing an accessibility test report for a release.

Product: [name and type]
Release: [version]
Testing scope: [pages and components tested]
Target standard: WCAG 2.1 AA
Automated scan findings: [tool name and findings summary]
Manual testing findings: [issues discovered through manual testing]
Assistive technology test results: [screen reader and keyboard navigation outcomes]
Release disposition: [pass / fail / conditional]

Produce a complete accessibility test report with findings organized by WCAG criterion,
severity classification, assistive technology results, quality gate verdict,
and remediation tracking.
Level A failures must always block release without exception.
```

---

*Skill file version: 1.0 | Phase: 07 - Quality Assurance | Company type: Product*
