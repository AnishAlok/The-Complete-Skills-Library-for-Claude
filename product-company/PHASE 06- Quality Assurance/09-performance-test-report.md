# performance-test-report.md

> **Skill:** Produces a QA-focused performance testing results report documenting SLO pass/fail results, bottleneck findings, and the release quality gate verdict.

---

## TLDR

A QA performance test report documents whether the system meets its performance SLOs: which test scenarios passed and failed, where bottlenecks were identified, and the release quality gate decision. Focused on the go/no-go verdict for release rather than engineering capacity analysis (which is covered by performance-benchmarks.md in Phase 05 Engineering).

---

## Topic Explanation

### Performance Testing as a QA Gate

Performance testing in QA is a release gate: before a release ships, QA confirms that performance SLOs are met. The report documents that gate with a clear pass/fail verdict, not just observations and data.

This is the critical distinction from an engineering performance benchmark report. QA asks: "Is the system ready to ship from a performance perspective?" Engineering asks: "Where are the bottlenecks and how do we optimize capacity?"

### SLO Types Verified in QA Performance Testing

**Response time SLOs:** specific API endpoint or page load time targets at defined percentiles under expected peak load. Example: "Search results must return within 2 seconds at p95 under 500 concurrent users."

**Throughput SLOs:** the system must handle N transactions per second without error rate degradation.

**Error rate SLOs:** error rate must remain below X% under expected peak load.

**Resource SLOs:** CPU and memory must not exceed Y% of available capacity at peak load.

### Coordination with Engineering

The QA performance test report and the engineering performance-benchmarks.md cover the same test execution from different perspectives. Both reference the same test run data. QA focuses on the release gate verdict. Engineering focuses on capacity planning and optimization analysis.

---

## Output Format

```
1. REPORT HEADER
   Release version, test date, QA lead, test environment, tools used.
   Reference to engineering benchmark report for full capacity analysis.

2. EXECUTIVE SUMMARY
   Overall result: PASS / FAIL / CONDITIONAL PASS.
   SLOs tested: [N total]. SLOs passed: [N]. SLOs failed: [N].
   Blocking findings summary.

3. SLO RESULTS TABLE

   SLO ID | Description | Target | Actual | Result
   PERF-01 | Search API p95 response | < 2.0s | 1.8s | PASS
   PERF-02 | Checkout error rate at 500 RPS | < 0.5% | 1.2% | FAIL
   PERF-03 | Dashboard page load p99 | < 5.0s | 4.1s | PASS

4. TEST SCENARIOS EXECUTED
   For each scenario:
   - Scenario name and purpose
   - Load profile: concurrent users or RPS, duration
   - SLOs measured
   - Pass/fail summary

5. FAILED SLOs - DETAIL
   For each failing SLO:
   - Description and target
   - Actual measured value and test conditions when failure occurred
   - Severity classification: blocks release / must fix before next sprint / monitor
   - Engineering findings reference (link to benchmark report)
   - Remediation required: owner and target date

6. CONDITIONAL PASS ITEMS
   Any SLO conditionally passed with documented mitigation or accepted risk.
   Owner of the condition and verification method.

7. QUALITY GATE VERDICT

   PASS: All SLOs met. System is approved for release from a performance perspective.

   CONDITIONAL PASS: System is approved for release subject to:
   [list specific conditions]

   FAIL: System does not meet performance requirements.
   The following SLO failures block release: [list]

8. REMEDIATION TRACKING
   For each failing item: owner, fix approach, retest date.
```

---

## Starter Prompt

```
You are a QA engineer producing a performance test report for a release.

Release: [version]
Performance SLOs: [the target for each measured metric]
Test scenarios run: [load profiles applied]
Results: [actual values under each test scenario]
Failing SLOs: [which targets were not met]
Release disposition: [pass / fail / conditional]

Produce a complete performance test report with SLO results table,
detailed failure analysis for each failing SLO, quality gate verdict,
and remediation tracking.
Every failing SLO must be classified as blocking release or non-blocking.
```

---

*Skill file version: 1.0 | Phase: 07 - Quality Assurance | Company type: Product*
