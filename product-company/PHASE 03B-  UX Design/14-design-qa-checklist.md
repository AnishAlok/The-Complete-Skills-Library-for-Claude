# design-qa-checklist.md

> **Skill:** Produces a pre-launch design QA checklist for verifying that an implemented feature matches the design specification across visual accuracy, interactive states, accessibility, and responsive behavior.

---

## TLDR

Design QA is the process of comparing a live implementation against the approved design to find discrepancies before launch. This checklist covers the full scope of design QA: visual accuracy, state coverage, interaction behavior, accessibility, responsiveness, and copy. Used by designers, QA engineers, or product managers doing the final design check before release.

---

## Topic Explanation

### Why Design QA Is Distinct from Engineering QA

Engineering QA tests whether the code works as specified. Design QA tests whether the implementation matches the design intent. These are different questions and they catch different issues.

Engineering QA will find: crashes, broken functionality, API errors, incorrect data.
Design QA will find: wrong spacing, missing hover states, incorrect font weights, broken responsive layouts, inaccessible focus indicators, incorrect copy.

Both are necessary. Design QA without engineering QA ships broken features. Engineering QA without design QA ships functional but misaligned products.

### When Design QA Should Happen

Ideally, design QA happens in two passes:
1. **During implementation:** Designer reviews work in progress before it is "complete." Easier to fix issues before they are baked in.
2. **Pre-launch gate:** A formal checklist review of the complete implementation before release.

Some teams add a third pass post-launch to verify that nothing changed between the pre-launch check and the actual production deployment.

---

## Output Format

```
1. QA SESSION HEADER
   Feature, implementation URL or environment, build version, reviewer,
   date, design file reference.
   Result: Pass / Fail / Pass with issues.

2. VISUAL ACCURACY CHECKS
   [ ] Spacing matches spec (padding, margins, gaps)
   [ ] Typography: font, weight, size, line height correct
   [ ] Colors match design tokens
   [ ] Border radii correct
   [ ] Icon sizes and styles correct
   [ ] Images/assets load and display correctly
   Notes:

3. STATE COVERAGE CHECKS
   [ ] Default state correct
   [ ] Hover state implemented correctly
   [ ] Focus state: visible and correct
   [ ] Active/pressed state correct
   [ ] Disabled state correct
   [ ] Loading state correct
   [ ] Error state correct
   [ ] Empty state correct
   [ ] Success state correct
   Notes:

4. INTERACTION BEHAVIOR CHECKS
   [ ] Click/tap behavior as specified
   [ ] Keyboard navigation works correctly
   [ ] Form validation fires at correct moment
   [ ] Animations/transitions match motion spec
   [ ] No unexpected layout shifts
   Notes:

5. COPY AND CONTENT CHECKS
   [ ] All copy matches approved copy
   [ ] Error messages are specific and actionable
   [ ] No placeholder text in production
   [ ] Character limits and truncation work correctly
   [ ] No copy that violates writing guidelines
   Notes:

6. ACCESSIBILITY CHECKS
   [ ] All interactive elements keyboard accessible
   [ ] Focus order is logical
   [ ] ARIA labels present where needed
   [ ] Color contrast passes WCAG AA
   [ ] Error messages associated with form fields
   [ ] Images have alt text
   Notes:

7. RESPONSIVE CHECKS
   [ ] Mobile layout correct (375px)
   [ ] Tablet layout correct (768px)
   [ ] Desktop layout correct (1280px)
   [ ] No horizontal scroll at any breakpoint
   [ ] Touch targets minimum size on mobile
   Notes:

8. EDGE CASE CHECKS
   [ ] Empty state displays correctly
   [ ] Maximum content doesn't break layout
   [ ] Long text truncates correctly
   [ ] Offline state handled gracefully
   Notes:

9. ISSUES LOG
   Issue # / Description / Severity / Screenshot / Assigned to / Status
```

---

## Starter Prompt

```
You are a designer conducting design QA on a new feature implementation.

Feature: [what is being QA'd]
Design file: [reference to the approved design]
Implementation URL: [where to review the implementation]
Key concerns: [any areas likely to have issues based on complexity]
Accessibility standard: [WCAG 2.1 AA or other]
Required breakpoints: [which screen sizes to test]

Produce a complete design QA checklist pre-populated with feature-specific checks
in addition to standard checks. Include an issues log format for tracking findings.
```

---

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
