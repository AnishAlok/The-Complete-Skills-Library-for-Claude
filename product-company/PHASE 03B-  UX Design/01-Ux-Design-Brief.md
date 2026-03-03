# ux-design-brief.md

> **Skill:** Produces a UX design brief that defines the problem to be solved, the user context, constraints, success criteria, and design goals before any design work begins.

---

## TLDR

This skill helps you answer: *"What exactly are we designing, for whom, within what constraints, and how will we know if we succeeded?"* It produces a structured design brief that aligns the design team, product managers, and engineering on the problem before solutions are explored. Used at the start of any significant design initiative to prevent misaligned execution.

---

## Topic Explanation

### Why Design Briefs Prevent Expensive Mistakes

Most UX failures are not execution failures. They are problem-definition failures: the team built the wrong thing correctly. Design briefs are the primary tool for catching problem-definition failures before design work begins.

Without a brief, each team member carries a different mental model of the problem, the user, and what success looks like. These invisible misalignments surface in review meetings after weeks of work have already been invested. A brief makes the mental models explicit and visible before any pixels are moved.

### What a Design Brief Is Not

A design brief is not a requirements document. Requirements specify what the system must do. A design brief specifies what the user needs to be able to accomplish and within what constraints. Requirements come from the design brief, not the other way around.

A design brief is not a wireframe or prototype specification. Those documents describe the solution. The brief describes the problem. The brief should be written before any solution is conceived.

### The Problem Statement Format

The most important element of a design brief is the problem statement. A well-formed problem statement names the user, their context, what they need, and why. The most useful format:

**[User type] in [context] needs to [accomplish goal] because [underlying motivation], but currently [the barrier or failure state].**

Example: "Restaurant operators managing multiple locations need to verify that tip pool distributions are compliant with state wage law before approving payroll, because non-compliance exposes them to audit risk, but currently they must cross-reference physical state regulation documents manually because the software provides no compliance guidance."

This format prevents the brief from sliding into solution descriptions, keeps the focus on the human need, and provides a testable definition of success.

### Constraints as Creative Material

Design constraints are often treated as limitations to work around. The better frame is that constraints define the design space: they identify the boundaries within which creative work should happen. A brief that does not document constraints forces designers to discover them mid-project, which is significantly more expensive.

Constraint types to document:
- **Technical:** What the engineering stack can and cannot do, performance requirements, API limitations
- **Business:** Launch timeline, budget, compliance requirements, brand guidelines
- **User:** Accessibility requirements, device and browser targets, user technical proficiency
- **Design system:** Which existing components must be used, what can be newly created

---

## When to Use This Skill

Use when:
- Starting any significant UX design initiative (new feature, redesign, or new product area)
- A design project has drifted and the team needs to re-anchor on the original problem
- Handoff between a discovery phase and a design phase requires documentation
- Multiple designers will work on the same project area and alignment is needed upfront

Do NOT use when:
- Making small, isolated UI fixes that do not require problem definition
- A design brief already exists and only needs updating

---

## Dos

- **Do write the problem statement before any solution ideas exist.** The brief should be solution-agnostic. If wireframes already exist, the brief is being written too late.
- **Do include what is explicitly out of scope.** Out-of-scope statements prevent scope creep and protect the team from stakeholder additions mid-project.
- **Do define success measurably.** "Improve the onboarding experience" is not a success criterion. "80% of new users complete their first payroll run without contacting support" is.
- **Do co-create the brief with the team.** A brief written by one person and handed to others produces less ownership than a brief developed collaboratively.
- **Do include a "known constraints" section.** Constraints discovered mid-design cause rework. Document all known constraints at brief-writing time.

---

## Donts

- **Dont include solution ideas in the problem statement.** "Users need a modal dialog to confirm..." has already jumped to a solution. Stay in problem space.
- **Dont write a brief so long that it is never read.** A two-page brief that gets read is better than a ten-page brief that gets filed.
- **Dont omit the user type.** "Users need to..." is not specific enough. Name the user type, role, or persona.
- **Dont write success criteria that cannot be measured.** "Better user experience" is not measurable. Task completion rate, time on task, support ticket reduction, or NPS change are measurable.

---

## Ideal Inputs

```
1. THE PRODUCT OR FEATURE CONTEXT
   What product area is this? What currently exists?

2. THE USER TYPE
   Who is the primary user? What is their role, context, and relevant experience?

3. THE PROBLEM BEING SOLVED
   What failure state or unmet need is the design addressing?
   Evidence for the problem (research data, support tickets, analytics).

4. KNOWN CONSTRAINTS
   Technical, business, user, and design system constraints.

5. SUCCESS DEFINITION
   How will you know the design worked?
   What metrics or observable behaviors define success?

6. TIMELINE AND SCOPE
   When is this needed?
   What is explicitly in scope and out of scope?
```

---

## Output Format

```
1. BRIEF HEADER
   Project name, date, version, designer(s), PM, engineering lead, status.

2. PROBLEM STATEMENT
   [User type] in [context] needs to [accomplish goal] because [motivation],
   but currently [the barrier or failure state].

3. USER CONTEXT
   Who specifically is this for?
   Key characteristics relevant to this design challenge.
   Any prior research that describes this user's behavior or needs.

4. DESIGN GOALS
   3 to 5 specific goals this design must achieve.
   Ordered by priority.

5. SUCCESS CRITERIA
   How success will be measured.
   Quantitative targets where possible.

6. CONSTRAINTS
   Technical constraints.
   Business and timeline constraints.
   Accessibility and device requirements.
   Design system constraints (what must use existing components).

7. OUT OF SCOPE
   Explicit list of what this design initiative will NOT address.

8. OPEN QUESTIONS
   Unresolved questions that could affect the design direction.
   Who is responsible for resolving each question and by when.

9. REFERENCES
   Relevant prior research.
   Competitive examples.
   Design system documentation.
   Related feature documentation.

10. APPROVALS
    Who must sign off on this brief before design begins.
    Date approved.
```

---

## Starter Prompt

```
You are a UX designer writing a design brief for a new design initiative.

Product or feature context: [what is being designed and what currently exists]
User type: [who the primary user is and their key characteristics]
Problem being solved: [the failure state or unmet need, with evidence]
Known constraints: [technical, business, user, and design system constraints]
Success definition: [how you will measure whether the design worked]
Timeline and scope: [when it is needed and what is in vs. out of scope]
Open questions: [unresolved issues that could affect design direction]

Please produce a complete UX design brief including:
1. A well-formed problem statement using the [user type] + [context] + [need] + [motivation] + [barrier] format
2. User context section
3. Prioritized design goals (3 to 5)
4. Measurable success criteria
5. Full constraints section covering technical, business, accessibility, and design system
6. Explicit out-of-scope statement
7. Open questions with owners and deadlines
8. References

Flag if the problem statement contains any implied solutions.
Flag any constraint that seems likely to conflict with the design goals.
```

---

## Related Skills

| Use This Next | Why |
|---|---|
| `design-spec.md` | The brief feeds into component and interaction specifications |
| `prototype-spec.md` | Brief constraints define prototype scope |
| `information-architecture.md` | IA decisions are informed by the design goals in the brief |
| `persona-doc.md` | If personas do not exist, create them before finalizing the brief |
| `ux-research-plan.md` | Brief may reveal research gaps that must be filled before design |

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
