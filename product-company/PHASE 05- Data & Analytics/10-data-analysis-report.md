# data-analysis-report.md

> **Skill:** Produces a structured general data analysis report with clear question framing, methodology, findings, statistical context, and actionable recommendations.

---

## TLDR

A data analysis report documents an analytical investigation from question to recommendation. It states the business question, describes the methodology and data, presents findings with appropriate statistical context, and concludes with clear recommendations. Designed to be readable by non-technical stakeholders while being rigorous enough for technical review.

---

## Topic Explanation

### The Analyst's Communication Challenge

Data analysts face a consistent communication challenge: the analysis process (data cleaning, exploration, statistical testing, multiple dead ends) is very different from the communication artifact (a clear narrative from question to answer). The report should present the latter, not document the former.

The "pyramid principle" (Barbara Minto) is the standard structure for analytical communication: lead with the answer, then support it with evidence. Do not make the reader work through the methodology before knowing what you found.

### Correlation vs. Causation

Every data analysis that draws conclusions must be explicit about whether it is demonstrating correlation (two things move together) or causation (one thing causes another). Most observational data analysis demonstrates correlation.

Causal claims require either randomized experiments or quasi-experimental methods (difference-in-differences, regression discontinuity, instrumental variables). Analysts who present correlational findings as causal conclusions produce incorrect recommendations.

### Confidence and Uncertainty Quantification

Good analysis quantifies uncertainty. Point estimates (the average is 42) without confidence intervals or uncertainty ranges can be misleading. The reader needs to know: how confident should they be in this number?

---

## Output Format

```
1. REPORT HEADER
   Analysis title, analyst, date, stakeholder, data period, version.

2. EXECUTIVE SUMMARY (lead with the answer)
   The key finding in 2 to 3 sentences.
   The recommendation that follows.
   Confidence level: High / Medium / Low and why.

3. QUESTION AND CONTEXT
   The specific business question this analysis addresses.
   Why this question matters and what decision it will inform.
   What was known before this analysis.

4. DATA AND METHODOLOGY
   Data sources used.
   Time period analyzed.
   Analytical approach: descriptive / diagnostic / predictive / prescriptive.
   Key assumptions.
   Limitations of the data or methodology.

5. FINDINGS

   FINDING 1: [Title]
   - Observation with supporting data
   - Statistical context: n, confidence interval, significance if applicable
   - Visualization reference
   - What this means in plain language

   [Repeat for each major finding]

6. ALTERNATIVE EXPLANATIONS
   Other explanations for the observed patterns.
   Evidence that supports or refutes each alternative.
   Why the primary interpretation is most likely.

7. LIMITATIONS AND CAVEATS
   What the data cannot tell us.
   Selection bias or measurement issues.
   Time period considerations.
   Correlation vs. causation statement.

8. RECOMMENDATIONS
   For each recommendation:
   - The action recommended
   - The finding that supports it
   - Expected impact
   - Confidence in the recommendation
   - Owner and suggested timeline

9. APPENDIX
   Detailed methodology.
   SQL or code used.
   Additional charts.
   Data quality notes.
```

---

## Starter Prompt

```
You are a data analyst writing an analysis report.

Business question: [what question the analysis answers]
Data used: [sources, period, key metrics]
Key findings: [what the analysis found]
Alternative explanations considered: [other interpretations]
Limitations: [what the data cannot tell you]
Recommendations: [actions that follow from the findings]
Audience: [who will read this and their technical level]

Produce a complete data analysis report using the pyramid structure:
lead with the answer, then support it with evidence.
Explicitly state whether findings are correlational or causal.
Include confidence levels and uncertainty quantification.
```

---

*Skill file version: 1.0 | Phase: 06 - Data and Analytics | Company type: Product*
