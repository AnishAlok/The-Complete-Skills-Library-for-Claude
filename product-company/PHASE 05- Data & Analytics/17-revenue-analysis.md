# revenue-analysis.md

> **Skill:** Produces a revenue breakdown and trend analysis covering MRR/ARR movements, revenue by segment, expansion and contraction drivers, and forecast vs. actuals comparison.

---

## TLDR

A revenue analysis report breaks down revenue performance: MRR/ARR movements by component (new, expansion, contraction, churn), revenue by customer segment and product line, trends, and variance from forecast. Used monthly by finance and revenue leadership to understand what is driving revenue change and what requires attention.

---

## Topic Explanation

### MRR Movement Categories

Monthly Recurring Revenue changes by category:

**New MRR:** Revenue from customers who did not exist last month. Driven by sales volume and deal size.

**Expansion MRR:** Additional revenue from existing customers (upsells, plan upgrades, seat additions). A high-quality growth signal: customers are getting more value and paying for it.

**Contraction MRR:** Reduced revenue from existing customers (downgrades, seat reductions). A signal of declining value perception.

**Churned MRR:** Revenue from customers who have cancelled entirely.

**Net New MRR = New + Expansion - Contraction - Churn**

### Net Revenue Retention (NRR)

Net Revenue Retention (also called Net Dollar Retention) measures whether existing customers are growing or shrinking in aggregate:

**NRR = (Beginning MRR + Expansion MRR - Contraction MRR - Churn MRR) / Beginning MRR × 100%**

NRR > 100%: Existing customers are generating more revenue than they were a year ago despite churn. The business grows even without new customer acquisition.

NRR < 100%: Contraction and churn exceed expansion. The business must constantly acquire new customers to offset shrinkage.

Elite SaaS benchmarks: NRR > 120% is excellent. NRR > 110% is good. NRR < 100% is a red flag.

---

## Output Format

```
1. REPORT HEADER
   Period, analyst, date. MRR or ARR basis. Currency.

2. EXECUTIVE SUMMARY
   Ending MRR/ARR and growth rate (MoM and YoY).
   Net New MRR.
   NRR.
   Headline finding and action item.

3. MRR WATERFALL

   | Component | Value | MoM change |
   | Beginning MRR | $X | - |
   | + New MRR | +$A | % |
   | + Expansion MRR | +$B | % |
   | - Contraction MRR | -$C | % |
   | - Churned MRR | -$D | % |
   | Ending MRR | $Y | % |
   | Net New MRR | $Y - $X | |

4. NRR CALCULATION
   NRR for the period.
   NRR trend: 12-month rolling.
   Gross Revenue Retention (GRR): Ending MRR excluding expansion / Beginning MRR.

5. REVENUE BY SEGMENT
   MRR by plan tier.
   MRR by customer size (SMB / Mid-market / Enterprise).
   MRR by acquisition channel.
   MRR by product line (if applicable).

6. NEW REVENUE ANALYSIS
   New MRR by source.
   Average deal size trend.
   Sales velocity: deals closed vs. pipeline.

7. EXPANSION REVENUE ANALYSIS
   Expansion MRR drivers: which products or plans customers are expanding to.
   Expansion rate: expansion MRR / beginning MRR.
   Which segments expand most?

8. CHURN AND CONTRACTION ANALYSIS
   Gross churn rate trend.
   Churned MRR by customer size and tenure.
   Contraction MRR by reason (if tracked).
   Cohort churn: which signup cohorts are churning?

9. FORECAST VS. ACTUALS
   This period: forecast vs. actual MRR.
   Variance by component.
   Explanation of variances > 5%.

10. OUTLOOK
    Forward forecast: next 3 months.
    Key assumptions.
    Risks to the forecast.
```

---

## Starter Prompt

```
You are a finance analyst producing a monthly revenue analysis.

Period: [month/year]
MRR waterfall components: [beginning MRR, new, expansion, contraction, churn, ending]
Revenue by segment: [plan tier, customer size, channel]
Forecast vs. actual: [plan and actuals]
Key drivers: [what drove the notable movements this period]
Forward outlook: [known pipeline and risk factors]

Produce a complete revenue analysis with MRR waterfall, NRR calculation,
segment breakdown, churn analysis, forecast variance, and outlook.
```

---

*Skill file version: 1.0 | Phase: 06 - Data and Analytics | Company type: Product*
