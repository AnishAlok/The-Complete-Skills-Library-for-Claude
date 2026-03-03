# ci-cd-pipeline-doc.md

> **Skill:** Produces CI/CD pipeline documentation covering pipeline stages, quality gates, deployment targets, secret management, and troubleshooting for a software delivery pipeline.

---

## TLDR

CI/CD pipeline documentation describes how code moves from a developer's branch to production: the stages, what checks happen at each stage, how artifacts are built and stored, how deployments are triggered, and how to troubleshoot pipeline failures. Used to onboard new engineers, debug pipeline issues, and plan pipeline changes.

---

## Topic Explanation

### CI vs. CD

**Continuous Integration (CI):** The practice of automatically building and testing code on every commit. Goal: detect integration problems early.

**Continuous Delivery (CD):** The practice of automatically deploying every successful build to at least a staging environment, with a manual gate before production. Goal: always have a deployable artifact.

**Continuous Deployment:** Every successful build is automatically deployed to production. No manual gate. Only appropriate for mature teams with high test coverage and robust monitoring.

Most teams practice CI and Continuous Delivery with a manual production deployment gate.

### Pipeline Stage Best Practices

**Fail fast:** Put the fastest checks first. Linting and unit tests should run before integration tests. Integration tests before performance tests. Don't make developers wait for slow checks when fast ones would have caught the issue.

**Artifact promotion:** Build the artifact once. Promote the same artifact through environments. Don't rebuild for staging vs. production. Rebuilding introduces the risk of non-deterministic build outputs.

**Environment parity:** Staging should mirror production as closely as possible. Config differences should be minimal and documented.

---

## Output Format

```
1. PIPELINE OVERVIEW
   Service, CI/CD platform, deployment targets, pipeline trigger conditions.
   Diagram: stages and flow.

2. PIPELINE STAGES

   For each stage:
   - Stage name
   - Trigger: what causes this stage to run
   - Duration: typical execution time
   - What it does: specific steps
   - Quality gate: what must pass to proceed
   - Artifacts produced or consumed
   - Failure behavior: what happens when this stage fails

3. ENVIRONMENT CONFIGURATION
   Environments: dev / staging / production.
   For each environment:
   - How deployments are triggered
   - Manual vs. automatic promotion
   - Configuration differences from production

4. SECRET AND CREDENTIAL MANAGEMENT
   Where secrets are stored.
   How they are injected into the pipeline.
   Rotation procedure.
   Who has access to secrets.

5. ARTIFACT MANAGEMENT
   What is built and where it is stored.
   Artifact naming and versioning.
   Retention policy.
   How artifacts are promoted between environments.

6. NOTIFICATIONS AND ALERTS
   Who is notified on pipeline failure.
   Channel (Slack, email, pagerduty).
   What information is included in notifications.

7. ROLLBACK PROCEDURE
   How to trigger a rollback from the pipeline.
   How to redeploy a specific artifact version.

8. TROUBLESHOOTING GUIDE
   Common pipeline failures with resolution steps.
   How to access logs for each stage.
   Who to contact for pipeline infrastructure issues.

9. PIPELINE MAINTENANCE
   How to update pipeline configuration.
   Testing pipeline changes (pipeline for the pipeline).
   Documentation update responsibility.
```

---

## Starter Prompt

```
You are a platform engineer writing CI/CD pipeline documentation.

Service: [what is being built and deployed]
CI/CD platform: [GitHub Actions / Jenkins / CircleCI / GitLab CI / etc.]
Pipeline stages: [the stages from commit to production]
Deployment targets: [dev / staging / production environments]
Secret management: [how credentials are handled]
Artifact strategy: [how build artifacts are managed]
Rollback capability: [how to rollback deployments]

Produce complete CI/CD pipeline documentation including stage descriptions,
quality gates, environment configuration, secret management, and
troubleshooting guide with common failure resolutions.
```

---

*Skill file version: 1.0 | Phase: 05 - Engineering | Company type: Product*
