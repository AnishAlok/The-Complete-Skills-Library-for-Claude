# card-sorting-report.md

> **Skill:** Produces a card sort analysis report with cluster analysis, similarity matrix, and IA recommendations based on open, closed, or hybrid card sorting data.

---

## TLDR

A card sorting report synthesizes data from a card sorting exercise to reveal how users naturally group and label information, providing evidence for information architecture decisions. Open sorts reveal user-generated groupings. Closed sorts validate proposed groupings. The analysis produces category recommendations and naming guidance based on user mental models.

---

## Topic Explanation

### Card Sort Types

**Open card sort:** Participants group cards however feels natural and label the groups themselves. Used when you do not yet have a proposed IA and want to discover user-generated categories. Produces the most generative insights but harder to analyze quantitatively.

**Closed card sort:** Participants sort cards into predefined categories. Used to validate a proposed IA. Easier to analyze quantitatively. Does not reveal alternative categorizations.

**Hybrid card sort:** Participants sort into predefined categories but can also create new ones. Balances validation and discovery.

### Analysis Methods

**Similarity matrix:** Shows what percentage of participants grouped each pair of items together. High percentages (80%+) indicate strong grouping agreement. Low percentages indicate items that participants disagreed on.

**Cluster analysis:** Groups items by similarity scores into dendrograms (tree diagrams). Shows which items naturally form clusters and at what threshold of agreement.

**Category label analysis (open sorts only):** Qualitative analysis of the labels participants created for their groups. Reveals user vocabulary for naming categories.

**Agreement score:** For closed sorts, the percentage of participants who placed each item in each category. Items with low agreement scores are mismatches between the current IA and user mental models.

### Sample Size Requirements

- Open sort for discovery: 15 to 30 participants
- Closed sort for validation: 20 to 40 participants
- Statistical significance for dendrogram analysis: 15+ participants

---

## Output Format

```
1. STUDY OVERVIEW
   Sort type (open/closed/hybrid), participant count, cards included,
   categories provided (closed), tool used, date.

2. SIMILARITY MATRIX SUMMARY
   Highest-agreement item pairs (80%+ grouped together).
   Lowest-agreement items (participants disagreed on placement).
   Notable surprises where expected groupings did not materialize.

3. CLUSTER ANALYSIS
   Dendrogram or cluster groups with agreement thresholds.
   Recommended IA categories based on cluster analysis.
   Items that do not clearly belong to any cluster.

4. CATEGORY LABEL ANALYSIS (open sorts)
   Most common labels participants created.
   Vocabulary recommendations for category naming.
   Labels that reveal user mental model vs. current product terminology.

5. AGREEMENT SCORE TABLE (closed sorts)
   Per-item placement percentages across categories.
   Items with low agreement scores flagged for IA reconsideration.

6. IA RECOMMENDATIONS
   Proposed category structure based on sort findings.
   Naming recommendations using user-generated vocabulary.
   Items requiring further testing.
   Confidence level for each recommendation.

7. NEXT STEPS
   Tree testing plan to validate the recommended IA.
```

---

## Starter Prompt

```
You are a UX researcher analyzing card sort results.

Sort type: [open / closed / hybrid]
Participant count and data: [results or summary statistics]
Cards included: [the items that were sorted]
Categories provided (if closed): [the predefined categories]
Purpose: [what IA decision this is informing]

Produce a complete card sort report including similarity analysis,
cluster groupings, vocabulary recommendations, and IA recommendations.
```

---

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
