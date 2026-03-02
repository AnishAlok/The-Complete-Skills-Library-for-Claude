# business-model-canvas.md

> **Skill:** Generates a fully completed Business Model Canvas (BMC) and Lean Canvas for a product or business idea, with structured prompts for each block and strategic analysis of the overall model.

---

## TLDR

This skill helps you answer: *"How does our business actually work as a system, and is it coherent?"* It produces a completed Business Model Canvas and/or Lean Canvas by walking through each building block with depth, identifying gaps and tensions in the model, and surfacing strategic questions the model raises. Used for early-stage business design, investor preparation, strategy reviews, and pivots.

---

## Topic Explanation

### What Is the Business Model Canvas?

The Business Model Canvas (BMC) is a strategic management tool created by Alexander Osterwalder and Yves Pigneur, introduced in their 2010 book *Business Model Generation*. It visualizes the entire logic of a business on a single page using nine interconnected building blocks.

The BMC forces a team to articulate not just what they build, but how they create value, deliver it, capture it, and sustain the economics that make it all work. It is most useful when treated as a thinking tool, not a form to fill out.

### The Nine Building Blocks of the BMC

**1. Customer Segments**
Who are the specific groups of people or organizations you are creating value for? The BMC forces you to be specific. "Small businesses" is not a segment. "US-based e-commerce merchants with $1M to $10M annual revenue selling on Shopify" is a segment.

Key questions:
- Who are your most important customers?
- Are you serving one segment or multiple distinct segments with different needs?
- Are there mass market, niche market, segmented, diversified, or multi-sided platform dynamics at play?

**2. Value Propositions**
What bundle of products and services creates value for each customer segment? What pain do you relieve or what gain do you create?

Key questions:
- What problems are you solving?
- What customer jobs are you helping get done?
- What makes your value proposition different from alternatives?
- Is the value primarily about performance, customization, cost reduction, risk reduction, accessibility, or convenience?

**3. Channels**
How do you reach your customer segments to deliver your value proposition? Channels cover awareness, evaluation, purchase, delivery, and post-sale.

Key questions:
- How do customers want to be reached?
- Which channels work best and are most cost-efficient?
- Are your channels owned (direct sales, website) or partner (resellers, marketplaces)?
- How are channels integrated across the customer journey?

**4. Customer Relationships**
What type of relationship does each customer segment expect? Relationships range from highly personal to fully automated.

Key questions:
- What kind of relationship have you established with each segment?
- How costly is each relationship type?
- How do relationships affect acquisition, retention, and upsell?
- Types include: personal assistance, dedicated personal assistance, self-service, automated services, communities, co-creation.

**5. Revenue Streams**
For what value is each customer segment truly willing to pay? How do they prefer to pay?

Key questions:
- What are customers currently paying for? What are they paying for alternatives?
- What would they be willing to pay for and in what form?
- Revenue types: asset sale, usage fee, subscription, licensing, brokerage/commission, advertising, freemium.
- What is the pricing mechanism: fixed, dynamic, auction, market, volume-dependent?

**6. Key Resources**
What assets are required to deliver your value proposition, maintain channels, keep customer relationships, and earn revenue?

Key questions:
- What physical, intellectual, human, or financial resources do you need?
- Which resources are you building vs. buying vs. partnering for?
- Which resources are genuinely proprietary and defensible?

**7. Key Activities**
What are the most important things your company must do to make the business model work?

Key questions:
- What activities are required to deliver your value proposition?
- What activities are required for your channels, customer relationships, and revenue streams?
- Are your activities primarily production, problem-solving, or platform/network management?

**8. Key Partnerships**
Who are the key partners and suppliers that make the business model work?

Key questions:
- Who are your key suppliers?
- Which key resources do you acquire from partners?
- Which key activities do partners perform?
- What motivates partnerships: optimization and economy, reduction of risk, acquisition of particular resources or activities?

**9. Cost Structure**
What are the most important costs inherent in the business model?

Key questions:
- What are the most expensive key resources, activities, and partnerships?
- Is the business more cost-driven or value-driven?
- What are the fixed costs, variable costs, and economies of scale or scope?

### The Lean Canvas

The Lean Canvas, created by Ash Maurya as an adaptation of the BMC for early-stage startups, replaces four blocks with more founder-relevant ones:

| BMC Block Replaced | Lean Canvas Replacement |
|---|---|
| Key Partners | Problem |
| Key Activities | Solution |
| Key Resources | Key Metrics |
| Customer Relationships | Unfair Advantage |

The Lean Canvas is better suited to pre-product or early-stage companies where the business model is still being validated. The BMC is better suited to companies with an established or clearer business model.

### Business Model Patterns

Osterwalder identified recurring business model patterns. Recognizing which pattern your business follows helps stress-test and strengthen the model:

- **Unbundling:** Separating customer relationship, product innovation, and infrastructure businesses
- **The Long Tail:** Offering many niche products, each in small volume (e.g., Spotify, App Store)
- **Multi-sided Platforms:** Serving two or more interdependent customer segments (e.g., Airbnb, Uber)
- **Free/Freemium:** One segment subsidizes another (e.g., free users monetized via premium or advertising)
- **Open Business Model:** Collaborating externally to create and capture value (e.g., open source with enterprise tier)

---

## When to Use This Skill

Use when:
- Designing a new business or product from scratch and needing to think through the full model
- Evaluating a pivot and needing to compare the current model against a proposed new one
- Preparing an investor pitch and needing to explain the business logic clearly and completely
- Running a strategy session with a leadership team to stress-test the current model
- Onboarding a new executive who needs to understand how the business creates and captures value
- Identifying which parts of the business model are weak, unvalidated, or missing
- Comparing two or more business model options before committing to one

Do NOT use when:
- You need a detailed financial model (use `financial-model-doc.md`)
- You need a competitive positioning document (use `positioning-doc.md`)
- You need a product roadmap (use `product-roadmap.md`)
- You need a detailed go-to-market plan (use `gtm-strategy.md`)

---

## Dos

- **Do treat it as a hypothesis map, not a completed document.** Every block should be labeled with your current confidence level. Unknown or untested blocks are as important to surface as completed ones.
- **Do complete customer segments and value proposition first.** Everything else flows from who you serve and what value you create for them. Starting with revenue or cost structure is backwards.
- **Do be painfully specific in every block.** "Enterprise customers" is not a segment. "Our channel is digital" is not a channel description. Vagueness in the canvas signals vagueness in the strategy.
- **Do check for internal coherence.** Each block should logically support the others. A mismatch, for example a high-touch enterprise value proposition paired with a self-serve only channel, is a tension that must be resolved.
- **Do identify the riskiest assumption.** Once the canvas is complete, explicitly name the one assumption that, if wrong, would break the entire business model.
- **Do build separate canvases for distinct customer segments.** If you serve two very different customer types, they likely have different value propositions, channels, and relationship types. One canvas cannot represent both accurately.
- **Do use it as a living document.** The canvas should be reviewed and updated quarterly as you learn more from customers and the market.
- **Do compare your canvas to your competitors' implied canvases.** Reverse-engineering a competitor's business model onto a canvas reveals structural differences and potential advantages.

---

## Donts

- **Dont fill it in as a formality.** A canvas completed in 20 minutes to satisfy a process requirement is worthless. The value comes from the thinking and debate each block forces.
- **Dont use it only for communication.** The BMC is often used only to explain a business to outsiders. Its higher value is as an internal stress-testing and alignment tool.
- **Dont ignore the cost and revenue blocks.** Many product-focused teams fill in the top half of the canvas (value, channels, segments) and rush through the bottom half (costs, revenue). The economic logic of the model lives in those blocks.
- **Dont confuse activities with resources.** Activities are things you do. Resources are things you have or build. This distinction matters because activities require ongoing capacity while resources can be acquired once.
- **Dont list every possible partner.** Key partners are only the ones without whom the business model would not function. Listing every vendor or tool as a partner dilutes the strategic clarity.
- **Dont skip the Lean Canvas if you are pre-product.** The BMC assumes more certainty than a pre-product startup has. Use Lean Canvas until you have validated your problem, customer, and solution.
- **Dont treat it as finished.** A completed canvas is the beginning of a validation agenda, not the end of a design process.

---

## Ideal Inputs

### Required
```
1. BUSINESS OR PRODUCT DESCRIPTION
   What does your business do? What product or service do you offer?

2. TARGET CUSTOMER
   Who are you building this for? Be as specific as possible about
   the customer segment(s).

3. CORE VALUE PROPOSITION
   What problem do you solve or what gain do you create?
   How is that different from what exists today?

4. STAGE OF BUSINESS
   Pre-idea / pre-product / MVP / launched / scaling?
   This determines whether BMC or Lean Canvas is more appropriate.

5. CANVAS TYPE PREFERENCE
   BMC, Lean Canvas, or both?
```

### Optional but Valuable
```
6. KNOWN REVENUE MODEL
   How do you currently charge or plan to charge?

7. CURRENT CHANNELS
   How do you reach or plan to reach customers?

8. KEY ASSUMPTIONS YOU WANT TO TEST
   What are the parts of the model you are least certain about?

9. COMPETITOR BUSINESS MODELS
   Who are your key competitors and how do they make money?
   Useful for comparison and differentiation.

10. PURPOSE OF THE CANVAS
    Investor pitch? Internal alignment? Pivot evaluation?
    Strategy offsite? This shapes how much analysis to include.
```

### Example of a Strong Input Prompt
```
Business: Marketplace connecting independent financial advisors with
compliance and back-office services on demand
Target customer: Independent RIAs (Registered Investment Advisors) with 1 to 5 staff,
managing $50M to $500M in AUM, currently handling compliance manually or with a single hire
Core value proposition: Get enterprise-grade compliance infrastructure without hiring a
full-time compliance officer
Stage: 8 paying customers, pre-Series A
Canvas type: Both BMC and Lean Canvas
Revenue model: Monthly SaaS fee per advisor plus per-filing fees
Key unknowns: Whether advisors will pay for this vs. hiring in-house,
and what our unfair advantage is vs. general compliance consultants
Purpose: Series A investor preparation
```

---

## Output Format

```
1. LEAN CANVAS (if pre-product or early stage)
   All nine blocks completed with specific, non-generic content:
   - Problem (top 3 problems for your customer)
   - Customer Segments (early adopter definition)
   - Unique Value Proposition (single clear message)
   - Solution (top 3 features)
   - Channels
   - Revenue Streams and pricing
   - Cost Structure
   - Key Metrics
   - Unfair Advantage

2. BUSINESS MODEL CANVAS (if post-launch or for investor use)
   All nine blocks completed:
   - Customer Segments
   - Value Propositions
   - Channels
   - Customer Relationships
   - Revenue Streams
   - Key Resources
   - Key Activities
   - Key Partnerships
   - Cost Structure

3. INTERNAL COHERENCE CHECK
   Analysis of how well the nine blocks fit together.
   Specific tensions or mismatches identified and flagged.

4. RISKIEST ASSUMPTIONS
   Top 3 assumptions in the model that, if wrong, break the business.
   Each with a suggested validation method.

5. BUSINESS MODEL PATTERN IDENTIFICATION
   Which of Osterwalder's patterns does this model follow?
   What does that pattern tell us about scaling dynamics and risks?

6. STRATEGIC QUESTIONS RAISED
   The 5 to 7 most important unanswered questions the canvas surfaces
   that the team needs to resolve.

7. COMPARISON CANVAS (if competitor or alternative model provided)
   Side-by-side analysis of your model vs. the comparison.
   Key differences and strategic implications noted.
```

---

## Starter Prompt

```
You are a business model strategist helping me build and analyze a Business Model Canvas
and Lean Canvas for my business.

Business description: [what your business does]
Target customer: [who you serve, as specifically as possible]
Core value proposition: [the problem you solve or gain you create]
Stage: [pre-product / MVP / launched / scaling]
Current revenue model: [how you charge or plan to charge]
Current channels: [how you reach customers]
Key unknowns: [the parts of the model you are least certain about]
Competitors and their models: [how key competitors make money]
Purpose: [investor pitch / internal alignment / pivot evaluation / strategy session]

Please produce:
1. A completed Lean Canvas with all nine blocks filled in specifically (not generically)
2. A completed Business Model Canvas with all nine blocks filled in
3. An internal coherence check identifying tensions or mismatches between blocks
4. The top 3 riskiest assumptions in the model with suggested validation methods
5. The business model pattern this most closely follows and what that implies
6. The 5 most important strategic questions this canvas raises that we need to answer

Be direct. If a block is vague or under-developed, say so and ask for more input.
If the model has a structural problem (e.g., the cost structure does not support the
pricing model), flag it explicitly.
```

---

## Related Skills

| Use This Next | Why |
|---|---|
| `market-opportunity-analysis.md` | Validate that the customer segments in your canvas represent a large enough market |
| `product-strategy-doc.md` | Translate the value proposition block into a product strategy |
| `gtm-strategy.md` | Develop the channels block into a full go-to-market plan |
| `pricing-strategy.md` | Develop the revenue streams block into a full pricing model |
| `investment-thesis.md` | Use the canvas to structure the business logic section of an investor memo |

| Use This Before | Why |
|---|---|
| `customer-discovery-interview.md` | Validate your customer segment and value proposition assumptions with real conversations |
| `jobs-to-be-done.md` | JTBD interviews strengthen the value proposition and customer segment blocks |

---

## Reference Frameworks

| Framework | Use For |
|---|---|
| Business Model Canvas (Osterwalder) | Established business or investor-facing model documentation |
| Lean Canvas (Ash Maurya) | Pre-product or early-stage model with high uncertainty |
| Value Proposition Canvas | Deep-diving the value proposition block with customer jobs, pains, and gains |
| Business Model Patterns (Osterwalder) | Identifying which scaling archetype your model follows |
| Jobs-to-be-Done (Christensen) | Anchoring value propositions in customer outcome language |

---

*Skill file version: 1.0 | Phase: 01 - Ideation and Market Research | Company type: Product*
