# sre-runbook.md

> **Skill:** Produces a Site Reliability Engineering (SRE) runbook that defines SLOs, error budgets, toil reduction targets, and operational procedures for a production service.

---

## TLDR

An SRE runbook extends the operational runbook with SRE-specific concepts: Service Level Objectives, error budget tracking, toil measurement and reduction, and the reliability work backlog. It is the document that operationalizes the reliability posture of a service. Used by SRE teams and engineering teams with SRE practices.

---

## Topic Explanation

### SLIs, SLOs, and SLAs

**SLI (Service Level Indicator):** A specific metric that measures a dimension of service quality. Availability rate, latency p99, error rate.

**SLO (Service Level Objective):** The target value for an SLI. "Availability > 99.9% over a 30-day window." Internal commitment. Not contractual.

**SLA (Service Level Agreement):** The contractual commitment to customers. Usually less aggressive than the SLO, with defined remedies for breaches. Legal commitment.

The hierarchy: SLO is the internal target. SLA is the customer commitment. SLOs should be more aggressive than SLAs to provide a buffer.

### Error Budget

The error budget is the allowed amount of unreliability in a given period. If the SLO is 99.9% availability, the error budget is 0.1%: about 43 minutes of downtime per 30 days.

The error budget is a shared resource owned by both SRE and product engineering. When the error budget is healthy (not being consumed), product engineering can move fast. When the error budget is depleted, reliability work takes priority over new feature work.

### Toil

Toil is manual, repetitive operational work that scales with service volume and has no enduring value. Responding to alerts that require the same manual fix every time. Running manual deployment steps. Scaling resources manually.

SRE teams aim to keep toil below 50% of their time. Toil above this level prevents reliability improvement work. The SRE runbook should track toil sources and the automation work that eliminates them.

---

## Output Format

```
1. SRE RUNBOOK HEADER
   Service, SRE owner, product engineering owner, last updated.

2. SERVICE RELIABILITY OVERVIEW
   Service tier: Tier 1 (critical) / Tier 2 (important) / Tier 3 (standard).
   Business impact of downtime.
   Recovery Time Objective (RTO): maximum acceptable downtime.
   Recovery Point Objective (RPO): maximum acceptable data loss.

3. SERVICE LEVEL OBJECTIVES

   For each SLI/SLO:
   | SLI | SLO Target | Measurement Window | Current 30-day | Trend |
   | Availability | 99.9% | 30 days | 99.95% | Stable |
   | p99 latency | < 500ms | 7 days | 340ms | Stable |
   | Error rate | < 0.1% | 24 hours | 0.03% | Stable |

4. ERROR BUDGET
   Current error budget remaining.
   Budget consumption rate.
   Budget policy: what triggers reliability freeze.
   Error budget stakeholders: who reviews budget status.

5. RELIABILITY INCIDENTS
   Incidents in the last 90 days with error budget impact.
   Recurring patterns.

6. TOIL REGISTER
   Current sources of toil.
   For each: description / frequency / hours/week / automation status / priority.
   Toil as % of SRE time: current and target.

7. RELIABILITY WORK BACKLOG
   Infrastructure improvements.
   Automation projects.
   Monitoring improvements.
   Ordered by reliability impact.

8. INCIDENT RESPONSE

   Alert → Triage → Mitigation → Resolution → Post-mortem

   ALERT RESPONSE PLAYBOOKS:
   For each alert:
   - Alert name and condition
   - Immediate triage steps
   - Mitigation options
   - Escalation trigger

9. CAPACITY PLANNING
   Current resource utilization.
   Growth projections.
   Scaling triggers and procedures.

10. RELIABILITY REVIEW CADENCE
    Weekly: error budget review.
    Monthly: toil review and SLO trending.
    Quarterly: reliability roadmap review.
```

---

## Starter Prompt

```
You are an SRE writing an SRE runbook for a production service.

Service: [name and tier]
SLIs and SLOs: [the indicators and targets]
Current reliability status: [recent error budget consumption]
Known toil sources: [manual operational work]
Reliability work backlog: [planned reliability improvements]
Alert inventory: [current alerts and their response procedures]

Produce a complete SRE runbook covering SLOs, error budget policy,
toil register, reliability work backlog, and incident response playbooks.
Every alert must have a triage procedure and escalation trigger.
```

---

*Skill file version: 1.0 | Phase: 05 - Engineering | Company type: Product*
