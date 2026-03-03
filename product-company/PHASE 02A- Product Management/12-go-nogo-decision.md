# go-nogo-decision.md

> **Skill:** Produces a go/no-go decision framework document that structures the evidence, criteria, and recommendation for whether to proceed with a product launch, feature release, or strategic bet.

---

## TLDR

A go/no-go decision document structures the judgment call about whether to proceed with a launch or release. It makes explicit what criteria must be met, what the current evidence shows against each criterion, who has decision authority, and what the recommendation is. Used before launches, releases, and major product bets.

---

## Topic Explanation

### Why Explicit Go/No-Go Criteria Matter

Launch decisions made without explicit criteria are made differently by different people based on their individual risk tolerance, organizational pressure, and incomplete information. Explicit criteria make the decision:
- Transparent: everyone can see the basis for the decision
- Consistent: the same criteria apply to every launch
- Defensible: the team can explain why they went or did not go
- Learnable: criteria that were wrong can be identified and changed

### Common Go/No-Go Criteria Categories

**Functionality:** Is the required scope complete and working?
**Quality:** Does the defect rate meet the threshold?
**Performance:** Do latency and uptime meet targets?
**Accessibility:** Are WCAG requirements met?
**Security:** Has a security review been completed?
**Operational readiness:** Is support trained? Is monitoring in place?
**Business readiness:** Is pricing set? Is legal reviewed? Is marketing ready?
**Risk:** Are known risks within acceptable bounds?

Not all criteria are equal. Define which are mandatory (blocking) vs. advisory (can proceed with a mitigation plan).

---

## Output Format

```
1. DECISION HEADER
   Initiative, planned launch date, decision owner, date of review.

2. SCOPE OF WHAT IS LAUNCHING
   Exact scope in this release.
   What is explicitly excluded.

3. GO/NO-GO CRITERIA TABLE
   For each criterion:
   - Criterion name
   - Type: Blocking / Advisory
   - Threshold: what "pass" looks like
   - Current status: Pass / Fail / Partial / Unknown
   - Evidence
   - Owner

4. OPEN RISKS
   Known risks that exist even if criteria are met.
   Mitigation plan for each.
   Risk owner.

5. RECOMMENDATION
   Go / No-Go / Conditional Go (with conditions listed)
   Rationale.
   Decision authority sign-off.

6. IF NO-GO: PATH TO GO
   What must change for a go decision.
   Revised timeline.
   Owner for each blocker.

7. POST-LAUNCH MONITORING PLAN
   Key metrics to watch in the first 24/48/72 hours.
   Rollback trigger: what would cause an immediate rollback.
   Rollback procedure.
```

---

## Starter Prompt

```
You are a product manager running a go/no-go decision review.

Initiative: [what is being launched]
Launch scope: [exact feature or product scope]
Planned launch date: [when]
Current status: [what is done vs. not done]
Known risks: [issues or uncertainties]
Decision authority: [who can approve a go decision]
Post-launch monitoring: [what you will watch]

Produce a complete go/no-go decision document with criteria table,
risk assessment, recommendation, and post-launch monitoring plan.
Distinguish blocking criteria from advisory criteria.
```

---

*Skill file version: 1.0 | Phase: 02 - Product Management | Company type: Product*
