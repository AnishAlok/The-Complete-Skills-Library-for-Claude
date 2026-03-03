# sow-statement-of-work.md

> **Skill:** Produces a Statement of Work (SOW) that defines the scope, deliverables, timeline, payment terms, and governance for a vendor or contractor engagement.

---

## TLDR

A Statement of Work is the contract document that defines exactly what a vendor or contractor will deliver, under what terms, and how disputes about scope or quality will be resolved. A well-written SOW prevents scope creep, late deliverables, and invoice disputes. A poorly written SOW produces all three. Used whenever engaging an external vendor or contractor for a defined body of work.

---

## Topic Explanation

### SOW vs. Master Service Agreement

**MSA (Master Service Agreement):** The umbrella contract governing the relationship between two parties. Covers standard legal terms, liability, IP ownership, confidentiality. Usually signed once.

**SOW:** The work-specific document. Defines scope, deliverables, timelines, and payment for a specific engagement. A new SOW is executed for each project under the MSA.

In practice, both should exist. Embedding all legal terms in each SOW is redundant and creates inconsistency. The MSA holds the legal framework; the SOW holds the work definition.

### The Most Litigated SOW Sections

Based on common vendor disputes, these sections require the most care:

**Deliverable definitions:** Vague deliverables ("a working mobile app") produce the most scope disputes. Deliverables should be specific, include quality criteria, and reference acceptance criteria.

**Change control:** What happens when the client requests work outside the original scope? Without a change control clause, every scope request is either denied (bad relationship) or absorbed without compensation (bad for the vendor).

**Acceptance process:** Who accepts deliverables, using what criteria, within what timeframe? Without this, deliverables are perpetually "in review" and payment is blocked.

**IP ownership:** Who owns the work product? In most software development SOWs, the client owns what they commission. This must be explicit.

---

## Output Format

```
1. SOW HEADER
   Parties: client company, vendor company.
   SOW number, effective date, MSA reference.
   Authorized signatories.

2. PROJECT OVERVIEW
   Purpose and business objective.
   Background context.

3. SCOPE OF WORK
   Detailed description of work to be performed.
   What is explicitly included.
   What is explicitly excluded.

4. DELIVERABLES
   For each deliverable:
   - Name and description
   - Quality criteria / acceptance criteria
   - Due date
   - Format or medium

5. TIMELINE AND MILESTONES
   Project start and end dates.
   Milestone table: Milestone / Due date / Deliverables associated

6. VENDOR RESPONSIBILITIES
   What the vendor will provide.
   Key personnel committed to the engagement.

7. CLIENT RESPONSIBILITIES
   What the client must provide: access, information, approvals, resources.
   Response time commitments (e.g., feedback within 5 business days).

8. ACCEPTANCE PROCESS
   Who reviews and accepts each deliverable.
   Acceptance criteria.
   Acceptance timeframe.
   Dispute resolution if deliverable is rejected.

9. PAYMENT TERMS
   Total contract value.
   Payment schedule: milestone-based, time-based, or completion-based.
   Invoice submission process.
   Payment terms (net 30, etc.).

10. CHANGE CONTROL
    How changes to scope are requested and approved.
    Change order process.
    Impact of changes on timeline and price.

11. INTELLECTUAL PROPERTY
    Ownership of work product.
    Pre-existing IP retained by vendor.
    License grants if applicable.

12. CONFIDENTIALITY REFERENCE
    Reference to MSA confidentiality provisions or inline clause.

13. SIGNATURES
    Authorized representative signatures and dates.
```

---

## Starter Prompt

```
You are a program manager drafting a Statement of Work.

Client: [company engaging the vendor]
Vendor: [company being engaged]
Work to be performed: [description of the project or engagement]
Deliverables: [specific outputs required]
Timeline: [start date, end date, key milestones]
Budget: [total contract value and payment structure]
Client responsibilities: [what the client must provide]
IP ownership: [who owns the work product]

Produce a complete SOW. Define deliverables specifically with acceptance criteria.
Include a change control clause. Be explicit about what is out of scope.
Flag any section where the description is too vague to prevent scope disputes.
```

---

*Skill file version: 1.0 | Phase: 04 - Program and Project Management | Company type: Product*
