# marketing-metrics-report.md

> **Skill:** Produces a marketing performance report covering demand generation, content, brand, and channel metrics with analysis, anomalies, and recommended actions.

---

## TLDR

A marketing metrics report communicates what happened, why it matters, and what to do next. Not a data dump: a structured narrative that starts with the headline finding, explains the drivers, flags anomalies, and ends with specific recommended actions. This skill produces the report structure and a fully written example report with all sections.

---

## Topic Explanation

### The Difference Between a Data Report and a Metrics Report

A data report: tables and charts of numbers. Requires the reader to form their own interpretation.

A metrics report: numbers plus analysis plus recommended action. The author has done the interpretive work and is presenting a conclusion, not just data.

Marketing leaders reading a metrics report should be able to get the key insight in 60 seconds and the full picture in 10 minutes. They should not have to stare at a spreadsheet and figure out what it means.

### The Report Hierarchy

Most marketing reports make the mistake of presenting all metrics with equal weight. Readers do not know what matters. A well-structured report follows a clear hierarchy:

**The headline:** one sentence describing the most important finding this period.

**Performance vs. goals:** are we on track, ahead, or behind on the primary KPI?

**What drove performance:** the 2 to 3 factors that most explain the results.

**Anomalies and flags:** anything surprising, broken, or worth investigating.

**Channel breakdown:** detail by channel for the reader who needs it.

**Recommended actions:** the 2 to 3 specific things the report argues the team should do.

### Metric Selection Principles

Not every metric belongs in every report. Metrics should be selected based on:

**Actionability:** can the reader do something about this number? Metrics that cannot be acted on are noise.

**Leading vs. lagging:** lagging indicators (revenue, customers won) tell you what happened. Leading indicators (pipeline, trial signups, content traffic) tell you what will happen. Reports should include both.

**North star focus:** one primary metric that defines marketing success for this period. Everything else is context.

---

## Output Format

```
MARKETING METRICS REPORT

Period: [Month / Quarter / Year]
Report owner: [marketing lead] | Date: [date]
Distribution: [who receives this report]

---

EXECUTIVE SUMMARY (half page)
Headline finding: [one sentence on the most important thing that happened this period]
Overall performance vs. goal: [on track / ahead / behind on primary KPI, by how much]
Top driver: [the most important factor explaining performance]
Key risk or flag: [the most important thing to watch or fix]
Recommended action: [the one thing the executive should approve or act on]

---

PRIMARY KPI PERFORMANCE
Metric: [the north-star metric for this period]
Goal: [target]
Actual: [result]
vs. Prior period: [% change]
vs. Same period last year: [% change if available]
Trend: [3-period sparkline description or chart reference]
Analysis: [2 to 3 sentences explaining the result]

---

DEMAND GENERATION
New MQLs: [actual vs. goal vs. prior period]
MQL to SQL conversion rate: [actual vs. target]
Pipeline generated: [actual vs. goal]
CPL (cost per lead): [actual vs. target]
Top channel for MQLs this period: [channel + volume + % of total]
Bottom channel: [channel + volume + note on cause if known]
Analysis: [what drove demand gen performance this period]

---

CONTENT PERFORMANCE
Organic sessions: [actual vs. goal vs. prior period]
Top 3 pages by traffic: [URL + sessions + change]
New keyword rankings: [notable gains or losses]
Content-attributed leads: [if tracked]
Newsletter: [subscribers + open rate + click rate vs. benchmarks]
Analysis: [what drove content performance]

---

CHANNEL PERFORMANCE BREAKDOWN
For each active channel:
Channel | Spend | Leads | CPL | Conv. Rate | MoM change | Notes

---

BRAND AND AWARENESS (if tracked)
Share of voice vs. key competitors: [if tracked]
Media mentions: [count and notable placements]
Social following growth: [by platform]
Branded search volume trend: [increasing / stable / decreasing]

---

ANOMALIES AND FLAGS
[List any metric that was significantly above or below expectation, any tracking issue
detected, any external factor that affected performance, and any channel or campaign
that warrants investigation.]
Anomaly | Observed | Expected | Likely cause | Recommended action

---

RECOMMENDED ACTIONS
1. [Specific action: what to do, by whom, by when, and why]
2. [Specific action]
3. [Specific action]

---

APPENDIX: FULL DATA TABLES
[Reference to dashboard or attached data for readers who want full detail]
```

---

## Starter Prompt

```
You are a marketing analyst writing a marketing performance report.

Reporting period: [month / quarter]
Primary KPI and goal: [the north-star metric and target]
Actual results: [key numbers for this period]
Prior period results: [for comparison]
Channel breakdown: [performance by channel]
Anomalies: [anything that was surprising or broken]
Distribution: [who will read this report]

Produce a complete marketing metrics report.
The executive summary must start with a one-sentence headline finding.
Every anomaly must have a likely cause and a recommended action.
Recommended actions must be specific: who does what by when.
```

---

*Skill file version: 1.0 | Phase: 09 - Marketing | Company type: Product*
