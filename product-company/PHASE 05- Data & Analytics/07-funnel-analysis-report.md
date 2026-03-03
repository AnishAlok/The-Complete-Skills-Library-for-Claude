# funnel-analysis-report.md

> **Skill:** Produces a funnel analysis report that documents step-by-step conversion rates, drop-off points, segment comparisons, and actionable recommendations for improving funnel performance.

---

## TLDR

A funnel analysis report documents how users move through a defined sequence of steps, where they drop off, and what the drop-off patterns reveal about friction and opportunity. This skill produces a structured analysis with conversion rates by step, segment breakdowns, drop-off hypotheses, and prioritized recommendations.

---

## Topic Explanation

### Funnel Analysis Fundamentals

A funnel is a defined sequence of steps that users must complete to reach a goal. The analysis measures:
- Conversion rate at each step (users who completed step N / users who started step N)
- Overall funnel conversion (users who completed the last step / users who started the first step)
- Drop-off rate at each step (1 - step conversion rate)
- Time to conversion between steps

The highest drop-off steps are the highest-value improvement opportunities. However, not all drop-off is equal: some steps are naturally lower conversion because they ask more of the user. Context is essential.

### Entry Point vs. Step Conversion

**Entry point selection:** Which users are included in the funnel? The funnel conversion rate changes dramatically based on who is counted at the top. "All signed-up users" produces a different conversion rate than "users who visited the onboarding page."

**Step conversion:** The percentage of users who completed step N and also completed step N+1. This measures friction at each step.

**Overall conversion:** The percentage of users at the funnel entry who complete the goal. This measures total funnel effectiveness.

### Cohort Comparisons in Funnels

Funnels should always be analyzed for multiple segments: new vs. returning users, by plan type, by acquisition channel, by device type. The aggregate funnel may look acceptable while hiding a severely broken experience for a specific segment.

---

## Output Format

```
1. REPORT HEADER
   Funnel name, analysis period, analyst, date, data source.

2. EXECUTIVE SUMMARY
   Overall funnel conversion rate.
   Biggest drop-off step.
   Primary finding and recommendation in 3 sentences.

3. FUNNEL DEFINITION
   Entry event: who is included at the top of the funnel.
   Steps in order.
   Goal event: the completion step.
   Analysis window: how long users have to complete the funnel.
   Attribution: how users are attributed to funnel entry.

4. OVERALL FUNNEL RESULTS

   | Step | Step name | Users entering | Users completing | Step conversion | Cumulative conversion | Drop-off |
   | 1 | [Step] | N | M | X% | X% | (100-X)% |
   | 2 | [Step] | M | P | Y% | XY% | (100-Y)% |
   ...

   Visualization: funnel chart with absolute numbers and rates.

5. DROP-OFF ANALYSIS
   For each step with significant drop-off:
   - Observed drop-off rate
   - Benchmark or target for this step
   - Variance from benchmark
   - Hypotheses for the drop-off
   - Evidence supporting each hypothesis

6. SEGMENT BREAKDOWN
   Funnel performance by key segments:
   - New vs. returning users
   - By plan type
   - By acquisition channel
   - By device / platform
   - Any other relevant segment

   For each segment: step conversion rates and notable differences from aggregate.

7. TIME-TO-CONVERT ANALYSIS
   Median time between each step.
   Distribution of time-to-convert.
   Users who convert same-session vs. multi-session.

8. COHORT COMPARISON (if applicable)
   Funnel performance by signup cohort.
   Trend: is funnel performance improving or degrading over time?

9. FINDINGS AND RECOMMENDATIONS
   For each significant finding:
   - Step affected
   - Current conversion rate and gap from target
   - Recommended intervention
   - Expected impact
   - Priority: High / Medium / Low
   - Owner

10. APPENDIX
    SQL queries used.
    Data quality notes.
```

---

## Starter Prompt

```
You are a product analyst writing a funnel analysis report.

Funnel: [the name and purpose of the funnel]
Analysis period: [date range]
Funnel steps: [ordered list of steps]
Data: [conversion rates at each step, or raw event data]
Segments to analyze: [key breakdowns]
Target conversion rates: [benchmarks if available]
Known context: [any recent changes or external factors]

Produce a complete funnel analysis report with step-by-step results,
segment breakdowns, drop-off hypotheses, and prioritized recommendations.
Flag any step with drop-off significantly above expectations.
```

---

*Skill file version: 1.0 | Phase: 06 - Data and Analytics | Company type: Product*
