# design-handoff-doc.md

> **Skill:** Produces a design handoff document with engineering annotations, implementation notes, component references, and clarification guides that reduce back-and-forth between design and engineering.

---

## TLDR

A design handoff document is the package of context, annotations, and decisions that engineering needs to implement a design correctly and independently. It accompanies the design files and reduces the number of questions engineering must bring back to design. Used when a feature moves from design complete to engineering implementation.

---

## Topic Explanation

### Why Handoffs Fail

Most implementation bugs and design divergence trace back to handoff failures. The three most common:

**Incomplete state coverage:** The design file shows the happy path. Engineering implements the happy path. Error states, loading states, and edge cases are invented under time pressure.

**Missing decision rationale:** Engineering makes a "small" visual judgment call that seemed unimportant but violated a design pattern. If the rationale had been documented, the pattern would have been understood and followed.

**Ambiguous measurements:** Figma measurements do not always communicate spacing intent. "Is this 16px because the design system dictates it or because you eyeballed it?" Documentation of what is a system value vs. a one-off prevents inconsistency.

### What Belongs in Handoff vs. What Belongs in the Spec

**Design spec:** Complete documentation of all states, behaviors, and edge cases. Written before implementation begins. The reference document.

**Handoff doc:** The curated implementation guide. Points to the spec for detail. Adds annotations, component references, and engineering-specific notes that are most useful during active implementation. More concise than the spec.

Both should exist. The handoff doc does not replace the spec; it guides the engineer to the right parts of it.

---

## Output Format

```
1. HANDOFF HEADER
   Feature name, design file link (and specific pages/frames), designer,
   engineering lead, PM, date, implementation ticket reference.

2. IMPLEMENTATION OVERVIEW
   Brief description of what is being built.
   New vs. modified vs. using existing components.
   Estimated complexity: S / M / L.

3. DESIGN FILE GUIDE
   Which frames are canonical (vs. exploration or archive).
   How the file is organized.
   Which page has the latest approved version.

4. COMPONENT REFERENCE
   For each UI element: design system component used (with link).
   Any components that require new development.
   Properties and variants to use for each instance.

5. INTERACTION NOTES
   Key behaviors that are not visible in static files.
   Reference to interaction design doc for full detail.
   Any animations or transitions.

6. COPY AND CONTENT
   Reference to microcopy doc for all UI text.
   Placeholder copy that must be replaced with real content.
   Character limits and truncation rules.

7. RESPONSIVE NOTES
   How the layout changes at key breakpoints.
   Reference to responsive design spec.

8. ACCESSIBILITY CHECKLIST
   ARIA requirements for this feature.
   Keyboard behavior.
   Any accessibility-specific implementation notes.

9. EDGE CASES TO IMPLEMENT
   The 5 to 10 most important edge cases.
   Reference to design spec for complete list.

10. OPEN QUESTIONS
    Any decisions not yet made that engineering may encounter.
    How to escalate questions during implementation.
    Expected response time.

11. QA GUIDANCE
    What to verify before marking implementation complete.
    Reference to design QA checklist.
    How to share builds for design review.
```

---

## Starter Prompt

```
You are a UX designer creating a design handoff document for engineering.

Feature name: [what is being handed off]
Design file: [location and which frames are canonical]
Components used: [design system components and any new ones]
Key interactions: [behaviors not visible in static files]
Edge cases: [the most important edge cases to implement]
Accessibility requirements: [ARIA, keyboard, and focus requirements]
Open questions: [anything not yet resolved]

Produce a complete design handoff document.
Distinguish between what uses existing design system components and what requires new work.
Highlight edge cases that are most likely to be missed.
```

---

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
