# roi-calculator-doc.md

> **Skill:** Produces the methodology documentation for an ROI calculator tool, including the business value model, input variables, calculation formulas, assumptions with sources, and sales usage guidance.

---

## TLDR

An ROI calculator helps prospects quantify the financial value of purchasing a product. This skill produces the methodology documentation: the business value model, input variables, calculation logic, assumptions with sources, sensitivity analysis, and sales usage guidance. Used to support enterprise deals where economic justification is required for internal purchase approval.

---

## Topic Explanation

### What Makes ROI Models Credible

The most common ROI calculator failure: wildly optimistic numbers that destroy credibility with a financially sophisticated buyer. A CFO or procurement team that sees a 10x ROI claim in year one will dismiss the entire model.

Credibility principles:
- Source every assumption from customer interviews, industry research, or analyst data
- Default to conservative estimates; aggressive "stretch" scenarios are available but clearly labeled
- Show the calculation logic, not just the output. Buyers trust models they can audit.
- Provide sensitivity analysis so the buyer can see how the ROI changes if assumptions are halved
- Connect to metrics the economic buyer already tracks and reports on

### ROI vs. TCO vs. Business Case

ROI calculator: quantifies the return on investment. How much value does the product create relative to its cost? Focused on benefits.

TCO (Total Cost of Ownership) calculator: quantifies full solution cost including implementation and operations. Focused on costs.

Business case document: combines both into a full investment justification. The ROI calculator and TCO analysis are inputs to the business case.

---

## Output Format

```
ROI CALCULATOR METHODOLOGY

Product: [name]
Calculator version: [X.X] | Date: [date] | Owner: [PMM or Finance]

1. BUSINESS VALUE MODEL
   Value categories this product creates:
   Category 1: [e.g., Time savings from automation]
   Category 2: [e.g., Error reduction / rework cost elimination]
   Category 3: [e.g., Revenue impact from faster processes]
   Category 4: [e.g., Headcount avoidance or redeployment]

2. INPUT VARIABLES (provided by the user)
   Variable | Description | Default | Source of default
   [e.g., Affected users | Number of employees using the product | 50 | User entered]
   [e.g., Hours per week on manual task | Time spent before product | 5 hrs | Industry benchmark]

3. ASSUMPTION VARIABLES (built into the model)
   Assumption | Value used | Source | Conservative range
   [e.g., % time saved | 40% | Customer interviews (N=12) | 25% to 55%]
   [e.g., Hourly fully-loaded cost | $85/hr | BLS + benefits multiplier | $60 to $110]

4. CALCULATION FORMULAS
   For each value category, show the explicit formula:
   Category name: [description]
   Formula: [Input A] x [Input B] x [Assumption C] = [Annual Value]
   Example: 50 users x 5 hrs/week x 40% saved x 50 weeks x $85/hr = $X

5. TOTAL ROI CALCULATION
   Annual benefit: sum of all value categories
   Annual product cost: [list based on pricing structure]
   Net annual benefit: Annual benefit minus Annual cost
   ROI %: (Net annual benefit / Annual cost) x 100
   Payback period: Annual cost / Monthly benefit (expressed in months)

6. SENSITIVITY ANALYSIS
   Scenario: assumptions at 50% of base case
   Scenario: assumptions at 75% of base case (conservative)
   Scenario: base case
   Scenario: assumptions at 125% of base case (optimistic)
   Break-even: minimum efficiency gain required to justify cost

7. SALES USAGE GUIDANCE
   When to introduce: [deal stage and buyer type where it is most effective]
   How to frame it: [specific language to introduce the calculator]
   If the output seems too high: [how to handle skepticism by walking through assumptions]
   If the output seems too low: [when this tool is not the right asset for this deal]
   Approval required to share externally: [process]
```

---

## Starter Prompt

```
You are a product marketer documenting an ROI calculator methodology.

Product: [name]
Value categories: [types of value the product creates]
Target buyer for the calculator: [who will review the output]
Key input variables: [what the buyer will provide]
Key assumptions: [what the model assumes, with evidence sources]
Calculation logic: [how inputs become output]
Conservative vs. optimistic scenarios: [the range of credible outcomes]

Produce complete ROI calculator documentation with all formulas shown explicitly,
assumption sourcing, sensitivity analysis, and sales usage guidance.
Every assumption must have a documented source.
Use conservative defaults.
```

---

*Skill file version: 1.0 | Phase: 08 - Product Marketing | Company type: Product*
