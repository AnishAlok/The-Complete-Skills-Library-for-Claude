# design-principles-doc.md

> **Skill:** Produces a team design principles document that defines how design decisions are made, what the design stands for, and how tradeoffs are resolved when values are in tension.

---

## TLDR

Design principles are the values that guide design decision-making. Good principles are specific enough to actually resolve design debates, not so abstract that they could apply to any product. This skill produces a design principles document with principles, explanations, examples, and anti-examples that make the principles actionable.

---

## Topic Explanation

### What Makes a Design Principle Useful

The test of a design principle is whether it can resolve a design debate. "Be useful" is not a useful principle. Every designer believes they are being useful. "Show users only what they need for the task at hand, nothing more" resolves a specific category of debate: do we show this additional context or not?

Characteristics of a useful design principle:
- **Specific enough to rule things out.** If the principle would not rule out any design decision, it is not a principle.
- **Controversial enough that the opposite is defensible.** If no one would disagree with the principle, it is not making a real choice.
- **Prioritized.** When two principles conflict, which wins? Explicitly ranked principles are far more useful than unordered principles.

### Principle Format

Each principle should have:
- A memorable name (2 to 5 words)
- A one-sentence statement
- An explanation of what it means and why
- A "do" example: a design decision this principle supports
- A "don't" example: a design decision this principle rules out
- An "in tension with" note: what the principle must be balanced against

### How Many Principles

3 to 7 principles is the optimal range. Below 3, principles are too broad to be useful. Above 7, principles cannot all be held in mind simultaneously and the list becomes decorative rather than functional.

---

## Output Format

```
1. INTRODUCTION
   What these principles are for.
   Who they apply to.
   How to use them when making design decisions.

2. PRINCIPLES (3 to 7)
   For each principle:
   - Name (memorable 2 to 5 word label)
   - Statement (one clear sentence)
   - Explanation (why this matters for this product and this user)
   - In practice: what this looks like in real design decisions
   - Do example: a specific design decision this principle supports
   - Don't example: a specific design decision this principle rules out
   - In tension with: what principle or value this must be balanced against

3. PRIORITY ORDER
   When principles conflict, which takes precedence?
   Example: "Clarity before delight. When a charming interaction reduces clarity, clarity wins."

4. HOW TO USE THESE PRINCIPLES
   In design critique: how to invoke principles as critique evidence.
   In design review: which principles to check against.
   When principles conflict: how to document the tradeoff and decision.

5. PRINCIPLES CHANGELOG
   Version history.
   How to propose principle changes.
```

---

## Starter Prompt

```
You are a design leader writing a design principles document for a product team.

Product type and user: [what the product does and who it serves]
Current design debates: [recurring disagreements or tensions the team faces]
What the product should never sacrifice: [the non-negotiables]
What differentiates this product's design: [what should make it distinct]
Product stage: [early / growth / mature - affects what principles are relevant]

Produce 3 to 7 design principles, each with name, statement, explanation,
do and don't examples, and in-tension notes.
Principles should be specific enough to resolve real design debates.
Include a priority ordering for when principles conflict.
```

---

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
