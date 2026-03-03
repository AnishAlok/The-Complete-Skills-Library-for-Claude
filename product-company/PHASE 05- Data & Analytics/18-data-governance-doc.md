# data-governance-doc.md

> **Skill:** Produces a data governance policy document covering data ownership, quality standards, access controls, retention policies, and processes for maintaining data integrity across the organization.

---

## TLDR

A data governance document defines the policies and standards for how data is managed, who owns it, who can access it, how long it is retained, and how quality is maintained. It prevents the organizational dysfunction that comes from unmanaged data: conflicting definitions, unknown data owners, uncontrolled access, and compliance exposure from poor data hygiene.

---

## Topic Explanation

### Data Governance vs. Data Management

**Data governance:** The policies, roles, and processes that define how data should be managed. "Who decides how customer data is used?" Governance.

**Data management:** The technical practices that implement those policies. "How is customer data stored and protected?" Management.

Governance sets the rules. Management implements them. Both are necessary; neither substitutes for the other.

### The Three Core Questions of Data Governance

**Who owns this data?** Every dataset, table, and critical metric should have a named owner accountable for its quality and appropriate use.

**Who can access this data?** Access should follow the principle of least privilege: people access what they need for their work, nothing more.

**How long is this data retained?** Data that is not needed should be deleted. Retaining unnecessary data creates compliance exposure and storage cost.

### The DAMA-DMBOK Framework

The Data Management Body of Knowledge (DAMA-DMBOK) is the industry standard reference for data management disciplines. It covers eleven knowledge areas including data governance, data quality, master data management, data warehousing, and metadata management. Data governance policies should align with DAMA-DMBOK principles where applicable.

---

## Output Format

```
1. POLICY HEADER
   Version, effective date, owner, approved by.
   Scope: which data, systems, and teams this policy covers.

2. PURPOSE AND PRINCIPLES
   Why this governance policy exists.
   Core data governance principles.

3. ROLES AND RESPONSIBILITIES
   Data Owner: accountable for a domain of data. Sets access rules. Ensures quality.
   Data Steward: day-to-day management. Implements owner's policies.
   Data Consumer: uses data within granted permissions.
   Data Governance Council: cross-functional body that resolves disputes and sets policy.

   For each role: responsibilities, authority, accountability.

4. DATA CLASSIFICATION
   Classification tiers:
   - Public: no restrictions
   - Internal: employees only
   - Confidential: need-to-know
   - Restricted: specific authorization required (PII, financial, PHI)

   Classification assignment process.
   How classification drives access and retention decisions.

5. DATA OWNERSHIP REGISTRY
   For each major data domain: named data owner.
   Domain / Owner / Steward / Classification / Systems.

6. ACCESS CONTROL POLICIES
   Access request process: how to request access.
   Approval requirements by classification tier.
   Access review cadence.
   Offboarding data access revocation.
   Third-party access policy.

7. DATA QUALITY STANDARDS
   Completeness, accuracy, consistency, timeliness standards.
   Data quality measurement approach.
   Issue escalation and resolution process.
   Who is accountable for data quality by domain.

8. DATA RETENTION POLICY
   Retention periods by data type and classification.
   Deletion procedures.
   Legal hold process.
   Archival policy.

9. INCIDENT AND BREACH RESPONSE
   What constitutes a data incident.
   Reporting requirements and timelines.
   Response procedures.
   Documentation requirements.

10. POLICY COMPLIANCE AND EXCEPTIONS
    How compliance is monitored.
    Exception request process.
    Consequences of non-compliance.
    Policy review cadence.
```

---

## Starter Prompt

```
You are a data governance lead writing a data governance policy.

Organization context: [size, industry, regulatory environment]
Data domains to cover: [the major data domains in the organization]
Regulatory requirements: [GDPR, CCPA, HIPAA, SOC2, etc.]
Current governance gaps: [known problems to address]
Data classification needs: [the sensitivity levels in the data]
Access control approach: [role-based, attribute-based, etc.]

Produce a complete data governance document covering all sections.
Align retention policies with stated regulatory requirements.
Every data domain should have a named owner.
```

---

*Skill file version: 1.0 | Phase: 06 - Data and Analytics | Company type: Product*
