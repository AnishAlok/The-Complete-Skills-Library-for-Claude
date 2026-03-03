# vendor-evaluation.md

> **Skill:** Produces a vendor evaluation scorecard and recommendation document that structures the assessment of competing vendors against defined criteria.

---

## TLDR

A vendor evaluation document structures the selection process to ensure it is rigorous, defensible, and not dominated by any single factor (like price or a compelling demo). It defines evaluation criteria and weights upfront, scores each vendor against those criteria, and produces a recommendation with documented rationale. Used for any significant vendor or software selection.

---

## Topic Explanation

### Why Structured Vendor Evaluation Matters

Unstructured vendor selection produces two common failure modes:

**Demo bias:** The vendor with the most polished demo wins, regardless of fit to actual requirements. Sales-optimized demos are designed to show strengths and hide weaknesses.

**Price anchoring:** The lowest-cost vendor wins without accounting for total cost of ownership (TCO), implementation effort, or long-term support quality.

Structured evaluation with pre-defined criteria weights defuses both failure modes by requiring evidence against specific requirements rather than an overall impression.

### Criteria Categories

**Functional fit:** Does the vendor's product do what is required? Scored against a requirements list.
**Technical fit:** Does it integrate with the existing tech stack? What are the implementation requirements?
**Vendor health:** Is the vendor a viable long-term partner? Financials, roadmap, customer base.
**Support and SLA:** What is the support quality and contractual commitment?
**Total cost of ownership:** Not just license cost, but implementation, integration, training, and ongoing fees.
**Security and compliance:** Does it meet security and regulatory requirements?
**References:** What do current customers say?

Define criteria and weights BEFORE seeing vendor demos. Criteria defined after demos are unconsciously shaped by the most impressive demo.

---

## Output Format

```
1. EVALUATION HEADER
   Decision being made, evaluation team, timeline, decision date.

2. REQUIREMENTS SUMMARY
   Functional requirements the vendor must meet.
   Technical requirements.
   Mandatory (must-have) vs. preferred (nice-to-have) requirements.

3. EVALUATION CRITERIA AND WEIGHTS
   Table: Criterion / Weight (% of total) / Description
   Weights must sum to 100%.
   Criteria and weights set before vendor demos.

4. VENDOR PROFILES
   For each vendor evaluated:
   - Company overview
   - Product overview
   - Key strengths
   - Key weaknesses or concerns
   - Pricing model and estimated TCO

5. SCORING SCORECARD
   For each criterion x vendor:
   - Score (1-5)
   - Evidence or notes supporting the score
   - Weighted score
   Total weighted score per vendor.

6. REFERENCE CHECK SUMMARY
   Questions asked.
   Responses by vendor.
   Key themes from references.

7. RISK ASSESSMENT
   For each vendor: key risks of selection.
   Mitigation options.

8. RECOMMENDATION
   Recommended vendor with rationale.
   Second choice if primary is unavailable.
   Key conditions or negotiation points before signing.
   Decision authority and approval needed.
```

---

## Starter Prompt

```
You are a program manager running a vendor evaluation.

What is being evaluated: [the tool, service, or capability]
Vendors being considered: [list of vendors]
Requirements: [functional and technical requirements]
Evaluation team: [who is scoring]
Budget constraint: [if relevant]
Timeline for decision: [when the decision must be made]

Produce a complete vendor evaluation including:
1. Requirements summary with must-have vs. nice-to-have
2. Evaluation criteria with weights (must sum to 100%, set before demos)
3. Scoring scorecard with evidence notes
4. Recommendation with rationale and negotiation guidance
```

---

*Skill file version: 1.0 | Phase: 04 - Program and Project Management | Company type: Product*
