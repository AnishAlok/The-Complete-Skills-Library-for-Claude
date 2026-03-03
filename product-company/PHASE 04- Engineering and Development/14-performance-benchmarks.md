# performance-benchmarks.md

> **Skill:** Produces a performance testing report documenting baseline benchmarks, test methodology, results, bottleneck analysis, and optimization recommendations.

---

## TLDR

A performance benchmarks document captures the results of performance testing: what was tested, how, the baseline and post-change metrics, identified bottlenecks, and the actions being taken to address performance issues. Used before major launches, after significant architecture changes, and as a regular performance health check.

---

## Topic Explanation

### Performance Testing Types

**Baseline testing:** Measure current performance under normal load. Establishes the starting point for comparison.

**Load testing:** Test performance under expected peak load. Confirms the system can handle anticipated traffic.

**Stress testing:** Test performance beyond expected peak load to find the breaking point. Identifies failure modes under extreme conditions.

**Soak testing:** Test performance under sustained normal load over a long period. Finds memory leaks, connection pool exhaustion, and other resource degradation issues.

**Spike testing:** Test performance during sudden sharp increases in load. Confirms the system can handle traffic spikes (marketing campaigns, viral moments).

### Key Performance Metrics

**Latency percentiles:** p50 (median), p95, p99, p99.9. Percentiles are more informative than averages because averages hide the tail experience. The p99 latency is the experience of your worst 1% of requests. For user-facing APIs, p99 is often more important than p50.

**Throughput:** Requests per second the system can handle. At what throughput does latency degrade unacceptably?

**Error rate:** Percentage of requests that fail under load. Should remain at or near 0% under expected load.

**Resource utilization:** CPU, memory, database connections, I/O at load. Identifies which resource is the bottleneck.

---

## Output Format

```
1. BENCHMARK REPORT HEADER
   System/feature, test date, tester, environment, tools used, version tested.

2. TEST OBJECTIVES
   What performance questions this test answers.
   SLOs being validated.

3. TEST ENVIRONMENT
   Infrastructure: instance types, counts, configuration.
   Test data: volume and characteristics.
   Network conditions.
   Tools: k6 / Gatling / Locust / JMeter / etc.

4. TEST SCENARIOS
   For each scenario:
   - Scenario name and description
   - Load profile: users, ramp-up, duration, think time
   - What is being measured

5. RESULTS

   SLO COMPLIANCE SUMMARY:
   | Metric | SLO Target | Actual | Pass/Fail |

   LATENCY RESULTS (by scenario):
   | Endpoint | p50 | p95 | p99 | p99.9 | Max |

   THROUGHPUT RESULTS:
   | Scenario | Target RPS | Achieved RPS | Error rate at peak |

   RESOURCE UTILIZATION AT PEAK:
   | Resource | Baseline | At load | % used |

6. BOTTLENECK ANALYSIS
   Where the system degraded under load.
   Root cause of each bottleneck.
   Evidence (graphs, traces, query plans).

7. COMPARISON TO BASELINE
   If this is a change assessment: before vs. after metrics.
   Regressions identified.
   Improvements observed.

8. FINDINGS AND RECOMMENDATIONS
   For each performance issue:
   - Finding description
   - Severity: blocks launch / should fix / monitor
   - Recommended fix
   - Expected improvement
   - Owner

9. NEXT TEST PLAN
   When to retest.
   What to retest after optimizations.
```

---

## Starter Prompt

```
You are an engineer producing a performance benchmarks report.

System: [what was tested]
Test environment: [infrastructure and tools]
Test scenarios: [what load profiles were run]
SLO targets: [the performance requirements being validated]
Results: [key metrics from the test run]
Bottlenecks identified: [where performance degraded]
Baseline comparison: [before/after if applicable]

Produce a complete performance benchmarks report including results tables,
bottleneck analysis with evidence, and prioritized recommendations.
Flag any metric that fails to meet its SLO target.
Flag any finding that should block launch.
```

---

*Skill file version: 1.0 | Phase: 05 - Engineering | Company type: Product*
