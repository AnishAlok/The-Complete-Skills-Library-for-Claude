# runbook.md

> **Skill:** Produces an operational runbook for a service or system that guides engineers through common operational tasks, troubleshooting procedures, and routine maintenance.

---

## TLDR

A runbook is the operational manual for a service: the document an on-call engineer reaches for at 2am when something is wrong. It covers how the service works, how to access it, common failure modes and their remedies, and routine operational tasks. Written to be usable under pressure by someone who may not be deeply familiar with the service.

---

## Topic Explanation

### Writing for the 2am Reader

The defining constraint of a good runbook: it must be usable by an engineer who is tired, under stress, and may be encountering this system for the first time at 2am when something is broken.

This means:
- No assumed knowledge: state what commands to run, not just "restart the service"
- Copy-pasteable commands: reduce the chance of typos under stress
- Numbered steps for each procedure: no ambiguity about sequence
- Decision trees for branching scenarios: "if X then do Y, if Z then do W"
- Quick links at the top: dashboards, logs, escalation contacts

### Runbooks vs. Documentation

**Documentation:** Explains how things work. For understanding and learning.
**Runbook:** Explains what to do. For execution under operational pressure.

A runbook references documentation but does not duplicate it. The runbook procedure says "restart the worker service with [command]." The documentation says "here is how the worker service processes jobs and why it occasionally gets stuck."

---

## Output Format

```
1. RUNBOOK HEADER
   Service name, owner team, on-call rotation, last updated, version.

2. QUICK REFERENCE
   Dashboard links.
   Log locations.
   Escalation contacts with Slack handles and phone.
   Key environment variables and config locations.

3. SERVICE OVERVIEW
   What this service does in 2 to 3 sentences.
   Key dependencies: what it calls and what calls it.
   Scale: expected traffic and normal resource usage.

4. ACCESS AND AUTHENTICATION
   How to access the service's host / container / cluster.
   Required credentials and where to find them.
   Access verification command.

5. HEALTH CHECK
   How to verify the service is healthy.
   Expected output of health check.
   What an unhealthy response looks like.

6. COMMON OPERATIONAL TASKS
   For each task (e.g., restart service, scale up, flush cache, run migration):
   - Task name
   - When to perform it
   - Exact commands (copy-pasteable)
   - Expected output
   - Verification step

7. TROUBLESHOOTING GUIDE
   For each known failure mode:
   - Symptom / alert name
   - How to diagnose (commands + expected output)
   - Remediation steps
   - Escalation trigger: if remediation does not work within X minutes, escalate to Y

8. INCIDENT RESPONSE
   Severity assessment guide: how to classify the incident.
   Immediate mitigation options (rollback, feature flag, kill switch).
   Communication template for customer impact.

9. MAINTENANCE PROCEDURES
   Scheduled maintenance tasks with procedure and frequency.
   How to put the service into maintenance mode.

10. KNOWN ISSUES AND WORKAROUNDS
    Current known limitations with workarounds.
```

---

## Starter Prompt

```
You are an engineer writing an operational runbook for a service.

Service: [name and brief description]
Owner team and on-call: [who maintains it]
Key dependencies: [what it connects to]
Common failure modes: [known things that go wrong]
Routine operational tasks: [regular maintenance needed]
Access method: [how engineers access the service]
Monitoring links: [dashboards and log locations]
Escalation path: [who to call when problems exceed the runbook]

Produce a complete operational runbook designed for use under pressure by
an on-call engineer who may be unfamiliar with the service.
All commands must be exact and copy-pasteable.
Every troubleshooting procedure must include a "when to escalate" trigger.
```

---

*Skill file version: 1.0 | Phase: 05 - Engineering | Company type: Product*
