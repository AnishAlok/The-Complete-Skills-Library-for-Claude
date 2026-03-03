# cognitive-walkthrough.md

> **Skill:** Produces a cognitive walkthrough evaluation documenting step-by-step learnability analysis for a specific task flow, identifying where first-time users are likely to fail and why.

---

## TLDR

A cognitive walkthrough is a structured expert inspection method focused specifically on learnability: can first-time or infrequent users figure out how to accomplish a task without training? It walks through each step of a task and applies four questions to identify where users are likely to fail. More focused than a heuristic evaluation and more specific to first-time use.

---

## Topic Explanation

### The Four Cognitive Walkthrough Questions

For each step in a task, the evaluator asks:

1. **Will the user try to achieve the right effect?** Does the user know they need to take an action at this step to progress toward their goal?

2. **Will the user notice that the correct action is available?** Is the correct control visible, accessible, and findable given the user's current state?

3. **Will the user associate the correct action with the desired effect?** Does the label, icon, or description of the control match the user's expectation of what it does?

4. **If the user takes the correct action, will they see that they are making progress?** Does the system provide adequate feedback that the action was successful and the goal is progressing?

A "No" answer to any of these questions identifies a learnability failure at that step.

### Cognitive Walkthrough vs. Heuristic Evaluation

| Dimension | Cognitive Walkthrough | Heuristic Evaluation |
|---|---|---|
| Focus | Learnability (first-time use) | General usability across heuristics |
| Method | Step-by-step task analysis | Interface inspection by heuristic |
| Output | Per-step failure analysis | Issue list by heuristic |
| Best for | Onboarding flows, first-time tasks | General usability audit |

Use cognitive walkthrough when learnability of a specific flow is the primary concern. Use heuristic evaluation for a broader usability audit.

---

## Output Format

```
1. WALKTHROUGH HEADER
   Task(s) evaluated, user type assumed (prior knowledge, role),
   prototype or interface version, evaluator(s), date.

2. TASK DESCRIPTION
   The goal the user is trying to accomplish.
   The assumed starting state.

3. STEP-BY-STEP ANALYSIS
   For each step:
   - Step description (what the user must do)
   - Q1: Will they try the right thing? [Pass/Fail + rationale]
   - Q2: Will they notice the action? [Pass/Fail + rationale]
   - Q3: Will they interpret it correctly? [Pass/Fail + rationale]
   - Q4: Will they receive adequate feedback? [Pass/Fail + rationale]
   - Overall: Pass or Fail with severity (1 to 4)
   - Recommendation for failed questions

4. CRITICAL FAILURE POINTS SUMMARY
   Steps with failures rated Severity 3 or 4.
   The most common failure type across steps.

5. OVERALL LEARNABILITY ASSESSMENT
   Ratio of passing to failing steps.
   Severity distribution.
   Overall learnability rating: Good / Adequate / Poor.

6. RECOMMENDATIONS
   Specific design changes to address each failure point.
   Prioritized by severity.
```

---

## Starter Prompt

```
You are a UX specialist conducting a cognitive walkthrough.

Task being evaluated: [the specific user goal and task flow]
User type: [prior knowledge, technical experience, role]
Interface description: [describe each step of the task flow]
Known concerns: [any steps where learnability problems are suspected]

Apply the four cognitive walkthrough questions to each step.
Document pass/fail for each question with rationale.
Summarize critical failure points and produce specific design recommendations.
```

---

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
