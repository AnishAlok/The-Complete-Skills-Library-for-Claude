# uat-sign-off.md

> **Skill:** Produces a UAT sign-off and formal acceptance document recording test completion, outstanding issues, acceptance conditions, and the authorized decision to accept or reject the system for production deployment.

---

## TLDR

The UAT sign-off document formally records the outcome of UAT: what was tested, the results, outstanding issues and how they will be resolved, and the authorized acceptance or rejection of the system. It is the contractual record that stakeholders have reviewed, evaluated, and either accepted the system or documented the conditions of acceptance.

---

## Topic Explanation

### Why Formal Sign-Off Matters

Informal sign-off creates three recurring problems:

No audit trail when issues arise post-launch. "But you said it was fine" is not a useful record when a defect surfaces in production.

Scope creep from undocumented post-acceptance requests. Stakeholders who did not formally commit to accepting the system continue requesting changes indefinitely.

Projects that never close. Without a formal sign-off event, UAT lingers in a perpetual "almost done" state that delays deployment and consumes resources.

A sign-off document closes the loop cleanly: what was tested, what was accepted, under what conditions, and what is deferred.

### Conditional Acceptance

Perfect UAT completion is rare. Conditional acceptance is the practical and acceptable outcome: the system is approved for production with documented conditions that must be met before or shortly after go-live.

Every deferred defect must specify: the owner responsible for fixing it, the target resolution date, whether a workaround exists, and the named stakeholder who accepts the risk of deferral. Vague deferral statements are not acceptable.

---

## Output Format

```
UAT SIGN-OFF DOCUMENT

Project: [name]
Release version: [version]
UAT period: [start date to end date]
Sign-off date: [date]
Document version: [1.0]

1. UAT EXECUTION SUMMARY
   Scenarios planned: [N]
   Scenarios executed: [N]
   Scenarios passed: [N]
   Scenarios failed: [N]
   Scenarios not run: [N] with reasons

2. DEFECT SUMMARY
   Total defects raised during UAT: [N]
   By severity: Critical [N] / High [N] / Medium [N] / Low [N]
   Resolved during UAT: [N]
   Deferred to post-launch: [N]

3. DEFERRED DEFECTS
   For each deferred defect:
   - Defect ID and description
   - Severity
   - Workaround: available [description] / not available
   - Owner: [named person]
   - Target resolution date: [date]
   - Risk accepted by: [name and role]

4. CONDITIONS FOR ACCEPTANCE
   For each condition attached to acceptance:
   - Condition description
   - Owner
   - Due date
   - Verification method: how completion will be confirmed

5. ACCEPTANCE DECISION

   ACCEPTED
   The system has been tested and meets the business requirements
   defined in the UAT plan. Approved for production deployment.

   ACCEPTED WITH CONDITIONS
   The system is approved for production deployment subject to
   all conditions in Section 4 being met as specified.

   NOT ACCEPTED
   Outstanding issues preventing acceptance:
   Required actions before resubmission:

6. AUTHORIZED SIGNATURES
   Name | Role | Signature | Date
   [One row per required signatory]

7. DOCUMENT DISTRIBUTION
   Recipients: [list]
   Stored at: [document location]
```

---

## Starter Prompt

```
You are preparing a UAT sign-off document.

UAT results: [scenarios run, passed, failed, not run with reasons]
Defects raised: [list with severities]
Defects resolved during UAT: [count]
Deferred defects: [list with workarounds and resolution commitments]
Acceptance conditions: [any conditions attached to sign-off]
Signatories: [names and roles required to sign]
Decision: [accepted / accepted with conditions / not accepted]

Produce a complete UAT sign-off document.
Every deferred defect must have a named owner, a specific due date,
a workaround assessment, and explicit risk acceptance by a named stakeholder.
Every acceptance condition must be specific and verifiable.
```

---

## Related Skills

| Use This Before | Why |
|---|---|
| `uat-plan.md` | Sign-off document is the outcome record of the UAT plan |

*Skill file version: 1.0 | Phase: 07 - Quality Assurance | Company type: Product*
