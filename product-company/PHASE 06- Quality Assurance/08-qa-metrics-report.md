# qa-metrics-report.md

> **Skill:** Produces a QA metrics report covering test coverage, pass rates, defect density, defect escape rate, and testing efficiency metrics that communicate quality health to technical and business audiences.

---

## TLDR

A QA metrics report quantifies the health of the testing process and the quality of software being shipped. It answers: how well are we testing, how much is passing, how many defects are we finding vs. missing, and is quality improving or degrading over time? Used weekly or monthly by QA leads, engineering managers, and product leadership.

---

## Topic Explanation

### The QA Metrics That Matter

**Test coverage:** percentage of requirements or user stories covered by at least one test case. A baseline measure of testing completeness.

**Test pass rate:** percentage of executed test cases that passed. A high pass rate near release is expected; a very high pass rate early in testing may indicate insufficient negative test cases.

**Defect density:** defects found per unit of software (per feature, per story point). Identifies high-defect areas needing engineering attention.

**Defect escape rate:** defects that reached production vs. total defects found. The most important quality metric. A high escape rate means customers are finding defects that QA missed.

**Mean time to detect (MTTD):** how long after a defect is introduced before QA finds it. Lower is better. Correlates with shift-left testing maturity.

**Mean time to resolve (MTTR):** how long open defects take to be fixed. Indicates engineering responsiveness to quality issues.

**Automation coverage:** percentage of test cases that are automated. Higher coverage enables faster regression cycles.

### Defect Escape Rate: The Most Important Metric

Escape rate = (Production-found defects / Total defects found) x 100%

A team finding 100 total defects, 10 of which were found by customers in production, has a 10% escape rate. Most mature QA teams target below 5% for critical functionality. Track by functional area to identify where the testing strategy has gaps.

A rising escape rate is a signal that the testing approach is not keeping pace with the product's complexity or change velocity.

---

## Output Format

```
1. REPORT HEADER
   Period, QA lead, date, intended audience.

2. EXECUTIVE SUMMARY
   Overall quality health: Green / Amber / Red.
   Headline metric and its trend direction.
   Key concern requiring attention.
   Recommended action.

3. TEST EXECUTION METRICS
   Coverage: requirements and user stories with at least one test case.
   Execution breakdown: planned / executed / passed / failed / blocked / not run.
   Pass rate trend vs. prior 3-6 periods.

4. DEFECT METRICS
   Open defects by severity: S1 / S2 / S3 / S4.
   Opened this period / Resolved this period / Net change.
   Defects aging over 30 days (requiring attention).
   Defect density by feature area.
   Defect escape rate: calculation shown, trend displayed.

5. PROCESS EFFICIENCY METRICS
   MTTD: average time from code merge to defect detection. Trend.
   MTTR by severity: S1 target and actual / S2 target and actual / S3 target and actual.

6. AUTOMATION METRICS
   Total test cases vs. automated (percentage).
   Automation pass rate this period.
   Flaky test count requiring investigation.
   Coverage trend: automation percentage over time.

7. TRENDS AND ANALYSIS
   3 to 6 period trend for all key metrics.
   Areas showing measurable improvement.
   Areas showing measurable degradation.

8. RECOMMENDATIONS
   Specific actions to address identified quality gaps.
   Process changes indicated by metric trends.
   Owner suggested for each recommendation.
```

---

## Starter Prompt

```
You are a QA lead producing a metrics report.

Period: [sprint / month / week]
Audience: [QA team / engineering management / product leadership]
Test execution data: [planned, executed, passed, failed, blocked, not run]
Defect data: [opened, resolved, open by severity, by feature area]
Production defects this period: [customer-found defects for escape rate calculation]
Automation status: [automated vs. manual test case counts]
Prior period data: [for trend comparison]
MTTR data: [defect resolution times by severity]

Produce a complete QA metrics report with executive summary,
all metric categories, trend analysis, and recommendations.
Escape rate must be calculated and prominently displayed.
Flag every metric that degraded significantly vs. the prior period.
```

---

*Skill file version: 1.0 | Phase: 07 - Quality Assurance | Company type: Product*
