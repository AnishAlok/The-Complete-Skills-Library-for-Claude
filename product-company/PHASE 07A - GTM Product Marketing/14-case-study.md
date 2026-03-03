# case-study.md

> **Skill:** Produces a customer case study in the standard problem-solution-result format documenting a specific customer success story for use in sales and marketing.

---

## TLDR

A case study documents how a specific customer used a product to solve a real problem and achieve a measurable outcome. It is the most credible form of product marketing content because it replaces vendor claims with customer evidence. This skill produces the structured case study: company background, challenge, solution, results, and customer quote.

---

## Topic Explanation

### What Makes a Case Study Get Used

Case studies that get used in deals share three characteristics: the customer looks like the prospect, the problem matches what the prospect experiences, and the results are specific enough to be credible.

Generic case studies fail on one or more of these. "A large enterprise company improved efficiency" is not a case study anyone will use in a deal. "Acme Corp, a 500-person logistics company, reduced invoice processing time from 4 days to 6 hours after deploying [product] in Q3" is.

### The Critical Results Section

The results section determines whether a case study gets used in sales. Results must be:
- Specific (a number, not a description)
- Attributable to the product (not just correlation)
- Meaningful to the next buyer (a metric they track and care about)
- Approved by the customer for external use

The best results combine a hard metric with a business outcome: "Reduced onboarding time by 65%, enabling the team to handle 40% more clients without adding headcount."

---

## Output Format

```
CASE STUDY

Headline: "[Company Name] [Achieves Specific Result] with [Product Name]"
[Make the result the headline. Not "How Company X Uses Product Y."]

COMPANY AT A GLANCE
Industry: [industry]
Size: [employees or revenue range]
Location: [HQ]
Use case: [how they use the product]

THE CHALLENGE
[3 to 5 sentences. The specific problem before the product.
What they were doing. What was not working. The cost or consequence of the problem.
Use the customer's language where possible.]

WHY [PRODUCT NAME]
[2 to 3 sentences. What the evaluation process looked like.
What alternatives were considered. What made the difference in selecting this product.]

THE SOLUTION
[3 to 5 sentences. What was implemented and how.
How the product was deployed. Key integrations or configurations.
Timeline from decision to value.]

THE RESULTS

[Result 1]: [Specific metric and what it means for the business]
[Result 2]: [Specific metric]
[Result 3]: [Specific metric]

[1 to 2 sentences of narrative context: what these results enabled or changed.]

IN THEIR OWN WORDS
"[Customer quote: 2 to 4 sentences in the customer's natural voice.
Should describe the impact they experienced, not repeat the metrics above.]"
[Full Name], [Title], [Company Name]

ABOUT [PRODUCT NAME]
[1 to 2 sentence boilerplate]
```

---

## Starter Prompt

```
You are a product marketer writing a customer case study.

Customer: [company name, industry, company size]
The challenge: [specific problem before the product, in their language]
Alternatives they evaluated: [what else they considered]
What was implemented: [how they use the product]
Results achieved: [specific metrics, ideally 3 to 5]
Customer quote: [name, title, and what they said or want to say]
Approved for external use: [confirm which metrics and the customer name are approved]

Produce a complete case study.
The headline must feature the most compelling specific result.
Results must include at least 3 numeric outcomes.
The quote must add insight not already present in the results section.
```

---

*Skill file version: 1.0 | Phase: 08 - Product Marketing | Company type: Product*
