# opportunity-solution-tree.md

> **Skill:** Produces an Opportunity Solution Tree (OST) documentation that maps desired outcomes to product opportunities to potential solutions to experiments, enabling structured product discovery.

---

## TLDR

The Opportunity Solution Tree (Teresa Torres) is a visual framework for connecting product discovery to delivery. It maps the path from desired outcome to identified opportunity to potential solution to the experiment that tests whether the solution addresses the opportunity. This skill documents an OST and the thinking behind each node.

---

## Topic Explanation

### OST Structure

The Opportunity Solution Tree has four levels:

**Desired outcome (root):** The metric the team is trying to move. Not a solution. "Increase the percentage of new users who complete their first payroll run within 7 days of signup."

**Opportunity nodes:** Problems customers experience, needs they have, or pain points that, if addressed, would move the desired outcome. Based on customer research. NOT solutions. "New users don't know what data they need to gather before starting payroll."

**Solution nodes:** Product changes or features that address a specific opportunity. Solutions live below the opportunities they address. "An onboarding checklist that shows required data before the user starts."

**Experiment nodes:** The test that determines whether a solution actually addresses its parent opportunity. "A/B test: onboarding checklist vs. current flow. Measure 7-day activation rate."

### Why OSTs Prevent Common Product Mistakes

**Prevents jumping to solutions:** By explicitly mapping opportunities before solutions, OSTs force teams to understand the problem before proposing answers.

**Prevents the one-solution trap:** An OST typically maps 3 to 5 solutions per opportunity. This prevents teams from falling in love with the first solution.

**Connects experiments to outcomes:** Every experiment is connected to an opportunity which is connected to an outcome. Teams can trace any experiment back to the business goal it serves.

**Reveals opportunity space:** By mapping all opportunities before choosing which to address, teams can compare opportunities by size, addressability, and strategic importance.

---

## Output Format

```
1. OST HEADER
   Team, product area, date, version.

2. DESIRED OUTCOME
   The metric being targeted.
   Current baseline.
   Target.
   Why this outcome matters.

3. OPPORTUNITY MAP
   For each identified opportunity:
   - Opportunity statement (a customer problem or need, not a solution)
   - Evidence: research that supports this opportunity's existence
   - Customer quote(s) that illustrate it
   - Estimated opportunity size: how many customers are affected and how much
   - Addressability: how feasible is it to address this opportunity

4. OPPORTUNITY PRIORITIZATION
   Which opportunities are being pursued and why.
   The opportunity being prioritized for this sprint/quarter.

5. SOLUTION EXPLORATION
   For the prioritized opportunity:
   3 to 5 potential solutions with brief descriptions.
   Rough effort estimate for each.
   Assumed mechanism: how each solution would address the opportunity.

6. SELECTED SOLUTION
   Which solution was selected and why.
   Key assumptions embedded in this solution.

7. EXPERIMENT DESIGN
   The experiment that will test whether the solution works.
   Linked to hypothesis statement.
   The metric that determines success.

8. LEARNING LOG
   Results from prior experiments in this tree.
   How prior learning influenced current direction.
```

---

## Starter Prompt

```
You are a product manager building an Opportunity Solution Tree.

Desired outcome: [the metric you are trying to move]
Customer research findings: [opportunities discovered in research]
Potential solutions identified: [options being considered]
Current experiment: [the test being run]
Prior learning: [what previous experiments taught you]

Produce a complete OST documentation including opportunity map,
prioritization rationale, solution exploration, and experiment design.
Each opportunity node must be a customer problem, not a solution.
```

---

*Skill file version: 1.0 | Phase: 02 - Product Management | Company type: Product*
