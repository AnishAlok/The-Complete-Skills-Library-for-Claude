# segment-analysis.md

> **Skill:** Produces a user segment analysis that profiles key user segments by behavior, value, and needs, enabling segment-specific product and marketing decisions.

---

## TLDR

Segment analysis divides a user population into meaningful groups based on shared characteristics or behaviors and compares how those groups differ in engagement, retention, revenue contribution, and product usage. It turns "our users" into actionable personas backed by data, enabling targeted product improvements and growth strategies.

---

## Topic Explanation

### Segmentation Approaches

**Demographic segmentation:** Who they are. Company size, industry, role, geography. Available from signup data or enrichment. Easy to implement; may not predict behavior.

**Behavioral segmentation:** What they do. Feature usage, engagement frequency, actions taken. Derived from product analytics. More predictive of future behavior than demographics.

**Value-based segmentation (RFM):** Recency, Frequency, Monetary value. Best for identifying high-value users and those at churn risk. Classic in e-commerce; highly applicable to SaaS.

**Lifecycle stage segmentation:** Where they are in the customer journey. New / activating / engaged / power user / at-risk / churned. Drives lifecycle marketing and product interventions.

**Need-based segmentation:** What job they are hiring the product to do. Requires research. Produces the most strategically valuable segments but is hardest to implement at scale.

### The Pareto Principle in Segment Analysis

Most products follow a Pareto distribution: 20% of users generate 80% of engagement or revenue. Identifying that 20% and understanding what makes them different is often the highest-value segment analysis. What did they do differently in onboarding? What features do they use? What did they have in common at acquisition?

---

## Output Format

```
1. REPORT HEADER
   Analysis purpose, date, analyst, data period, segmentation method.

2. SEGMENTATION APPROACH
   What method was used and why.
   How segments were defined.
   Any clustering or statistical method used.

3. SEGMENT OVERVIEW
   Table: Segment name / Size (users) / % of total / Key characteristic

4. SEGMENT PROFILES

   For each segment:
   - Segment name and defining characteristic
   - Size and % of user base
   - Demographic profile (if available)
   - Behavioral profile: feature usage, engagement frequency, key actions
   - Value metrics: ARPU, LTV, conversion rate
   - Retention rate
   - Most common use case or JTBD
   - Representative user quote or persona description (if research available)

5. COMPARATIVE ANALYSIS
   Cross-segment comparison table.
   Key metrics by segment: engagement / retention / revenue / NPS.
   Which segment drives the most value?
   Which segment is fastest-growing?
   Which segment is most at-risk?

6. SEGMENT VALUE ANALYSIS
   Revenue concentration: what % of revenue comes from each segment?
   Retention comparison: which segments retain best?
   Acquisition efficiency: which segments are cheapest to acquire?
   Expansion potential: which segments are most likely to expand?

7. PRODUCT USAGE DIFFERENCES
   Features most used by each segment.
   Features underused by high-value segments.
   Features that predict high-value segment membership.

8. STRATEGIC IMPLICATIONS
   Which segment(s) to prioritize for product investment?
   Which segment(s) to prioritize for growth?
   Segment-specific product gaps or opportunities.

9. RECOMMENDED ACTIONS
   For each key finding: the recommended product or marketing action.
   Priority and expected impact.
```

---

## Starter Prompt

```
You are a product analyst conducting a user segment analysis.

Product: [what it does and who it serves]
Segmentation method: [demographic / behavioral / RFM / lifecycle / need-based]
Data available: [what user and behavioral data is available]
Key segments identified: [initial segments with their characteristics]
Metrics by segment: [engagement, retention, revenue data]
Business question: [what the analysis should answer]

Produce a complete segment analysis with profiles, comparative analysis,
value assessment, and strategic recommendations.
Identify which segment represents the highest-value growth opportunity.
```

---

*Skill file version: 1.0 | Phase: 06 - Data and Analytics | Company type: Product*
