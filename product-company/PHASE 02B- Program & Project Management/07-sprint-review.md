# sprint-review.md

> **Skill:** Produces a sprint review document that captures what was completed against the sprint goal, demonstrates work to stakeholders, and surfaces learnings that inform the next sprint.

---

## TLDR

The sprint review is the agile ceremony that closes the loop: did the team accomplish the sprint goal? What did they learn? What does the product backlog look like now? This skill produces the sprint review documentation: a structured record of what was completed, what was not, key demonstrations, stakeholder feedback, and backlog implications.

---

## Topic Explanation

### Sprint Review vs. Sprint Retrospective

These ceremonies are frequently conflated:

**Sprint review:** Outward-facing. Focused on the product. What was built? Does it meet the sprint goal? What did stakeholders see and say? What is the current state of the product backlog?

**Sprint retrospective:** Inward-facing. Focused on the team. How did we work? What should we do differently? What is slowing us down?

Both are necessary. Running them in the same meeting conflates product inspection with process improvement and tends to produce neither well.

### What "Done" Means in a Sprint Review

"Done" in agile has a specific meaning: the team's Definition of Done (DoD) has been met. If a story is code-complete but not tested, not documented, or not deployed to a reviewable environment, it is not done by most teams' DoD.

The sprint review must make the distinction between:
- Stories that meet the Definition of Done
- Stories that are in progress and will carry into the next sprint
- Stories that were descoped during the sprint and why

Counting in-progress stories as "done" inflates velocity and degrades forecast reliability.

### Stakeholder Feedback Capture

The sprint review's most valuable output is often stakeholder feedback on the work demonstrated. This feedback:
- Validates or invalidates assumptions embedded in the work
- Surfaces requirements that were missed
- Builds stakeholder understanding of the product
- Creates shared ownership between business and product/engineering

Feedback captured at the sprint review should be translated into backlog items before the next sprint planning.

---

## Output Format

```
1. SPRINT REVIEW HEADER
   Sprint number, dates, team, PM, attendees.
   Sprint goal (as stated at sprint planning).

2. SPRINT GOAL ASSESSMENT
   Was the sprint goal achieved? Yes / Partially / No.
   Brief explanation of outcome vs. goal.

3. COMPLETED WORK (meets Definition of Done)
   For each completed story:
   - Story ID and title
   - Demo summary: what was shown
   - Acceptance criteria met: Yes / No / Partial
   - Points delivered

4. INCOMPLETE WORK
   Stories started but not completed.
   Reason for incompletion.
   Decision: carry to next sprint / return to backlog / descope.

5. VELOCITY
   Points planned vs. points delivered.
   3-sprint rolling average.
   Notable factors affecting this sprint's velocity.

6. STAKEHOLDER FEEDBACK
   Feedback by story or feature area.
   For each feedback item: description, priority implication, backlog action.

7. PRODUCT BACKLOG IMPLICATIONS
   New items added from sprint learning or stakeholder feedback.
   Items reprioritized based on what was learned.
   Items removed based on new information.

8. NEXT SPRINT PREVIEW
   Top backlog items being considered for the next sprint.
   Any known constraints or capacity issues.
```

---

## Starter Prompt

```
You are a Scrum Master or PM facilitating a sprint review.

Sprint goal: [what the team committed to at sprint planning]
Completed stories: [stories that meet Definition of Done with point values]
Incomplete stories: [stories started but not finished and why]
Planned points vs. delivered: [velocity data]
Stakeholder feedback received: [key reactions and inputs from the review]
Backlog changes: [new items, reprioritizations, or removals]

Produce a complete sprint review document capturing sprint goal assessment,
velocity analysis, stakeholder feedback with backlog implications,
and next sprint preview.
```

---

*Skill file version: 1.0 | Phase: 04 - Program and Project Management | Company type: Product*
