# ab-test-plan.md

> **Skill:** Produces an A/B test design document covering hypothesis, metrics, variants, sample size calculation, segment definition, guardrails, and execution plan.

---

## TLDR

An A/B test plan is the pre-registration document for an experiment: it defines the hypothesis, variants, primary and secondary metrics, required sample size, target audience, duration, and guardrails before the test runs. Writing it before launch forces rigorous experimental design and prevents the most common analysis errors (underpowered tests, metric switching, peeking).

---

## Topic Explanation

### Pre-Registration and Why It Matters

Pre-registration means documenting the experimental design, primary metric, and analysis plan before any data is collected. It prevents:

**HARKing (Hypothesizing After Results Known):** Claiming the hypothesis was always "feature B will increase engagement" after finding that feature B increased engagement but not the originally intended conversion metric.

**Metric switching:** Starting with conversion rate as primary metric, not seeing a significant result, and switching to "clicks" which happened to be significant.

**Optional stopping / peeking:** Checking results daily and stopping as soon as significance is reached, which dramatically inflates false positive rates.

Pre-registered tests have much higher scientific validity because the analysis cannot be shaped by knowing the results.

### Statistical Concepts for A/B Testing

**Statistical significance (p-value):** The probability of seeing the observed difference (or more extreme) if there were truly no difference. Threshold: typically p < 0.05. A significant result means the observed difference is unlikely to be noise.

**Statistical power:** The probability of detecting a true effect of a given size. Typically target 80% power. Low power means the test may miss a real effect.

**Minimum Detectable Effect (MDE):** The smallest effect size the test is designed to detect reliably. The MDE drives sample size: smaller effects require larger samples.

**Sample size calculation:** Given the baseline rate, MDE, significance threshold (α), and power (1-β), calculate the minimum users per variant. Under-powered tests produce unreliable results in both directions.

### Common A/B Testing Mistakes

**Running the test for too short a time:** Even after reaching sample size, tests should run for at least one full business cycle (typically 1-2 weeks) to account for day-of-week effects.

**Testing multiple things in one variant:** If variant B has both a new button color and new copy, you cannot know which change drove the result.

**Not accounting for novelty effects:** New UI elements often get temporary engagement boosts simply because they are new, not because they are better.

**Ignoring network effects:** If users interact with each other, a change to one user affects other users, violating the independence assumption.

---

## When to Use This Skill

Use when:
- Planning any controlled experiment on a product change
- A product decision requires data to resolve a genuine disagreement
- A feature hypothesis needs validation before full rollout
- Building experimentation culture and need a standard template

---

## Dos

- **Do write the test plan before any data is collected or any variant is shipped.** Post-hoc "test plans" have no scientific validity.
- **Do specify exactly one primary metric.** Multiple primary metrics require Bonferroni correction and produce harder-to-interpret results.
- **Do calculate the required sample size before running the test.** Running the test and then checking "is this significant yet?" inflates false positives.
- **Do specify guardrail metrics.** A test that lifts the primary metric while degrading revenue or retention is not a win.
- **Do define the analysis method before the test starts.** Frequentist or Bayesian? How will you handle novelty effects? How will you handle the test ending before reaching sample size?

---

## Donts

- **Dont peek at results and stop early.** Set a stopping criterion before the test starts and respect it.
- **Dont change the primary metric after seeing results.** This invalidates the statistical guarantees.
- **Dont run multiple tests on overlapping populations simultaneously without accounting for interaction effects.**

---

## Output Format

```
1. TEST PLAN HEADER
   Test name, owner, start date, planned end date, status.
   Feature area, platform.

2. HYPOTHESIS
   Full hypothesis statement:
   "We believe [change] for [users] will [effect on metric]
   because [reason]. We will know this is true when [primary metric]
   changes by at least [MDE] within [duration]."

3. VARIANTS
   Control (A): exact description of current state.
   Variant B: exact description of the change.
   Variant C (if any): description.
   Screenshots or design references for each variant.

4. PRIMARY METRIC
   Exactly one primary metric.
   Definition: how it is calculated.
   Baseline rate: current observed value.
   Minimum Detectable Effect (MDE): the smallest change worth detecting.
   Why this is the right primary metric.

5. SECONDARY METRICS
   Metrics that provide context but do not determine the winner.
   Definition of each.

6. GUARDRAIL METRICS
   Metrics that must not degrade.
   Threshold: how much degradation triggers stopping the test.
   Who has authority to stop the test.

7. SAMPLE SIZE AND DURATION

   Sample size calculation:
   - Baseline conversion rate: [X%]
   - MDE: [Y%] relative change / [Z%] absolute change
   - Significance level (α): 0.05
   - Statistical power (1-β): 0.80
   - Required users per variant: [calculated value]
   - Expected daily traffic to test: [N users/day]
   - Required test duration: [days]
   - Minimum run time regardless of sample size: [1 full week minimum]

8. TARGET AUDIENCE
   Which users are eligible for the test.
   Exclusion criteria: who is excluded and why.
   Expected eligible population size.

9. RANDOMIZATION UNIT
   The unit of randomization: user / session / device / account.
   Why this unit is appropriate.
   How tie-breaking is handled.

10. ANALYSIS PLAN
    Statistical method: frequentist (t-test, chi-squared) or Bayesian.
    How to handle unequal sample sizes.
    How to handle early stopping if guardrail is breached.
    Subgroup analyses planned (must be pre-specified).

11. RISKS AND LIMITATIONS
    Threats to validity.
    Novelty effect risk and mitigation.
    External validity: which users/contexts results generalize to.

12. DECISION CRITERIA
    If primary metric improves by MDE with p < 0.05: ship variant.
    If primary metric is flat: [decision].
    If primary metric degrades: [decision].
    If guardrail is breached: stop test immediately.
```

---

## Starter Prompt

```
You are a product analyst designing an A/B test.

Feature being tested: [what change is in the test]
Hypothesis: [what you expect to happen and why]
Primary metric: [the single metric that determines success]
Baseline rate: [current value of the primary metric]
MDE: [minimum change worth detecting]
Target audience: [who is eligible for the test]
Daily eligible traffic: [users/day who qualify]
Guardrail metrics: [metrics that must not degrade]
Platform: [web / mobile / both]

Produce a complete A/B test plan including:
1. Formal hypothesis statement
2. Full variant descriptions
3. Sample size calculation with all inputs shown
4. Required test duration
5. Analysis plan pre-specified
6. Decision criteria for all outcomes
7. Risks and threats to validity

Flag if the test is underpowered for the stated MDE.
Flag if the test duration is under one week regardless of sample size.
```

---

## Related Skills

| Use This Next | Why |
|---|---|
| `ab-test-results.md` | Test plan becomes the reference for results analysis |
| `experiment-results.md` | Full experiment documentation after results are in |
| `hypothesis-statement.md` | Hypothesis in the test plan should follow this format |

*Skill file version: 1.0 | Phase: 06 - Data and Analytics | Company type: Product*
