# project-status-report.md

> **Skill:** Produces a project status report that communicates current status, progress against plan, key risks and issues, and upcoming milestones to project stakeholders.

---

## TLDR

A project status report answers: *"Where are we, are we on track, and what do stakeholders need to know or decide right now?"* It is the primary regular communication artifact between the PM and stakeholders. This skill produces a structured status report for weekly or monthly cadences, formatted for the appropriate audience.

---

## Topic Explanation

### The RAG Status System

Red / Amber / Green (RAG) is the standard visual status system for project reporting:

**Green:** On track. No significant issues. The project is proceeding as planned.
**Amber:** At risk. Issues exist but are being managed. Attention is needed but the project can still be delivered on time and budget with action.
**Red:** Off track. Significant issues that threaten delivery. Intervention required. Escalation may be needed.

RAG status should be assigned to: overall project, schedule, budget, scope, and quality separately. A project can be green on budget but amber on schedule.

### The Most Common Status Report Failure: Green-Washing

Green-washing is the systematic over-reporting of green status to manage stakeholder anxiety. It is understandable, organizationally damaging, and ubiquitous.

The consequence: by the time a project appears amber or red on the status report, it is usually much worse. Stakeholders receive no early warning, can take no early action, and lose trust in the PM when the true situation is revealed.

The PM's professional obligation is to report status accurately. An amber or red status report that enables early intervention is better for everyone than a false green report that delays necessary action.

### The Audience Principle

Status reports are audience-specific documents. A weekly technical status for the engineering team looks very different from a monthly executive status for the steering committee. Key differences:
- **Technical report:** Detailed, specific, includes open issues requiring team decisions
- **Executive report:** Summary, exception-based, includes decisions requiring executive authority

Both are needed. Sending the technical report to executives creates information overload. Sending the executive summary to the engineering team creates information deficit.

---

## Output Format

```
1. REPORT HEADER
   Project name, reporting period, report date, PM, audience.

2. EXECUTIVE SUMMARY (3 to 5 sentences)
   Overall status: RAG
   The single most important thing stakeholders need to know.
   Any action or decision required from stakeholders.

3. STATUS DASHBOARD
   | Dimension | Status | Last Period | Trend |
   | Overall   | 🟡 AMBER | 🟢 GREEN | Declining |
   | Schedule  | 🟡 AMBER | 🟢 GREEN | Declining |
   | Budget    | 🟢 GREEN | 🟢 GREEN | Stable |
   | Scope     | 🟢 GREEN | 🟢 GREEN | Stable |
   | Quality   | 🟢 GREEN | 🟢 GREEN | Stable |

4. PROGRESS THIS PERIOD
   Milestones completed.
   Key accomplishments.
   Percentage complete vs. plan.

5. UPCOMING NEXT PERIOD
   Milestones due.
   Key activities planned.
   Decisions needed.

6. RISKS AND ISSUES

   ACTIVE ISSUES (problems occurring now):
   For each: description / impact / owner / action / due date

   TOP RISKS (potential future problems):
   For each: description / probability / impact / mitigation

7. SCHEDULE STATUS
   Current milestone: on track / ahead / behind.
   Projected completion vs. planned.
   Variance explanation if behind.

8. BUDGET STATUS
   Spent to date vs. plan.
   Forecast to complete.
   Variance explanation if significant.

9. DECISIONS AND ACTIONS REQUIRED
   Any decision needed from stakeholders.
   Who must decide, by when, and what the consequence of delay is.

10. CHANGES SINCE LAST REPORT
    Approved scope changes.
    Timeline changes.
    Budget changes.
```

---

## Starter Prompt

```
You are a PM writing a project status report.

Project: [name and brief context]
Reporting period: [dates covered]
Audience: [team / PM / steering committee / executive]
Current status: [overall RAG and per-dimension RAG]
Progress this period: [what was completed]
Upcoming: [what is planned for next period]
Issues: [active problems and their impact]
Risks: [top risks and mitigation status]
Decisions needed: [any stakeholder decisions required]
Budget status: [spent vs. planned]
Schedule status: [on track / variance from plan]

Produce a complete status report formatted for the stated audience.
Be specific about RAG status and the specific reason for any amber or red rating.
Do not green-wash: report status accurately.
```

---

*Skill file version: 1.0 | Phase: 04 - Program and Project Management | Company type: Product*
