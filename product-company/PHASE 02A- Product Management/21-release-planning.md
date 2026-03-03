# release-planning.md

> **Skill:** Produces a release plan that defines scope, dates, owners, release strategy, rollout plan, and success criteria for a product release.

---

## TLDR

A release plan is the operational document that coordinates everything needed to ship: what is included, who does what, when it ships, to whom, and how success is measured. It bridges product completion and customer delivery. Used when planning any significant product release or feature launch.

---

## Topic Explanation

### Release vs. Launch vs. Deploy

**Deploy:** The technical act of moving code to production. Can happen independently of a release.
**Release:** Making a feature or product available to users. A deploy becomes a release when users can access the change.
**Launch:** A go-to-market event around a release. Not all releases are launches. Launches involve marketing, sales enablement, and customer communication.

Decoupling deploy from release (using feature flags) is now standard practice. It allows code to be deployed to production and tested before users can see it.

### Release Strategies

**Big bang:** All users get the change at once. Simplest operationally. Highest risk.
**Percentage rollout:** Release to a percentage of users, monitor, then expand. Reduces blast radius of issues.
**Beta release:** Release to a defined group of willing users. Collects early feedback. Requires managing beta group.
**Canary release:** Release to a small percentage of servers/users in parallel with the old version. Quickly roll back if issues emerge.
**Feature flag:** Feature is deployed but behind a flag. Can be enabled/disabled instantly per user, segment, or globally.

---

## Output Format

```
1. RELEASE HEADER
   Release name/version, target date, PM, engineering lead, release strategy, status.

2. RELEASE SCOPE
   Features and changes included in this release.
   What was explicitly cut or deferred.
   Known limitations or temporary workarounds.

3. RELEASE STRATEGY
   Which release strategy (big bang / percentage / beta / feature flag).
   Rollout sequence: who gets it when.
   Timeline for full rollout if not big bang.

4. PRE-RELEASE CHECKLIST
   Engineering: code complete, tests passing, performance validated.
   Design: QA complete, sign-off obtained.
   Documentation: updated and published.
   Support: trained and briefed.
   Monitoring: alerts configured.
   Rollback: rollback procedure tested.

5. COMMUNICATION PLAN
   Internal communication: who is notified and when.
   Customer communication: in-app, email, changelog.
   Sales enablement: battlecard, demo script updates.
   Customer success: briefing on what changed and how to support.

6. LAUNCH ACTIVITIES (if this is a launch, not just a release)
   Marketing activities: blog post, social, PR.
   Sales activities: updated collateral, customer outreach.
   Timeline for each activity.

7. MONITORING AND SUCCESS METRICS
   Key metrics to watch in the 24/48/72 hours post-release.
   Baseline values before release.
   Thresholds that would trigger rollback or fast-follow fix.

8. ROLLBACK PLAN
   Rollback procedure.
   Decision criteria: what triggers a rollback vs. a fast follow-up fix.
   Owner for the rollback decision.
```

---

## Starter Prompt

```
You are a product manager writing a release plan.

Release scope: [features and changes being released]
Target date: [when it ships]
Release strategy: [big bang / percentage / beta / feature flag]
Pre-release requirements: [what must be done before shipping]
Communication audiences: [who needs to be notified and how]
Success metrics: [what to watch post-release]
Rollback criteria: [what would trigger a rollback]

Produce a complete release plan with scope, strategy, pre-release checklist,
communication plan, monitoring metrics, and rollback procedure.
```

---

*Skill file version: 1.0 | Phase: 02 - Product Management | Company type: Product*
