# cohort-analysis-report.md

> **Skill:** Produces a cohort retention analysis report that documents user retention curves by signup cohort, identifies retention trends, compares cohort performance, and interprets product-market fit signals.

---

## TLDR

Cohort analysis measures what percentage of users who started using a product in a given period are still using it in subsequent periods. It is one of the most important analyses for any subscription or recurring-use product. This skill produces a structured cohort retention report with retention curves, cohort comparisons, product-market fit assessment, and recommendations.

---

## Topic Explanation

### Why Cohort Analysis Beats Aggregate Metrics

Aggregate retention metrics hide the most important signal: whether retention is improving or deteriorating over time. If new user volume is growing, even declining retention can produce stable aggregate retention numbers because the growing base of new users masks the churning older users.

Cohort analysis isolates each group of users who started in the same period, allowing direct comparison of retention curves across cohorts. If newer cohorts retain better than older cohorts, the product is improving. If they retain worse, the product is deteriorating despite potentially growing user numbers.

### The Retention Curve Shape

**Flat at zero:** Almost all users churn quickly. Classic "leaky bucket" problem. Product-market fit has not been found.

**Decaying to a floor:** Users churn initially, then a core group stays. The floor level indicates the size of the product's engaged core. A higher floor = better retention = stronger product-market fit signal.

**Smile curve:** Retention drops initially, then recovers. May indicate users who return after an initial lull. Investigate what brings them back.

**The flattening question:** Does the cohort curve flatten, and at what level? A curve that flattens above zero indicates a retained core user base. A curve that never flattens and approaches zero over time indicates a product that is not retaining users long-term.

### Retention Metrics

**N-day retention:** What percentage of users who signed up on day 0 are still active on day N?

**Rolling retention:** What percentage of users who signed up in week W were active in week W+N?

**Bracket retention:** What percentage of users were active in weeks 1-2, 3-4, 5-8, etc.?

The right retention metric depends on the expected usage frequency. Daily-use products measure day-1, day-7, day-30 retention. Weekly-use products measure week-1, week-4, week-12. Monthly-use products measure month-1, month-3, month-6.

---

## Output Format

```
1. REPORT HEADER
   Analysis period, cohort definition, retention metric, analyst, date, data source.

2. EXECUTIVE SUMMARY
   Key finding: is retention healthy / improving / declining?
   The most important retention number and its interpretation.
   Primary recommendation.

3. COHORT DEFINITION
   What event defines cohort entry (signup, first purchase, first core action).
   Cohort period: weekly / monthly.
   Activity definition: what counts as "retained" (any login / core action / purchase).
   Analysis window.

4. RETENTION CURVES

   Retention table (cohort x period):
   | Cohort | Period 0 | Period 1 | Period 2 | ... | Period N |
   | [Month] | 100% | X% | Y% | ... | Z% |

   Retention curve visualization (described or referenced).

5. KEY RETENTION METRICS
   D1, D7, D30 retention (for daily-use products).
   W1, W4, W12 retention (for weekly-use products).
   M1, M3, M6, M12 retention (for monthly-use products).
   Benchmark comparison if available.

6. COHORT COMPARISON
   Are newer cohorts retaining better or worse than older cohorts?
   What changed between cohorts that could explain differences?
   Best-performing cohort: what was different about that period?

7. PRODUCT-MARKET FIT ASSESSMENT
   Does the retention curve flatten at a meaningful level?
   What does the curve shape indicate about product-market fit?
   Comparison to industry benchmarks.

8. SEGMENT ANALYSIS
   Retention by acquisition channel.
   Retention by plan type.
   Retention by onboarding completion.
   Retention by feature adoption.
   Which segment retains best and what can be generalized?

9. LEADING INDICATOR ANALYSIS
   Which early behaviors predict long-term retention?
   The "magic moment" or activation milestone if identified.

10. RECOMMENDATIONS
    Interventions to improve retention at the key drop-off period.
    Segments to prioritize.
    Experiments to run.
```

---

## Starter Prompt

```
You are a product analyst writing a cohort retention analysis.

Product type: [subscription / marketplace / consumer app / B2B SaaS]
Cohort definition: [signup date / first purchase / first core action]
Retention definition: [what counts as active]
Analysis period: [how many cohorts and periods]
Retention data: [the cohort x period retention matrix]
Segment data: [any segment-level retention available]
Industry benchmarks: [if available]

Produce a complete cohort retention analysis with retention curves,
cohort comparison, product-market fit assessment, and recommendations.
Interpret the curve shape explicitly: does it flatten and at what level?
```

---

*Skill file version: 1.0 | Phase: 06 - Data and Analytics | Company type: Product*
