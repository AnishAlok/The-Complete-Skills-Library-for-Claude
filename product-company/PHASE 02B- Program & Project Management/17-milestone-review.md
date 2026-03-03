# milestone-review.md

> **Skill:** Produces a milestone review document that evaluates project status at a key milestone, assesses readiness to proceed, and produces a go/no-go decision with documented rationale.

---

## TLDR

A milestone review is a structured checkpoint at a planned project milestone that asks: *"Are we ready to proceed to the next phase, or do we need to resolve issues before moving forward?"* It produces a documented assessment against pre-defined criteria and a go/no-go decision. Used at each planned milestone to prevent problems from compounding across phases.

---

## Topic Explanation

### Milestone Reviews vs. Status Reports

**Status reports:** Continuous. Report on progress toward the next milestone. May surface issues but do not make go/no-go decisions.

**Milestone reviews:** Point-in-time. Evaluate whether a specific milestone has been met. Make a formal go/no-go decision. More consequential.

Milestone reviews should be defined in the project charter with their criteria documented before the project begins. Criteria defined at the milestone review, after the team knows whether they have met them, are subject to bias.

### Pre-Defined Exit Criteria

The most important design decision in a milestone review process is defining the exit criteria for each milestone before the project begins. Exit criteria are the specific conditions that must be true to proceed to the next phase.

Good exit criteria are:
- Binary: either met or not met (no partial credit)
- Observable: evidence can be gathered to confirm them
- Meaningful: they genuinely indicate readiness for the next phase

Common exit criteria by phase type:
- **Discovery exit:** Research complete, problem validated, target user defined
- **Design exit:** Design approved, usability tested, spec complete
- **Build exit:** Code complete, tests passing, performance validated
- **Launch exit:** All go/no-go criteria in the launch checklist met

### The Escalation Principle

If a milestone review produces a no-go decision, it must be escalated to the project sponsor immediately. A no-go decision means the project cannot proceed as planned. This is a sponsor-level decision, not a PM-level decision.

---

## Output Format

```
1. REVIEW HEADER
   Project name, milestone name, review date, attendees.
   Review facilitator, decision authority.

2. MILESTONE DEFINITION
   What this milestone represents.
   Why it is a meaningful checkpoint.
   The original planned date vs. actual review date.

3. EXIT CRITERIA ASSESSMENT
   For each exit criterion:
   - Criterion description
   - Status: Met / Not met / Partially met
   - Evidence
   - Owner of the criterion

4. DELIVERABLES REVIEW
   For each planned deliverable at this milestone:
   - Deliverable name
   - Status: Complete / In progress / Not started
   - Quality assessment
   - Acceptance: Accepted / Not accepted / Pending review

5. OUTSTANDING ISSUES AND RISKS
   Any open issues that are unresolved at this milestone.
   Any elevated risks since the last milestone review.
   Impact of each on the decision.

6. GO / NO-GO DECISION

   RECOMMENDATION: Go / No-Go / Conditional Go

   GO: All exit criteria met. Proceed to next phase.

   CONDITIONAL GO: [conditions that must be met before or during next phase]
   - Condition 1: [description] / Owner / Due date
   - Condition 2: [description] / Owner / Due date

   NO-GO: [the specific criteria not met]
   PATH TO GO:
   - Action required / Owner / Timeline
   Revised milestone date.

7. DECISION AUTHORITY SIGN-OFF
   Decision authority name, signature, date.
   Sponsor notification if No-Go.

8. LESSONS APPLICABLE TO NEXT PHASE
   What this phase taught the team.
   Adjustments to the plan for the next phase.
```

---

## Starter Prompt

```
You are a PM facilitating a milestone review.

Project: [name and context]
Milestone: [what this milestone represents]
Planned date vs. actual: [dates]
Exit criteria: [the pre-defined criteria for this milestone]
Deliverables due: [what should be complete]
Current status: [which criteria are met vs. not met]
Outstanding issues: [any open issues]
Decision authority: [who must sign off on the go/no-go]

Produce a complete milestone review document with exit criteria assessment,
deliverables review, and a clear go/no-go recommendation with documented rationale.
If no-go, produce a specific path-to-go with owners and dates.
```

---

## Related Skills

| Use This Before | Why |
|---|---|
| `project-charter.md` | Exit criteria defined in the charter are reviewed here |
| `risk-register.md` | Risk register is reviewed at every milestone |
| `escalation-protocol.md` | No-go decisions trigger escalation to sponsor |

*Skill file version: 1.0 | Phase: 04 - Program and Project Management | Company type: Product*
