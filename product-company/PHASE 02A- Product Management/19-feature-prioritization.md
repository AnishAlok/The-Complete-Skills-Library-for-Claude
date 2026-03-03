# feature-prioritization.md

> **Skill:** Produces a structured feature prioritization analysis using RICE, ICE, Kano, or custom scoring to rank a backlog of features or initiatives and produce a defensible prioritization recommendation.

---

## TLDR

Feature prioritization frameworks turn a backlog of competing requests into an ordered list with a defensible rationale. This skill applies the right framework to the prioritization challenge and produces a scored, ranked list with a recommendation. Used for quarterly planning, backlog grooming, and when stakeholders have competing priorities.

---

## Topic Explanation

### RICE Scoring (Intercom)

RICE = (Reach × Impact × Confidence) / Effort

- **Reach:** How many users will be affected per quarter?
- **Impact:** How much will it move the north star? (3=massive, 2=high, 1=medium, 0.5=low, 0.25=minimal)
- **Confidence:** How confident are we in the estimates? (100%=high, 80%=medium, 50%=low)
- **Effort:** How many person-months will it take?

RICE is most useful for comparing features with very different reach and effort profiles.

### ICE Scoring

ICE = Impact × Confidence × Ease

Simpler than RICE. Useful for early-stage teams or rapid scoring. Each dimension scored 1 to 10. No effort estimation required. Good for fast prioritization sessions.

### Kano Model

Classifies features into five categories:
- **Must-be (basic):** Expected by customers. Not having them causes dissatisfaction. Having them does not increase satisfaction.
- **Performance (linear):** More is better. Direct correlation between investment and satisfaction.
- **Excitement (delighters):** Unexpected features that create high satisfaction when present. Not missed when absent.
- **Indifferent:** Neither satisfying nor dissatisfying.
- **Reverse:** Actually causes dissatisfaction for some users.

Kano is most useful for deciding what type of feature to invest in, not for comparing across all features.

### When to Use Which Framework

- **RICE:** Comparing features with quantifiable reach and clear effort estimates
- **ICE:** Fast, relative scoring when precision is less important
- **Kano:** Understanding customer value type before scoring
- **Custom weighted criteria:** When specific strategic factors must be weighted (e.g., regulatory compliance, strategic partner commitments)

---

## Output Format

```
1. PRIORITIZATION CONTEXT
   The strategic goals this prioritization serves.
   The time horizon (what quarter or planning cycle).
   Framework selected and rationale.

2. BACKLOG INPUT
   Complete list of features/initiatives being scored.
   Source of each item (customer request, internal initiative, strategic bet).

3. SCORING TABLE
   For each item: all framework inputs and final score.
   Sorted by score descending.

4. SCORING NOTES
   Assumptions behind key estimates.
   Items with high uncertainty in scoring.
   Confidence level for the overall prioritization.

5. RECOMMENDED PRIORITIZATION
   Top items to pursue in this planning cycle.
   Items deprioritized and brief rationale.
   Items held for future consideration.

6. STAKEHOLDER CONFLICTS
   Items where stakeholder priorities differ from the scoring.
   Recommended approach for resolving conflicts.

7. REVIEW TRIGGERS
   Conditions that would warrant re-prioritizing before the next cycle.
```

---

## Starter Prompt

```
You are a product manager prioritizing a feature backlog.

Features to prioritize: [list of features or initiatives]
Strategic goals: [what outcomes you are optimizing for]
Framework: [RICE / ICE / Kano / custom criteria]
Time horizon: [what planning cycle]
Available capacity: [how many items can realistically be done]
Stakeholder inputs: [any pre-existing priorities or commitments]

Score each item using the specified framework.
Produce a ranked list with scoring rationale and a clear recommendation
for what to pursue in the current planning cycle.
Flag any item where scoring confidence is low.
```

---

*Skill file version: 1.0 | Phase: 02 - Product Management | Company type: Product*
