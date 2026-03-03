# expert-review.md

> **Skill:** Produces a structured expert UX review evaluating an interface for usability, design quality, and effectiveness using expert judgment, with prioritized recommendations for improvement.

---

## TLDR

An expert UX review (also called an expert inspection or UX audit) is a systematic evaluation of a product's user experience by one or more UX experts. Unlike heuristic evaluation (which applies a fixed framework) or cognitive walkthrough (which focuses on learnability), an expert review brings broader UX judgment to bear: evaluating the product holistically against best practices, domain knowledge, and competitive context. Produces a prioritized list of observations and recommendations.

---

## Topic Explanation

### Expert Review vs. Heuristic Evaluation vs. Usability Test

| Method | Who evaluates | Framework | What it finds |
|---|---|---|---|
| Expert review | UX expert(s) | Expert judgment + best practices | Broad UX quality issues |
| Heuristic evaluation | 3 to 5 evaluators | Nielsen's 10 heuristics | Specific heuristic violations |
| Cognitive walkthrough | Researcher | 4 questions | Learnability barriers |
| Usability test | Real users | Task performance | Actual user failures |

Expert reviews produce the widest range of findings with the most context. Heuristic evaluations are more systematic and comparable across reviewers. Usability tests produce the most valid findings about real user behavior but require participant recruitment.

### Expert Review Dimensions

A comprehensive expert review evaluates:

**Findability and navigation:** Can users find what they need? Is the IA logical? Are labels clear?

**First-time experience:** Does the onboarding support new users effectively?

**Task flow efficiency:** Are common tasks completed in a reasonable number of steps? Are there unnecessary interruptions?

**Error prevention and recovery:** Are destructive actions protected? Are error messages helpful?

**Visual hierarchy and information density:** Is the most important information visually prominent? Is the interface overwhelming?

**Consistency:** Are patterns used consistently throughout? Do similar actions have similar affordances?

**Mobile and responsive experience:** Does the experience translate well across screen sizes?

**Performance perception:** Does the interface respond quickly and provide appropriate loading feedback?

**Emotional tone:** Does the design feel appropriately professional, trustworthy, and aligned with the brand?

---

## Output Format

```
1. REVIEW HEADER
   Product reviewed, reviewer(s) and expertise, scope, date, version.

2. EXECUTIVE SUMMARY
   Overall UX quality rating: Excellent / Good / Adequate / Poor.
   Top 3 strengths.
   Top 3 most impactful issues.

3. STRENGTHS
   What the design does particularly well.
   Why these are strengths worth preserving.

4. FINDINGS BY DIMENSION
   For each UX dimension reviewed:
   - Observations (specific, evidence-based)
   - Severity: Critical / Serious / Moderate / Minor
   - Recommendation

5. CONSOLIDATED ISSUE LIST
   All issues sorted by severity.
   Including: dimension, description, specific location, recommendation, effort estimate.

6. BENCHMARKING (optional)
   Comparison against industry standards or specific competitors on key dimensions.

7. QUICK WINS
   High-impact, low-effort improvements.
   Can be addressed without a redesign.

8. STRATEGIC RECOMMENDATIONS
   Longer-term improvements requiring more significant investment.
```

---

## Starter Prompt

```
You are a senior UX expert conducting a comprehensive expert review.

Product and interface: [describe the product and the flows to review]
User type: [who uses this product and their key characteristics]
Known issues or concerns: [any specific areas to pay particular attention to]
Competitive context: [what competitors or best-in-class examples to reference]
Scope: [which parts of the product are in scope]

Conduct a comprehensive expert review across all UX dimensions.
Document strengths, findings by dimension with severity ratings,
quick wins, and strategic recommendations.
Be specific about location and provide actionable remediation guidance for each finding.
```

---

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
