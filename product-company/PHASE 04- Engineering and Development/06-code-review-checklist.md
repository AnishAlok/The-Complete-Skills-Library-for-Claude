# code-review-checklist.md

> **Skill:** Produces a code review checklist and standards guide that helps reviewers evaluate correctness, security, maintainability, performance, and test coverage consistently.

---

## TLDR

A code review checklist provides reviewers with a consistent set of questions to ask about every pull request, reducing the chance that important concerns are missed and raising the floor of review quality across the team. This skill produces a checklist organized by concern area, paired with a standards guide that explains the reasoning behind each check.

---

## Topic Explanation

### What Code Review Is For (and What It Is Not)

Code review serves multiple purposes:
- Catching bugs and logic errors
- Identifying security vulnerabilities
- Ensuring code meets team standards
- Knowledge sharing across the team
- Building collective code ownership

What code review is NOT for:
- Style enforcement (that is what linters and formatters are for)
- Demonstrating reviewer superiority
- Blocking work due to personal taste differences

The checklist should focus on objective concerns (correctness, security, performance, testability) not subjective ones (variable naming preferences, code organization habits).

### The Conventional Comment Standard

Conventional Comments (conventionalcomments.org) provides a vocabulary for code review feedback that communicates type and urgency:

- `suggestion:` Nice to have. Reviewer would change it but it is not blocking.
- `issue:` Must be resolved. Blocking concern.
- `question:` Asking for understanding, not necessarily requesting a change.
- `nit:` Minor style or preference. Non-blocking.
- `praise:` Acknowledging something done well.
- `thought:` An idea for consideration. Not a blocking request.

Teams that use conventional comments reduce friction and misunderstanding in code review significantly.

### Review Time Allocation

Reviewers who spend more than 60 to 90 minutes on a single review produce diminishing returns and miss issues due to fatigue. Large PRs should be broken into smaller ones. A PR larger than 400 lines of changed code is typically too large for a single effective review.

---

## Output Format

```
1. REVIEW STANDARDS INTRODUCTION
   Purpose of code review at this organization.
   Scope: what types of PRs require review.
   SLA: expected response time.
   Conventional comment vocabulary used.

2. PRE-REVIEW CHECKLIST (Author, before submitting)
   [ ] PR description explains what changed and why
   [ ] PR is scoped appropriately (< 400 lines changed)
   [ ] Self-review completed
   [ ] Tests written and passing
   [ ] Linter passing
   [ ] No debug code or TODOs without tracking issues

3. REVIEWER CHECKLIST

   CORRECTNESS
   [ ] Logic is correct for all stated cases
   [ ] Edge cases are handled
   [ ] Error handling is complete and appropriate
   [ ] No race conditions in concurrent code
   [ ] Off-by-one errors in loops and indexes

   SECURITY
   [ ] No secrets, credentials, or PII in code or logs
   [ ] Input validation present for all user-controlled input
   [ ] SQL queries use parameterized queries (no string interpolation)
   [ ] Authentication and authorization checks are correct
   [ ] Dependencies do not introduce known CVEs

   PERFORMANCE
   [ ] No N+1 query patterns introduced
   [ ] Database queries use appropriate indexes
   [ ] No unnecessarily expensive operations in hot paths
   [ ] Caching opportunities considered

   MAINTAINABILITY
   [ ] Code is understandable without excessive explanation
   [ ] Functions and variables are named clearly
   [ ] Complex logic has explanatory comments
   [ ] No unnecessary duplication
   [ ] Abstractions are at the right level

   TESTING
   [ ] Happy path is tested
   [ ] Error cases are tested
   [ ] Edge cases identified in the code are tested
   [ ] Tests are actually testing behavior, not implementation

   API AND INTERFACES
   [ ] Public interfaces are backward compatible (or version bump justified)
   [ ] Breaking changes are documented
   [ ] API contracts match the API design doc

   DATA
   [ ] Database migrations are reversible
   [ ] Data migrations handle existing data correctly
   [ ] Schema changes are backward compatible during rollout

4. APPROVAL STANDARDS
   Required approvals before merge.
   Blocking vs. non-blocking comment resolution policy.
   How to handle reviewer disagreements.

5. CONVENTIONAL COMMENT GUIDE
   Full vocabulary with examples.
```

---

## Starter Prompt

```
You are an engineering lead writing a code review checklist and standards guide.

Team: [size and technical context]
Tech stack: [languages and frameworks]
Specific concerns: [any areas of particular importance, e.g., security-sensitive codebase]
Current review problems: [issues with current review culture or consistency]
PR size norms: [typical PR sizes]
Approval requirements: [how many approvals are required]

Produce a complete code review checklist organized by concern area.
Include a standards guide explaining the reasoning behind key checks.
Include conventional comment vocabulary.
Flag which checks are blocking (must be resolved) vs. non-blocking.
```

---

*Skill file version: 1.0 | Phase: 05 - Engineering | Company type: Product*
