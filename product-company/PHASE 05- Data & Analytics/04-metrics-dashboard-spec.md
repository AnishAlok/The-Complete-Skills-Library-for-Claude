# metrics-dashboard-spec.md

> **Skill:** Produces a dashboard specification that defines the metrics, dimensions, visualizations, filters, and data sources for a business intelligence or product analytics dashboard.

---

## TLDR

A dashboard spec is the requirements document for a dashboard: what metrics to show, how to visualize them, what filters to provide, what the data sources are, and who the audience is. Written before dashboard development begins to ensure the dashboard answers the right questions for the right audience rather than being rebuilt after delivery.

---

## Topic Explanation

### Dashboard Design Principles

**One audience, one purpose.** A dashboard trying to serve the board, the product team, and customer success simultaneously serves none of them well. Define one primary audience and their core question.

**Lead with the most important number.** The primary metric should be the first thing the viewer sees, with full context (trend, target, variance from target).

**Contextualize every metric.** A number without context is a guess. Always show: trend over time, comparison to target, comparison to prior period.

**Limit to 10 to 12 metrics.** A dashboard with 30 metrics is not a dashboard; it is a data dump. Force prioritization.

**Design for the question, not the data.** "What data do we have?" produces bad dashboards. "What question does the audience need to answer?" produces useful ones.

### Visualization Choice

**Single KPI:** One number with trend indicator. Best for the headline metric.
**Line chart:** Trends over time. Best for continuous metrics.
**Bar chart:** Comparisons across categories. Best for ranked items.
**Stacked bar:** Part-to-whole over time. Best for composition changes.
**Funnel:** Sequential conversion steps. Best for activation and conversion flows.
**Table:** Detailed breakdown with multiple dimensions. Best for drill-down.
**Heatmap:** Two-dimensional patterns. Best for day-of-week or time-of-day analysis.

Match the visualization to the insight type, not personal preference.

---

## Output Format

```
1. DASHBOARD SPEC HEADER
   Dashboard name, owner, audience, purpose, platform, refresh cadence.

2. AUDIENCE AND PURPOSE
   Who is the primary audience?
   The single question this dashboard must answer.
   How the audience will use this dashboard (daily monitoring / weekly review / ad hoc).

3. DASHBOARD LAYOUT

   SECTION 1: [Section name]
   For each panel in this section:
   - Panel name
   - Metric(s) shown
   - Visualization type
   - Time range and granularity
   - Comparison: prior period / target / benchmark
   - Filters that apply

   [Repeat for each section]

4. METRIC DEFINITIONS
   For each metric shown:
   - Name
   - Definition (or cross-reference to data dictionary)
   - Calculation
   - Data source and table
   - Refresh frequency

5. FILTERS AND DIMENSIONS
   Global filters available to the viewer.
   Panel-specific filters.
   Default filter values.

6. DATA SOURCES
   For each data source:
   - Table or view name
   - Grain
   - Update frequency
   - Owner

7. PERFORMANCE REQUIREMENTS
   Expected load time.
   Data freshness requirement.
   Concurrent user expectation.

8. ACCESS AND PERMISSIONS
   Who can view.
   Who can edit.
   Embed or sharing requirements.

9. ACCEPTANCE CRITERIA
   How the requester will validate the dashboard before sign-off.
   Test cases with expected values.
```

---

## Starter Prompt

```
You are a data analyst writing a dashboard specification.

Dashboard purpose: [what question this dashboard answers]
Audience: [who will use it and how often]
Key metrics: [the metrics to display]
Dimensions and filters: [how viewers will slice the data]
Data sources: [where the data lives]
Platform: [Looker / Tableau / Mode / Metabase / etc.]
Refresh requirement: [how fresh the data must be]

Produce a complete dashboard spec with layout, metric definitions,
visualization choices, and acceptance criteria.
Every metric must have a definition and data source.
Limit the spec to 12 or fewer distinct metrics.
```

---

*Skill file version: 1.0 | Phase: 06 - Data and Analytics | Company type: Product*
