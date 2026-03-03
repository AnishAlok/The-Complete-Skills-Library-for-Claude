# infra-as-code-doc.md

> **Skill:** Produces infrastructure-as-code documentation covering the IaC tool and structure, resource inventory, environment management, state management, and operational procedures.

---

## TLDR

Infrastructure-as-code (IaC) documentation describes how infrastructure is defined, organized, and managed through code: what tool is used, how the code is structured, what resources are managed, how environments are differentiated, and how to safely make infrastructure changes. Used to onboard engineers to the infrastructure, plan changes, and troubleshoot issues.

---

## Topic Explanation

### IaC Tools Landscape

**Terraform:** The most widely used. Cloud-agnostic. Declarative. Large ecosystem of providers. State management is a key operational concern.

**AWS CDK / Pulumi:** Infrastructure defined in general-purpose languages (TypeScript, Python). More expressive than HCL. Better IDE support.

**Ansible:** Configuration management. Better for provisioning and configuration than resource lifecycle management.

**Helm:** Kubernetes package manager. Templated YAML for Kubernetes resources.

Most production environments use a combination: Terraform for cloud resources, Helm for Kubernetes workloads.

### State Management

Terraform and similar tools maintain state: a record of the current known state of managed resources. State management considerations:
- State should be stored remotely (S3, Terraform Cloud), not locally
- State should be locked during operations to prevent concurrent modifications
- State drift (real infrastructure diverging from state) must be detected and resolved

### Change Management for Infrastructure

Infrastructure changes carry higher risk than application code changes because they can affect availability, security, and data integrity. A plan/review/apply workflow:
1. **Plan:** Generate and review the execution plan before applying. What will change?
2. **Review:** Infrastructure changes should go through code review.
3. **Apply:** Apply in non-production first. Then production with a maintenance window if necessary.

---

## Output Format

```
1. IaC OVERVIEW
   Tool and version.
   What is managed with IaC vs. what is manually managed.
   Repository structure.
   Cloud provider(s).

2. REPOSITORY STRUCTURE
   Annotated directory tree.
   Organization principle: by environment / by service / by resource type.
   Module structure (if using modules).

3. RESOURCE INVENTORY
   All managed resources by category:
   - Compute (instances, containers, functions)
   - Networking (VPCs, subnets, security groups, load balancers)
   - Storage (databases, object storage, caches)
   - Security (IAM roles, policies, KMS keys)
   - Monitoring (log groups, dashboards, alerts)

4. ENVIRONMENT MANAGEMENT
   Environments managed.
   How environments are differentiated: workspace / directory / variables.
   Shared vs. environment-specific resources.

5. STATE MANAGEMENT
   State backend location and configuration.
   State locking mechanism.
   How to view current state.
   How to handle state drift.

6. VARIABLE AND SECRET MANAGEMENT
   Input variables and their sources.
   Sensitive variables: where stored, how injected.
   Environment-specific variable management.

7. CHANGE PROCEDURE
   How to make an infrastructure change:
   1. Branch and make changes
   2. Run plan and review output
   3. Submit for code review
   4. Apply to staging
   5. Verify in staging
   6. Apply to production
   7. Verify in production

8. COMMON OPERATIONS
   For each common task: exact commands with explanation.
   Adding a new resource.
   Modifying an existing resource.
   Destroying a resource.
   Importing an existing resource into state.

9. TROUBLESHOOTING
   Common IaC errors and resolutions.
   How to debug plan failures.
   State recovery procedures.
```

---

## Starter Prompt

```
You are a platform engineer writing infrastructure-as-code documentation.

IaC tool: [Terraform / CDK / Pulumi / etc.]
Cloud provider: [AWS / GCP / Azure / multi-cloud]
Repository structure: [how the IaC code is organized]
Managed resources: [what infrastructure is managed]
Environment strategy: [how environments are differentiated]
State backend: [where state is stored]
Change process: [how infrastructure changes are reviewed and applied]

Produce complete IaC documentation including resource inventory,
environment management approach, state management, change procedure,
and common operations reference with copy-pasteable commands.
```

---

*Skill file version: 1.0 | Phase: 05 - Engineering | Company type: Product*
