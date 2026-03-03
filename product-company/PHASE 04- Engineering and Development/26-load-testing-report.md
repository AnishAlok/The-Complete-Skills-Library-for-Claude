# load-testing-report.md

> **Skill:** Produces a load and stress test documentation report covering test objectives, methodology, load profiles, results analysis, bottleneck findings, and capacity recommendations.

---

## TLDR

A load testing report documents the results of load and stress testing a system: the methodology, the load profiles applied, the performance observed under each profile, the bottlenecks identified, and the capacity and scaling recommendations that follow. Used before major launches, after significant architecture changes, and as regular capacity planning input.

---

## Topic Explanation

### Load Testing Types (and When to Use Each)

**Load test:** Validate that the system meets performance SLOs under expected peak load. "Can we handle 1,000 concurrent users at our p99 latency target?"

**Stress test:** Find the system's breaking point. Increase load beyond expected peak until the system fails or degrades unacceptably. "What is our maximum capacity and what fails first?"

**Soak test (endurance test):** Run at sustained load for an extended period (hours or days). Find resource leaks, connection pool exhaustion, gradual memory growth. "Will the system degrade over time under normal load?"

**Spike test:** Apply a sudden, sharp increase in load. "Can the system handle a 10x traffic spike in 30 seconds (marketing campaign, viral event)?"

A complete pre-launch test suite typically includes a load test and a stress test at minimum. Soak and spike tests for services with those specific risk profiles.

### Virtual Users vs. Requests Per Second

Most load testing tools model load as virtual users (VUs): simulated users executing a scenario concurrently. The relationship between VUs and RPS depends on think time (the time a user spends between requests). A VU with zero think time generates maximum RPS. A VU with 3-second think time generates about 0.33 RPS.

Modeling with realistic think time produces more accurate load simulation. Modeling with zero think time finds the raw throughput ceiling.

### Percentile Latency Under Load

Latency percentiles typically degrade as load increases. The p99 degrades much faster than the p50 as the system approaches saturation. Plotting p50, p95, and p99 latency against load level shows when tail latency starts to degrade significantly, which is often the practical capacity limit even if the system has not yet hit error rate thresholds.

---

## Output Format

```
1. TEST REPORT HEADER
   Service, test date, lead engineer, environment, tools, version tested.

2. TEST OBJECTIVES
   What questions this test answers.
   SLOs being validated.
   Specific risks being investigated.

3. TEST ENVIRONMENT
   Infrastructure: instance types, counts, auto-scaling config.
   Network configuration.
   Test data: volume and characteristics.
   Tool: k6 / Locust / Gatling / Artillery / JMeter.
   Monitoring: what was observed during the test.

4. TEST SCENARIOS AND LOAD PROFILES
   For each test scenario:
   - Test type: load / stress / soak / spike
   - Load profile: VU count / ramp-up duration / steady state / ramp-down
   - Endpoints exercised with relative distribution
   - Think time model

5. RESULTS

   SLO VALIDATION TABLE:
   | SLO | Target | Achieved | Pass/Fail | At what load level |

   LATENCY BY LOAD LEVEL:
   | Load (RPS or VUs) | p50 | p95 | p99 | Error rate |

   BREAKING POINT (stress test):
   Maximum sustained load before SLO breach.
   First failure mode observed.
   Second and third failure modes.

   SOAK TEST RESULTS (if run):
   Metric trends over time: memory, connection pool, latency.
   Resource exhaustion observed? When?

   SPIKE TEST RESULTS (if run):
   Spike profile: baseline → peak → baseline.
   Latency and error rate during spike.
   Recovery time after spike.

6. RESOURCE UTILIZATION AT LOAD
   CPU, memory, DB connections, I/O at key load levels.
   Which resource constrained first.

7. BOTTLENECK ANALYSIS
   Primary bottleneck: the resource or component that limited throughput.
   Supporting evidence.
   Secondary bottlenecks.

8. CAPACITY RECOMMENDATIONS
   Safe operating capacity: recommended maximum traffic before scaling.
   Scaling strategy: horizontal / vertical / which component to scale.
   Autoscaling recommendation: trigger thresholds.
   Infrastructure changes required to meet SLOs.

9. FINDINGS AND ACTION ITEMS
   For each finding:
   - Severity: blocks launch / must fix / should fix / monitor
   - Description
   - Recommended action
   - Owner
   - Due date
```

---

## Starter Prompt

```
You are a performance engineer producing a load testing report.

Service: [what was tested]
Test types run: [load / stress / soak / spike]
Environment: [infrastructure and tools]
Test scenarios: [the load profiles applied]
SLO targets: [performance requirements being validated]
Results: [observed metrics at each load level]
Bottlenecks: [where the system was constrained]
Breaking point: [maximum load before SLO breach, if found]

Produce a complete load testing report including results tables,
bottleneck analysis, capacity recommendations, and prioritized action items.
Every SLO should show pass/fail status with the load level at which it was evaluated.
```

---

*Skill file version: 1.0 | Phase: 05 - Engineering | Company type: Product*
