# mvp-definition.md

> **Skill:** Produces an MVP (Minimum Viable Product) definition that scopes the smallest version of a feature or product that can test the core hypothesis and deliver real value to users.

---

## TLDR

An MVP definition is not a scope-cutting exercise. It is a precision instrument for identifying the minimum set of capabilities that tests the most important hypothesis while delivering genuine user value. This skill produces an MVP scope with hypothesis, inclusions, exclusions, and success criteria.

---

## Topic Explanation

### What MVP Actually Means (and What It Does Not)

Eric Ries's original definition: "A Minimum Viable Product is that version of a new product which allows a team to collect the maximum amount of validated learning about customers with the least effort."

The key word is "validated learning." An MVP is not:
- The cheapest possible thing to build
- A buggy half-feature released without confidence
- "Version 1.0" with everything cut

An MVP is the minimum that allows learning whether the core hypothesis is correct.

### The MVP Is Defined by the Hypothesis

The right MVP scope is determined by the hypothesis it is testing. If the hypothesis is "restaurant operators will pay for automated compliance monitoring," the MVP must include enough automation to make the value real, but does not need every compliance category, every report format, or every integration.

If the MVP cannot test the hypothesis, it is not a valid MVP. It is just a small version of something.

### The Concierge MVP

A useful concept: the concierge MVP delivers value through manual human effort rather than building the automated system. If restaurant operators need compliance reports, a concierge MVP has a human analyst review payroll and produce the report manually. This tests whether operators value the output without building the automation.

Concierge MVPs are under-used. They test desirability without any technical investment and produce rich customer insight.

---

## Output Format

```
1. MVP CONTEXT
   What is being built.
   The stage in product development: new product, new feature, major redesign.

2. THE HYPOTHESIS BEING TESTED
   The core assumption this MVP will validate or invalidate.
   How the MVP tests it.

3. MVP SCOPE: WHAT IS INCLUDED
   The specific capabilities included.
   For each: what it does and why it is necessary to test the hypothesis.

4. MVP SCOPE: WHAT IS EXPLICITLY EXCLUDED
   Features and capabilities that are out of scope.
   For each: why it is not needed to test the hypothesis.
   When it would be considered (Post-MVP phases).

5. MVP DESIGN PRINCIPLES
   The quality standard: what "good enough" looks like for an MVP.
   The known shortcuts being taken and their acceptable consequences.

6. USER EXPERIENCE STANDARD
   What experience MVP users should expect.
   What they should not experience: tolerability thresholds.

7. SUCCESS CRITERIA
   What outcomes would confirm the hypothesis.
   What outcomes would disconfirm it.
   The measurement approach.
   The timeline for evaluation.

8. POST-MVP ROADMAP SIGNAL
   What the MVP will teach that shapes the post-MVP roadmap.
   Decisions that are deferred until MVP learning is complete.
```

---

## Starter Prompt

```
You are a product manager defining the MVP for a new feature or product.

What is being built: [the feature or product]
The hypothesis: [the core assumption being tested]
Full ideal scope: [everything that could eventually be built]
Timeline constraint: [when the MVP must ship]
Team capacity: [available development resources]
User experience floor: [minimum acceptable quality]

Produce an MVP definition with explicit inclusions and exclusions.
Every inclusion should be justified by its necessity to test the hypothesis.
Every exclusion should note when it would be considered (post-MVP phases).
Flag if the proposed MVP scope cannot actually test the stated hypothesis.
```

---

*Skill file version: 1.0 | Phase: 02 - Product Management | Company type: Product*
