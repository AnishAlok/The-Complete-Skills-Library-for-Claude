# ltv-cac-analysis.md

> **Skill:** Produces an LTV:CAC analysis that calculates customer lifetime value and customer acquisition cost by segment, assesses unit economics health, and identifies optimization opportunities.

---

## TLDR

The LTV:CAC ratio is the foundational unit economics metric for subscription and recurring-revenue businesses. It answers: "For every dollar we spend acquiring a customer, how many dollars of value do we receive?" This skill produces an LTV:CAC analysis with calculations by acquisition channel and customer segment, health assessment, and recommendations for improving unit economics.

---

## Topic Explanation

### LTV Calculation

Customer Lifetime Value (LTV) is the total revenue (or gross profit) expected from a customer over their entire relationship with the business.

**Simple LTV (cohort-based):**
LTV = ARPU × Gross Margin × Customer Lifetime
Customer Lifetime = 1 / Monthly Churn Rate

Example: ARPU $100/month × 75% gross margin × 20 months (5% monthly churn) = $1,500 LTV

**Discounted LTV:** Accounts for the time value of money by discounting future cash flows. More accurate but more complex.

**LTV by cohort:** The most reliable method. Calculate actual cumulative revenue from real customer cohorts over time. Requires patience to accumulate sufficient history.

### CAC Calculation

Customer Acquisition Cost (CAC) is the total cost of acquiring one new customer.

**Blended CAC:** Total sales and marketing spend / Total new customers
Simple to calculate. Mixes channels with very different economics.

**Paid CAC:** Paid marketing spend / Customers acquired through paid channels
More useful for evaluating paid acquisition efficiency.

**Channel CAC:** Spend per channel / Customers acquired per channel
The most useful for optimization. Requires proper attribution.

### The LTV:CAC Ratio

**LTV:CAC < 1:** Destroying value. Each customer costs more to acquire than they will ever return. Unsustainable.

**LTV:CAC 1-3:** Marginal. The business may be viable but there is little room for operational efficiency.

**LTV:CAC > 3:** Healthy for most SaaS businesses. Standard benchmark.

**LTV:CAC > 5:** Either the business is very capital efficient, or CAC is being underestimated (e.g., not fully loading sales costs).

**Payback period:** Time to recover CAC from gross profit contribution. Target: < 12 months for efficient SaaS businesses. < 24 months acceptable for enterprise.

---

## Output Format

```
1. ANALYSIS HEADER
   Period, analyst, segments analyzed, methodology notes.

2. EXECUTIVE SUMMARY
   Overall LTV:CAC ratio.
   Payback period.
   Health assessment: strong / acceptable / concerning / critical.
   One key finding and recommendation.

3. LTV CALCULATION

   Inputs:
   - ARPU: average revenue per user per month
   - Gross margin: %
   - Monthly churn rate: %
   - Customer lifetime: 1 / churn rate (months)

   LTV = ARPU × Gross Margin × Customer Lifetime = $X

   By segment:
   | Segment | ARPU | Gross margin | Churn rate | Lifetime | LTV |

4. CAC CALCULATION

   Inputs:
   - Total S&M spend: $X
   - New customers acquired: N
   - Blended CAC: $X/N

   By channel:
   | Channel | Spend | New customers | CAC |

5. LTV:CAC RATIO

   | Segment / Channel | LTV | CAC | LTV:CAC | Payback (months) |

6. TREND ANALYSIS
   LTV:CAC trend over 12 months.
   Is the ratio improving or deteriorating?
   What is driving the change?

7. SENSITIVITY ANALYSIS
   What happens to LTV:CAC if churn increases by 1%?
   What happens if ARPU increases by 10%?
   What is the CAC threshold that keeps LTV:CAC > 3?

8. BENCHMARKING
   LTV:CAC vs. industry benchmarks.
   Payback period vs. benchmarks.
   Gross margin comparison.

9. OPTIMIZATION OPPORTUNITIES
   Levers to improve LTV: reduce churn, increase ARPU, improve gross margin.
   Levers to reduce CAC: improve channel mix, optimize spend, improve conversion.
   Priority recommendation with expected impact.
```

---

## Starter Prompt

```
You are a finance or growth analyst producing an LTV:CAC analysis.

ARPU: [average revenue per user per month]
Gross margin: [%]
Monthly churn rate: [%]
Total S&M spend: [last 12 months]
New customers acquired: [last 12 months]
Channel breakdown: [spend and customers by acquisition channel]
Segment data: [LTV and CAC by customer segment if available]

Produce a complete LTV:CAC analysis with LTV and CAC calculations by segment,
ratio and payback period, trend analysis, and optimization recommendations.
Include sensitivity analysis for key assumptions.
```

---

*Skill file version: 1.0 | Phase: 06 - Data and Analytics | Company type: Product*
