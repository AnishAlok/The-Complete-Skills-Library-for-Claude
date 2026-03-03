# gtm-strategy.md

> **Skill:** Produces a go-to-market strategy document that defines how a product will reach its target market, achieve adoption, and generate revenue through coordinated positioning, channel, and launch decisions.

---

## TLDR

A GTM strategy answers: "How will we bring this product to market and win?" It defines the target customer, the value proposition, how the product positions against alternatives, which channels reach buyers, how revenue is generated, and what success looks like at 90 days and one year. Used before a major product launch, a new market entry, or a significant product pivot.

---

## Topic Explanation

### GTM Strategy vs. Marketing Plan

GTM strategy: the foundational decisions about who you are selling to, why they should buy, and how you will reach them. Strategic and relatively stable for the duration of a launch cycle.

Marketing plan: the execution plan implementing the GTM strategy. Campaigns, content calendar, channel budgets, timelines. Tactical and frequently changing.

The GTM strategy must be decided before the marketing plan is written. A marketing plan without a GTM strategy is activity without direction.

### The Three Core GTM Questions

Every GTM strategy must answer three questions precisely:

**Who:** The specific target customer. Not "SMBs" but "operations leads at logistics companies with 50 to 500 employees running manual route planning." The more specific the ICP, the more resonant the messaging.

**Why us:** The differentiated value proposition. Why this customer should choose this product over every available alternative, including doing nothing.

**How:** The go-to-market motion. Product-led growth, sales-led, partner-led, or a combination. The motion determines which channels, which team investments, and which success metrics matter most.

### GTM Motions

**Product-led growth (PLG):** The product itself drives acquisition, expansion, and retention through a free trial or freemium model. Requires a product that delivers value quickly without heavy onboarding.

**Sales-led:** A revenue team drives acquisition through outbound prospecting, inbound qualification, and managed sales cycles. Appropriate for high-ACV deals with complex evaluation processes.

**Partner-led:** Distribution through channel partners, resellers, or integrations. Appropriate when partners already have trusted relationships with the target buyer.

Most modern B2B products use a hybrid: PLG for self-serve adoption plus a sales motion for expansion and enterprise accounts.

---

## Dos

- **Do define the ICP with enough specificity to use as a targeting filter.** "Mid-market B2B companies" is not an ICP. "VP of Engineering at SaaS companies with 100 to 500 employees who have shipped at least one major product in the last 24 months" is.
- **Do decide the GTM motion before designing channels.** Channels are downstream of motion. Choosing channels first produces a fragmented strategy.
- **Do set specific, time-bound success metrics.** "Grow awareness" is not a metric. "1,000 trial signups within 90 days of launch" is.

---

## Donts

- **Dont try to target everyone.** A strategy targeting all company sizes, all industries, and all buyer roles is a strategy that resonates with no one deeply.
- **Dont confuse launch activities with GTM strategy.** A launch plan is the execution of the GTM strategy. Writing a press release is not the same as having a strategy.

---

## Output Format

```
1. GTM STRATEGY HEADER
   Product, market, version, date, owner, stakeholders.

2. EXECUTIVE SUMMARY
   The product and the problem it solves in two sentences.
   The target market and why now.
   The GTM motion and primary channel.
   The revenue target for year one.

3. MARKET OPPORTUNITY
   Total Addressable Market (TAM): full market if 100% captured.
   Serviceable Addressable Market (SAM): segment the product can realistically serve.
   Serviceable Obtainable Market (SOM): realistic year-one capture target.
   Market timing rationale: why this market is ready now.

4. TARGET CUSTOMER
   Ideal Customer Profile (ICP): company-level firmographic definition.
   Buyer persona: the decision-maker who approves purchase.
   User persona: the person who uses the product daily.
   Economic buyer: who controls budget.
   Champion profile: who inside the account advocates for the purchase.

5. PROBLEM AND SOLUTION
   The specific pain the ICP experiences today.
   How they currently solve it (the incumbent approach).
   Why current solutions are inadequate.
   How this product solves the problem differently.

6. POSITIONING AND MESSAGING SUMMARY
   Positioning statement in standard format:
   For [target customer] who [has this problem], [product] is a [category]
   that [delivers this value]. Unlike [primary alternative], [product] [key differentiator].
   Core message pillars: the 3 to 4 claims that define the product story.
   Reference: detailed work lives in positioning-doc.md and messaging-framework.md.

7. COMPETITIVE LANDSCAPE
   Direct competitors: products solving the same problem.
   Indirect competitors: alternative approaches including status quo.
   Competitive moat: the sustainable differentiation.
   Win/loss data if available.

8. GTM MOTION AND CHANNELS
   Primary GTM motion: PLG / sales-led / partner-led / hybrid.
   Acquisition channels ranked by expected volume and efficiency.
   Revenue model: subscription / usage / per-seat / transaction.
   Pricing strategy relative to value and competition.

9. LAUNCH PLAN SUMMARY
   Launch tier: major / minor / soft launch.
   Key launch milestones and dates.
   Reference: full execution in launch-plan.md.

10. SUCCESS METRICS
    Primary metric: the one number defining GTM success.
    30-day targets: early signal metrics.
    90-day targets: leading indicators of traction.
    Year-one targets: revenue, customers, market share.

11. RISKS AND MITIGATIONS
    Top 3 to 5 GTM risks with probability and mitigation plan.

12. RESOURCE REQUIREMENTS
    Functions required: PMM, demand gen, sales, CS.
    Headcount and budget implications.
    Open decisions blocking execution.
```

---

## Starter Prompt

```
You are a product marketing lead writing a go-to-market strategy.

Product: [name and what it does in plain language]
Target market: [who it is for]
Problem solved: [the specific pain addressed]
Key differentiators: [what makes it different from alternatives]
Pricing model: [how it will be priced]
GTM motion: [PLG / sales-led / partner-led / hybrid]
Launch timeline: [planned date or window]
Year-one revenue target: [ARR or revenue goal]
Competitive landscape: [key competitors]

Produce a complete GTM strategy covering all 12 sections.
The ICP must be specific enough to use as a targeting filter.
The positioning statement must follow the standard format.
Every success metric must have a specific numeric target and timeframe.
Flag any section where a key decision has not yet been made.
```

---

## Related Skills

| Use This Next | Why |
|---|---|
| `positioning-doc.md` | GTM positioning summary becomes the full positioning document |
| `launch-plan.md` | GTM motion and channels become the launch execution plan |
| `messaging-framework.md` | Positioning feeds the detailed messaging framework |

*Skill file version: 1.0 | Phase: 08 - Product Marketing | Company type: Product*
