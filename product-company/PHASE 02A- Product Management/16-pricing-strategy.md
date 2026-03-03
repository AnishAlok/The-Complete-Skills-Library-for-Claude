# pricing-strategy.md

> **Skill:** Produces a pricing strategy analysis covering pricing model options, value metric selection, tier design, price point analysis, and pricing change communication for a SaaS or subscription product.

---

## TLDR

This skill helps you answer: *"What should we charge, how should we structure the pricing, and how do we change it without damaging customer relationships?"* It produces a pricing strategy document covering model selection, value metric analysis, tier architecture, and competitive pricing context. Used when launching a new product, redesigning pricing, or evaluating a pricing change.

---

## Topic Explanation

### The Value Metric

The most important pricing decision is the value metric: what the price scales with as the customer gets more value. A good value metric:
- Increases as customers get more value
- Is easily understood by customers
- Is measurable and auditable
- Aligns cost with value received

Common SaaS value metrics: per seat (users), per usage (API calls, transactions), per outcome (revenue processed, compliance reports), per asset (locations, employees, properties).

Seat-based pricing is simple to understand but misaligns when value comes from automation, not user count. Usage-based pricing aligns perfectly with value but creates revenue unpredictability and makes it harder to close deals.

### Pricing Model Options

**Per seat / user:** Price scales with number of users. Simple, predictable, common. Misaligns when value is in volume of work processed rather than users.

**Usage-based:** Price scales with consumption. Best value alignment. Revenue unpredictability. Customers worry about runaway bills.

**Tiered (feature-based):** Good / Better / Best packages. Predictable for customer. Requires disciplined packaging decisions. Risk of artificial tier barriers.

**Flat rate:** One price for everything. Simple but leaves significant revenue on the table from high-value customers.

**Hybrid:** Flat base + usage. Increasingly common. Provides floor revenue and scales with value.

### Willingness to Pay Research

Pricing decisions not grounded in willingness to pay research are guesses. Key methods:
- **Van Westendorp Price Sensitivity Meter:** Four survey questions that reveal acceptable price range
- **Conjoint analysis:** Quantitative method for trading off features and price
- **Sales conversation mining:** What customers say when discussing pricing in deals
- **Win/loss analysis:** When is price a genuine factor in competitive losses?

---

## Output Format

```
1. PRICING STRATEGY CONTEXT
   What is being priced and for whom.
   The strategic goals pricing must serve (growth, revenue expansion, competitive position).

2. VALUE METRIC ANALYSIS
   Options evaluated for the value metric.
   For each option: alignment with value, customer comprehension, measurability.
   Recommended value metric with rationale.

3. PRICING MODEL RECOMMENDATION
   Model options evaluated.
   Recommendation with rationale.
   How the model aligns with the value metric.

4. TIER ARCHITECTURE
   Number of tiers and rationale.
   For each tier:
   - Name
   - Target customer
   - Key features / inclusions
   - Price
   - The upgrade trigger (what makes a customer need the next tier)

5. PRICE POINT ANALYSIS
   Willingness to pay research findings.
   Competitive pricing context.
   Unit economics: what price point supports target margins.
   Recommended price points with confidence level.

6. FREEMIUM / FREE TRIAL ANALYSIS (if applicable)
   Whether a free tier or trial is warranted.
   Free tier scope: what is free and what is the conversion path.
   Free-to-paid conversion benchmarks and targets.

7. PACKAGING DECISIONS
   What is bundled vs. add-on.
   Feature packaging logic: what drives tier differentiation.
   Add-on candidates.

8. PRICING CHANGE COMMUNICATION (if updating existing pricing)
   Grandfathering policy.
   Notice period.
   Customer communication approach.
   Risk: potential churn from the change.

9. METRICS AND MONITORING
   How pricing effectiveness will be measured.
   LTV, ARPU, and tier distribution targets.
   Signals that would prompt pricing reassessment.
```

---

## Starter Prompt

```
You are a product manager developing a pricing strategy.

Product: [what is being priced]
Customer segments: [who buys and the range of value they get]
Value delivered: [how customers get value from the product]
Competitive pricing: [what competitors charge and how they structure pricing]
Current pricing (if updating): [existing model and its problems]
Business goals: [what pricing must achieve for the business]
Willingness to pay data: [any research on what customers will pay]

Produce a complete pricing strategy document covering value metric selection,
model recommendation, tier architecture with upgrade triggers,
price point analysis, and packaging decisions.
If this is a pricing change, include communication strategy.
```

---

*Skill file version: 1.0 | Phase: 02 - Product Management | Company type: Product*
