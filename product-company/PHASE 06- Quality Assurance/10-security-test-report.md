# security-test-report.md

> **Skill:** Produces a security testing findings report documenting vulnerabilities, CVSS severity scores, evidence, remediation requirements, and the security quality gate verdict for release sign-off.

---

## TLDR

A security test report documents the findings of security testing: vulnerabilities found, CVSS severity scores, evidence, and required remediation. It is the QA record of whether security quality gates were met and which findings block production deployment.

---

## Topic Explanation

### Security Testing Coverage in QA

QA security testing typically covers four areas:

**OWASP Top 10 manual testing:** manually testing for the most common web application vulnerabilities as part of pre-release QA.

**SAST (Static Application Security Testing):** automated source code analysis run in CI/CD pipelines on every build.

**DAST (Dynamic Application Security Testing):** automated testing of running applications for vulnerabilities, run against staging environments.

**Dependency scanning:** checking third-party packages and libraries for known CVEs.

Penetration testing (adversarial testing by security specialists) is typically conducted separately and reported under a different document. The QA security test report covers the four areas above.

### CVSS Scoring System

The Common Vulnerability Scoring System provides standardized severity scores:

- Critical (9.0 to 10.0): immediate exploitation likely, severe impact. Must be fixed before release, no exceptions.
- High (7.0 to 8.9): significant risk. Must be fixed before release or explicitly accepted with CISO or security lead sign-off.
- Medium (4.0 to 6.9): moderate risk. Fix within 30 days post-release.
- Low (0.1 to 3.9): minimal risk. Fix within 90 days or accept as known risk.

### Automated vs. Manual Security Testing

Automated tools detect common vulnerability patterns efficiently. Manual security testing finds business logic vulnerabilities, complex authentication and authorization flaws, and context-dependent issues that automated tools cannot detect. Both are required for meaningful security test coverage.

---

## Output Format

```
1. REPORT HEADER
   Release version, test date, QA lead, security reviewer, tools used.
   Scope: what systems, pages, and functions were tested.

2. EXECUTIVE SUMMARY
   Security test result: PASS / FAIL / CONDITIONAL PASS.
   Critical findings: [N]. High: [N]. Medium: [N]. Low/Info: [N].
   Release recommendation in one sentence.

3. TESTING SCOPE AND METHODS
   Areas tested. Methods applied: OWASP manual / SAST / DAST / dependency scan.
   Areas explicitly not tested and rationale.

4. FINDINGS SUMMARY TABLE

   ID | Title | OWASP Category | CVSS Score | Severity | Status | Blocks release?

5. FINDING DETAILS
   For each finding:

   FINDING ID: [SEC-XXX]
   Title: [short description]
   OWASP Category: [e.g., A01:2021 Broken Access Control]
   CVSS Score: [X.X] / Severity: [Critical / High / Medium / Low]

   Description: [what the vulnerability is and why it creates risk]
   Evidence / Reproduction: [how it was found and how to reproduce]
   Impact: [what an attacker could do if this is exploited]
   Affected Component: [specific area of the codebase or system]
   Remediation Required: [specific fix recommended]
   References: [CVE number, CWE number, OWASP reference]
   Status: [Open / In progress / Fixed / Accepted risk]
   Owner: [developer or team]
   Due date: [based on severity]

6. DEPENDENCY SCAN RESULTS
   Tool used and scan date.
   CVEs found in third-party dependencies.
   Severity distribution.
   Packages requiring updates.

7. SECURITY QUALITY GATE

   PASS: No Critical or High findings open. Release approved from security perspective.

   CONDITIONAL PASS: No Critical findings open. High findings accepted with
   documented risk rationale and CISO/security lead sign-off.
   Conditions: [specific findings to be fixed before go-live or by a specific date]

   FAIL: Critical or High findings are open without accepted risk documentation.
   Release is blocked until findings are resolved or formally accepted.

8. RISK ACCEPTANCE DOCUMENTATION
   For any finding accepted as known risk rather than fixed:
   Finding ID, severity, risk rationale, accepted by (name and role), date.
```

---

## Starter Prompt

```
You are a QA engineer writing a security test report for a release.

Release: [version]
Testing methods applied: [OWASP manual / SAST / DAST / dependency scan]
Findings: [list of vulnerabilities with CVSS scores]
Remediation status: [which are fixed vs. open]
Risk acceptance decisions: [any findings being formally accepted rather than fixed]
Release disposition: [pass / fail / conditional]

Produce a complete security test report with findings detail,
CVSS scores, quality gate verdict, and remediation tracking.
Critical and High findings must each have an explicit block/accept decision.
Any accepted risk must identify the name and role of the accepting authority.
```

---

*Skill file version: 1.0 | Phase: 07 - Quality Assurance | Company type: Product*
