# value-proposition-canvas.md

> **Skill:** Produces a completed Value Proposition Canvas mapping customer jobs, pains, and gains to product features, pain relievers, and gain creators, with a fit assessment and messaging implications.

---

## TLDR

The Value Proposition Canvas (Osterwalder et al.) ensures product-market fit at the messaging level: it maps what the customer is trying to accomplish to what the product delivers. This skill produces the completed canvas with validated vs. assumed distinctions, a fit quality assessment, and the messaging implications that direct where product marketing should focus.

---

## Topic Explanation

### The Two Sides of the Canvas

**Customer Profile (right circle):**

Customer jobs: what the customer is trying to accomplish. These operate at three levels:
- Functional jobs: specific tasks or problems ("prepare the monthly compliance report")
- Social jobs: how they want to be perceived ("look competent and in control to leadership")
- Emotional jobs: how they want to feel ("confident that nothing has fallen through the cracks")

Pains: the obstacles, frustrations, and risks the customer experiences while trying to accomplish their jobs. What makes their work harder, slower, or riskier.

Gains: the outcomes and benefits the customer wants to achieve — from expected to desired to unexpected pleasant surprises.

**Value Map (left square):**

Products and services: the complete list of what you offer.
Pain relievers: how specific offerings reduce or eliminate specific customer pains.
Gain creators: how specific offerings produce or enhance specific customer gains.

**Fit** is achieved when pain relievers address significant customer pains and gain creators deliver desired gains. The fit must be validated with real customers, not assumed from product team intuition.

### Jobs-to-be-Done Connection

The customer jobs section connects directly to Jobs-to-be-Done theory (Christensen, Ulwick): customers "hire" products to accomplish jobs in their lives or work. Understanding the job being done more precisely than competitors produces durable positioning advantage.

Critical insight: functional jobs are the most visible but often not the most powerful purchase motivator. Social and emotional jobs frequently drive buying decisions in ways that product teams miss entirely.

---

## Dos

- **Do distinguish between validated insights and assumptions explicitly.** Every entry should be tagged. Unvalidated assumptions in the canvas lead to messaging built on guesses.
- **Do rank pains by severity and gains by relevance before assessing fit.** A product that addresses five low-severity pains has worse fit than one that fully addresses one extreme pain.
- **Do derive messaging implications from the canvas, not just complete the canvas.** The value of the exercise is the marketing direction it produces.

---

## Donts

- **Dont complete the canvas without talking to customers.** A canvas completed entirely from internal assumptions will confirm what the team already believes. That is not research; it is documentation of bias.
- **Dont try to address every pain and gain.** A product that claims to solve everything credibly solves nothing. Identify the highest-value fit and focus the messaging there.

---

## Output Format

```
1. CANVAS HEADER
   Product, target customer segment, date, PM/PMM owner.
   Research methods used to populate this canvas.

2. CUSTOMER PROFILE

   CUSTOMER JOBS (ranked by importance to the customer)
   For each job:
   - Description of the job
   - Type: functional / social / emotional
   - Importance: critical / significant / minor
   - Source: validated (method and N) / assumed

   CUSTOMER PAINS (ranked by severity)
   For each pain:
   - Description
   - Severity: extreme / moderate / mild
   - Frequency: daily / weekly / monthly / occasional
   - Source: validated / assumed

   CUSTOMER GAINS (ranked by relevance)
   For each gain:
   - Description
   - Relevance: essential / expected / desired / unexpected delight
   - Source: validated / assumed

3. VALUE MAP

   PRODUCTS AND SERVICES
   Complete list of offerings mapped to this customer segment.

   PAIN RELIEVERS
   For each significant pain (focus on extreme and moderate):
   - Pain addressed
   - How the product relieves it
   - Completeness: fully relieved / partially relieved / minimally addressed

   GAIN CREATORS
   For each relevant gain (focus on essential and expected):
   - Gain targeted
   - How the product creates it
   - Magnitude: substantial / moderate / marginal

4. FIT ASSESSMENT
   Extreme pains addressed: [N of N extreme pains] at what quality
   Essential gains created: [N of N essential gains] at what magnitude
   Fit quality: Strong / Moderate / Weak / Misaligned
   Unaddressed extreme pains: pains the product does not touch
   Undelivered essential gains: gains customers need but the product does not create
   Product roadmap implications from gaps

5. VALIDATION STATUS
   Which jobs, pains, and gains are validated vs. assumed.
   Research methods used and sample sizes for each.
   Confidence level for key claims: high / medium / low.

6. MESSAGING IMPLICATIONS
   Top 3 pains to lead with: highest severity plus strongest pain relief.
   Top gains to feature: most desired plus most substantially created.
   Jobs to anchor the brand story around.
   Validated insights vs. assumptions to treat with caution in messaging.
   Canvas gaps that represent both product risk and messaging risk.
```

---

## Starter Prompt

```
You are a product marketer or product manager completing a Value Proposition Canvas.

Target customer segment: [specific customer type]
Customer research available: [interviews, surveys, usage data, win/loss analysis and volumes]
Known customer jobs: [functional, social, and emotional tasks with importance]
Known customer pains: [frustrations, obstacles, risks with severity]
Known customer gains: [desired outcomes with relevance]
Product features and capabilities: [what the product offers]
Validated vs. assumed: [explicitly tag which insights are research-backed]

Produce a complete Value Proposition Canvas with fit assessment and messaging implications.
Distinguish clearly between validated insights and assumptions throughout every section.
Rank pains by severity and gains by relevance before assessing fit.
Identify the top 3 pains to lead with based on severity and quality of relief.
```

---

## Related Skills

| Use This Before | Why |
|---|---|
| `positioning-doc.md` | Canvas findings inform which attributes to position around |
| `messaging-framework.md` | Messaging implications from the canvas become the framework's pillars |

*Skill file version: 1.0 | Phase: 08 - Product Marketing | Company type: Product*
