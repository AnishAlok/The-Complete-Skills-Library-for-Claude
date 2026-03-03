# positioning-doc.md

> **Skill:** Produces a product positioning document that defines how the product occupies a distinct place in the target customer's mind, what category it owns, and why it wins against alternatives.

---

## TLDR

Positioning is the act of defining how a product occupies a specific, differentiated place in the mind of the target customer. A positioning document is the internal strategic foundation that all external marketing is built on: category, target customer, value frame, differentiation, and competitive comparison. If the positioning is wrong, everything built on top of it is wrong.

---

## Topic Explanation

### April Dunford's Positioning Framework

The most rigorous modern positioning framework (April Dunford, Obviously Awesome) defines positioning through five components:

**Competitive alternatives:** What would customers do if your product did not exist? The real competitive set includes direct competitors, indirect alternatives, and doing nothing. Positioning is always relative to alternatives, never absolute.

**Unique attributes:** What does your product have or do that alternatives genuinely cannot? Must be factual, not subjective. Not "better UX" but "the only solution with native integration to [system X]."

**Value:** What is the business outcome those unique attributes deliver? Attributes are features; value is what those features mean for the customer's business. Not "real-time sync" but "your team always works from current data, eliminating the coordination errors that cost X hours per week."

**Target market characteristics:** Who cares most about that value? The segment for whom the unique attributes deliver the highest payoff. Positioning is not for everyone — it is for the buyers who will appreciate it most.

**Market category:** What frame of reference helps the buyer understand what the product is and why they should care? Category choice is a strategic decision that determines who you compete with and how you get evaluated.

### Category Creation vs. Category Entry

Entering an existing category: the buyer knows the problem and is evaluating options. Easier to sell into because buyers understand the need; harder to differentiate because you are competing on identical criteria.

Creating a new category: the product solves a problem buyers did not know they had, or reframes an existing problem. Salesforce did not position as "better Siebel" on day one; it positioned as "software as a service," which changed the evaluation criteria entirely.

---

## Dos

- **Do root unique attributes in facts, not feelings.** Claims that cannot be verified are not positioning. Claims that can be demonstrated in a proof of concept or customer reference are.
- **Do distinguish between table stakes and differentiators.** Security, reliability, and support are expected by buyers. They are only differentiators when you are dramatically better than all alternatives — and even then, rarely the primary reason to buy.
- **Do test the positioning statement with real customers.** If customers do not recognize themselves in the target segment description or the problem statement, the positioning has missed.

---

## Donts

- **Dont use positioning language that every competitor also uses.** "Easy to use," "powerful," "flexible," and "scalable" appear in every competitor's positioning. They communicate nothing.
- **Dont let the engineering team write the positioning.** Features are not positioning. The translation from "what it does" to "why it matters to this specific buyer" is the PMM's job.

---

## Output Format

```
1. POSITIONING DOCUMENT HEADER
   Product, version, date, PMM owner. Review cadence and next review date.

2. COMPETITIVE ALTERNATIVES
   What customers do today without this product.
   For each alternative:
   - Description of the approach
   - Why customers currently choose it
   - Its key weaknesses from the target customer's perspective

3. UNIQUE ATTRIBUTES
   What the product has or does that alternatives cannot.
   Each must be factual and demonstrable, not a subjective claim.

   | Attribute | Why alternatives cannot easily replicate it |

4. VALUE TRANSLATION
   For each unique attribute: the specific business outcome it delivers.
   "Because [attribute], customers achieve [specific outcome]."

5. TARGET MARKET CHARACTERISTICS
   Specific firmographic and behavioral characteristics of buyers who value the attributes most.
   Why this segment values the product more than adjacent segments.

6. MARKET CATEGORY
   The category the product competes in and why it was chosen.
   Who the product is compared against in this frame.
   Categories considered and rejected with reasoning.

7. POSITIONING STATEMENT
   For: [target customer description]
   Who: [has this specific, named problem]
   [Product name] is a [market category]
   That: [delivers this primary value]
   Unlike: [the primary alternative]
   [Product name]: [key differentiator stated as observable fact]

8. PROOF POINTS
   Evidence supporting each positioning claim.
   Customer quotes, case study data, third-party validation.

9. WHAT THIS PRODUCT IS NOT
   Claims explicitly not made. Things this product does not claim to be.
   Prevents positioning drift across teams.

10. POSITIONING VALIDATION STATUS
    How this positioning was tested.
    Customer feedback received on the positioning.
    Win/loss data supporting or challenging it.
    Open questions still under investigation.
```

---

## Starter Prompt

```
You are a product marketing manager developing a positioning document.

Product: [name and what it does]
Competitive alternatives: [what customers use or do today instead]
Unique attributes: [what the product does that alternatives genuinely cannot]
Target customer: [the specific segment who values the product most]
Category choice: [what category the product will compete in]
Known proof points: [customer data, quotes, or case study results available]

Produce a complete positioning document using the Dunford five-component framework.
Unique attributes must be factual and demonstrable, not subjective claims.
The positioning statement must follow the standard format exactly.
Flag any attribute a well-funded competitor could replicate within 12 months.
```

---

## Related Skills

| Use This Before | Why |
|---|---|
| `gtm-strategy.md` | GTM strategy informs the positioning decisions made here |

| Use This Next | Why |
|---|---|
| `messaging-framework.md` | Positioning is the foundation for all messaging work |
| `competitive-battlecard.md` | Positioning competitive comparisons feed each battlecard |

*Skill file version: 1.0 | Phase: 08 - Product Marketing | Company type: Product*
