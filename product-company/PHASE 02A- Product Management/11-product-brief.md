# product-brief.md

> **Skill:** Produces a concise product brief that aligns stakeholders on the problem, proposed solution, success criteria, and key decisions needed before a product initiative begins.

---

## TLDR

A product brief is a 1 to 2 page alignment document for stakeholders who do not need or want full PRD detail. It communicates what problem is being solved, what the proposed solution is, what success looks like, and what decisions need to be made. Used to get cross-functional buy-in before investing in full discovery and design.

---

## Topic Explanation

### Product Brief vs. PRD vs. Feature Spec

**Product brief:** The alignment document. Short, stakeholder-facing. "Here is what we are doing and why. Do you agree we should do it?"
**PRD:** The requirements document. Detailed, team-facing. "Here is what we need to build."
**Feature spec:** The implementation document. Very detailed, engineering-facing. "Here is exactly what to build."

These are sequential. The brief comes first. If stakeholders align on the brief, the team invests in the PRD. If they align on the PRD, the team writes feature specs.

### One-Page Discipline

A product brief that requires more than two pages to communicate has not been sufficiently thought through. The constraint forces ruthless prioritization: what is the most important information stakeholders need to decide whether to proceed?

---

## Output Format

```
1. BRIEF HEADER
   Initiative name, date, PM, status.

2. THE PROBLEM (3 to 5 sentences)
   What specific problem exists?
   Who experiences it?
   What is the cost of not solving it?
   Evidence.

3. THE PROPOSED SOLUTION (3 to 5 sentences)
   What we are building.
   Why this solution over alternatives.
   What it will and will not do.

4. WHO IT IS FOR
   Primary user type.
   Their key context relevant to this initiative.

5. SUCCESS DEFINITION
   How we will know this worked.
   3 measurable criteria.

6. WHAT WE ARE NOT DOING
   Explicit exclusions.

7. KEY DECISIONS NEEDED
   What must be decided before this initiative can proceed.
   Decision owner for each.

8. TIMELINE AND INVESTMENT
   Rough timeline.
   Team involved.
   Known dependencies.

9. RISKS AND OPEN QUESTIONS
   Top 3 risks.
   Open questions that need answers.
```

---

## Starter Prompt

```
You are a product manager writing a product brief for stakeholder alignment.

Initiative: [what is being proposed]
Problem: [the specific problem and evidence]
Proposed solution: [what you want to build]
User type: [who it is for]
Success criteria: [how you will measure success]
Explicit exclusions: [what is out of scope]
Decisions needed: [what must be resolved]
Timeline and team: [rough scope]

Produce a concise 1 to 2 page product brief.
Every section should be stakeholder-appropriate: business context, not implementation detail.
```

---

*Skill file version: 1.0 | Phase: 02 - Product Management | Company type: Product*
