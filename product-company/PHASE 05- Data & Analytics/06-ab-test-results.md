# ab-test-results.md

> **Skill:** Produces an A/B test results analysis and recommendation document that reports statistical outcomes, interprets the results in business context, and makes a clear ship/no-ship recommendation.

---

## TLDR

An A/B test results document reports what happened in an experiment: the statistical results for each metric, the interpretation of those results in business terms, a clear recommendation (ship / do not ship / run follow-on test), and the reasoning behind it. The results document should reference the original test plan and confirm that the analysis followed the pre-specified plan.

---

## Topic Explanation

### Statistical Significance vs. Practical Significance

These are different and both matter:

**Statistical significance:** The result is unlikely to be due to random chance (p < 0.05). A test can be statistically significant but practically meaningless if the effect size is tiny.

**Practical significance:** The effect is large enough to matter for the business. A statistically significant 0.01% lift in conversion rate on a low-traffic flow may not be worth shipping and maintaining.

Results analysis must address both: is the result real (statistical), and is it meaningful (practical)?

### Interpreting Non-Significant Results

A non-significant result (p ≥ 0.05) does not mean "the variant had no effect." It means: "we cannot confidently conclude there is an effect with this sample size." This is different from "there is no effect."

The correct interpretation of a non-significant result depends on:
- Was the test adequately powered? (Did we reach the planned sample size?)
- What does the confidence interval include? (If the CI includes the MDE, the test was inconclusive. If the CI excludes anything practically meaningful, we can conclude the variant likely has no meaningful effect.)

### Novelty Effects and Long-Term Effects

Many A/B test results show stronger effects in the first week than in subsequent weeks, because users are responding to novelty rather than inherent value. Results should note whether a novelty effect is likely and whether a longer-running test or holdout is recommended to assess long-term impact.

---

## Output Format

```
1. RESULTS HEADER
   Test name, test period, analyst, date of analysis.
   Reference to original test plan.
   Test status: completed as planned / stopped early / extended.

2. EXECUTIVE SUMMARY
   Recommendation: SHIP / DO NOT SHIP / ITERATE / RUN FOLLOW-ON TEST
   Primary metric result in plain language.
   Confidence in the recommendation: High / Medium / Low.
   Key insight in 2 to 3 sentences.

3. TEST VALIDITY CHECK
   Was the test run as planned? (Duration, sample size, randomization integrity)
   Sample ratio mismatch check: were variant sizes as expected?
   Any external events during the test that could confound results?
   Confirmation that analysis followed the pre-registered plan.

4. RESULTS TABLE

   | Metric | Type | Control | Variant B | Absolute diff | Relative diff | p-value | Significant? |
   | [Primary metric] | Primary | X% | Y% | +Z% | +W% | 0.03 | Yes |
   | [Secondary metric 1] | Secondary | ... |
   | [Guardrail metric 1] | Guardrail | ... |

5. STATISTICAL DETAILS
   Sample sizes per variant.
   Confidence intervals for the primary metric.
   Statistical method used.
   Any corrections applied (multiple comparisons, etc.)

6. RESULTS INTERPRETATION
   Primary metric: what the result means in business terms.
   Secondary metrics: what additional context they provide.
   Guardrail metrics: were any guardrails triggered?
   Subgroup analysis: any notable variation by segment.

7. CONFIDENCE ASSESSMENT
   How confident are we in this result?
   Threats to validity that remain.
   Novelty effect assessment.

8. RECOMMENDATION AND REASONING
   Ship / Do not ship / Iterate / Follow-on test.
   Detailed reasoning.
   What this result tells us about the underlying hypothesis.

9. NEXT STEPS
   If shipping: rollout plan and post-launch monitoring.
   If not shipping: what would change the recommendation.
   If iterating: what to change and test next.
   Learnings to document in the hypothesis log.
```

---

## Starter Prompt

```
You are a product analyst reporting A/B test results.

Test plan reference: [link or description of original test plan]
Test period: [start and end dates]
Sample sizes: [users per variant]
Primary metric results: [control vs. variant with statistical details]
Secondary metric results: [other metrics observed]
Guardrail metric results: [whether guardrails were triggered]
Statistical validity: [any issues with the test execution]
Business context: [any external factors during the test period]

Produce a complete test results document with executive summary,
validity check, results table, interpretation, and recommendation.
Address both statistical and practical significance.
If the primary metric is non-significant, interpret the confidence interval.
```

---

*Skill file version: 1.0 | Phase: 06 - Data and Analytics | Company type: Product*
