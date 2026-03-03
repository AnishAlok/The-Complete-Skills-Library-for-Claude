# benchmark-study.md

> **Skill:** Produces a UX benchmark study design and report format that measures product usability against quantitative metrics for tracking improvement over time or comparing against competitors.

---

## TLDR

A UX benchmark study establishes quantitative baseline metrics for task completion rate, time on task, error rate, and satisfaction, enabling rigorous comparison of UX quality before and after a design change or against a competitor. Used when you need to demonstrate improvement with data rather than observation alone.

---

## Topic Explanation

### Why Benchmark Studies Are Different from Standard Usability Tests

Standard usability tests are optimized for finding problems. They use small samples (5 to 8 participants) to identify issues efficiently. Benchmark studies are optimized for measuring performance precisely. They use larger samples (20 to 50+ participants) to produce statistically meaningful metrics.

This distinction matters for:
- **Sample size:** Much larger for benchmarks
- **Participant diversity:** Broader sample to represent the user population
- **Protocol:** Less probing, more standardized task administration
- **Analysis:** Statistical analysis (means, confidence intervals, t-tests) vs. thematic synthesis

You can run both in parallel: a large benchmark study to measure performance, and a smaller qualitative component to understand why performance is at that level.

### Core UX Benchmark Metrics

**Task completion rate:** % of participants who completed the task successfully. The primary effectiveness metric.

**Time on task:** Mean and median time to complete each task. The efficiency metric.

**Error rate:** Number of errors per task attempt. Indicates reliability.

**Single Ease Question (SEQ):** A 7-point post-task rating of ease. Standardized and validated by Jeff Sauro.

**System Usability Scale (SUS):** A 10-item, 5-point scale administered post-session. Produces a 0 to 100 score with well-established industry benchmarks. An SUS score of 68 is the average. Above 80 is excellent.

**Task-level satisfaction ratings:** Custom post-task items for domain-specific dimensions.

### Benchmarking Approaches

**Within-subjects (longitudinal):** Same participants complete the same tasks at Time 1 and Time 2. Strongest design for detecting change but requires participant re-engagement.

**Between-subjects (cross-sectional):** Different participants complete tasks at Time 1 and Time 2. Easier logistically but requires larger samples and careful sampling equivalence.

**Competitive benchmark:** Participants complete the same tasks on your product and a competitor's product. Typically within-subjects with counterbalancing to control order effects.

---

## Output Format

```
1. STUDY DESIGN
   Study type (longitudinal / competitive), participant count and criteria,
   tasks included, metrics collected, protocol (moderated/unmoderated), date(s).

2. METRICS SUMMARY TABLE
   Per task: completion rate, mean time, error rate, SEQ score.
   Overall: SUS score, composite usability score.
   With confidence intervals for all metrics.

3. LONGITUDINAL OR COMPETITIVE COMPARISON (if applicable)
   Before/after comparison with significance testing.
   Competitive comparison with your product vs. competitor.
   Visualization: charts showing metric changes or comparisons.

4. INDUSTRY BENCHMARK COMPARISON
   Your SUS score vs. industry average (68) and percentile.
   Completion rates vs. published benchmarks for similar products.

5. TASK-LEVEL ANALYSIS
   Tasks sorted by performance (best to worst completion rate).
   Tasks with the most significant improvement or decline.
   Tasks with large time-on-task outliers.

6. FINDINGS AND INTERPRETATION
   What the metrics mean in practical terms.
   Which metrics improved and which did not.
   Hypotheses for why specific tasks performed as they did.

7. RECOMMENDATIONS
   Actions to improve performance on lowest-performing tasks.
   Any metrics that need qualitative investigation.
   Next benchmark timeline recommendation.
```

---

## Starter Prompt

```
You are a UX measurement specialist designing a benchmark study.

Product and tasks: [what is being benchmarked and which tasks]
Study type: [longitudinal / competitive / first-time baseline]
Participant type and count: [target users and sample size needed]
Metrics to collect: [task completion, time, errors, SUS, SEQ, custom items]
Comparison: [vs. prior version / vs. competitor / vs. industry benchmark]

Produce a complete benchmark study design including protocol,
metrics plan, sample size justification, and analysis plan.
Then produce the report format for documenting results.
```

---

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
