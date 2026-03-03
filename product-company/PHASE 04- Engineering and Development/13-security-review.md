# security-review.md

> **Skill:** Produces a security threat model and review document that identifies attack surfaces, potential threats, security controls, and remediation requirements for a feature or system.

---

## TLDR

A security review documents the security analysis of a feature or system: what the attack surface is, what threats could exploit it, what controls are in place, and what additional controls are needed before launch. Used before any feature that handles sensitive data, modifies authentication or authorization, exposes a new API surface, or has potential for significant security impact.

---

## Topic Explanation

### STRIDE Threat Model

STRIDE (Microsoft) is the most widely used framework for threat identification:

**S - Spoofing:** An attacker impersonates another user or system. Mitigation: strong authentication.
**T - Tampering:** Data is modified in transit or at rest. Mitigation: integrity controls, signatures, HTTPS.
**R - Repudiation:** Actions cannot be traced to who performed them. Mitigation: audit logging.
**I - Information disclosure:** Sensitive data is exposed to unauthorized parties. Mitigation: encryption, access controls, data minimization.
**D - Denial of service:** The system is made unavailable. Mitigation: rate limiting, input validation, circuit breakers.
**E - Elevation of privilege:** A user gains unauthorized capabilities. Mitigation: authorization checks, principle of least privilege.

### OWASP Top 10

The OWASP Top 10 is the most referenced list of critical web application security risks. A security review for a web feature should check against the current OWASP Top 10, which includes: broken access control, cryptographic failures, injection, insecure design, security misconfiguration, vulnerable components, authentication failures, software integrity failures, logging and monitoring failures, SSRF.

### Security Review Triggers

Not every feature change requires a full security review. Common triggers:
- Changes to authentication or authorization logic
- New API endpoints exposed externally
- Changes to how PII is stored, transmitted, or processed
- New external integrations
- New file upload or processing capabilities
- Changes to payment or financial processing

---

## Output Format

```
1. REVIEW HEADER
   Feature/system, reviewer(s), date, severity finding summary, sign-off.

2. SCOPE
   What is being reviewed.
   Systems and components in scope.
   Explicit out-of-scope items.

3. ATTACK SURFACE ANALYSIS
   New attack surface introduced by this change.
   Data inputs and their trust levels.
   Authentication and authorization boundaries.
   External integrations and their trust levels.

4. THREAT MODEL (STRIDE)

   For each identified threat:
   - Threat ID
   - STRIDE category
   - Description: how this threat could be exploited
   - Affected component
   - Likelihood: High / Medium / Low
   - Impact: High / Medium / Low
   - Risk score
   - Existing controls
   - Additional controls required
   - Owner of remediation

5. OWASP TOP 10 CHECKLIST
   For each relevant OWASP category: applicable / not applicable / mitigated / finding.

6. SECURITY CONTROLS REVIEW
   Authentication: how users are authenticated.
   Authorization: how access is controlled.
   Input validation: how inputs are validated and sanitized.
   Output encoding: how outputs are encoded to prevent injection.
   Encryption: data in transit and at rest.
   Secrets management: how credentials and keys are stored.
   Audit logging: what security events are logged.

7. FINDINGS SUMMARY
   For each finding:
   - Severity: Critical / High / Medium / Low
   - Description
   - Remediation required
   - Owner
   - Due date (Critical: before launch, High: before launch, Medium: within 30 days)

8. SIGN-OFF
   Conditions for security approval.
   Outstanding items blocking approval.
   Security reviewer sign-off.
```

---

## Starter Prompt

```
You are a security engineer conducting a security review.

Feature/system being reviewed: [description]
Authentication mechanism: [how users authenticate]
Authorization model: [how access is controlled]
Data handled: [what sensitive data is involved]
New external surface: [any new APIs or integrations]
Trust boundaries: [where trust transitions occur]
Known concerns: [any security issues already identified]

Produce a complete security review including STRIDE threat model,
OWASP Top 10 checklist, security controls review, and findings summary.
Every Critical and High finding must have a named owner and a due date.
Findings rated Critical or High are blockers for launch.
```

---

*Skill file version: 1.0 | Phase: 05 - Engineering | Company type: Product*
