# heuristic-evaluation.md

> **Skill:** Produces a structured heuristic evaluation report applying Nielsen's 10 usability heuristics to identify, classify, and prioritize usability issues in a product interface.

---

## TLDR

A heuristic evaluation is an expert inspection method in which evaluators examine an interface against established usability principles (heuristics) to identify issues. It produces a severity-rated list of usability problems without requiring participant recruitment. Fast, inexpensive, and complementary to user testing. Best conducted by 3 to 5 evaluators independently, then combined.

---

## Topic Explanation

### Nielsen's 10 Usability Heuristics

1. **Visibility of system status:** The system keeps users informed about what is going on through appropriate feedback within reasonable time.

2. **Match between system and the real world:** The system uses words, phrases, and concepts familiar to the user rather than system-oriented terms.

3. **User control and freedom:** Users make mistakes and need clearly marked "emergency exits" to leave unwanted states without extended dialogue.

4. **Consistency and standards:** Users should not have to wonder whether different words, situations, or actions mean the same thing.

5. **Error prevention:** Even better than good error messages is a careful design which prevents a problem from occurring in the first place.

6. **Recognition rather than recall:** Minimize the user's memory load by making objects, actions, and options visible.

7. **Flexibility and efficiency of use:** Accelerators allow expert users to speed up interaction while the system remains accessible to novice users.

8. **Aesthetic and minimalist design:** Dialogues should not contain irrelevant or rarely needed information.

9. **Help users recognize, diagnose, and recover from errors:** Error messages should be expressed in plain language, precisely indicate the problem, and constructively suggest a solution.

10. **Help and documentation:** Even though it is better if the system can be used without documentation, help and documentation may be necessary.

### Severity Ratings

Each identified issue should be assigned a severity rating:

- **Severity 4 (Catastrophic):** Must be fixed before launch. Prevents users from completing their goal.
- **Severity 3 (Major):** High priority fix. Causes significant frustration or errors.
- **Severity 2 (Minor):** Should fix if resources allow. Causes some friction.
- **Severity 1 (Cosmetic):** Fix only if time permits. Violates the heuristic but causes minimal friction.

### How Many Evaluators

Nielsen's research shows diminishing returns above 5 evaluators. Three to five evaluators each working independently, then combining findings, is the optimal protocol. A single evaluator misses approximately 35% of issues. Three evaluators find approximately 65 to 75%.

---

## When to Use This Skill

Use when:
- A design is ready for review but user research is not yet possible
- A quick expert review is needed before a usability test to find obvious issues
- Auditing an existing product for a redesign initiative
- Conducting a competitive evaluation of a competitor's product

---

## Dos

- **Do have evaluators work independently before combining.** Individual evaluators uncontaminated by others' findings is what gives the method its validity.
- **Do go through the interface multiple times.** First pass for general orientation, subsequent passes focused on specific heuristics.
- **Do evaluate from the target user's perspective.** Apply heuristics relative to the expected user population's knowledge and experience.
- **Do include positive findings.** Note what the design does well, not only problems.

---

## Output Format

```
1. EVALUATION HEADER
   Product/interface evaluated, evaluators, date, scope, heuristics framework used.

2. EVALUATION SCOPE
   Which flows or screens were evaluated.
   What was out of scope.

3. ISSUES BY HEURISTIC
   For each heuristic:
   - Issues found (with screenshot references if available)
   - Severity rating for each issue
   - Specific recommendation

4. CONSOLIDATED ISSUE LIST
   All issues sorted by severity (4 to 1).
   Including: heuristic violated, location, description, recommendation.

5. SUMMARY STATISTICS
   Total issues by severity.
   Most violated heuristic.
   Overall usability health assessment.

6. POSITIVE FINDINGS
   What the design does well against the heuristics.

7. PRIORITY RECOMMENDATIONS
   Top 5 issues to address immediately.
   With effort estimate (low/medium/high) if possible.
```

---

## Starter Prompt

```
You are a UX expert conducting a heuristic evaluation.

Product or interface: [what is being evaluated]
Evaluator perspective: [who the target user is]
Scope: [which flows or screens are in scope]
Specific concerns: [any known problem areas to pay attention to]

Apply Nielsen's 10 usability heuristics to the described interface.
For each heuristic, identify issues, assign severity ratings (1 to 4),
and provide specific design recommendations.
Produce a consolidated issue list sorted by severity and a priority
recommendation list for the top 5 issues.
```

---

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
