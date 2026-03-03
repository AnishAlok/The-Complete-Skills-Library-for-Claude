# tree-testing-report.md

> **Skill:** Produces a tree testing analysis report with task success rates, directness scores, and navigation recommendations for validating or improving an information architecture.

---

## TLDR

Tree testing evaluates a proposed IA by asking participants to find items using only the category structure and labels, without any visual design. It isolates navigation effectiveness from interface design. The report produces per-task success rates, directness scores, and specific navigation recommendations.

---

## Topic Explanation

### What Tree Testing Measures

Tree testing answers: "Can users find what they are looking for using this navigation structure?" It removes interface design variables (color, typography, visual hierarchy) so only the IA logic and labeling are tested.

**Task success rate:** The percentage of participants who found the correct location for each task. Success rates below 70% indicate a navigation problem for that task.

**Directness score:** The percentage of participants who found the correct location without backtracking. High success with low directness suggests users are getting to the right place through trial and error rather than intuitive navigation.

**First click:** Where participants clicked first for each task. First-click data reveals initial mental model assumptions about where something should be found.

**Time on task:** Longer time indicates more exploration and uncertainty.

### Interpreting Results

| Success Rate | Interpretation |
|---|---|
| 90%+ | Excellent. No changes needed. |
| 70 to 89% | Good. Minor labeling improvements may help. |
| 50 to 69% | Problematic. Review category labels and placement. |
| Below 50% | Critical. The item is fundamentally miscategorized. |

**Success with low directness** (finding the right answer after backtracking): Users are guessing. The category labels are not providing strong enough signals. Fix with better labeling rather than structural changes.

**Low success on multiple items in one category:** The category itself may be too broad, too vague, or poorly labeled.

---

## Output Format

```
1. STUDY OVERVIEW
   Tree tested, participant count, tasks included, tool used, date.

2. OVERALL RESULTS SUMMARY
   Average task success rate across all tasks.
   Average directness score.
   Tasks sorted from highest to lowest success rate.

3. PER-TASK ANALYSIS
   For each task:
   - Task description
   - Success rate with confidence interval
   - Directness score
   - Most common correct path taken
   - Most common incorrect paths
   - First-click distribution
   - Diagnosis: labeling problem / structural problem / unclear task wording

4. PROBLEM AREAS IDENTIFIED
   Categories with multiple low-success tasks.
   Labels that attracted wrong clicks consistently.
   Items that participants looked for in a different location than the current one.

5. IA RECOMMENDATIONS
   Specific label changes recommended.
   Structural changes recommended (moving items, splitting categories).
   Items requiring further research.
   Priority: Must fix / Should fix / Consider fixing.

6. BEFORE/AFTER COMPARISON (if re-testing an existing IA)
   Success rate changes per task.
   Overall improvement or decline.
```

---

## Starter Prompt

```
You are a UX researcher analyzing tree testing results.

Tree structure tested: [the category hierarchy]
Participant count: [number of participants]
Task results: [success rates, directness scores, first-click data per task]
Purpose: [validating a proposed IA / diagnosing navigation problems]

Produce a complete tree testing report with per-task analysis,
problem area identification, and specific IA recommendations.
```

---

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
