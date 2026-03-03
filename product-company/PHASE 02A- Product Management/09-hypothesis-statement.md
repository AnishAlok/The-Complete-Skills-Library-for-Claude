# hypothesis-statement.md

> **Skill:** Produces well-formed lean/agile hypothesis statements that define the expected outcome of a product change, the metric that will be measured, and the threshold that constitutes confirmation or disconfirmation.

---

## TLDR

A hypothesis statement frames a product decision as a testable prediction: if we do X for user Y, we expect outcome Z, as measured by metric M. This framing prevents shipping and hoping, and creates a learning culture where every product change is an opportunity to confirm or refute an assumption.

---

## Topic Explanation

### Why Hypothesis-Driven Development Matters

Traditional feature development ends at launch. Hypothesis-driven development begins at launch: the launch is the test, and the metric is the result. This shift produces several benefits:
- Teams ship smaller, testable changes rather than large, untestable bets
- Learning is captured explicitly and informs future decisions
- Scope is bounded by what is needed to test the hypothesis
- Resources are not committed to features that underperform before the team knows

### The Hypothesis Format

The standard lean hypothesis format:
"We believe [doing this] for [these users] will achieve [this outcome]. We will know this is true when we see [this measurable signal] within [this timeframe]."

The most common weakness in hypothesis statements is the "measurable signal" clause. "We will know this is true when we see user satisfaction improve" is not testable. "We will know this is true when the task completion rate for new users in the onboarding flow increases by 15% within 30 days" is testable.

### Types of Hypotheses

**Desirability hypothesis:** Do users want this? (Do they use it, do they ask for it, do they pay for it)
**Usability hypothesis:** Can users use this? (Can they complete the task, without error, in a reasonable time)
**Feasibility hypothesis:** Can we build this? (Technical hypothesis, often engineering-owned)
**Viability hypothesis:** Is this worth building? (Does it produce business value)

Most product hypotheses are desirability or usability. Make the type explicit.

---

## Output Format

```
HYPOTHESIS STATEMENT:
We believe [doing this / building this feature / making this change]
for [these users in this context]
will result in [this behavior change or outcome]
because [the reasoning behind this prediction].

HYPOTHESIS TYPE: [Desirability / Usability / Feasibility / Viability]

WHAT WE ARE TESTING:
The specific assumption this hypothesis tests.

SUCCESS METRIC:
Primary metric: [the single number that most directly measures the hypothesis]
Secondary metrics: [supporting signals]
Counter-metrics: [metrics that should NOT get worse]

THRESHOLD FOR CONFIRMATION:
We will consider this hypothesis confirmed if [metric] reaches [value] within [timeframe].
We will consider this hypothesis disconfirmed if [metric] does not reach [value] by [date].

MINIMUM EXPERIMENT:
The smallest change we can make to test this hypothesis.
What is explicitly excluded from the MVP experiment.

CONFIDENCE LEVEL:
Our prior confidence before testing: [High / Medium / Low]
What evidence supports the prediction: [existing data or research]
```

---

## Starter Prompt

```
You are a product manager writing a hypothesis statement.

Feature or change being proposed: [what you are building or changing]
User type: [who this is for]
Expected outcome: [what you predict will happen]
Reasoning: [why you expect this outcome]
Available metrics: [what can be measured]
Timeframe: [how long the test will run]
Existing evidence: [any data or research supporting the hypothesis]

Produce a complete hypothesis statement with success metric, threshold,
minimum experiment definition, and confidence level assessment.
Flag if the success metric is not directly measurable.
```

---

*Skill file version: 1.0 | Phase: 02 - Product Management | Company type: Product*
