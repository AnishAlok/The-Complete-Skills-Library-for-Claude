# onboarding-flow-spec.md

> **Skill:** Produces a complete onboarding flow specification covering the steps, UI design, copy, progress indicators, skip logic, activation milestones, and success metrics for a product onboarding experience.

---

## TLDR

This skill helps you answer: *"What exact experience should new users have from signup to first value, and how do we make sure they get there?"* It produces a complete onboarding flow spec covering each step's purpose, UI, copy, and logic, along with activation milestones and measurement criteria. Used when designing or redesigning a new user onboarding experience.

---

## Topic Explanation

### The Activation Milestone

The single most important concept in onboarding design is the activation milestone: the specific moment when a new user first experiences the core value of the product. Until activation, the user has not yet decided whether the product is for them. After activation, retention probability increases significantly.

Onboarding must be designed backward from the activation milestone:
1. Define the activation milestone precisely (the "aha moment")
2. Identify the minimum steps required to reach it
3. Remove every step that is not required to reach it
4. Design each step to motivate progress to the next one

The most common onboarding failure is requiring users to complete too much before they reach activation. Every setup step added before first value is a conversion risk.

### Onboarding Patterns

**Empty state onboarding:** No explicit onboarding flow. Users land in the product, see empty states with clear calls to action. Low friction, high abandonment for complex products.

**Checklist onboarding:** A persistent checklist of setup tasks users can complete in any order. Good for products with multiple independent setup dimensions.

**Progressive onboarding:** Features are introduced in context as users encounter them, rather than upfront. Best for complex products with high learning curves.

**Wizard onboarding:** A linear step-by-step flow that guides users through setup before accessing the product. Best for products where setup is required before the product is useful.

Most products combine patterns: a short wizard for critical setup, empty states with guidance for secondary features.

---

## Output Format

```
1. ONBOARDING STRATEGY
   Activation milestone: the precise definition of first value.
   Onboarding pattern selected and rationale.
   Minimum steps to activation.
   What can be deferred until after first activation.

2. STEP-BY-STEP FLOW SPECIFICATION
   For each step:
   - Step name and number
   - Purpose: what must be accomplished here and why
   - Required vs. optional: can this step be skipped?
   - UI description: layout, components, key visual elements
   - Copy: heading, body, CTA label, helper text
   - Input requirements: what the user must provide
   - Validation: what is checked and error states
   - Skip behavior: where skipping leads and what is defaulted
   - Progress indicator state

3. SKIP AND DEFER LOGIC
   Which steps can be skipped.
   What happens to skipped steps (deferred, defaulted, prompted later).
   How deferred items are surfaced after onboarding.

4. PROGRESS INDICATION
   How progress is communicated to the user.
   Number of steps shown vs. hidden.
   Whether total steps are shown upfront.

5. ACTIVATION MILESTONE DESIGN
   The specific screen or moment that represents first value.
   How it is designed to feel rewarding.
   What happens immediately after.

6. POST-ONBOARDING EXPERIENCE
   What the product looks like after onboarding is complete.
   Any follow-up guidance or tooltips for the first session.

7. COPY INVENTORY
   All headings, body copy, CTA labels, helper text, and error messages.
   Reference to microcopy doc.

8. MEASUREMENT AND SUCCESS CRITERIA
   Onboarding completion rate target.
   Activation rate target (% reaching activation milestone).
   Time-to-activation target.
   Drop-off points to monitor.
```

---

## Starter Prompt

```
You are a UX designer writing an onboarding flow specification.

Product: [what the product does]
User type: [who is going through onboarding]
Activation milestone: [the moment of first value you are designing toward]
Required setup steps: [what the user must do before the product is useful]
Optional setup steps: [what can be deferred]
Onboarding pattern: [wizard / checklist / progressive / combination]
Copy guidelines: [voice, tone, and writing principles to follow]
Success metrics: [how onboarding success is measured]

Produce a complete onboarding flow spec including strategy, step-by-step specs
with purpose and copy for each step, skip and defer logic, progress indication,
activation milestone design, and measurement criteria.
```

---

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
