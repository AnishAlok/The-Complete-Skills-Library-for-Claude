# incident-report.md

> **Skill:** Produces an incident post-mortem document that captures a timeline of events, root cause analysis, contributing factors, impact assessment, and action items to prevent recurrence.

---

## TLDR

This skill helps you answer: *"What happened, why did it happen, how bad was it, and what are we doing to prevent it from happening again?"* An incident post-mortem is a blameless investigation of a production incident. It produces a permanent record of the event and the systemic improvements made in response. Used after any significant production incident or outage.

---

## Topic Explanation

### Blameless Post-Mortems

The foundational principle of post-mortem culture, established at Google and widely adopted across the industry: post-mortems must be blameless. People acted given the information available at the time. The goal is to identify and fix systemic factors, not to assign personal blame.

Blameless post-mortems produce better outcomes because:
- Engineers report incidents promptly rather than hiding problems out of fear
- Root cause analysis goes deeper than "engineer made a mistake"
- Systemic fixes are identified rather than performative discipline
- The organization learns rather than just punishing

The blameless framing does not mean "without accountability." Engineers are accountable for participating in the post-mortem and implementing improvements. They are not accountable in a punitive sense for being part of a system that had failure modes.

### The Five Whys

The Five Whys technique, originating from Toyota's production system, is the most widely used root cause analysis tool for incident post-mortems. Starting with the symptom, ask "why?" repeatedly until the systemic root cause is reached.

Example:
- Why did the service go down? Because the database ran out of connections.
- Why did the database run out of connections? Because connection pool exhaustion was not monitored.
- Why was it not monitored? Because we had no standard for which database metrics to alert on.
- Why did we have no standard? Because our monitoring setup process predates our current database usage patterns.
- Root cause: Monitoring setup process is not updated as infrastructure scales.

The fix is now systemic (update the monitoring setup process) rather than tactical (add one more alert for this one database).

### Incident Severity Levels

Standard severity classification used in most on-call systems:

**SEV-1 (Critical):** Full service outage. All customers impacted. Requires immediate all-hands response. Post-mortem required.

**SEV-2 (Major):** Significant degradation. Large percentage of customers impacted or core functionality broken. Post-mortem required.

**SEV-3 (Minor):** Partial degradation. Limited customer impact. Internal functionality affected. Post-mortem encouraged for repeat incidents.

**SEV-4 (Low):** Minor issues. Minimal customer impact. Log and monitor.

---

## When to Use This Skill

Use when:
- Any SEV-1 or SEV-2 incident has been resolved
- A SEV-3 incident recurs
- A near-miss occurs that had significant potential impact
- A deployment caused unexpected production issues

---

## Dos

- **Do hold the post-mortem within 48 to 72 hours of incident resolution.** Details fade quickly. Timeline reconstruction is more accurate when immediate.
- **Do start with the timeline before the root cause.** A complete timeline often reveals the root cause more clearly than jumping directly to analysis.
- **Do include contributing factors alongside the root cause.** Root causes rarely operate alone. Contributing factors are often where the most actionable improvements are found.
- **Do make action items specific, owned, and time-bound.** "Improve monitoring" is not an action item. "Add P95 latency alert for the payment service by [date], owned by [name]" is.
- **Do track action item completion.** A post-mortem whose action items are never completed produces the illusion of learning without the substance.

---

## Donts

- **Dont use blame language.** "The engineer incorrectly configured the deployment" focuses on the person. "The deployment configuration had insufficient validation" focuses on the system.
- **Dont declare root cause before completing the Five Whys analysis.** The first "why" answer is rarely the root cause. It is usually a proximate cause.
- **Dont skip the timeline section.** The timeline is the most important section for understanding the full sequence of events, including why detection was delayed.

---

## Output Format

```
1. INCIDENT SUMMARY
   Incident title, date and time (start / detected / resolved),
   duration, severity, services affected, customers impacted,
   incident commander, post-mortem author, review date.

2. EXECUTIVE SUMMARY (4 to 6 sentences)
   What happened, how it was detected, how long it lasted,
   customer impact, and the root cause in plain language.

3. IMPACT ASSESSMENT
   Customer-facing impact: what could customers not do?
   Scope: what percentage of customers were affected?
   Financial impact (if calculable).
   SLA implications.
   Reputational considerations.

4. TIMELINE
   Chronological log of events from first symptom to full resolution.
   Format: [Timestamp UTC] [Actor] [Action or observation]
   Include: first alert / detection / escalation / mitigation attempts /
   resolution / all-clear.
   Mark: when customer impact began / when customer impact ended.

5. ROOT CAUSE ANALYSIS
   The Five Whys analysis.
   The identified root cause (the systemic failure, not the proximate symptom).
   Supporting evidence.

6. CONTRIBUTING FACTORS
   Other factors that made the incident worse or harder to detect/resolve.
   Each contributing factor is a candidate for an action item.

7. WHAT WENT WELL
   Actions taken that limited impact, accelerated resolution, or
   demonstrated effective incident response.
   These should be reinforced and systematized.

8. WHAT WENT POORLY
   Actions or omissions that delayed detection, extended duration,
   or increased impact.
   Framed as system failures, not personal failures.

9. ACTION ITEMS
   For each action item:
   - Description: specific, concrete improvement
   - Type: preventive / detective / corrective / process
   - Owner: named individual
   - Due date
   - Priority: P1 / P2 / P3
   - Status: open / in progress / complete

10. LESSONS LEARNED
    Insights applicable to the broader engineering organization.
    Changes to engineering practices, processes, or standards.

11. APPENDIX
    Links to monitoring dashboards, logs, and relevant data.
    Support ticket references.
    Communication thread links.
```

---

## Starter Prompt

```
You are an engineer writing a post-mortem for a production incident.

Incident: [brief description of what happened]
Timeline: [chronological sequence of events with timestamps]
Severity: [SEV-1 / SEV-2 / SEV-3]
Services affected: [what systems were involved]
Customer impact: [what customers experienced and for how long]
Root cause hypothesis: [initial understanding of what caused it]
Contributing factors: [other factors that made it worse]
What went well: [effective response actions]
Action items identified: [improvements being made]

Please produce a complete blameless post-mortem including:
1. Executive summary in plain language
2. Impact assessment with scope and duration
3. Full timeline from first symptom to all-clear
4. Five Whys root cause analysis
5. Contributing factors
6. What went well and what went poorly sections
7. Specific, owned, time-bound action items with priority
8. Lessons learned for the broader organization

Use blameless language throughout: system failures, not personal failures.
Flag if the root cause analysis stops at a proximate cause rather than
continuing to a systemic root cause.
```

---

## Related Skills

| Use This Next | Why |
|---|---|
| `runbook.md` | Action items often produce new runbook entries |
| `sre-runbook.md` | SRE runbooks are updated based on incident learnings |
| `observability-plan.md` | Detection gaps found in incidents improve the observability plan |

*Skill file version: 1.0 | Phase: 05 - Engineering | Company type: Product*
