# developer-guide.md

> **Skill:** Produces a developer onboarding guide covering local environment setup, codebase overview, development workflow, testing, and contribution standards for a new engineer joining a team.

---

## TLDR

A developer guide is the document a new engineer follows on day one to get from zero to a working development environment and their first contribution. It covers: environment setup, codebase navigation, development workflow, testing approach, and team standards. Written to be self-service: a new engineer should be able to follow it without blocking on anyone.

---

## Topic Explanation

### The Time-to-First-PR Metric

The quality of a developer guide can be measured by time-to-first-PR: how long does it take a new engineer to make their first real contribution? A good developer guide enables time-to-first-PR in under two weeks. A poor one means the first PR takes a month because the engineer spent weeks resolving setup issues and navigating undocumented conventions.

### What New Engineers Actually Need

New engineers consistently report the same gaps in developer documentation:
- **Environment setup:** The README says "run `make setup`" but it fails for 3 different reasons depending on the developer's OS and configuration. Complete setup with troubleshooting for common errors.
- **Codebase navigation:** Where is the code for X? What is this folder for? An annotated directory structure solves this.
- **The unwritten rules:** Code style, PR conventions, testing standards, the informal process for how decisions are made. These are never in documentation but every new engineer needs them.
- **Who to ask:** When the guide doesn't answer a question, who should they ask? Named contacts for different topics.

---

## Output Format

```
1. GUIDE HEADER
   Service/codebase, team, last updated. Estimated setup time.

2. PREREQUISITES
   Required accounts (with links to request access).
   Required software with minimum versions.
   Required hardware specs.

3. LOCAL ENVIRONMENT SETUP
   Step-by-step with exact commands.
   Expected output at each step.
   Troubleshooting for the most common setup errors.
   Verification: "You know setup is complete when..."

4. CODEBASE OVERVIEW
   Annotated directory structure.
   Key entry points: where does the application start?
   Key files: configuration, main application logic, tests.
   Architectural overview with pointer to system design doc.

5. DEVELOPMENT WORKFLOW
   Branching strategy and naming conventions.
   How to pick up a ticket.
   Development loop: code, test locally, commit.
   How to run the application locally.
   How to run tests locally.

6. TESTING
   How to run the full test suite.
   How to run a specific test.
   Test organization: where to find tests, how to name them.
   Coverage requirements.

7. SUBMITTING CODE
   PR process: how to open a PR.
   PR description template.
   Code review process: what to expect, typical turnaround.
   CI checks: what must pass before merge.
   Merge strategy: squash / rebase / merge commit.

8. TEAM CONVENTIONS
   Code style and linting (with automation setup).
   Logging conventions.
   Error handling patterns.
   Documentation requirements.
   Commit message format.

9. TEAM CONTACTS
   By topic: who to ask about what.
   Where to ask: Slack channels for different topics.
   Meeting schedule: standups, planning, reviews.

10. COMMON TASKS REFERENCE
    Quick reference for the tasks done most frequently:
    start local server, run tests, add a migration, deploy to staging, etc.
```

---

## Starter Prompt

```
You are a senior engineer writing a developer onboarding guide.

Service/codebase: [what this guide covers]
Tech stack: [languages, frameworks, databases, infrastructure]
Prerequisites: [required accounts, tools, and hardware]
Setup process: [steps to get a working local environment]
Development workflow: [how code gets from idea to production]
Testing approach: [how the team writes and runs tests]
Team conventions: [code style, PR process, standards]
Common issues: [setup problems new engineers frequently encounter]

Produce a complete developer guide that enables a new engineer to reach
a working development environment and first PR without blocking on others.
Include troubleshooting for common setup issues.
All commands must be exact and copy-pasteable.
```

---

*Skill file version: 1.0 | Phase: 05 - Engineering | Company type: Product*
