# epic-breakdown.md

> **Skill:** Breaks a large epic into a coherent set of user stories, tasks, and subtasks sized for sprint delivery, with clear dependencies and sequencing.

---

## TLDR

Epics are too large to estimate, build, and ship in a single sprint. Epic breakdown is the process of decomposing a large body of work into independently deliverable user stories with clear sequencing and dependencies. This skill produces a complete breakdown with stories sized for delivery and sequenced for learning.

---

## Topic Explanation

### What Is an Epic?

An epic is a large user story that cannot be completed in a single sprint. Epics typically represent a major feature, a significant improvement to an existing capability, or a user journey across multiple touchpoints. Epics should be broken down before sprint planning.

### Decomposition Strategies

**By user role:** If multiple user types use the feature, start with one user type's full flow before adding others.
**By workflow step:** Break the epic along the stages of the user's workflow.
**By happy path first:** Build the happy path as the first stories. Add error handling, edge cases, and refinements as subsequent stories.
**By data/interface split:** Build the data layer and the interface as separate stories that can be independently tested.
**By read/write split:** Read operations and write operations can often be separate stories.

### The Walking Skeleton

A useful concept from Alistair Cockburn: the "walking skeleton" story delivers the thinnest possible end-to-end implementation of the feature. It is functional but missing all polish, edge case handling, and optimization. Building the walking skeleton first gives engineering a working foundation to iterate on and gives product something to demo and test early.

---

## Output Format

```
1. EPIC SUMMARY
   Epic name and description.
   User type(s) served.
   Strategic rationale: why this epic, why now.
   Total estimated size.

2. WALKING SKELETON STORY
   The thinnest end-to-end implementation.
   What it delivers and what it explicitly omits.

3. STORY MAP
   Stories organized by workflow stage (rows) and iteration (columns).
   Shows which stories are in the MVP slice vs. later iterations.

4. STORY LIST
   For each story in priority order:
   - Story number and title
   - User story statement
   - Key acceptance criteria
   - Estimated size (story points or T-shirt size)
   - Dependencies: must be completed before this story

5. TECHNICAL TASKS
   Engineering tasks not expressed as user stories:
   - Infrastructure or backend setup
   - API development
   - Data migration
   Each task: name, description, estimate, dependency.

6. DEPENDENCY DIAGRAM
   Visual or text-based dependency sequencing.
   Which stories can run in parallel vs. which must be sequential.

7. DEFINITION OF DONE FOR THE EPIC
   What must be true for the full epic to be considered complete.
```

---

## Starter Prompt

```
You are a product manager breaking down an epic for sprint planning.

Epic: [name and description of the epic]
User type(s): [who this epic serves]
Current state: [what exists today]
Target state: [what the epic should achieve]
Known technical dependencies: [backend, API, or infrastructure work needed]
Team velocity: [approximate story points per sprint, if known]

Break this epic into:
1. A walking skeleton story
2. A full story map organized by workflow stage
3. All user stories with acceptance criteria and estimates
4. Technical tasks for non-story work
5. A dependency sequence showing what must be built in what order

Size every story for a single sprint (flag anything larger for further breakdown).
Identify which stories can be delivered to users incrementally vs. which
require the full epic to be complete before releasing.
```

---

*Skill file version: 1.0 | Phase: 02 - Product Management | Company type: Product*
