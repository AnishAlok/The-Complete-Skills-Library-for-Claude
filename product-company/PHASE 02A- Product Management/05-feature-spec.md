# feature-spec.md

> **Skill:** Produces a feature specification with user stories, acceptance criteria, edge cases, and engineering context that is precise enough for implementation without prescribing the solution.

---

## TLDR

A feature spec translates a PRD requirement into engineering-ready detail. It contains user stories with acceptance criteria, edge cases, error states, non-functional requirements, and design references. More detailed than a PRD, less prescriptive than a design spec, a feature spec is the primary artifact engineering uses to build.

---

## Topic Explanation

### Feature Spec vs. PRD vs. Design Spec

**PRD:** The "what and why" at the initiative level. Problem, goals, requirements. Written before design.
**Feature spec:** The "what exactly" at the feature level. Stories, AC, edge cases. Written during design.
**Design spec:** The "how it looks and behaves" at the component level. Visual, interaction, state detail. Written by design.

A feature spec bridges the PRD and the design spec: it takes the PRD's requirements and translates them into implementation-ready stories while leaving the visual and interaction implementation to the design spec.

### Acceptance Criteria Quality

Acceptance criteria are the most important part of a feature spec. They define the boundary between "done" and "not done." Good AC is:

**Specific:** "The user receives an email within 5 seconds of submitting the export request" is specific. "The user receives a confirmation" is not.

**Testable:** A QA engineer should be able to write a test case directly from the AC without interpretation.

**User-focused:** "Given a logged-in user on the reports page, when they click Export, then a PDF is generated and downloaded automatically" is user-focused. "The export function shall generate a PDF" is not.

**Complete:** AC that does not cover the error case, the edge case, and the happy path is incomplete.

The Given/When/Then (Gherkin) format is the most widely used structure for AC:
- **Given:** The precondition and context
- **When:** The action the user takes
- **Then:** The expected outcome

---

## When to Use This Skill

Use when:
- A PRD requirement needs to be broken down into engineering-ready stories
- Engineering is starting sprint planning and needs AC for estimation
- A feature is complex enough that verbal requirements would cause implementation divergence
- QA needs clear test cases before implementation begins

---

## Dos

- **Do write AC in Given/When/Then format.** This format forces explicit precondition, action, and outcome.
- **Do write one story per user goal.** Stories that combine multiple goals are harder to estimate and test.
- **Do include the negative cases.** The AC for "what happens when the export fails" is as important as the success case.
- **Do link to the design spec.** The feature spec references the design file; it does not describe the UI.
- **Do get engineering to review before sprint planning.** Stories with unclear AC cost more time in implementation than writing them well upfront.

---

## Donts

- **Dont write acceptance criteria that test the implementation.** "The system uses a background job to generate the PDF" is an implementation. "The UI remains usable while the export is being generated" is a behavior.
- **Dont write stories so large they cannot be completed in a sprint.** If a story takes more than 3 to 5 days to implement and test, it is an epic, not a story.

---

## Output Format

```
1. FEATURE SPEC HEADER
   Feature name, version, date, PM, design reference, engineering owner.
   Link to parent PRD.

2. FEATURE OVERVIEW
   What this feature does in 2 to 3 sentences.
   Which PRD requirement(s) this spec implements.
   The user type and goal this serves.

3. USER STORIES
   For each story:
   - Story title
   - User story: As a [user type], I want [goal] so that [reason]
   - Acceptance criteria in Given/When/Then format
   - Story points estimate (if applicable)
   - Dependencies on other stories

4. EDGE CASES AND ERROR STATES
   For each identified edge case:
   - Condition
   - Expected behavior
   - Error message or fallback if applicable

5. NON-FUNCTIONAL REQUIREMENTS
   Performance: response time, load requirements
   Security: auth, data access rules
   Accessibility: WCAG requirements for this feature

6. OUT OF SCOPE
   Explicit items not in this spec.

7. DESIGN REFERENCES
   Links to design files (specific frames)
   Links to design spec and microcopy doc

8. TESTING NOTES
   Key test scenarios for QA
   Any testing considerations or environment requirements

9. OPEN QUESTIONS
   Unresolved items with owner and deadline
```

---

## Starter Prompt

```
You are a product manager writing a feature specification.

Feature: [what the feature does]
Parent PRD: [the requirement this spec implements]
User type: [who uses this feature]
User stories: [the capabilities to specify]
Edge cases: [known edge conditions]
Non-functional requirements: [performance, security, accessibility needs]
Design reference: [link to design files]

Produce a complete feature spec with user stories in As/Want/So format,
acceptance criteria in Given/When/Then format, edge cases, and error states.
Make every AC testable and specific enough for a QA engineer to write test cases directly.
Flag any story that is too large for a single sprint.
```

---

*Skill file version: 1.0 | Phase: 02 - Product Management | Company type: Product*
