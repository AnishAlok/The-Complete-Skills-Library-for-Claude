# deployment-guide.md

> **Skill:** Produces a deployment process guide covering pre-deployment checks, deployment steps, verification procedures, rollback instructions, and post-deployment monitoring for a service.

---

## TLDR

A deployment guide documents the complete procedure for deploying a service to production: the prerequisites, the deployment steps, how to verify success, and how to roll back if something goes wrong. Written so that any engineer on the team can perform a deployment confidently and safely.

---

## Topic Explanation

### Zero-Downtime Deployment Strategies

**Blue-green deployment:** Maintain two identical environments (blue and green). Deploy to the inactive one, verify, then switch traffic. Instant rollback by switching back. Requires 2x infrastructure.

**Canary deployment:** Route a small percentage of traffic to the new version. Monitor. Gradually increase. Roll back by returning all traffic to the old version. Lower infrastructure cost than blue-green.

**Rolling deployment:** Replace instances one by one. Lower infrastructure requirement. Some instances running old code, some running new code simultaneously. Requires backward-compatible code changes.

**Feature flags:** Deploy code but control feature activation separately. Instant rollback by disabling the flag. Best for features that can be implemented behind a toggle.

The deployment guide should document which strategy is used and why, and the specific procedure for that strategy.

### Pre-Deployment Checklist

Many production incidents are caused by deployments that skip required pre-deployment checks. A mandatory pre-deployment checklist that must be completed before any deployment begins significantly reduces deployment-caused incidents. The checklist should be short enough to actually be used: 5 to 10 items maximum.

---

## Output Format

```
1. DEPLOYMENT GUIDE HEADER
   Service, deployment strategy, owner team, last updated.

2. DEPLOYMENT OVERVIEW
   Deployment strategy: blue-green / canary / rolling / feature flag.
   Typical deployment duration.
   Deployment frequency: how often deployments happen.
   Deployment window: any time restrictions.

3. PRE-DEPLOYMENT CHECKLIST
   [ ] All tests passing in CI
   [ ] Code review approved and merged
   [ ] Database migrations reviewed (if any)
   [ ] Dependent services notified (if breaking changes)
   [ ] Rollback plan confirmed
   [ ] On-call notified
   [ ] Any other team-specific checks

4. DEPLOYMENT STEPS
   Numbered, exact steps with copy-pasteable commands.
   For each step: what it does, expected output, time it takes.
   Decision points: "if you see X, proceed; if you see Y, stop and investigate."

5. DATABASE MIGRATIONS
   How to run migrations.
   How to verify migration success.
   How to roll back a migration.
   Caution: irreversible migrations (dropping columns, etc.)

6. VERIFICATION PROCEDURE
   Health check command and expected output.
   Smoke test procedure.
   Key metrics to verify are normal post-deployment.
   Timeframe to monitor before declaring deployment successful.

7. ROLLBACK PROCEDURE
   Step-by-step rollback commands.
   How to confirm rollback is complete.
   Any additional cleanup steps after rollback.
   Rollback decision criteria: what triggers a rollback.

8. POST-DEPLOYMENT MONITORING
   Dashboards to watch.
   Metrics to monitor and their expected values.
   Error rate and latency alert thresholds.
   How long to monitor before sign-off.

9. TROUBLESHOOTING COMMON DEPLOYMENT ISSUES
   For each common issue: symptom / cause / resolution.
```

---

## Starter Prompt

```
You are an engineer writing a deployment guide.

Service: [name]
Deployment strategy: [blue-green / canary / rolling / feature flag]
CI/CD platform: [Jenkins / GitHub Actions / CircleCI / etc.]
Infrastructure: [Kubernetes / ECS / bare metal / etc.]
Database migrations: [yes/no, and migration tool used]
Rollback capability: [how rollback works]
Monitoring: [what to watch post-deployment]

Produce a complete deployment guide with numbered, copy-pasteable steps.
Every step must include expected output and a decision point.
Rollback procedure must be as detailed as the deployment procedure.
```

---

*Skill file version: 1.0 | Phase: 05 - Engineering | Company type: Product*
