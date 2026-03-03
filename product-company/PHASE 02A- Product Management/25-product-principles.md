# product-principles.md

> **Skill:** Produces a product principles document that defines the core beliefs guiding product decisions, with specific examples of how each principle is applied and what it rules out.

---

## TLDR

Product principles are the beliefs that guide decision-making when data, frameworks, and stakeholder opinions are all pointing in different directions. Unlike strategy (which changes with market conditions) or roadmaps (which change frequently), principles should be durable. This skill produces a set of product principles with applications and counter-examples that make them genuinely actionable.

---

## Topic Explanation

### Product Principles vs. Design Principles vs. Company Values

**Company values:** Describe the character of the organization and how people treat each other. "Integrity," "customer-first." Apply broadly to all functions.

**Product principles:** Describe how the product team makes decisions about the product. "We build for the operator, not the investor" or "default to simplicity." Apply specifically to product decisions.

**Design principles:** Describe how design decisions are made. "Clarity before delight." Apply specifically to design.

All three are needed. Product principles are the middle layer: they translate company values into product-specific decision guidance.

### What Makes a Product Principle Useful

The same test as design principles applies: a useful product principle resolves a real product debate. "We build for users" does not resolve any debate. "When the needs of our power users and new users conflict, we optimize for new users first" resolves every new-user vs. power-user debate.

The most valuable product principles are often the uncomfortable ones: the ones that make an explicit choice that not everyone agrees with. "We do not build features that benefit a single customer no matter how large that customer is" is uncomfortable and useful. "We build features customers ask for" is comfortable and useless.

### Principles Hierarchy

Product principles can be tiered:

**Core principles:** The non-negotiable beliefs that define the product. Very rarely change.

**Operating principles:** How the team works and makes decisions day-to-day. May evolve as the team and product mature.

**Anti-principles:** What the product explicitly is not. Often the most useful for avoiding feature and scope creep.

---

## Output Format

```
1. INTRODUCTION
   Why these principles exist.
   Who they apply to.
   How to use them when making decisions.

2. CORE PRODUCT PRINCIPLES (5 to 7)
   For each principle:
   - Name: 2 to 5 words, memorable
   - Statement: one clear sentence
   - What it means: explanation of the belief behind the principle
   - In practice: a specific real or hypothetical product decision this guides
   - What it rules out: a specific decision or direction this principle prevents
   - In tension with: what other principle or value this must be balanced against

3. ANTI-PRINCIPLES
   What this product explicitly is not.
   What we will not build even if we could.
   Why.

4. WHEN PRINCIPLES CONFLICT
   How to resolve conflicts between principles.
   The priority order when two principles point in different directions.

5. PRINCIPLES REVIEW
   How frequently principles are reviewed.
   How to propose a principle change.
   What evidence would justify changing a principle.
```

---

## Starter Prompt

```
You are a product leader writing a product principles document.

Product type and user: [what the product does and who it serves]
Recurring product debates: [decisions the team debates regularly]
What the product must never sacrifice: [the non-negotiables]
What makes this product different: [the distinctive choices it makes]
Company values to express in product: [relevant company values to ground in]

Produce 5 to 7 product principles, each with name, statement, explanation,
in-practice application, what it rules out, and tension notes.
Include an anti-principles section and a conflict resolution framework.
Principles should be specific enough to resolve real product debates.
```

---

## Related Skills

| Use This Next | Why |
|---|---|
| `product-strategy-doc.md` | Strategy is informed by principles |
| `feature-prioritization.md` | Principles become criteria in prioritization |
| `design-principles-doc.md` | Product principles and design principles should be coherent |

*Skill file version: 1.0 | Phase: 02 - Product Management | Company type: Product*
