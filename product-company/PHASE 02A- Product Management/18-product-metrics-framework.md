# product-metrics-framework.md

> **Skill:** Produces a product metrics framework that organizes leading and lagging indicators into a coherent hierarchy connecting daily product activity to business outcomes.

---

## TLDR

A product metrics framework answers: *"What numbers should we watch, in what order of importance, and what do they tell us about whether the product is working?"* It organizes metrics into a hierarchy from north star to leading indicators to lagging outcomes, ensuring teams focus on signals that actually predict success rather than vanity metrics.

---

## Topic Explanation

### Metric Hierarchy

**North star metric:** The single metric that best captures the core value the product delivers to customers. Increases when customers succeed. Decreases when they don't. Every team should be able to connect their work to this metric. (See `north-star-metric.md` for full treatment.)

**L1 input metrics (levers):** The 3 to 5 metrics that, when moved, predictably move the north star. These are the metrics product teams directly influence through their work.

**L2 diagnostic metrics:** Metrics that explain why L1 metrics moved. Used for diagnosis, not as primary targets.

**Business outcome metrics:** Revenue, retention, growth. Lagging indicators that reflect the cumulative effect of product performance. Important but not directly actionable by product teams.

**Guardrail metrics:** Metrics that must not get worse even while pursuing north star improvement. Often: support volume, error rate, churn for features not being invested in.

### Leading vs. Lagging Indicators

**Lagging indicators:** Measure outcomes after they have occurred. Revenue, churn, annual retention. Can only confirm what happened, not predict what will happen.

**Leading indicators:** Measure behaviors that predict future outcomes. Activation rate predicts 30-day retention. Feature adoption predicts expansion revenue. Feature engagement in the first week predicts annual retention.

A good metrics framework has more leading indicators than lagging ones at the operational level. Lagging indicators confirm that leading indicators are working.

### The HEART Framework (Google)

Happiness, Engagement, Adoption, Retention, Task success. A user-centered metric framework useful for product team metrics:
- **Happiness:** User satisfaction (NPS, CSAT, survey)
- **Engagement:** Frequency and depth of product use
- **Adoption:** New users and features successfully adopted
- **Retention:** Users returning over time
- **Task success:** Completion rates, errors, efficiency

---

## Output Format

```
1. NORTH STAR METRIC
   The metric. Current value. Target.
   Why this captures core product value.

2. INPUT METRICS (L1)
   The 3 to 5 metrics that move the north star.
   For each:
   - Metric name and definition
   - Current value
   - Target
   - How it connects to the north star
   - The team or initiative responsible

3. DIAGNOSTIC METRICS (L2)
   Supporting metrics used for diagnosis.
   For each: name, definition, what it explains.

4. BUSINESS OUTCOME METRICS
   Revenue metrics: MRR/ARR, ARPU, LTV.
   Retention metrics: gross retention, net revenue retention.
   Growth metrics: new customer acquisition, expansion revenue.

5. GUARDRAIL METRICS
   Metrics that must not decline.
   Current values and acceptable floor thresholds.

6. METRIC DEFINITIONS
   Precise definitions for every metric in the framework.
   Data source.
   Calculation method.
   Update frequency.

7. INSTRUMENTATION STATUS
   Which metrics are currently tracked.
   Which require new instrumentation.
   Timeline for gaps.

8. REVIEW CADENCE
   Which metrics are reviewed daily / weekly / monthly / quarterly.
   By whom.
```

---

## Starter Prompt

```
You are a product manager building a metrics framework.

Product: [what it does and who it serves]
Core value delivered: [how customers succeed with the product]
Current metrics tracked: [what is already being measured]
Business outcomes to drive: [revenue, retention, growth targets]
Team structure: [how teams are organized, for metric ownership]
Instrumentation gaps: [what is not currently tracked]

Produce a complete product metrics framework with north star,
input metrics, diagnostic metrics, business outcomes, and guardrails.
Include precise definitions and instrumentation status for each metric.
Identify which metrics are leading indicators and which are lagging.
```

---

*Skill file version: 1.0 | Phase: 02 - Product Management | Company type: Product*
