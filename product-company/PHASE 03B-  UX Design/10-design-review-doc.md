# design-review-doc.md

> **Skill:** Produces a design review checklist and sign-off document used to formally evaluate design work against quality standards before handoff to engineering or launch.

---

## TLDR

A design review document is the formal gate check that a design must pass before being handed off to engineering. Unlike a critique (which improves design in progress), a review verifies that a completed design meets all required standards: completeness, consistency, accessibility, responsiveness, and alignment with the brief. It produces a documented sign-off record.

---

## Topic Explanation

### Review vs. Critique

**Critique:** Exploratory. Happens during the design process. Purpose is to improve the design. The right answer is unknown.

**Review:** Evaluative. Happens when design is considered complete. Purpose is to verify it meets standards. The right answers are defined in advance.

Both are necessary. Critique without review produces beautiful designs that are incomplete. Review without critique produces checklist-compliant designs that do not solve the right problem.

### What a Design Review Checks

A comprehensive design review checks five categories:

**Completeness:** Are all required states, flows, and edge cases designed? Does the spec cover everything engineering will need?

**Consistency:** Does the design use established design system components correctly? Is terminology consistent with the rest of the product?

**Accessibility:** Does the design meet WCAG 2.1 AA requirements? Are all interactive elements keyboard accessible?

**Responsiveness:** Does the design specify behavior at all required breakpoints?

**Brief alignment:** Does the final design achieve the goals stated in the design brief? Does it solve the stated problem for the stated user?

---

## Output Format

```
1. REVIEW HEADER
   Feature name, design file link, designer, reviewer(s), date, version.
   Review type: pre-handoff / pre-launch / design system contribution.

2. BRIEF ALIGNMENT CHECK
   [ ] Design solves the problem stated in the design brief
   [ ] All design goals from the brief are addressed
   [ ] Success criteria can be measured against this design
   [ ] Out-of-scope items are not included
   Notes:

3. COMPLETENESS CHECK
   [ ] All required user flows are designed
   [ ] All states documented: default, hover, focus, active, disabled, loading, error, empty
   [ ] Edge cases documented
   [ ] Design spec is complete and up to date
   [ ] Handoff doc is prepared
   Notes:

4. DESIGN SYSTEM CONSISTENCY CHECK
   [ ] Uses correct components from the design system
   [ ] Uses correct design tokens (no hard-coded values)
   [ ] Follows spacing and layout grid
   [ ] Typography uses the defined type scale
   [ ] New patterns documented or proposed for design system
   Notes:

5. COPY AND CONTENT CHECK
   [ ] All copy follows UX writing guidelines
   [ ] Error messages are specific and actionable
   [ ] Empty states are designed
   [ ] All copy has been reviewed by UX writer (if applicable)
   Notes:

6. ACCESSIBILITY CHECK
   [ ] Color contrast meets WCAG 2.1 AA (4.5:1 for text, 3:1 for UI elements)
   [ ] Touch targets meet minimum size requirements
   [ ] No information conveyed by color alone
   [ ] Focus states visible for all interactive elements
   [ ] ARIA requirements specified in handoff
   Notes:

7. RESPONSIVE CHECK
   [ ] Design specifies behavior at all required breakpoints
   [ ] Mobile layout reviewed and approved
   [ ] Responsive design spec updated
   Notes:

8. SIGN-OFF
   Design lead: [name] [date] [approved / approved with changes / rejected]
   PM: [name] [date] [approved / approved with changes / rejected]
   Engineering lead: [name] [date] [approved / approved with changes / rejected]
   Changes required before final approval: [list]
```

---

## Starter Prompt

```
You are a design lead conducting a formal design review.

Feature being reviewed: [what design is being evaluated]
Design brief: [the goals and success criteria the design must meet]
Design system: [what system the design should follow]
Accessibility standard: [WCAG 2.1 AA or other]
Required breakpoints: [which screen sizes must be specified]
Reviewers: [who must sign off]

Produce a complete design review checklist covering all five review categories
and a sign-off format for each required approver.
Pre-populate the checklist with the specific requirements for this feature.
```

---

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
