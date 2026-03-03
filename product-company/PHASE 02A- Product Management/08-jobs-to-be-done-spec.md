# jobs-to-be-done-spec.md

> **Skill:** Produces a JTBD-framed feature specification that grounds requirements in the job the customer is hiring the product to do, the desired outcomes they are seeking, and the forces that drive switching behavior.

---

## TLDR

A JTBD feature spec reframes requirements around the job the customer is trying to get done: the progress they are trying to make in their situation. Instead of "users want a compliance report export feature," it says "operators need to demonstrate compliance to their accountant without spending time manually assembling documentation." This framing produces more durable and targeted requirements.

---

## Topic Explanation

### The Job Statement

A JTBD job statement (Ulwick format): [direction verb] + [object] + [context/clarifier]

"Minimize the time required to demonstrate payroll compliance to an external auditor."
"Increase confidence that tip pool distributions are legally defensible."

Job statements describe the outcome the customer seeks, not the feature they want.

### Outcome Statements

Outcomes are the criteria customers use to evaluate whether the job is being done well. Ulwick's format: [direction] + [performance metric] + [object] + [context]

"Minimize the likelihood of errors in overtime calculations during payroll processing."
"Minimize the time needed to identify which employees need corrective action."

Opportunity scoring combines importance (how important is this outcome to the customer) with satisfaction (how well are current solutions delivering it). Outcomes with high importance and low satisfaction are underserved opportunities.

### Forces of Progress (Moesta)

The four forces that determine whether a customer adopts a new solution:
- **Push:** The dissatisfaction with the current situation driving change
- **Pull:** The attraction of the new solution
- **Anxiety:** The fear and uncertainty about adopting the new solution
- **Habit:** The inertia of the current way of doing things

A JTBD spec addresses all four forces: it ensures the product delivers enough pull to overcome habit and anxiety, and addresses the push that makes customers ready to change.

---

## Output Format

```
1. JOB CONTEXT
   The specific situation that triggers this job.
   Who is doing the job (job performer) and who benefits (beneficiary).

2. MAIN JOB STATEMENT
   The job in Ulwick format: [direction] + [object] + [context].

3. DESIRED OUTCOMES
   The criteria customers use to evaluate job completion.
   Format: [direction] + [metric] + [object] + [context].
   Opportunity scores if research data is available.

4. RELATED JOBS (job map)
   Upstream jobs: what the customer does before this job.
   Downstream jobs: what the customer does after.
   Emotional and social dimensions of the job.

5. FORCES ANALYSIS
   Push: what dissatisfaction makes customers ready for change.
   Pull: what must the solution offer to attract adoption.
   Anxiety: what concerns must the solution address.
   Habit: what inertia must the solution overcome.

6. SOLUTION REQUIREMENTS (JTBD-grounded)
   For each requirement, the outcome it serves.
   Makes explicit the connection between solution and job.

7. WHAT WOULD MAKE THE JOB "PERFECTLY DONE"
   The ideal outcome if there were no constraints.
   Used to identify the north star for the feature.
```

---

## Starter Prompt

```
You are a product manager writing a JTBD-framed feature specification.

Customer situation: [the context in which this job arises]
What the customer is trying to accomplish: [the progress they want to make]
Current solution: [how they currently do this job]
Research data: [interview quotes or findings about the job]
Feature being built: [what product capability is being specified]

Produce a JTBD feature spec including job statement, desired outcomes,
forces analysis, and JTBD-grounded solution requirements.
Connect each requirement explicitly to the outcome it serves.
```

---

*Skill file version: 1.0 | Phase: 02 - Product Management | Company type: Product*
