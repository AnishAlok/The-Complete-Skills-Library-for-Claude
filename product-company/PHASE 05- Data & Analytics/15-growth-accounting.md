# growth-accounting.md

> **Skill:** Produces a growth accounting analysis that decomposes net user or revenue growth into new, retained, resurrected, and churned components to reveal the true drivers of growth.

---

## TLDR

Growth accounting (also called the growth equation) decomposes net growth into its four components: new users acquired, retained users from last period, resurrected users who returned after churning, and churned users lost. This decomposition reveals whether growth is healthy (driven by retention and acquisition) or fragile (driven by acquisition masking high churn). Used monthly as a diagnostic for product and business health.

---

## Topic Explanation

### The Growth Accounting Framework

The growth equation for any period:

**Active users (this period) = New + Retained + Resurrected - Churned**

- **New:** Users active this period who were not active in any prior period
- **Retained:** Users active both this period and last period
- **Resurrected:** Users active this period who were inactive last period but active in some prior period
- **Churned:** Users active last period but inactive this period

The sum of New + Retained + Resurrected - Churned = net change in active users.

### What the Components Reveal

**High new, high churn:** Classic "leaky bucket." Acquisition is working but retention is not. Growth requires ever-increasing acquisition spend. Not sustainable.

**High retained, low churn:** Health signal. The core user base is stable. Growth requires acquisition, but the base does not erode.

**High resurrected:** Users are returning after lapsing. May indicate the product has improved, or that marketing re-engagement is working. Investigate what brings them back.

**Declining new:** Acquisition channels are saturating or performance is degrading. May not be visible in aggregate metrics if retention is high.

### Quick Ratio

The quick ratio (Mamoon Hamid) is a simple summary of growth quality:

**Quick Ratio = (New + Resurrected) / Churned**

A quick ratio > 1 means the user base is growing.
A quick ratio > 4 is generally considered healthy for a growth-stage company.
A quick ratio < 1 means the user base is shrinking even if acquisition looks strong.

---

## Output Format

```
1. REPORT HEADER
   Period, metric unit (users / paid accounts / MRR), analyst, data source.

2. GROWTH EQUATION SUMMARY

   | Component | Count / Value | % of ending base |
   | Beginning active | N | - |
   | + New | +X | % |
   | + Resurrected | +Y | % |
   | - Churned | -Z | % |
   | = Retained | R | % |
   | Ending active | M | - |
   | Net change | M - N | % |

   Quick Ratio: (New + Resurrected) / Churned = X

3. TREND ANALYSIS
   12-month view of each component.
   Trend in quick ratio.
   Are retention rates improving or declining?

4. COHORT CONTRIBUTION
   Which signup cohorts make up the retained base?
   Age distribution of active users.

5. COMPONENT DEEP DIVES

   NEW USERS:
   - Sources of new users
   - New user growth rate trend

   CHURNED USERS:
   - Churn rate trend
   - When in the lifecycle do users churn? (Day 1, day 7, day 30, month 6)
   - Segment composition of churned users

   RESURRECTED USERS:
   - What % of previously churned users are resurrecting?
   - Average time between churn and resurrection
   - What triggered resurrection?

6. GROWTH QUALITY ASSESSMENT
   Is growth healthy or fragile?
   Evidence for the assessment.
   Key risk: the biggest threat to growth health.

7. RECOMMENDATIONS
   The highest-leverage intervention based on the growth accounting.
   New vs. retain vs. resurrect: where should investment go?
```

---

## Starter Prompt

```
You are a product analyst producing a growth accounting analysis.

Period: [month or quarter being analyzed]
Metric: [users / paid accounts / MRR]
Growth accounting data:
  Beginning active: [N]
  New: [X]
  Resurrected: [Y]
  Churned: [Z]
  Retained: [R]
  Ending active: [M]
Trend data: [prior 12 months if available]
Segment data: [churn or new user breakdown if available]

Produce a complete growth accounting analysis with quick ratio,
trend analysis, component deep dives, growth quality assessment,
and investment recommendations.
```

---

*Skill file version: 1.0 | Phase: 06 - Data and Analytics | Company type: Product*
