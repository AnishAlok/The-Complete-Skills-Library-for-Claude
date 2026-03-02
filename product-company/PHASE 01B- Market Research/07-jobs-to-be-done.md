# jobs-to-be-done.md

> **Skill:** Applies the Jobs-to-be-Done (JTBD) framework to uncover the functional, emotional, and social outcomes customers are trying to achieve, producing interview guides, job statements, and opportunity maps that drive product and positioning decisions.

---

## TLDR

This skill helps you answer: *"What are customers actually trying to accomplish, and what is the full job they are hiring our product to do?"* It produces JTBD interview guides, job statements, opportunity landscapes, and strategic implications using the Jobs-to-be-Done framework. Used for product strategy, market segmentation, positioning, feature prioritization, and new product ideation when understanding the underlying customer motivation is more important than understanding product feature preferences.

---

## Topic Explanation

### What Is Jobs-to-be-Done?

Jobs-to-be-Done is a theory of consumer action that explains why people buy and use products. The core idea, developed by Clayton Christensen, Tony Ulwick, and Bob Moesta (with different but complementary framings), is that customers do not buy products. They hire products to make progress in specific circumstances.

The famous example from Christensen: McDonald's wanted to understand why people bought milkshakes. Traditional research segmented buyers by demographics and preferences. JTBD research revealed that a significant group of milkshake buyers were commuters hiring the milkshake to do a specific job: keep them occupied and satisfied during a boring commute without making a mess or creating hunger again before lunch. The competitor to the milkshake in this job was not other milkshakes. It was bananas, bagels, and donuts. This insight changed both the product (thicker, slower to consume) and the merchandising (readily available at the drive-through window before 8am).

JTBD thinking has three key implications:

1. **The unit of analysis is the job, not the customer.** Two customers with identical demographics may be hiring your product for completely different jobs. Two customers with different demographics may be hiring it for the same job.

2. **Competitors are defined by the job, not the category.** Every product that helps a customer do the same job is a competitor, even if it looks nothing like your product.

3. **Progress is the purchase.** Customers buy when they believe your product will help them make progress they could not make before, or make progress they were making before but better, faster, cheaper, or with less friction.

### The Three Schools of JTBD

**Christensen / Disruption Theory framing**
Focuses on the job that causes a customer to hire or fire a product. What is the situation, the struggle, and the hire? Uses the "switch interview" to understand what triggered a purchase decision and what the customer was firing before they hired the new product.

**Ulwick / Outcome-Driven Innovation (ODI) framing**
More structured and quantitative. Defines jobs as functional outcomes with a specific format: "Help me [verb] [object] [context]." Measures the importance and satisfaction gap for each outcome statement to identify opportunity scores. Produces an opportunity landscape that maps where to invest.

**Moesta / Demand-Side Sales framing**
Focuses on the four forces of progress: push (the struggle with the current situation), pull (the attraction of the new solution), anxiety (the worry about switching), and habit (the comfort of the familiar). Used primarily to understand buyer psychology and improve sales and positioning.

All three approaches are complementary. This skill draws primarily on Christensen's framing for interview design and Ulwick's outcome-driven approach for opportunity mapping.

### Job Types

**Functional jobs:** The practical task the customer wants to accomplish.
Example: "Process payroll for my restaurant without errors or compliance risk."

**Emotional jobs:** How the customer wants to feel while doing the functional job, or as a result of it.
Example: "Feel confident that I am not going to get audited." "Feel like a responsible employer."

**Social jobs:** How the customer wants to be perceived by others as a result of using the product.
Example: "Be seen as a professional operator by my staff and accountant."

A complete JTBD analysis captures all three types. Products that address only functional jobs often lose to products that also address emotional and social jobs, even if the functional performance is equivalent.

### The Job Statement Format (Ulwick)

A well-formed job statement follows this structure:

**[Direction verb] + [object] + [context/clarification]**

Examples:
- "Minimize the time it takes to verify employee hours before running payroll"
- "Reduce the likelihood of making a compliance error on tip credit calculations"
- "Increase my confidence that payroll has been processed correctly before approving payment"

Job statements are written from the customer's perspective, not the product's perspective. They describe outcomes the customer wants, not features the product provides.

### The Opportunity Score (Ulwick)

Once job statements are defined, they can be scored to identify the best product opportunities. The opportunity score is calculated from customer surveys:

**Opportunity Score = Importance + max(Importance - Satisfaction, 0)**

High importance + low satisfaction = high opportunity (unmet need)
Low importance + high satisfaction = low opportunity (overserved)
High importance + high satisfaction = table stakes (meet expectations but no innovation opportunity)

This produces an opportunity landscape that shows where customers are most underserved, which directly informs where to invest in product development.

---

## When to Use This Skill

Use when:
- Building a new product and needing to understand the underlying job before designing features
- Discovering why customers are not adopting key features despite completing onboarding
- Repositioning a product and needing to understand what job the market really hires it for
- Designing a market segmentation model based on jobs rather than demographics
- Understanding why customers churn (they have fired your product from a job)
- Identifying new product opportunities by finding jobs that are underserved in the market
- Building messaging and positioning grounded in what customers are actually trying to achieve
- Evaluating a potential acquisition target based on which jobs their product is hired to do

Do NOT use when:
- You need to evaluate the usability of a specific interface (use `usability-test-plan.md`)
- You need to size a market opportunity (use `market-opportunity-analysis.md`)
- You have a short timeline and need faster qualitative methods (use `customer-discovery-interview.md`)
- You need large-scale quantitative validation of known job statements (use `survey-design.md`)

---

## Dos

- **Do interview people immediately after a purchase or significant product decision.** The switch interview (Moesta's method) is most revealing when the decision is fresh. Memory of the reasons for switching degrades rapidly.
- **Do ask about the situation, not the product.** "Tell me about the last time you ran payroll and felt stressed about it" surfaces job context. "What features do you want in a payroll tool?" surfaces product preferences that may not reflect the real job.
- **Do probe the emotional and social dimensions.** Functional job answers come easily. Emotional and social jobs require more probing: "How did that make you feel?" "What were you most worried about?" "What would your accountant think if..."
- **Do ask about the "old solution" that was fired.** JTBD is most useful when you understand what the customer was doing before. The fired solution reveals the job better than the hired solution.
- **Do use the timeline technique.** Walk the customer back through their decision chronologically. "When did you first realize you needed a different solution? What happened that day? What did you do next?" Timelines reveal the push and pull forces.
- **Do look for patterns across multiple interviews before writing job statements.** A job statement is a synthesis across 8 to 15 interviews, not a quote from a single customer.
- **Do separate job discovery (qualitative) from opportunity sizing (quantitative).** Discover jobs through interviews first. Then validate importance and satisfaction through surveys with a larger sample.
- **Do test whether job statements pass the "progress" test.** A well-formed job statement describes progress: moving from a worse state to a better state. If your statement does not describe progress, revise it.

---

## Donts

- **Dont ask customers what they want in a product.** This produces feature requests, not job insights. The famous Henry Ford quote applies: asking customers what they want gets you a faster horse, not a car.
- **Dont write job statements in product language.** "Process payroll faster with AI" is a product description. "Reduce the time between closing the pay period and payment confirmation" is a job statement.
- **Dont confuse a job with a use case.** A use case describes how a product is used. A job describes why the customer needs that use case to exist. Use cases are functional. Jobs include the emotional and social context.
- **Dont conduct JTBD interviews with customers who have not made a recent decision.** The switch interview methodology depends on the customer being able to recall the specific event that triggered the decision. Customers who made decisions 2 or more years ago often cannot.
- **Dont ignore the social job.** In B2B especially, how a buyer will be perceived by their boss, peers, or direct reports is often as important as the functional outcome. Products that make the buyer look smart, safe, or competent often win over products that are technically superior.
- **Dont write too many job statements.** Ulwick recommends 50 to 150 outcome statements for a thorough ODI study. For most product teams, 15 to 30 prioritized job statements are more practical and still very actionable.
- **Dont confuse job segments with demographic segments.** Two customers with completely different demographics may be in the same job segment. Two customers in the same industry may be hiring your product for entirely different jobs. Job-based segments require JTBD research to identify.
- **Dont skip the anxiety and habit forces.** Moesta's switch interview framework reveals that customers who want to make progress are often held back by anxiety (will the new solution work?) and habit (the comfort of the current approach). Understanding these forces is critical for positioning and sales.

---

## Ideal Inputs

### Required
```
1. THE PRODUCT OR CATEGORY BEING STUDIED
   What product, feature, or category is this JTBD research about?

2. THE CUSTOMER TYPE
   Who are the customers to interview?
   What decision or behavior are you studying?
   (Recent purchasers? Recent churners? Non-adopters of a specific feature?)

3. THE DECISION OR BEHAVIOR TO INVESTIGATE
   What specific decision, purchase, or behavior is the focus?
   Example: "The decision to switch from manual payroll to software"
   or "The decision to stop using our reporting feature after 30 days"

4. WHAT YOU ALREADY KNOW
   What jobs or motivations does the team currently hypothesize?
   What surprises or inconsistencies in customer behavior have been observed?

5. HOW FINDINGS WILL BE USED
   Will this feed product strategy? Positioning? Segmentation? Pricing?
   The intended use shapes which aspects of JTBD to emphasize.
```

### Optional but Valuable
```
6. PRIOR RESEARCH
   Any prior customer interviews, surveys, or behavioral data
   that provides context for the JTBD study.

7. CHURN OR ADOPTION PATTERNS
   Which customers churn and which stay?
   Which features are adopted and which are not?
   These patterns reveal where jobs are being done well vs. poorly.

8. COMPETITOR CONTEXT
   What alternatives do customers use for the same job?
   What were they doing before they hired your product?

9. NUMBER OF INTERVIEWS PLANNED
   This affects how deeply to probe in each session.
   8 to 12 interviews are typically sufficient for job discovery.

10. JTBD SCHOOL PREFERENCE
    Christensen switch interview focus?
    Ulwick outcome-driven opportunity mapping?
    Moesta four forces of progress?
    Or a combination?
```

### Example of a Strong Input Prompt
```
Product: Restaurant payroll compliance software
Customer type: Restaurant operators who recently switched from manual payroll
to a software solution (including ours and competitors)
Decision to investigate: The decision to switch from manual payroll/spreadsheets
to dedicated payroll software
What we know: We know the functional job (process payroll, avoid compliance errors).
We do not understand the emotional triggers, the anxiety that delays switching,
or the social dimensions (accountant influence, staff perception).
How findings will be used: Positioning refresh for Series A, sales script for
overcoming objections, and product roadmap for next quarter
Prior research: 8 customer discovery interviews completed. Functional pain is confirmed.
Churn pattern: Customers who use only payroll processing churn at 18%.
Customers who also use compliance reporting churn at 3%.
Competitor context: Most customers were previously using QuickBooks or spreadsheets
Number of interviews: 10 to 12
JTBD school: Moesta switch interview primary, with Ulwick outcome statements for
the opportunity mapping phase
```

---

## Output Format

```
1. RESEARCH DESIGN
   The specific JTBD methodology to be used.
   Interview structure and timeline.
   Participant criteria and recruiting approach.

2. JTBD INTERVIEW GUIDE
   Opening and context-setting
   Timeline elicitation: "Take me back to when you first..."
   Push questions: What was struggling / frustrating / not working?
   Pull questions: What first caught your attention about a new solution?
   Anxiety questions: What almost stopped you from switching?
   Habit questions: What did you miss about the old way?
   Social and emotional probes throughout
   Closing and future-looking questions

3. SYNTHESIS TEMPLATE (for use after interviews)
   Timeline of the switch / decision
   The triggering moment (what happened that started the job)
   The functional job statement(s)
   The emotional job statement(s)
   The social job statement(s)
   The fired solution and why it was fired
   The anxiety that nearly prevented the switch
   The habit that had to be overcome

4. JOB STATEMENTS (produced after synthesis across interviews)
   Functional job statements in Ulwick format:
   [Direction verb] + [object] + [context]
   Emotional job statements
   Social job statements

5. OPPORTUNITY LANDSCAPE (if quantitative validation planned)
   Survey instrument for importance and satisfaction scoring
   Opportunity score calculation method
   Visualization: opportunity map showing high/low opportunity areas

6. JOB-BASED SEGMENTS
   Customer segments defined by which jobs they prioritize
   Rather than demographic characteristics

7. STRATEGIC IMPLICATIONS
   What the jobs analysis means for:
   - Product: where to invest to better serve the core job
   - Positioning: how to message in job language, not feature language
   - Sales: how to surface the job in discovery conversations
   - Pricing: what pricing structure aligns with the value of the job done
```

---

## Starter Prompt

```
You are a Jobs-to-be-Done research specialist helping me uncover the underlying
customer jobs that drive purchase and usage decisions.

Product or category: [what product, feature, or category is being studied]
Customer type: [who to interview and what decision or behavior to study]
Decision or behavior to investigate: [the specific switch, adoption, or churn to understand]
What we already know: [current hypotheses about jobs and motivations]
Churn and adoption patterns: [behavioral signals about which jobs are served well or poorly]
Competitor context: [what alternatives customers use for the same job]
How findings will be used: [product strategy / positioning / segmentation / pricing]
Number of interviews: [target number of sessions]
JTBD school preference: [Christensen switch interview / Ulwick ODI / Moesta four forces / combination]

Please produce:
1. A research design for this JTBD study
2. A complete switch interview guide with: timeline elicitation, push questions,
   pull questions, anxiety questions, habit questions, and emotional/social probes
3. A synthesis template for processing each interview after completion
4. A template for writing job statements in Ulwick format after synthesis
5. A cross-interview pattern recognition template for identifying the common job
   across multiple interviews
6. An opportunity landscape design if quantitative validation is planned
7. Strategic implications framework for connecting job findings to product,
   positioning, sales, and pricing decisions

Write interview questions that ask about situations and experiences,
not about product preferences. Flag any question that could produce
feature requests rather than job insights.
Remind me to probe for emotional and social jobs in addition to functional jobs.
```

---

## Related Skills

| Use This Next | Why |
|---|---|
| `market-segmentation.md` | Use job-based segments to replace or augment demographic segments |
| `positioning-doc.md` | Translate job statements into positioning language |
| `feature-prioritization.md` | Use opportunity scores to prioritize product investment |
| `messaging-framework.md` | Build messaging around the jobs customers hire the product to do |
| `research-synthesis-report.md` | Synthesize JTBD interview findings into a report |

| Use This Before | Why |
|---|---|
| `survey-design.md` | JTBD interviews generate the outcome statements surveys then validate at scale |
| `product-strategy-doc.md` | Job insights should inform the product bets in the strategy doc |
| `mvp-definition.md` | The core job defines the minimum feature set for an MVP |

---

## Reference Frameworks

| Framework | Use For |
|---|---|
| Jobs-to-be-Done Theory (Christensen) | Foundational framing: customers hire products to make progress |
| Outcome-Driven Innovation (Ulwick) | Structured job statement format and opportunity scoring methodology |
| Switch Interview (Moesta) | Timeline-based interview for understanding the four forces of progress |
| The Demand-Side Sales Framework (Moesta) | Connecting JTBD insights to sales motion and objection handling |
| Job Map (Ulwick) | Mapping the full sequence of steps in a customer job |

---

*Skill file version: 1.0 | Phase: 01 - Ideation and Market Research | Company type: Product*
