# engineering-spec.md

> **Skill:** Translates a product requirements document into engineering requirements, adding technical constraints, non-functional requirements, system context, and implementation guidance.

---

## TLDR

An engineering spec is the bridge between product requirements (what users need) and technical implementation (how to build it). It takes the PRD's requirements and adds: technical context, non-functional requirements, system constraints, integration requirements, and implementation guidance that engineers need but product managers do not typically write. Used when the PM has written the PRD and engineering needs to translate it into buildable specifications.

---

## Topic Explanation

### Product Requirements vs. Engineering Requirements

**Product requirement:** "Users can export compliance reports as PDF."
**Engineering requirement:** "PDF generation must complete within 5 seconds for reports up to 10,000 rows. Generation must run as a background job to prevent request blocking. The PDF must be stored in S3 with a pre-signed URL expiring after 24 hours. The endpoint must be authenticated via JWT. Rate limit: 10 export requests per user per hour."

The engineering spec takes the product requirement and makes it implementable by adding the technical dimensions the product spec does not capture.

### Non-Functional Requirements Categories

**Performance:** Latency targets, throughput requirements, resource utilization limits.
**Scalability:** How the feature must behave as user count, data volume, or request rate grows.
**Reliability:** Uptime requirements, error rate tolerance, recovery time objectives.
**Security:** Authentication, authorization, input validation, data exposure risks.
**Observability:** What must be logged, what metrics must be emitted, what must be alerted on.
**Maintainability:** Code organization, documentation requirements, test coverage requirements.

---

## Output Format

```
1. SPEC HEADER
   Feature, PRD reference, engineering lead, date, status.

2. PRODUCT CONTEXT SUMMARY
   Brief summary of the product requirement being implemented.
   Link to PRD.

3. TECHNICAL CONTEXT
   Relevant existing systems and how they connect to this feature.
   Constraints imposed by existing architecture.
   Services and systems this feature will depend on.

4. FUNCTIONAL REQUIREMENTS (engineering-level)
   For each product requirement: the engineering expression of it.
   Implementation-neutral but technically precise.

5. NON-FUNCTIONAL REQUIREMENTS
   Performance: latency and throughput targets with measurement method.
   Scalability: expected growth and requirements at 10x current scale.
   Reliability: uptime target, error rate tolerance, RTO/RPO.
   Security: auth requirements, input validation, data handling.
   Observability: required logs, metrics, and alerts.

6. INTEGRATION REQUIREMENTS
   External systems to integrate with.
   API contracts, authentication methods, rate limits.
   Failure handling for each integration.

7. DATA REQUIREMENTS
   Data to be stored and where.
   Schema changes required.
   Data retention and deletion requirements.
   PII handling requirements.

8. TESTING REQUIREMENTS
   Unit test coverage targets.
   Integration test requirements.
   Load test requirements.
   Security test requirements.

9. DEFINITION OF DONE
   The engineering-level definition of "done" for this feature.
   QA acceptance criteria.
   Monitoring and alerting in place.
   Documentation complete.
```

---

## Starter Prompt

```
You are a senior engineer writing an engineering spec from a product spec.

Product spec: [the PRD requirements being implemented]
Tech stack: [languages, frameworks, databases]
System context: [relevant existing services and constraints]
Performance targets: [latency, throughput, scale requirements]
Security requirements: [auth, data handling, input validation needs]
Integration requirements: [external systems to connect with]

Translate the product requirements into precise engineering requirements.
Add non-functional requirements for each functional requirement.
Flag any product requirement that cannot be implemented as stated
within the stated technical constraints.
```

---

*Skill file version: 1.0 | Phase: 05 - Engineering | Company type: Product*
