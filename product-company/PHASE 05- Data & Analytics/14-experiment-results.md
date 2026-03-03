# experiment-results.md

> **Skill:** Produces a comprehensive experiment results document that captures the full record of an experiment from hypothesis through to decision and learnings, serving as institutional memory.

---

## TLDR

An experiment results document is the permanent record of an experiment: the original hypothesis, methodology, results, interpretation, and decision. It captures not just what happened but what was learned and how that learning shaped future decisions. The experiment results document is longer and more complete than the A/B test results report; it is the institutional record that future teams reference.

---

## Topic Explanation

### Experiments as Institutional Learning

Most organizations run experiments and then move on. The hypothesis is loosely recalled, the results are summarized in a Slack message, and within six months the specific findings have been forgotten. A year later, a new team member runs the same experiment again.

Experiment results documents solve this by creating a searchable, durable record of what was tried, what was found, and what was learned. They are the product team's equivalent of a scientific lab notebook.

### The Decision vs. the Learning

An experiment has two outputs: a decision (ship / don't ship) and a learning (understanding of user behavior, the product, or the market). These are separate:
- A winning experiment produces both a decision to ship and a positive learning
- A losing experiment produces a decision not to ship and often an equally valuable negative learning
- An inconclusive experiment produces a deferred decision but still produces learning about effect sizes, user sensitivity, and what to test next

All three outcomes are valuable. The learning from losing experiments is often the most important because it rules out approaches and updates mental models.

---

## Output Format

```
1. EXPERIMENT RECORD HEADER
   Experiment name, ID, owner, team, start/end dates.
   Reference to test plan.

2. EXPERIMENT SUMMARY (for future reference)
   What was tested, in one sentence.
   What was found, in one sentence.
   What was decided, in one sentence.
   What was learned, in one sentence.

3. ORIGINAL HYPOTHESIS
   Exact hypothesis as stated in the test plan.
   Was the hypothesis confirmed, refuted, or inconclusive?

4. EXPERIMENT DESIGN
   Summary of methodology.
   Primary metric.
   Sample size and duration.
   Any deviations from the original test plan.

5. RESULTS (complete)
   Full results table including all metrics.
   Statistical details.
   Reference to A/B test results document for full analysis.

6. INTERPRETATION
   What the results mean.
   Business impact if shipped at 100%.
   Confidence in the interpretation.

7. DECISION
   Ship / Do not ship / Iterate / Follow-on experiment.
   Decision date and decision maker.
   Conditions attached to the decision.

8. LEARNINGS
   What this experiment taught us about our users.
   What this experiment taught us about our product.
   How this updates our mental model.
   What hypotheses this suggests for future experiments.

9. FOLLOW-ON ACTIONS
   If shipping: rollout plan.
   If iterating: what to change.
   Experiments this result suggests for the future.
   Hypothesis log update.

10. RETROSPECTIVE
    Did the test plan prove adequate?
    What would we do differently in the experimental design?
    Learnings for future experimentation methodology.
```

---

## Starter Prompt

```
You are documenting a completed experiment for institutional memory.

Experiment: [name and what was tested]
Original hypothesis: [as stated before the test]
Results: [summary of statistical outcomes]
Decision: [what was decided]
Learnings: [what was learned beyond the binary result]
Follow-on actions: [what happens next]

Produce a complete experiment results document designed to be useful
to a future team member reading it in 12 months.
The learnings section should be substantive: what do we now know about
our users or product that we did not know before?
```

---

*Skill file version: 1.0 | Phase: 06 - Data and Analytics | Company type: Product*
