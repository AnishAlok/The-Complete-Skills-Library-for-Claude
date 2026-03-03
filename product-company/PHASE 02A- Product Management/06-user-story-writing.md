# user-story-writing.md

> **Skill:** Produces well-formed user stories with clear user type, goal, rationale, and testable acceptance criteria following agile best practices.

---

## TLDR

User stories are the unit of product delivery in agile development. A well-written story communicates who needs something, what they need, and why, with acceptance criteria specific enough to test. This skill produces complete user stories that bridge product intent and engineering implementation.

---

## Topic Explanation

### The Three-Part Story

The standard user story format: "As a [user type], I want [goal] so that [reason]."

Each part does a specific job:
- **As a [user type]:** Names who the story is for. Not "the user" generically but a specific persona or role. This grounds development decisions in a real person's context.
- **I want [goal]:** States the capability needed. Written from the user's perspective, not the system's. "I want to see my compliance score" not "display the compliance score."
- **So that [reason]:** Provides the rationale. This is the most important and most often omitted part. It allows engineers to make implementation decisions that serve the goal.

### INVEST Criteria

Bill Wake's INVEST acronym is the quality standard for user stories:

**Independent:** Stories should be deliverable independently. Avoid dependencies between stories in the same sprint.
**Negotiable:** Stories are not contracts. Details can be renegotiated between PM and engineering.
**Valuable:** Every story should deliver user or business value. Infrastructure stories should be tied to user-visible outcomes.
**Estimable:** The story must be clear enough for engineers to estimate. Stories that cannot be estimated need splitting or clarifying.
**Small:** Stories should be completable within one sprint. Larger work is an epic.
**Testable:** Every story needs AC that can be tested. If you cannot test it, you cannot confirm it is done.

### Acceptance Criteria Formats

**Given/When/Then (Gherkin):** The most structured format. Best for complex behaviors with clear preconditions.
```
Given [context/precondition]
When [action taken]
Then [expected result]
```

**Checklist format:** Simpler. Best for straightforward requirements.
```
- [ ] User can export report as PDF
- [ ] Export includes data from the selected date range
- [ ] Export fails gracefully with a clear error message if generation fails
```

Both formats are valid. Gherkin is more testable. Checklists are faster to write.

---

## Output Format

```
For each user story:

STORY: [short descriptive title]
As a [specific user type],
I want [user goal or capability],
so that [reason / business value].

ACCEPTANCE CRITERIA:
Given [precondition]
When [action]
Then [expected outcome]

[Repeat for each significant scenario including error cases]

NOTES:
- Out of scope for this story: [explicit exclusions]
- Dependencies: [other stories or systems required]
- Design reference: [link to design]
- Edge cases to handle: [any edge cases not captured in AC]

STORY SIZE: [XS / S / M / L - flag L for potential splitting]
```

---

## Starter Prompt

```
You are a product manager writing user stories for a feature.

Feature context: [what feature area these stories cover]
User types: [who uses this feature]
Capabilities to express as stories: [what users need to be able to do]
Edge cases: [known edge conditions]
Design reference: [link to designs if available]

Write well-formed user stories in As/Want/So format with acceptance criteria
in Given/When/Then format. Include at least one error/failure AC per story.
Flag any story that violates INVEST criteria and suggest how to fix it.
```

---

*Skill file version: 1.0 | Phase: 02 - Product Management | Company type: Product*
