# product-requirements-doc.md

> **Skill:** Produces a Product Requirements Document (PRD) that defines the problem, user context, goals, functional requirements, non-functional requirements, and success criteria for a product feature or initiative.

---

## TLDR

This skill helps you answer: *"What are we building, for whom, and how do we know it is done?"* A PRD is the primary alignment document between product management, design, and engineering. It defines the problem and requirements without dictating the implementation. Used when a feature or initiative is large enough to need formal alignment documentation before design and engineering begin.

---

## Topic Explanation

### The PRD's Shifting Role

The PRD's role has evolved significantly in agile product development. Traditional PRDs were long documents specifying complete requirements before any development began. Modern PRDs are living documents that evolve alongside discovery and delivery.

The key shift: PRDs no longer specify implementation. They specify the problem to solve, the user context, the goals, and the constraints. Design and engineering determine implementation. This shift keeps PRDs useful and alive rather than large documents that become immediately outdated.

### What Goes in a PRD vs. What Does Not

**Goes in a PRD:**
- The problem being solved and the evidence for it
- Who the user is and what they need
- The goals this feature must accomplish
- Functional requirements: what the feature must do
- Non-functional requirements: performance, security, accessibility
- Success criteria and measurement approach
- Constraints: technical, business, regulatory
- Out of scope

**Does not go in a PRD:**
- Implementation details (how to build it)
- Visual design (belongs in design specs)
- Sprint plans (belongs in project management tools)
- Marketing copy (belongs in launch planning)

### Functional Requirements vs. User Stories

PRDs can express requirements in two main formats:

**Requirement statements:** "The system must allow users to export compliance reports in PDF format." Clear, testable, implementation-agnostic.

**User stories:** "As a restaurant operator, I want to export my compliance report as a PDF so that I can share it with my accountant during an audit." More context-rich, communicates the why.

Modern PRDs increasingly use user stories. The acceptance criteria that accompany user stories serve the same role as traditional requirement testability criteria.

---

## When to Use This Skill

Use when:
- A new feature or initiative requires cross-functional alignment before design and engineering begin
- A feature is complex enough that undocumented requirements create risk
- Engineering is asking for clarity on what to build before estimating
- Stakeholders have different assumptions about what a feature will do

---

## Dos

- **Do write requirements from the user's perspective, not the system's.** "Users can export reports" not "the system exports reports."
- **Do include the "why" behind requirements.** Requirements without rationale get changed without understanding consequences.
- **Do make success criteria measurable.** "Users find it easy to export" is not measurable. "80% of users who attempt an export complete it successfully in under 2 minutes" is.
- **Do include explicit out-of-scope items.** This prevents the silent inclusion of requirements that were never agreed upon.
- **Do link requirements to user research.** Requirements grounded in evidence are much more stable than requirements based on assumptions.

---

## Donts

- **Dont write implementation requirements.** "The export function shall use the LibreOffice API" is an implementation detail. Leave implementation to engineering.
- **Dont write a PRD so long it is never read.** A 2-page PRD that everyone reads is worth more than a 15-page PRD that sits in Confluence untouched.
- **Dont treat the PRD as final.** PRDs evolve. Version them. Update them as you learn. A PRD that never changes is a PRD that has been abandoned.

---

## Output Format

```
1. PRD HEADER
   Feature name, version, date, PM, design lead, engineering lead,
   status (draft / in review / approved), last updated.

2. TL;DR (3 to 5 sentences)
   What this is, why it matters, what it will accomplish.

3. PROBLEM STATEMENT AND CONTEXT
   The specific problem this feature solves.
   Evidence: user research, analytics, support tickets, business context.
   The cost of not solving it.

4. USER CONTEXT
   Who is this for? (persona or user type reference)
   What does their current experience look like?
   What are they trying to accomplish?
   Reference to relevant research.

5. GOALS
   Product goals: what the feature must accomplish for the product.
   User goals: what users should be able to do.
   Business goals: what business outcome this contributes to.
   These are NOT the requirements. They are the intended outcomes.

6. SUCCESS CRITERIA
   How we will measure whether this feature achieved its goals.
   Quantitative targets where possible.
   Timeline for measurement.

7. FUNCTIONAL REQUIREMENTS
   Organized by user journey or feature area.
   Format: numbered statements or user stories with acceptance criteria.
   Each requirement testable and verifiable.

8. NON-FUNCTIONAL REQUIREMENTS
   Performance requirements: load time, throughput, latency.
   Security requirements.
   Accessibility requirements (WCAG 2.1 AA).
   Reliability requirements.
   Data handling requirements.

9. OUT OF SCOPE
   Explicit list of what this feature will NOT do.
   Things deferred to a future phase with rationale.

10. CONSTRAINTS AND DEPENDENCIES
    Technical constraints.
    Business or regulatory constraints.
    Dependencies on other teams or systems.
    Timeline constraints.

11. OPEN QUESTIONS
    Unresolved questions with owner and deadline.

12. APPENDIX
    Relevant research links.
    Related feature documentation.
    Competitive examples.
```

---

## Starter Prompt

```
You are a product manager writing a Product Requirements Document.

Feature name: [what is being built]
Problem statement: [the specific problem and evidence for it]
User context: [who uses this and what they need]
Goals: [product, user, and business goals]
Functional requirements: [what the feature must do]
Non-functional requirements: [performance, security, accessibility needs]
Out of scope: [explicit exclusions]
Constraints: [technical, business, and regulatory constraints]
Dependencies: [other teams or systems involved]
Success criteria: [how you will measure success]

Please produce a complete PRD including:
1. TL;DR summary
2. Problem statement with evidence
3. User context with current experience description
4. Goals separated by product, user, and business
5. Measurable success criteria
6. Functional requirements as user stories or numbered statements
7. Non-functional requirements covering performance, security, accessibility
8. Explicit out-of-scope list
9. Constraints and dependencies
10. Open questions with owners

Write requirements from the user's perspective, not the system's.
Flag any requirement that implies an implementation rather than a behavior.
```

---

## Related Skills

| Use This Next | Why |
|---|---|
| `feature-spec.md` | Detailed feature specs break PRD requirements into implementable detail |
| `user-story-writing.md` | PRD functional requirements are expressed as user stories |
| `design-spec.md` | Design specs implement the requirements defined in the PRD |
| `mvp-definition.md` | PRD requirements may need MVP scoping |

*Skill file version: 1.0 | Phase: 02 - Product Management | Company type: Product*
