# design-spec.md

> **Skill:** Produces a component-level design specification documenting visual properties, interaction states, behaviors, edge cases, and engineering handoff details for a specific UI component or feature.

---

## TLDR

This skill helps you answer: *"What exactly should this component do in every state, with every content variation, and in every edge case?"* It produces a comprehensive design spec that gives engineering everything needed to implement a component correctly, without requiring constant designer clarification. Used for complex components, new design system additions, or any feature where state and behavior complexity is high.

---

## Topic Explanation

### What Belongs in a Design Spec (and What Does Not)

A design spec documents the design decisions that need to be communicated to engineering. It is not a visual specification tool (like a Figma file), though it accompanies one. It is the written companion to the visual design that explains intent, behavior, and edge cases that visuals alone cannot communicate.

**What belongs in a spec:**
- All interaction states: default, hover, focus, active, disabled, loading, error, empty
- Content variations: short labels, long labels, truncation behavior
- Edge cases: empty state, maximum items, error conditions
- Animation and transition behavior
- Accessibility requirements: keyboard behavior, ARIA roles, screen reader text
- Engineering notes: what is new vs. what reuses existing components
- Open questions and decisions made

**What does not belong in a spec:**
- Pixel-perfect measurements (these live in the design tool)
- Color hex values (these live in design tokens)
- Asset files (these are exported separately)
- Implementation code (engineering decides implementation)

### The State Inventory

The most common gap between design specs and implementation is missing states. Designers often design the happy path and forget the other states. Every interactive component needs a complete state inventory:

**Visual states:** Default, hover, focus, active/pressed, selected, disabled
**Data states:** Empty (no data), loading, error, success, partial data
**Content states:** Short content, long content, missing content, international/special characters
**Permission states:** User does not have access, user must upgrade

A spec that documents only the default and error states leaves engineering to guess about everything in between.

### Edge Cases Are Not Optional

Edge cases are where most implementation bugs live and where most user frustration originates. A spec without edge cases produces an implementation where the edge cases were handled by whoever happened to be writing the code that day. The design spec is the right place to make edge case decisions deliberately.

Common edge cases to document:
- What happens with 0 items, 1 item, the maximum number of items, and more than the maximum?
- What happens when text is very short? Very long? Includes special characters?
- What happens when a user loses connectivity mid-interaction?
- What happens if an operation takes longer than expected?
- What happens when the user has multiple browser tabs open?

---

## When to Use This Skill

Use when:
- Building a new UI component that will be reused across the product
- A component has complex interaction states that Figma annotations alone cannot capture
- Engineering has repeatedly misimplemented a component and the root cause is incomplete specs
- Adding a component to the design system and needing complete documentation

Do NOT use when:
- The component is a simple, one-off static element with no meaningful states
- The component already has a complete spec in the design system

---

## Dos

- **Do complete the state inventory before any other section.** It is much harder to add states retroactively after the spec is written.
- **Do document decisions and why they were made.** A spec that explains the reasoning behind a decision is much more useful than one that only documents the outcome.
- **Do include what reuses existing components.** Engineering time is saved when the spec clearly identifies which parts can use existing design system components vs. what requires new work.
- **Do write edge cases as explicit scenarios.** "What if the text is too long?" is a question. "If the label exceeds 40 characters, truncate with an ellipsis and show full text in a tooltip on hover" is a spec.
- **Do include accessibility requirements as first-class spec items.** Keyboard navigation and ARIA requirements are not optional additions to review after implementation.

---

## Donts

- **Dont write a spec before the design is stable.** Speccing a design in flux produces specs that are immediately out of date.
- **Dont assume engineering will handle edge cases as you would.** They will handle edge cases logically, which may not match the intended user experience. Spec every edge case explicitly.
- **Dont duplicate what is already in the design system.** Reference the design system for inherited behavior rather than respecifying it.
- **Dont leave open questions unanswered in the spec.** An open question in a spec is a decision that will be made by engineering under time pressure. Make the decision in the spec.

---

## Ideal Inputs

```
1. THE COMPONENT OR FEATURE TO SPEC
   What component or interaction is being specified?
   Is this new or a modification of an existing component?

2. THE DESIGN FILE
   The Figma (or equivalent) link to the design.
   Which frames or pages are the canonical reference.

3. THE USE CASES
   What will users be trying to do with this component?
   What are the primary and edge case scenarios?

4. EXISTING DESIGN SYSTEM COMPONENTS
   What existing components does this use or extend?
   What is genuinely new vs. reused?

5. ENGINEERING CONTEXT
   What platform/framework is being used?
   Are there known technical constraints relevant to this component?
```

---

## Output Format

```
1. SPEC HEADER
   Component name, version, design file link (and specific frame),
   designer, PM, engineering owner, last updated, status.

2. OVERVIEW
   What this component is and what problem it solves for users.
   Where and how it will be used in the product.
   What design system components it uses or extends.

3. STATE INVENTORY
   Complete list of all states this component can be in.
   Organized as: visual states, data states, content states, permission states.

4. DEFAULT STATE SPECIFICATION
   Visual description for the default state.
   Reference to design file frame.
   Content requirements: minimum and maximum.

5. STATE-BY-STATE SPECIFICATION
   For each state:
   - Trigger: what causes this state
   - Visual change from default
   - Behavior change from default
   - Transition to/from this state (timing, animation)
   - Exit conditions: what returns to another state

6. CONTENT AND COPY REQUIREMENTS
   Required text content and character limits.
   Truncation behavior.
   Required vs. optional fields.
   Fallback/placeholder text.
   Reference to UX writing guidelines or microcopy spec.

7. INTERACTION BEHAVIOR
   Click/tap behavior.
   Keyboard navigation: tab order, keyboard shortcuts, focus management.
   Touch gestures (if mobile).
   Drag, scroll, or swipe behavior if applicable.

8. EDGE CASES
   Explicit scenario for each edge case.
   Format: "When [condition], the component should [behavior]."
   Cover: empty state, maximum content, error, loading, offline.

9. ACCESSIBILITY REQUIREMENTS
   ARIA role, label, and description requirements.
   Focus behavior and visible focus indicator.
   Screen reader announcement for state changes.
   Color contrast requirements (reference tokens).
   Touch target size (if mobile).

10. ANIMATION AND MOTION
    Transition specifications: property, duration, easing.
    Reference to motion design spec if applicable.

11. RESPONSIVE BEHAVIOR
    How the component behaves at different breakpoints.
    Reference to responsive design spec if applicable.

12. ENGINEERING NOTES
    What is new vs. reused from the design system.
    Known implementation considerations.
    Testing requirements.

13. OPEN QUESTIONS AND DECISIONS LOG
    Any remaining questions with owner and deadline.
    Log of significant decisions made during spec creation with rationale.
```

---

## Starter Prompt

```
You are a UX designer writing a complete component design specification.

Component or feature: [what is being specified]
Design file location: [link or description of the canonical design]
Use cases: [primary and edge case user scenarios]
Existing design system components used: [what this builds on]
Engineering platform: [React / Vue / iOS / Android / etc.]
Known constraints: [technical or design system constraints]
Specific edge cases to document: [any known edge cases to include]

Please produce a complete design spec including:
1. Full state inventory across visual, data, content, and permission states
2. Default state specification
3. State-by-state specification with trigger, visual change, behavior, transition, and exit
4. Content requirements with character limits and truncation behavior
5. Keyboard and touch interaction behavior
6. Explicit edge case scenarios in "When X, component should Y" format
7. Accessibility requirements (ARIA, focus, screen reader)
8. Engineering notes distinguishing new vs. reused components

Write edge cases as explicit scenarios, not as questions.
Flag any state that is likely to be missed by engineering if not specified.
```

---

## Related Skills

| Use This Next | Why |
|---|---|
| `design-handoff-doc.md` | The spec is the primary input to the handoff document |
| `design-system-doc.md` | Reusable components get promoted to design system documentation |
| `microcopy-doc.md` | Copy requirements in the spec link to the microcopy doc |
| `design-qa-checklist.md` | The state inventory becomes the QA checklist |

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
