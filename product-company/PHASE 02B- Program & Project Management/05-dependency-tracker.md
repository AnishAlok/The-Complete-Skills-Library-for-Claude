# dependency-tracker.md

> **Skill:** Produces a structured dependency tracker that documents all cross-team and external dependencies with owners, due dates, status, and escalation flags.

---

## TLDR

A dependency tracker is the operational document for managing everything your team needs from outside itself to deliver. Unlike the project plan (which tracks internal work) or the risk register (which tracks potential problems), the dependency tracker specifically tracks commitments from other teams and external parties. Used actively and reviewed weekly to prevent dependencies from becoming blockers.

---

## Topic Explanation

### Dependency Types

**Finish-to-start:** The most common. The depending team cannot start until the providing team finishes. Team A cannot build the UI until Team B delivers the API endpoint.

**Start-to-start:** Both teams must start at the same time. Running in parallel with a shared milestone.

**Finish-to-finish:** Both must finish at the same time. One team cannot finish without the other finishing.

**External dependencies:** Vendor deliverables, customer decisions, regulatory approvals, procurement.

### The Dependency Conversation

Tracking a dependency is only half the work. The other half is the conversation: confirming that the providing team knows about the dependency, has it in their plan, and can commit to the needed timeline.

A dependency that has not been confirmed with the providing team is a "hoped-for dependency" and should be flagged as unconfirmed in the tracker. Unconfirmed dependencies are risks.

### Status Categories

**Confirmed:** The providing team has committed to the deliverable and timeline.
**Pending:** The conversation has not happened yet or is in progress.
**At risk:** The providing team has flagged they may not be able to deliver on time.
**Blocked:** The dependency has become a current blocker. Requires immediate escalation.
**Resolved:** The dependency has been delivered and is no longer pending.

---

## Output Format

```
1. TRACKER HEADER
   Project/program, date, PM. Review cadence (typically weekly).

2. SUMMARY DASHBOARD
   Total dependencies tracked.
   By status: Confirmed / Pending / At risk / Blocked / Resolved.
   Critical path dependencies flagged.
   Escalations required.

3. DEPENDENCY REGISTRY TABLE
   Columns:
   ID | Type | Description | From team | To team | Deliverable needed |
   Due date | Owner (providing) | Owner (needing) | Status |
   Confirmed date | Risk level | Notes / last update

4. AT-RISK AND BLOCKED DEPENDENCIES (expanded detail)
   For each at-risk or blocked dependency:
   - Full description of what is needed and why
   - Original commitment and what changed
   - Impact on the project if not resolved
   - Mitigation options
   - Escalation action and owner

5. DEPENDENCY SCHEDULE VIEW
   Dependencies plotted by due date.
   Critical path dependencies highlighted.

6. RESOLVED DEPENDENCIES (last 30 days)
   Archive of recently resolved dependencies.
   Actuals vs. committed dates.

7. ESCALATION LOG
   Dependencies escalated to leadership.
   Decision or action taken.
   Resolution date.
```

---

## Starter Prompt

```
You are a program manager building a dependency tracker.

Project/program: [what is being tracked]
Known dependencies: [list of cross-team and external dependencies]
Providing teams: [the teams that must deliver something]
Needing teams: [the teams that are waiting]
Critical path items: [dependencies that directly affect the project completion date]
Known at-risk items: [dependencies already flagged as uncertain]

Produce a complete dependency tracker with all dependencies registered,
status assigned, and owners named. Flag all unconfirmed dependencies as pending.
Expand detail for any at-risk or blocked dependency with mitigation options.
```

---

*Skill file version: 1.0 | Phase: 04 - Program and Project Management | Company type: Product*
