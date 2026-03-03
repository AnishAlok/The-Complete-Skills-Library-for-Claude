# technical-spec.md

> **Skill:** Produces a technical design document that captures architecture decisions, component design, data flows, tradeoffs considered, and implementation guidance for a software feature or system change.

---

## TLDR

This skill helps you answer: *"How exactly will we build this, what tradeoffs did we consider, and what does the team need to know to implement it correctly?"* A technical spec captures the engineering decision-making process before implementation begins. It aligns the team on the approach, surfaces disagreements early, and creates a permanent record of why architectural choices were made. Used for any feature or system change with non-trivial complexity.

---

## Topic Explanation

### Why Technical Specs Are Written Before Code

The most expensive time to discover an architectural problem is after a significant portion of the system has been built around it. A technical spec surfaces architectural concerns when the cost to change direction is low: before any code is written.

The secondary benefit: writing forces clarity. Engineers who can explain an approach in prose understand it well enough to implement it. Engineers who struggle to write the spec often discover mid-writing that they do not yet have a clear design.

### What Belongs in a Technical Spec (and What Does Not)

**Belongs in a technical spec:**
- The problem being solved at the technical level
- The proposed architecture and component design
- Data flows and interaction diagrams
- Key technical decisions and the alternatives considered
- Tradeoffs accepted and why
- Implementation guidance for the team
- Open technical questions

**Does not belong:**
- Product requirements (those live in the PRD)
- Implementation code (this is a design document, not the implementation)
- Visual design (that belongs in the design spec)
- Sprint-level task breakdown (that belongs in the feature spec)

### Architecture Decision Records vs. Technical Specs

A technical spec describes the full design for a feature or system. An Architecture Decision Record (ADR, see `adr-architecture-decision.md`) captures a single architectural decision. They are complementary: a technical spec may reference multiple ADRs, and a significant decision in a spec may be promoted to a standalone ADR.

### Alternatives Considered

The "alternatives considered" section is the most frequently omitted and most valuable section of a technical spec. Documenting alternatives serves two purposes:

1. It proves the team explored the solution space rather than defaulting to the first idea
2. It explains to future engineers reading the code why a particular approach was chosen over the seemingly simpler alternatives they are likely considering

A future engineer reading a technical spec with no alternatives section cannot tell whether the approach was carefully chosen or simply the first thing tried.

---

## When to Use This Skill

Use when:
- A feature requires non-trivial architectural decisions
- Multiple engineers will work on the same feature and need a shared design
- A system change has cross-team implications that require review
- A new service, database, or external integration is being added
- A significant refactoring is being planned

Do NOT use when:
- The change is a simple bug fix or minor UI adjustment
- The implementation approach is obvious and already standard in the codebase

---

## Dos

- **Do write the spec before any significant implementation begins.** A spec written after the code is documentation, not a design document.
- **Do document the problem at the technical level, not just the product level.** "Users need to export reports" is a product problem. "The export job must process up to 50,000 rows without blocking the request thread and complete within 30 seconds" is a technical problem.
- **Do include the alternatives you seriously considered and why you rejected them.** This is the most valuable section for future maintainers.
- **Do make the tradeoffs explicit.** Every architectural decision involves tradeoffs. Name them: "This approach optimizes for read performance at the cost of write complexity."
- **Do include failure modes.** How does the system behave when components fail? What are the degradation modes?

---

## Donts

- **Dont write a spec so detailed it is really just code in prose.** A spec should describe the architecture, not the implementation.
- **Dont skip the open questions section.** Unknown design questions that appear in a spec are better than unknown questions that appear in a code review.
- **Dont make the spec immutable.** Specs should evolve as implementation reveals new information. Version them and capture what changed.

---

## Ideal Inputs

```
1. PRODUCT CONTEXT
   Link to the PRD or feature spec this technical spec implements.

2. TECHNICAL PROBLEM STATEMENT
   What must the system do at the technical level?
   Performance, scale, and reliability requirements.

3. CURRENT SYSTEM STATE
   Relevant existing architecture.
   Systems this will interact with.
   Constraints imposed by existing architecture.

4. PROPOSED APPROACH
   The architecture being proposed.
   Key components and their responsibilities.
   Data flows between components.

5. ALTERNATIVES CONSIDERED
   Other approaches that were evaluated.
   Why each was rejected.

6. OPEN QUESTIONS
   Unresolved technical decisions that need team input.
```

---

## Output Format

```
1. SPEC HEADER
   Feature/system name, version, author(s), date, status, reviewer(s).
   Link to related PRD or feature spec.

2. PROBLEM STATEMENT
   The technical problem being solved.
   Functional requirements at the technical level.
   Non-functional requirements: performance, scale, reliability, security.

3. BACKGROUND AND CONTEXT
   Relevant existing architecture.
   Constraints and dependencies.
   Why this change is needed now.

4. PROPOSED SOLUTION

   4.1 ARCHITECTURE OVERVIEW
   High-level description with component diagram or ASCII diagram.
   Key components and their responsibilities.

   4.2 DATA FLOW
   How data moves through the system.
   Sequence diagrams for key operations.

   4.3 COMPONENT DESIGN
   For each major component:
   - Responsibility
   - Interface (inputs and outputs)
   - Key implementation decisions

   4.4 DATA MODEL CHANGES
   New tables, fields, or schema changes.
   Migration strategy.

   4.5 API CHANGES
   New or modified endpoints.
   Request/response changes.

   4.6 THIRD-PARTY DEPENDENCIES
   New external services or libraries.
   Why chosen and what they provide.

5. ALTERNATIVES CONSIDERED
   For each alternative:
   - Description of the approach
   - Why it was considered
   - Why it was rejected

6. TRADEOFFS AND CONSEQUENCES
   What this design optimizes for.
   What it sacrifices.
   Long-term maintenance implications.

7. FAILURE MODES AND RELIABILITY
   How the system behaves when each component fails.
   Degradation modes.
   Recovery mechanisms.

8. SECURITY CONSIDERATIONS
   Attack surface changes.
   Authentication and authorization implications.
   Data exposure considerations.
   Reference to security review if required.

9. TESTING STRATEGY
   How this change will be tested.
   What automated tests are required.
   Testing challenges specific to this design.

10. IMPLEMENTATION PLAN
    Suggested implementation sequence.
    What can be done in parallel vs. what is sequential.
    Rollout strategy: feature flag, gradual rollout, etc.

11. OPEN QUESTIONS
    Unresolved design questions.
    Owner of each question.
    Decision needed by date.

12. REFERENCES
    Related ADRs.
    External documentation.
    Relevant prior art or related systems.
```

---

## Starter Prompt

```
You are a senior engineer writing a technical design document.

Product context: [link to PRD or feature spec being implemented]
Technical problem: [what the system must do at the technical level]
Performance requirements: [scale, latency, throughput requirements]
Current architecture context: [relevant existing systems and constraints]
Proposed approach: [the architecture being proposed]
Alternatives considered: [other approaches evaluated and why rejected]
Security considerations: [any security implications]
Open questions: [unresolved technical decisions]

Please produce a complete technical spec including:
1. Technical problem statement with non-functional requirements
2. Architecture overview with component descriptions
3. Data flow diagrams (ASCII or text-based)
4. Component design with interfaces
5. Data model and API changes
6. Alternatives considered with rejection rationale
7. Explicit tradeoffs accepted
8. Failure modes and recovery mechanisms
9. Security considerations
10. Implementation sequencing guidance
11. Open questions with owners

Flag any design decision that implies a significant tradeoff not explicitly acknowledged.
Flag any open question that could materially change the architecture if answered differently.
```

---

## Related Skills

| Use This Next | Why |
|---|---|
| `adr-architecture-decision.md` | Key decisions in the spec become standalone ADRs |
| `api-design-doc.md` | API changes specified in the tech spec get full API documentation |
| `database-schema-doc.md` | Schema changes specified here get full schema documentation |
| `test-plan.md` | Testing strategy in the spec becomes the full test plan |
| `security-review.md` | Security considerations flagged here trigger a security review |

*Skill file version: 1.0 | Phase: 05 - Engineering | Company type: Product*
