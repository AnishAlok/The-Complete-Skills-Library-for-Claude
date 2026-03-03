# product-hypothesis-log.md

> **Skill:** Produces and maintains a structured running log of product hypotheses, their test results, and the decisions made based on learning, creating an institutional memory of product discovery.

---

## TLDR

A product hypothesis log is the institutional memory of a product team's learning. It records every hypothesis tested, the experiment run, the outcome, and the decision taken as a result. Over time, it reveals patterns in what works and what doesn't and prevents teams from re-testing hypotheses already answered. Used as a living document throughout a product's lifecycle.

---

## Topic Explanation

### Why Hypothesis Logs Get Abandoned

Most teams start hypothesis tracking with good intentions and abandon it within two quarters. The failure modes:
- The format is too burdensome to maintain
- Nobody reviews it, so there is no value visible from maintaining it
- New team members don't know it exists
- Results are recorded but decisions and follow-on actions are not

A hypothesis log that is maintained requires a simple format, a clear owner, a regular review ritual, and a specific moment in the product process where the log is consulted (e.g., before planning begins, the hypothesis log is reviewed to inform priorities).

### What Belongs in a Hypothesis Log Entry

- The hypothesis as originally stated (do not edit after the fact)
- The experiment that tested it
- The result: confirmed / disconfirmed / inconclusive
- The confidence level in the result
- The decision made based on the result
- The next hypothesis (what the team will test next)

Do not include: post-hoc rationalizations for results, experiments that were not run, or hypotheses stated so vaguely they cannot be tested.

---

## Output Format

```
1. LOG HEADER
   Product area, team, last updated, total entries.

2. HYPOTHESIS LOG TABLE
   Columns: ID / Date / Hypothesis / Type / Experiment / Result /
   Confidence / Decision Made / Next Hypothesis

3. ENTRY FORMAT
   For each hypothesis:
   ID: H-[sequential number]
   Date stated: [when the hypothesis was articulated]
   Hypothesis: [exact original statement]
   Type: Desirability / Usability / Feasibility / Viability
   Experiment: [what was built or tested to evaluate it]
   Duration: [how long the test ran]
   Metric: [what was measured]
   Result: Confirmed / Disconfirmed / Inconclusive
   Evidence: [the data or qualitative finding]
   Confidence: High / Medium / Low [with rationale]
   Decision: [what the team decided to do based on this result]
   Next hypothesis: [the hypothesis that follows from this result]

4. SUMMARY STATISTICS
   Total hypotheses logged.
   % Confirmed / Disconfirmed / Inconclusive.
   Average confidence level.
   Most valuable disconfirmations (what we were most wrong about).

5. REVIEW CADENCE
   When the log is reviewed (quarterly planning, retrospectives).
   Who maintains it.
   How new team members are introduced to it.
```

---

## Starter Prompt

```
You are a product manager setting up or updating a hypothesis log.

Product area: [what product or feature area]
Hypotheses to log: [the hypotheses and their test results]
Current summary statistics: [if updating an existing log]

Produce a hypothesis log in the specified format.
If setting up from scratch, include 3 to 5 example entries from past work
and a maintenance guide.
If updating, add new entries and update summary statistics.
```

---

*Skill file version: 1.0 | Phase: 02 - Product Management | Company type: Product*
