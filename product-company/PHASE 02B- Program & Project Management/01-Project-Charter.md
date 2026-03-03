# project-charter.md

> **Skill:** Produces a project charter that formally authorizes a project, defines its scope, objectives, stakeholders, authority structure, and success criteria before work begins.

---

## TLDR

This skill helps you answer: *"What exactly are we committing to, who has authority over what, and how will everyone know when we are done?"* A project charter is the founding document of a project. It establishes formal authorization, defines scope boundaries, assigns decision-making authority, and creates a shared definition of success. Used to kick off any project requiring cross-functional coordination.

---

## Topic Explanation

### Why Project Charters Prevent Expensive Misalignment

The project charter does one thing that no other project document does: it captures alignment across all parties before work begins. Teams that skip the charter often discover mid-project that stakeholders had different mental models of scope, authority, and success. By then, misalignment is expensive to correct.

The three most common misalignments a charter prevents:

**Scope misalignment:** The sponsor thought the project included X. The PM thought X was out of scope. A charter with explicit in-scope and out-of-scope statements resolves this before it becomes a conflict.

**Authority misalignment:** Two stakeholders both believe they have decision authority over a key aspect of the project. A charter with a defined RACI prevents this from becoming a power struggle.

**Success misalignment:** Leadership believes success means Y. The project team has been optimizing for Z. A charter with explicit success criteria ensures everyone is working toward the same definition of done.

### Charter vs. Project Plan

**Charter:** The authorization document. Defines what and why. Written before detailed planning begins. Relatively short. Changes infrequently.

**Project plan:** The execution document. Defines how, when, and who. Written after the charter is approved. More detailed. Updated frequently.

The charter should be approved before the project plan is written. A project plan without an approved charter is a plan for an unauthorized project.

### The Sponsor's Role

The project sponsor is the executive who owns the project's outcomes and has organizational authority to remove blockers, resolve escalations, and fund the work. Every project needs a named sponsor. Projects without a named sponsor have no one to escalate to when problems arise, and they frequently stall.

Sponsor responsibilities documented in the charter:
- Approving the charter
- Securing resources
- Removing organizational blockers
- Making decisions escalated from the PM
- Communicating project importance to the organization

---

## When to Use This Skill

Use when:
- Starting any project that involves more than one team or will last more than one sprint
- A cross-functional initiative needs formal authorization and scope definition
- A project has been informally running and needs to be formalized
- Stakeholders need to see formal documentation before approving resources

Do NOT use when:
- The work is a routine ongoing operation rather than a time-bounded project
- The scope is so small it fits in a single team's sprint without cross-functional coordination

---

## Dos

- **Do get the charter approved before detailed planning begins.** A charter that is approved after the plan is built is a rubber stamp, not an alignment document.
- **Do be explicit about what is out of scope.** Out-of-scope items that are not written down will be assumed to be in scope by someone.
- **Do name the sponsor, PM, and core team.** Anonymous roles produce unclear accountability.
- **Do include a constraints section.** Budget, timeline, technology, regulatory constraints known at project start belong in the charter.
- **Do write the success criteria in measurable terms.** "Improved user experience" is not a success criterion. "90% of new users complete onboarding in under 10 minutes" is.

---

## Donts

- **Dont write a charter so detailed it becomes a project plan.** The charter defines what and why. Leave how, when, and who for the project plan.
- **Dont let the charter be written by one person without stakeholder input.** A charter written in isolation and handed to stakeholders for signature is rarely aligned with their actual expectations.
- **Dont skip the assumptions section.** Unstated assumptions are future risks. Making them explicit enables early validation or mitigation.

---

## Ideal Inputs

```
1. PROJECT CONTEXT
   What is the project? What problem does it solve or opportunity does it pursue?

2. SPONSOR AND STAKEHOLDERS
   Who is the executive sponsor?
   Who are the key stakeholders?
   Which teams are involved?

3. SCOPE
   What is explicitly in scope?
   What is explicitly out of scope?

4. OBJECTIVES AND SUCCESS CRITERIA
   What must the project achieve?
   How will success be measured?

5. CONSTRAINTS
   Timeline, budget, technology, regulatory, or resource constraints.

6. ASSUMPTIONS AND RISKS
   Key assumptions the project rests on.
   Known risks at project start.
```

---

## Output Format

```
1. CHARTER HEADER
   Project name, version, date, status (draft / approved).
   Sponsor, PM, core team.
   Approved by and date.

2. EXECUTIVE SUMMARY (3 to 5 sentences)
   What the project is, why it is being done, and what it will produce.

3. BUSINESS CASE
   The specific problem or opportunity being addressed.
   Why this project, why now.
   Expected business value.

4. PROJECT OBJECTIVES
   3 to 5 specific, measurable objectives.
   Each one: what will be true when this objective is achieved?

5. SCOPE

   IN SCOPE:
   Explicit list of what this project will deliver.

   OUT OF SCOPE:
   Explicit list of what this project will NOT deliver.
   (This section is as important as In Scope.)

   DELIVERABLES:
   The specific tangible outputs the project will produce.

6. SUCCESS CRITERIA
   How the project's success will be measured.
   Quantitative targets where possible.
   Timeline for measurement.

7. STAKEHOLDERS AND AUTHORITY

   Sponsor: [name, role, authority]
   Project Manager: [name, authority]
   Core Team: [names, roles, responsibilities]
   Extended Stakeholders: [names, involvement type]

   DECISION AUTHORITY TABLE:
   Decision type | Owner | Consulted | Informed

8. TIMELINE
   High-level milestone schedule.
   Key phases with target dates.
   Hard deadlines and constraints.

9. BUDGET
   Approved budget envelope.
   Budget owner.
   Budget approval process for changes.

10. CONSTRAINTS
    Timeline constraints.
    Budget constraints.
    Technical or regulatory constraints.
    Resource constraints.

11. ASSUMPTIONS
    Key assumptions the project is built on.
    Who is responsible for validating each assumption.

12. RISKS
    Top 3 to 5 known risks at project start.
    Initial mitigation thinking for each.
    Reference to Risk Register for full treatment.

13. APPROVAL SIGNATURES
    Sponsor signature and date.
    PM acknowledgment.
    Key stakeholder sign-offs.
```

---

## Starter Prompt

```
You are a project manager writing a project charter.

Project context: [what the project is and why it is being done]
Sponsor: [the executive sponsor name and role]
Stakeholders: [key stakeholders and their involvement]
Scope: [what is in scope and what is explicitly out of scope]
Objectives: [what the project must achieve]
Success criteria: [how success will be measured]
Timeline constraints: [any hard deadlines]
Budget: [approved budget if known]
Known constraints: [technology, regulatory, resource constraints]
Known assumptions: [the assumptions the project rests on]
Known risks: [top risks at project start]

Please produce a complete project charter including:
1. Executive summary
2. Business case with specific problem or opportunity
3. Measurable objectives (3 to 5)
4. Explicit in-scope and out-of-scope lists
5. Success criteria with quantitative targets
6. Stakeholder table with authority and decision rights
7. High-level milestone schedule
8. Constraints, assumptions, and initial risk summary
9. Approval signature block

Flag any objective that is not measurable.
Flag any scope item that may be ambiguous between in-scope and out-of-scope.
```

---

## Related Skills

| Use This Next | Why |
|---|---|
| `project-plan.md` | Charter approval triggers detailed project planning |
| `risk-register.md` | Charter risks are developed into a full risk register |
| `stakeholder-alignment-doc.md` | Charter stakeholder section feeds into alignment planning |
| `wbs-breakdown.md` | Charter deliverables become WBS work packages |

*Skill file version: 1.0 | Phase: 04 - Program and Project Management | Company type: Product*
