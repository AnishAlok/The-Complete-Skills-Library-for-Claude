# wbs-breakdown.md

> **Skill:** Produces a Work Breakdown Structure that decomposes a project into hierarchical work packages and tasks, creating the foundation for scheduling, resourcing, and cost estimation.

---

## TLDR

A Work Breakdown Structure (WBS) is the hierarchical decomposition of all project work into manageable components. It answers the question: *"What exactly is all the work?"* before addressing when, who, or how much. Every project deliverable becomes a work package. Every work package breaks into tasks. The WBS ensures nothing is missed and creates the structure the project plan is built on.

---

## Topic Explanation

### The WBS Is Deliverable-Oriented, Not Activity-Oriented

The most important design principle of a WBS: it is organized around deliverables, not activities. The question at each level is "what must be produced?" not "what must be done?"

**Wrong (activity-oriented):** 1.0 Research, 2.0 Design, 3.0 Build, 4.0 Test
**Right (deliverable-oriented):** 1.0 User Research Report, 2.0 Design System Component, 3.0 Working Feature, 4.0 Tested and Signed-Off Feature

Deliverable-oriented WBS makes scope verification possible: you can check whether each deliverable was produced. Activity-oriented WBS makes it hard to verify completion.

### The 100% Rule

The 100% rule is the most important WBS quality check: the child level must represent 100% of the work in its parent. No work should be in a parent level that is not represented in a child. No work should be in a child that is not in the parent's scope.

### WBS Dictionary

Each WBS element should have a dictionary entry that describes:
- The deliverable or output
- The quality standard it must meet
- The acceptance criteria for completion
- The responsible person or team

The WBS dictionary is what transforms a task list into a requirements document.

### Level of Detail

Work packages should be sized such that:
- They can be completed within a single reporting period (typically 1 to 2 weeks)
- They can be estimated with reasonable accuracy
- Their completion can be clearly verified

Work that is too large to estimate or verify needs to be decomposed further.

---

## Output Format

```
1. WBS HEADER
   Project name, version, date, PM. WBS coding scheme used.

2. WBS TREE STRUCTURE
   Level 0: Project (total scope)
   Level 1: Major deliverables / phases
   Level 2: Sub-deliverables / work packages
   Level 3: Tasks (if needed for large work packages)

   Format: [ID] [Name] [Owner] [Estimated Effort]
   1.0 Project Name
     1.1 Deliverable 1
       1.1.1 Work Package A
         1.1.1.1 Task 1
         1.1.1.2 Task 2
       1.1.2 Work Package B
     1.2 Deliverable 2
       ...

3. WBS DICTIONARY
   For each work package (Level 2):
   - ID and name
   - Description: what must be produced
   - Acceptance criteria: how completion is verified
   - Responsible: named individual or team
   - Estimated effort
   - Dependencies: which packages must precede

4. SCOPE VERIFICATION CHECKLIST
   For each Level 1 deliverable:
   - Confirmation that 100% of scope is represented at lower levels
   - Items that are in scope but not yet fully decomposed (with plan to decompose)

5. EXCLUDED SCOPE
   Work explicitly excluded from the WBS and why.
   (Cross-reference with charter out-of-scope section)
```

---

## Starter Prompt

```
You are a project manager building a Work Breakdown Structure.

Project scope: [the deliverables the project must produce]
Charter out-of-scope: [what is explicitly excluded]
Team structure: [who will be doing the work]
Granularity needed: [how detailed the WBS should be]

Produce a complete WBS organized by deliverables (not activities) using
a hierarchical numbering scheme. Include a WBS dictionary for each work package.
Apply the 100% rule: verify that child elements account for all parent scope.
Flag any area where the work is not yet well-enough understood to decompose fully.
```

---

*Skill file version: 1.0 | Phase: 04 - Program and Project Management | Company type: Product*
