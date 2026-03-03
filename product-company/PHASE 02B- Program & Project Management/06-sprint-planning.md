# sprint-planning.md

> **Skill:** Produces a sprint planning document that defines the sprint goal, selected backlog items, acceptance criteria, team capacity, and commitment for a single agile sprint.

---

## TLDR

This skill helps you answer: *"What exactly is the team committing to this sprint, why, and how does it connect to the product goal?"* A sprint planning document captures the outcome of the sprint planning ceremony: the sprint goal, the selected stories, the capacity calculation, and the team's commitment. Used at the start of every sprint.

---

## Topic Explanation

### The Two Questions of Sprint Planning

The Scrum Guide defines sprint planning as answering two questions:

**Why is this sprint valuable?** The sprint goal. A single sentence that describes what the team will accomplish and why it matters. The sprint goal should describe a user-facing or business outcome, not a list of features.

**What can be done this sprint?** The sprint backlog. The stories and tasks selected from the product backlog that the team commits to completing within the sprint.

A common failure: teams skip the sprint goal and go straight to story selection. Without a sprint goal, the team lacks a principle for in-sprint decisions. When something comes up mid-sprint that competes with the planned work, the sprint goal is what helps them decide.

### Velocity and Capacity

**Velocity:** The team's historical average of story points completed per sprint. Used to calibrate how much to plan.

**Capacity:** The actual available hours or points this specific sprint, accounting for holidays, PTO, and any known interruptions.

Capacity is not the same as velocity. If three team members are on vacation during a sprint, capacity is lower than the velocity average. Plan to capacity, not to velocity.

### The Sprint Commitment

The sprint commitment is the team's collective agreement that they believe they can complete the selected stories within the sprint. It is not a guarantee, but it is a considered forecast made by the people doing the work.

Commitment requires that the team has:
- Reviewed and understood every story they are committing to
- Identified and discussed any significant risks or unknowns
- Ensured acceptance criteria are clear and testable
- Verified that dependencies are either resolved or will be resolved early in the sprint

---

## When to Use This Skill

Use when:
- Beginning sprint planning for any agile team
- The team is struggling with sprint planning effectiveness and needs a more structured approach
- Onboarding a new team member to the sprint planning process
- The PM or Scrum Master needs to facilitate sprint planning and wants a structure to follow

---

## Dos

- **Do write the sprint goal before selecting stories.** The goal should guide story selection, not be a summary of selected stories.
- **Do review every story the team is committing to.** Stories should not be silently dropped into the sprint backlog. Every story should be briefly reviewed for clarity and feasibility.
- **Do account for ceremonies and non-sprint work when calculating capacity.** Meetings, code review, on-call rotation, and other overhead reduce available capacity.
- **Do surface dependencies before committing.** If a story depends on something outside the team's control, name it explicitly and confirm it will be resolved before the sprint begins.

---

## Donts

- **Dont commit to more than capacity supports.** Teams that over-commit every sprint normalize incomplete sprints, which degrades forecast reliability.
- **Dont allow stories with unclear acceptance criteria into the sprint.** Unclear AC produces rework and scope disagreements mid-sprint.

---

## Output Format

```
1. SPRINT HEADER
   Sprint number, dates (start and end), team name, Scrum Master, PM.

2. SPRINT GOAL
   One sentence: what the team will accomplish and why it matters.
   How it connects to the current product or program goal.

3. CAPACITY CALCULATION
   For each team member:
   - Name, role
   - Available days this sprint
   - Planned time off or known interruptions
   - Estimated available capacity (hours or points)
   Team total capacity.

4. SPRINT BACKLOG

   For each story committed:
   - Story ID and title
   - User story statement
   - Story points
   - Assignee
   - Dependencies: internal or external
   - Acceptance criteria (brief reference or inline)
   - Risks or unknowns flagged at planning

5. CAPACITY VS. COMMITMENT
   Total points or hours planned vs. total capacity.
   Buffer remaining.

6. DEPENDENCIES FOR THIS SPRINT
   Anything outside the team's control that must happen for a story to complete.
   Owner of each dependency.
   Confirmation status: confirmed / pending.

7. DEFINITION OF DONE REMINDER
   The team's agreed Definition of Done for the sprint.

8. TEAM COMMITMENT
   Team sign-off: the team believes this sprint backlog is achievable.
   Date of commitment.
```

---

## Starter Prompt

```
You are a Scrum Master or PM facilitating sprint planning.

Sprint dates: [start and end dates]
Product goal: [the current product or program goal this sprint serves]
Team members and availability: [who is on the team and any PTO or interruptions]
Team velocity: [average story points per sprint]
Candidate stories: [stories from the backlog being considered]
Known dependencies: [anything outside the team's control]

Please produce a complete sprint planning document including:
1. A sprint goal that describes an outcome, not a feature list
2. Capacity calculation for each team member
3. Sprint backlog with stories, points, assignees, and dependencies flagged
4. Capacity vs. commitment comparison
5. Dependency confirmation status

Flag any story without clear acceptance criteria.
Flag any commitment that exceeds 90% of available capacity.
```

---

## Related Skills

| Use This Next | Why |
|---|---|
| `sprint-review.md` | Sprint review documents outcomes against the sprint goal |
| `retro-facilitation.md` | Retrospective follows the sprint review |
| `dependency-tracker.md` | Sprint dependencies feed into the broader dependency tracker |

*Skill file version: 1.0 | Phase: 04 - Program and Project Management | Company type: Product*
