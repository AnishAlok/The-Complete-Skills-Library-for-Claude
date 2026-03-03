# project-plan.md

> **Skill:** Produces a detailed project plan with phases, milestones, tasks, owners, dependencies, and timeline that serves as the operational guide for project execution.

---

## TLDR

This skill helps you answer: *"How exactly will we deliver on the project charter's commitments: who does what, in what sequence, by when?"* A project plan translates the charter's scope and objectives into an executable schedule of work. It is the PM's primary operational tool: used to track progress, surface dependencies, and communicate status throughout the project lifecycle.

---

## Topic Explanation

### Project Plan Components

A complete project plan has six components that work together:

**Work Breakdown Structure (WBS):** The hierarchical decomposition of all work. Every deliverable broken into work packages, work packages into tasks.

**Task dependencies:** Which tasks must finish before others can start. The critical path runs through the longest chain of dependent tasks.

**Resource assignments:** Who is responsible for each task. Not just which team, but which person.

**Duration estimates:** How long each task will take. Distinguish between duration (calendar time) and effort (person-hours). A task requiring 8 hours of effort may have a 3-day duration if the assignee is also doing other work.

**Baseline schedule:** The approved timeline with milestones. Deviations from baseline become variance that must be managed.

**Contingency:** Buffer time allocated to the project to absorb schedule risk. Typically 10 to 20% of project duration. Should be held at the project level, not hidden inside individual task estimates.

### Critical Path Method

The critical path is the longest sequence of dependent tasks. Any delay on the critical path delays the project. Tasks not on the critical path have float: time they can slip without affecting the project end date.

Every project plan should identify the critical path explicitly. The PM's primary schedule management job is protecting the critical path from delays.

### Effort Estimation Approaches

**Bottom-up estimation:** Estimate each task individually, then sum. Most accurate. Most time-consuming.

**Analogous estimation:** Use actuals from similar past projects. Fast. Accurate only when the analogy is strong.

**Parametric estimation:** Use a formula (e.g., X hours per feature based on historical data). Good for repetitive work where the relationship between size and effort is known.

**Three-point estimation:** (Optimistic + 4 × Most Likely + Pessimistic) / 6. Accounts for uncertainty. Good for novel work.

For product projects, a combination of bottom-up for well-understood tasks and three-point for novel or complex tasks works best.

---

## When to Use This Skill

Use when:
- A project charter has been approved and detailed planning is beginning
- A project is running without a formal plan and needs structure
- An existing plan needs to be rebuilt after a major scope or timeline change
- A new PM is taking over a project and needs to understand the full plan

---

## Dos

- **Do separate the baseline from the current schedule.** Track both: the original plan and the current projection. Variance between them is your performance signal.
- **Do identify the critical path explicitly.** Every team member should know which tasks are on the critical path.
- **Do hold contingency at the project level, not in individual task estimates.** Hidden task-level contingency inflates the schedule and cannot be managed.
- **Do include a RACI for key deliverables.** Task-level ownership is not sufficient. Deliverable-level accountability requires explicit RACI.
- **Do review and update the plan weekly.** A plan that is not updated weekly does not reflect reality and cannot be used to manage the project.

---

## Donts

- **Dont plan at the wrong level of detail.** Week-by-week plans for work six months out are false precision. Plan near-term work in detail, future work in phases.
- **Dont assign tasks to teams or roles without naming individuals.** "Engineering" does not have accountability. "Sarah Chen (Backend)" does.
- **Dont ignore soft dependencies.** Hard dependencies (Task B cannot start until Task A is complete) are visible. Soft dependencies (stakeholder review needed before proceeding) are often missed. Plan for both.

---

## Output Format

```
1. PLAN HEADER
   Project name, version, date, PM, phase, status.
   Last updated, next review date.

2. PROJECT SUMMARY
   Objectives, key deliverables, total timeline, total budget.
   Current phase and status (on track / at risk / behind).

3. PHASE BREAKDOWN
   For each phase:
   - Phase name and duration
   - Phase objective: what this phase must achieve
   - Key deliverables
   - Entry criteria: what must be true to begin
   - Exit criteria: what must be true to complete

4. MILESTONE SCHEDULE
   Table: Milestone name / Target date / Owner / Status
   Critical milestones highlighted.

5. WORK BREAKDOWN AND TASK SCHEDULE
   For each work package:
   - Work package name
   - Tasks within it: name, owner, start, end, effort, status
   - Dependencies: which tasks must precede
   - Critical path indicator

6. CRITICAL PATH
   The sequence of tasks that determines project completion date.
   Total float for non-critical tasks.

7. RESOURCE PLAN
   For each team member:
   - Allocation percentage by phase
   - Task assignments
   - Capacity conflicts flagged

8. DEPENDENCY SUMMARY
   Internal dependencies (within the project).
   External dependencies (other teams, vendors, decisions).
   Each with owner and risk level.

9. BUDGET TRACKING
   Approved budget vs. actual vs. forecast to complete.
   Variance explanation.

10. RISK SUMMARY
    Top 5 risks with mitigation status.
    Reference to full Risk Register.

11. CHANGE LOG
    Record of approved changes to scope, schedule, or budget.
    Impact of each change on the baseline.
```

---

## Starter Prompt

```
You are a project manager building a detailed project plan.

Project context: [reference to the approved charter]
Phases: [the major phases the project will go through]
Key deliverables: [the tangible outputs by phase]
Team members: [who is on the project and their roles]
Known dependencies: [internal and external dependencies]
Timeline constraints: [hard deadlines and constraints]
Budget: [approved budget]
Known risks: [risks that affect scheduling or resourcing]

Please produce a complete project plan including:
1. Phase breakdown with entry and exit criteria
2. Milestone schedule with owners
3. Work breakdown and task schedule with dependencies
4. Critical path identification
5. Resource plan with allocation percentages
6. Dependency summary distinguishing internal and external
7. Budget tracking structure
8. Risk summary with reference to risk register

Flag any task without a named individual owner.
Flag any task on the critical path that lacks a risk mitigation.
Identify where the plan has insufficient detail for near-term work.
```

---

## Related Skills

| Use This Next | Why |
|---|---|
| `wbs-breakdown.md` | The WBS is the foundation of the project plan's task structure |
| `risk-register.md` | Project plan risks are tracked in the full risk register |
| `dependency-tracker.md` | External dependencies get their own tracking document |
| `project-status-report.md` | Project plan is the baseline for status reporting |
| `milestone-review.md` | Each milestone triggers a formal milestone review |

*Skill file version: 1.0 | Phase: 04 - Program and Project Management | Company type: Product*
