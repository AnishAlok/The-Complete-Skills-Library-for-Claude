# smoke-test-checklist.md

> **Skill:** Produces a pre-release smoke test checklist that verifies critical system functionality within minutes of a deployment, confirming viability before full testing or broad user exposure.

---

## TLDR

A smoke test is the fastest possible sanity check after a deployment: a short ordered checklist of the most critical system behaviors verified in sequence to confirm the deployment did not break anything fundamental. Designed for under 15 minutes execution, unambiguous pass/fail outcomes per item, and a clear go/no-go decision. Run after every production deployment without exception.

---

## Topic Explanation

### What Smoke Testing Is and Is Not

The term comes from hardware testing: power on the device, and if it does not smoke, basic functionality testing can proceed. In software: deploy the build, run a fast critical-path check, and if nothing fundamental is broken, proceed with further testing or release.

Smoke testing is NOT: a replacement for regression testing, a comprehensive feature check, or a performance test.

Smoke testing IS: the deployment verification step. It is not optional even for small, "low-risk" changes. Changes interact with production infrastructure in ways staging cannot always replicate.

### Why 15 Minutes Is the Hard Limit

A smoke test that takes more than 15 to 20 minutes has too many test items and will be skipped under time and delivery pressure. When the smoke test gets skipped, the first sign of a broken deployment is a customer report. Keep the checklist ruthlessly short.

If you cannot verify critical system health in 15 minutes, the answer is more automation and better observability, not a longer smoke test checklist.

### Ordering by Criticality

Smoke test items must be ordered by criticality with the most fundamental checks first. Authentication must pass before any authenticated functionality can be verified. Core navigation must work before specific feature tests make sense. A failure at step 3 stops the checklist; items 4 through 12 should not run if the system cannot authenticate users.

---

## Output Format

```
SMOKE TEST CHECKLIST

Product: [name]
Environment: [production / staging]
Version deployed: [exact build or version number]
Tester: [name or "automated"]
Date/Time: [timestamp when smoke test began]
Target execution time: [X minutes]

CRITICAL PATHS (ordered by criticality)
First failure stops execution and triggers the no-go decision.

[ ] SMOKE-001: [Test name]
    Steps: [1 to 3 steps maximum. Fewer is better.]
    Expected: [specific, observable pass criterion]
    Result: Pass / Fail / Blocked
    Notes: [if failed or blocked]

[ ] SMOKE-002: [Test name]
    Steps: [steps]
    Expected: [specific criterion]
    Result: Pass / Fail / Blocked
    Notes: [if failed or blocked]

[Continue. Maximum 15 items total. If you have more than 15, some belong in regression, not smoke.]

EXAMPLE ITEM SET:
[ ] SMOKE-001: Application loads without error
    Steps: Navigate to [URL]
    Expected: Page renders within 5 seconds. No error messages, blank screen, or 500 error.

[ ] SMOKE-002: User authentication works
    Steps: Enter test credentials. Click Sign In.
    Expected: Successfully authenticated. Redirected to dashboard. User name displayed.

[ ] SMOKE-003: Core navigation is functional
    Steps: Click through each top-level navigation item.
    Expected: Each section loads. No 404 or 500 errors on any navigation item.

[ ] SMOKE-004: [Primary feature of this product]
    Steps: [minimal steps to exercise the primary feature]
    Expected: [specific observable outcome]

[ ] SMOKE-005: [Critical integration or secondary feature]
    Steps: [steps]
    Expected: [specific criterion]

RESULT SUMMARY
Items passed: [N of N] | Failed: [N] | Blocked: [N]

DEPLOYMENT DECISION:
[ ] GO: All critical paths pass. Deployment is viable. Proceed.
[ ] NO-GO: [N] critical path(s) failed. Initiating rollback / investigation.
[ ] CONDITIONAL GO: [specific alternative verification completed. Describe what was done.]

Decision made by: [name]
Decision timestamp: [time]
```

---

## Starter Prompt

```
You are a QA engineer building a smoke test checklist for a product.

Product: [name and type: web / mobile / API]
Most critical user journeys: [flows that absolutely must work post-deployment]
Key integrations: [third-party or internal integrations to verify quickly]
Previous production incidents: [any areas that have broken in past deployments]
Time target: [maximum 15 minutes]
Automation status: [which items can be automated vs. require manual verification]

Produce a smoke test checklist targeting execution in under [N] minutes.
Every item must have a specific, observable pass criterion.
Order items by criticality with the most fundamental checks first.
Do not exceed 15 total items.
Items requiring more than 3 steps belong in regression, not smoke.
```

---

*Skill file version: 1.0 | Phase: 07 - Quality Assurance | Company type: Product*
