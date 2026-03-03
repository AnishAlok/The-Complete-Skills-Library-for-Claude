# bi-report-template.md

> **Skill:** Produces a business intelligence report structure using data storytelling principles that leads with insight, provides context, and drives clear action from data.

---

## TLDR

A BI report template structures how analytical findings are communicated to business stakeholders: lead with the key insight, contextualize the data, tell a coherent story, and close with clear actions. This skill produces both the structural template and the storytelling guidance for transforming data into decisions.

---

## Topic Explanation

### Data Storytelling vs. Data Reporting

**Data reporting:** Presenting data as it is. Tables, charts, numbers. Leaves interpretation to the audience.

**Data storytelling:** Using data to make a specific argument or recommendation. Guides the audience from observation to insight to action.

Most BI reports are data reporting. The most valuable BI reports are data storytelling. The difference is not the data or the visualizations; it is the narrative structure and the explicit connection from data to decision.

### The SCR (Situation-Complication-Resolution) Structure

McKinsey's SCR structure is the standard for executive business communication:

**Situation:** The context the audience already knows. "Our onboarding completion rate has been declining."

**Complication:** The problem or tension that requires action. "The decline is concentrated in mobile users who joined in Q3, and those cohorts are churning at 2x the rate of desktop users."

**Resolution:** The recommended action. "We recommend prioritizing a mobile onboarding redesign targeted at Q3 acquisition channel users in the next sprint."

This structure works because it respects the audience's time (starts with what they know), creates tension (the complication demands a response), and resolves it (the recommendation).

### Chart Selection for Communication

The chart type should serve the insight, not the data:
- **Comparison over time:** Line chart (shows trend) or bar chart (shows magnitude)
- **Ranking:** Horizontal bar chart (easy to read labels)
- **Part-to-whole:** 100% stacked bar or pie (only use pie for 2-3 categories)
- **Distribution:** Histogram or box plot
- **Correlation:** Scatter plot
- **Change waterfall:** Waterfall chart (for MRR or user growth components)

Annotation is as important as the chart: mark the key insight directly on the visualization so the audience does not have to find it themselves.

---

## Output Format

```
1. REPORT HEADER
   Report title, period, author, audience, date, version.
   Distribution: who receives this report.

2. EXECUTIVE SUMMARY (pyramid structure)

   HEADLINE METRIC: [The single most important number]
   DIRECTION: Up X% / Down Y% vs. [comparison period]
   KEY FINDING: [The most important insight in one sentence]
   RECOMMENDED ACTION: [What to do about it]

3. SITUATION (context)
   The performance context the audience needs.
   Where we are relative to targets.
   The trend leading to this period.

4. COMPLICATION (the key findings)

   For each key finding:
   FINDING: [The insight stated directly]
   EVIDENCE: [The data that supports it, visualized]
   SO WHAT: [Why this matters for the business]

5. RESOLUTION (recommended actions)

   For each recommended action:
   - Action: what to do
   - Owner: who should do it
   - Timeline: by when
   - Expected impact: what it should achieve
   - Metric to watch: how to know it's working

6. SUPPORTING METRICS SECTION
   Full metrics tables for those who want detail.
   Secondary metrics with brief commentary.
   Period comparisons.

7. APPENDIX
   Methodology notes.
   Data sources.
   Definitions of key terms.
   Prior period reports for reference.
```

---

## Starter Prompt

```
You are a data analyst writing a BI report for business stakeholders.

Report type: [weekly / monthly / quarterly / ad hoc]
Audience: [executive / product / marketing / CS team]
Key metrics: [the headline numbers for this period]
Key findings: [the important insights from the data]
Recommended actions: [what the findings suggest doing]
Supporting data: [secondary metrics and context]

Produce a complete BI report using the SCR narrative structure.
Lead with the most important insight, not with the most data.
Every finding must connect to a recommended action.
Annotate the key insight on each visualization description.
```

---

## Related Skills

| Use This Before | Why |
|---|---|
| `data-analysis-report.md` | Analysis produces the findings that the BI report communicates |
| `metrics-dashboard-spec.md` | Dashboards surface the data that BI reports interpret |

*Skill file version: 1.0 | Phase: 06 - Data and Analytics | Company type: Product*
