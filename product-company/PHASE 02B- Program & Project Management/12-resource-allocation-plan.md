# resource-allocation-plan.md

> **Skill:** Produces a resource allocation and capacity plan that maps team capacity to project and program demand, identifies over-allocations, and informs hiring or contractor needs.

---

## TLDR

A resource allocation plan answers: *"Do we have the right people, with the right skills, available at the right times to deliver the work we have committed to?"* It maps planned demand (from the project portfolio) against available capacity (from the team roster) to surface over-allocations, under-utilizations, and gaps that require action. Used in portfolio planning and whenever a new project is being scoped.

---

## Topic Explanation

### Capacity vs. Availability

**Capacity:** The theoretical total working hours of the team. 40 hours per person per week.
**Availability:** Actual available project hours after accounting for overhead, meetings, on-call, PTO, and other non-project work.

In most knowledge work organizations, a person working 40 hours per week is available for 60 to 70% of that time for project work. The rest is absorbed by meetings, administrative work, and context switching. Planning to 100% of capacity is planning to over-deliver promises.

### The Resource Histogram

A resource histogram is a bar chart showing planned hours per person per week or per sprint across the project timeline. It makes over-allocation visible: bars that exceed available capacity identify resource conflicts that must be resolved before planning is confirmed.

Conflict resolution options:
- **Prioritize:** Do the most important work first, defer the rest
- **Level:** Spread the work over a longer timeline
- **Augment:** Hire, contract, or borrow capacity from another team
- **Descope:** Remove work from the plan

### Skills Inventory

Beyond headcount, resource allocation must consider skills. A project that requires three backend engineers but the available capacity is three frontend engineers has a capacity problem, not a resource allocation problem. Skills mapping identifies not just whether enough people are available, but whether the right people are available.

---

## Output Format

```
1. RESOURCE PLAN HEADER
   Program/project, planning period, PM, date.

2. TEAM ROSTER
   For each team member:
   - Name, role, skills
   - Total weekly capacity (hours)
   - Availability percentage (net of overhead)
   - Available hours per week for project work

3. PROJECT/PROGRAM DEMAND
   For each active or planned project:
   - Project name
   - Required skills
   - Effort by role (hours per week or sprint)
   - Duration

4. ALLOCATION MATRIX
   Rows: Team members
   Columns: Projects / time periods
   Cell: Allocated hours / percentage
   Total row: Total hours allocated per period
   Over-allocation highlighted (>100% of availability)

5. CAPACITY ANALYSIS
   By person: allocated vs. available (over/under allocation)
   By skill: demand vs. supply for each required skill
   By time period: peak demand weeks identified

6. GAPS AND CONFLICTS
   Over-allocations: who, when, how much
   Skill gaps: skills needed but not available
   Timeline conflicts: two priorities competing for the same resource

7. RESOLUTION RECOMMENDATIONS
   For each conflict:
   - Option A: prioritize (defer one project)
   - Option B: level (extend timeline)
   - Option C: augment (hire, contract, or borrow)
   Recommendation and rationale.

8. HIRING AND CONTRACTOR NEEDS
   Roles where demand exceeds internal capacity.
   Timeline for when capacity is needed.
   Make vs. buy recommendation.
```

---

## Starter Prompt

```
You are a program manager building a resource allocation plan.

Team members: [names, roles, and skills]
Active and planned projects: [list with effort requirements by role]
Planning period: [quarterly / annual]
Known constraints: [hiring freeze, budget limits, PTO]
Known over-allocations: [if already identified]

Produce a complete resource allocation plan including team roster with availability,
allocation matrix, capacity analysis, gap identification, and resolution recommendations.
Flag all over-allocations above 100% of availability.
```

---

*Skill file version: 1.0 | Phase: 04 - Program and Project Management | Company type: Product*
