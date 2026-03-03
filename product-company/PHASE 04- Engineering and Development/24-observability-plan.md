# observability-plan.md

> **Skill:** Produces an observability plan that defines the logging, metrics, tracing, and alerting strategy for a service, ensuring teams can understand and diagnose production system behavior.

---

## TLDR

An observability plan defines how a service will be instrumented to answer the question: *"What is happening in production right now, and when something goes wrong, can we understand why?"* It covers the three pillars of observability (logs, metrics, traces), the alerting strategy, and the dashboards that make system behavior visible. Written before a service launches and updated as the service evolves.

---

## Topic Explanation

### The Three Pillars of Observability

**Logs:** Timestamped records of events. Best for debugging specific incidents. The challenge: high volume, costly to query at scale. Log selectively: errors always, key business events always, debug logs in dev only.

**Metrics:** Numeric measurements over time. Best for dashboards, alerts, and trend analysis. Low cost at high volume. Cannot reconstruct event sequences. Key metrics: request rate, error rate, latency (RED method), and resource utilization (USE method).

**Traces:** Request flows across service boundaries. Best for diagnosing latency in distributed systems and understanding which service is responsible for slowness. More complex to implement.

### The RED Method for Service Metrics

The RED method (Tom Wilkie) defines the three metrics every service should have:
- **R - Rate:** Requests per second
- **E - Errors:** Error rate (errors per second or error percentage)
- **D - Duration:** Request latency (p50, p95, p99)

Every service should have RED metrics before it goes to production. If a service doesn't have RED metrics, on-call engineers cannot answer basic questions about its health.

### Alert Design Principles

**Alert on symptoms, not causes.** Alert when users are experiencing problems. "Error rate > 5%" is a symptom alert. "Redis CPU > 80%" is a cause alert. Cause alerts produce noise; symptom alerts produce signal.

**Every alert must be actionable.** If an alert fires and the on-call engineer cannot do anything about it, the alert is noise. Alerts with no runbook are noise.

**Avoid alert fatigue.** Too many alerts trains on-call engineers to ignore alerts. Fewer, higher-quality alerts are better than many low-quality ones.

---

## Output Format

```
1. OBSERVABILITY OVERVIEW
   Service, team, platforms used (logging, metrics, tracing tools).
   Current observability gaps being addressed.

2. LOGGING STRATEGY
   Log levels and when to use each.
   Structured logging format (JSON fields and schema).
   What is always logged: errors, key business events.
   What is never logged: PII, secrets, credentials.
   Log retention policy.
   Log aggregation platform and access.

3. METRICS STRATEGY
   RED metrics for this service (rate, error, duration).
   Business metrics: what key business events to measure.
   Infrastructure metrics: resource utilization.
   Metrics naming convention.
   Metrics platform and access.

4. DISTRIBUTED TRACING
   Tracing platform used.
   Which operations are traced.
   Sampling rate.
   Context propagation: how trace IDs are passed between services.

5. DASHBOARDS
   For each dashboard:
   - Dashboard name and link
   - Intended audience and use case
   - Panels included with description

6. ALERTING STRATEGY
   Alerting philosophy: symptom-based, actionable, runbook-linked.
   
   For each alert:
   - Alert name
   - Condition: metric / threshold / duration
   - Severity: P1 / P2 / P3
   - Runbook link
   - Escalation path
   - Suppression conditions (e.g., maintenance windows)

7. ON-CALL GUIDE
   How to access dashboards and logs.
   How to query traces.
   Baseline metric values (so on-call knows what "normal" looks like).

8. INSTRUMENTATION REQUIREMENTS
   For each new feature: what must be instrumented before it ships.
   Definition of Done observability checklist.
```

---

## Starter Prompt

```
You are a senior engineer writing an observability plan.

Service: [name and what it does]
Tech stack: [language, framework]
Scale: [request rate, data volume]
Observability platforms: [logging / metrics / tracing tools in use]
Business events to track: [key user actions and outcomes to measure]
Known failure modes: [what has gone wrong before or could go wrong]
On-call team: [who will be paged]

Produce a complete observability plan covering logging strategy,
RED metrics, business metrics, alerting with runbook links,
and dashboards.
Every alert must have a runbook reference.
Flag any failure mode without an alert or detection mechanism.
```

---

*Skill file version: 1.0 | Phase: 05 - Engineering | Company type: Product*
