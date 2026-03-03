# build-buy-partner.md

> **Skill:** Produces a build/buy/partner analysis that structures the evaluation of whether a capability should be built internally, acquired, or addressed through a partnership.

---

## TLDR

A build/buy/partner analysis is the structured evaluation of three options for acquiring a product capability: build it (internal development), buy it (acquire or license), or partner (integrate with or commercially partner with a third party). This skill produces a structured analysis with criteria, options assessment, and a recommendation.

---

## Topic Explanation

### When Each Option Makes Sense

**Build:**
- The capability is core to competitive differentiation
- No vendor provides what is specifically needed
- Long-term cost of ownership favors internal development
- Control over roadmap and customization is critical

**Buy (acquire or license):**
- The capability is needed faster than building allows
- A vendor has already solved the problem well
- The capability is not a core differentiator
- Acquisition brings additional assets (team, customers, IP)

**Partner:**
- A vendor provides the capability and integration is sufficient
- The capability is adjacent, not core
- Risk sharing or distribution benefits are available
- The market is too uncertain to fully commit resources

### The Tradeoffs

**Build:** Maximum control, maximum cost, maximum time to capability.
**Buy:** Medium control (if acquired), high upfront cost, fastest to capability.
**Partner:** Lowest control, lowest upfront cost, dependency risk.

---

## Output Format

```
1. DECISION CONTEXT
   Capability being evaluated.
   Why this capability is needed.
   Timeline pressure.
   Strategic importance: core differentiator vs. table stakes vs. supporting capability.

2. OPTIONS DESCRIPTION
   Build: what internal development would involve. Scope, team, timeline, cost.
   Buy: what vendors or acquisition targets are available. Cost, capability fit.
   Partner: what partnership options exist. Terms, risks, integration complexity.

3. EVALUATION CRITERIA
   Criteria table with weight:
   - Strategic control (does this need to be owned?)
   - Time to capability (how fast do we need this?)
   - Total cost of ownership (3-year)
   - Quality of available solutions
   - Risk (execution, dependency, competitive)
   - Alignment with core competency

4. OPTION SCORING
   Score each option against each criterion.
   Weighted total.

5. RISK ANALYSIS
   Key risks for each option.
   Risk mitigation for the preferred option.

6. RECOMMENDATION
   Recommended option with rationale.
   Key conditions under which the recommendation would change.
   Decision authority and timeline.

7. IMPLEMENTATION NEXT STEPS
   If build: team, timeline, milestones.
   If buy: vendor shortlist, procurement process.
   If partner: partner identification, negotiation approach.
```

---

## Starter Prompt

```
You are a product manager conducting a build/buy/partner analysis.

Capability needed: [what the team needs to be able to do]
Why it is needed: [the product or business goal it serves]
Timeline: [when it is needed by]
Strategic importance: [how core this is to competitive advantage]
Known options: [any specific vendors, partners, or build approaches already identified]
Budget context: [any relevant cost constraints]

Produce a complete build/buy/partner analysis with options description,
weighted evaluation criteria, option scoring, risk analysis, and recommendation.
```

---

*Skill file version: 1.0 | Phase: 02 - Product Management | Company type: Product*
