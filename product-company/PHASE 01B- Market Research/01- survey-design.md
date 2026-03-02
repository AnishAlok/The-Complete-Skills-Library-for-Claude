# survey-design.md

> **Skill:** Designs rigorous, unbiased surveys with correct question types, logical flow, proper scale construction, and analysis-ready structure for market research, customer feedback, and product validation.

---

## TLDR

This skill helps you answer: *"How do we design a survey that produces reliable, unbiased data we can actually act on?"* It produces a complete survey instrument with appropriate question types, logical flow, skip logic, scale construction, and an analysis plan. Used for market research, customer satisfaction measurement, product validation, NPS programs, and employee feedback.

---

## Topic Explanation

### What Makes a Survey Rigorous?

Most surveys produced by product and marketing teams fail at the most basic level: they ask leading questions, use inconsistent scales, mix question types inappropriately, and produce data that cannot be synthesized into clear conclusions. A rigorous survey is one whose design choices are made deliberately to minimize bias and maximize the usefulness of the resulting data.

Rigorous survey design requires attention to five dimensions:

1. **Question validity:** Does each question actually measure what it claims to measure?
2. **Response bias minimization:** Does the design avoid pushing respondents toward particular answers?
3. **Scale consistency:** Are rating scales used consistently throughout in a way that enables comparison?
4. **Logical flow:** Does the question order make sense to a respondent and not prime answers to later questions?
5. **Analysis readiness:** Will the data produced be analyzable in a way that answers the research questions?

### Question Types and When to Use Each

**Closed-ended questions (quantitative)**

Multiple choice (single select):
Best for: Categorical data where only one answer is correct or relevant.
Example: "Which of the following best describes your role?" with a mutually exclusive list.
Pitfall: Make sure the options are mutually exclusive and collectively exhaustive. Add "other (please specify)" if the list might be incomplete.

Multiple choice (multi-select / check all that apply):
Best for: When respondents may have multiple relevant answers.
Example: "Which of the following tools do you currently use?"
Pitfall: Multi-select data is harder to analyze than single-select. Avoid overuse.

Likert scale:
Best for: Measuring attitudes, agreement, satisfaction, or frequency.
Standard: 5-point scale (Strongly disagree / Disagree / Neutral / Agree / Strongly agree)
Extended: 7-point scale for more granularity when needed.
Pitfall: Always use the full scale including the neutral midpoint. Forced-choice scales (even number of points) generate artificial data.

Rating scale:
Best for: Evaluating quality, likelihood, or importance.
Example: "How likely are you to recommend us to a colleague? (0 to 10)"
Pitfall: Inconsistent scale direction across questions confuses respondents. Always anchor low (1 or 0 = negative) and high (10 = positive).

Ranking:
Best for: Determining relative priority among a defined set of options.
Example: "Rank the following features in order of importance to you (1 = most important)."
Pitfall: Ranking is cognitively demanding. Limit to 5 items maximum. Ranking data requires different analysis than rating data.

Matrix/grid:
Best for: Rating multiple items on the same scale efficiently.
Example: Rate each of the following features on importance (1 to 5): [list]
Pitfall: Matrix questions cause response fatigue and pattern answering (all midpoints). Limit matrix questions to 5 to 7 items per matrix.

**Open-ended questions (qualitative)**

Short text:
Best for: Collecting specific facts, labels, or brief explanations.
Example: "What is your job title?"

Long text:
Best for: Collecting rich qualitative context that closed-ended questions cannot capture.
Example: "What is the most frustrating part of your current workflow?"
Pitfall: Response rates on open text are low. Place open text questions strategically, not throughout. Analyze with thematic coding, not just reading.

**Demographic and classification questions**

Always place at the end of the survey, not the beginning. Respondents who see demographic questions first may adjust their other answers based on perceived expectations for their demographic group.

### Bias Types to Avoid

**Leading questions:** Containing language that implies a preferred answer.
Biased: "How much has our product improved your workflow?"
Neutral: "How, if at all, has our product affected your workflow?"

**Double-barreled questions:** Asking about two things in one question.
Biased: "Is our product easy to use and reliable?"
Better: Two separate questions, one for ease of use and one for reliability.

**Loaded questions:** Containing assumptions embedded in the question.
Biased: "When did you realize our onboarding was confusing?"
Neutral: "How would you describe your experience with our onboarding process?"

**Acquiescence bias:** The tendency of respondents to agree with statements.
Mitigation: Balance positive and negative items. Use rating scales that require more nuance than agree/disagree.

**Social desirability bias:** Respondents answering in ways they believe are socially acceptable.
Mitigation: Anonymous surveys, neutral question framing, behavioral questions instead of attitudinal ones.

**Recency bias:** Questions about general behavior elicit answers based on recent experience.
Mitigation: Specify time periods explicitly: "In the past 30 days, how often..."

### Survey Length and Completion Rate

Completion rate drops sharply with survey length:
- Under 5 minutes (up to 10 questions): 80 to 90% completion rate
- 5 to 10 minutes (10 to 20 questions): 60 to 70% completion rate
- 10 to 15 minutes (20 to 30 questions): 40 to 50% completion rate
- Over 15 minutes: significant drop-off

For most market research purposes: target under 10 minutes and under 20 questions. Every question that does not directly answer a research objective should be removed.

### Skip Logic and Branching

Skip logic routes respondents to different questions based on their previous answers. It improves relevance (respondents only see questions applicable to them) and reduces length (respondents skip irrelevant sections).

Example: If Q3 answer is "I do not currently use a payroll tool," skip to Q8 (questions 4 to 7 are only relevant for current tool users).

Good skip logic design requires mapping the question flow before writing questions, not after. Always pilot test skip logic before launching.

---

## When to Use This Skill

Use when:
- Conducting market research to validate a product idea or market sizing assumption
- Measuring customer satisfaction, NPS, or CSAT
- Collecting product feedback at scale (too many customers for individual interviews)
- Validating hypotheses generated from qualitative research
- Running employee engagement surveys
- Screening participants for qualitative research
- Collecting demographic or behavioral segmentation data

Do NOT use when:
- You need to understand the "why" behind behaviors (use qualitative interviews instead)
- You have fewer than 50 potential respondents (qualitative interviews will be more useful)
- The question requires nuanced exploration (use `customer-discovery-interview.md` or `focus-group-guide.md`)
- You need real-time behavioral data (use analytics and event tracking, not surveys)

---

## Dos

- **Do map research questions to survey questions before writing.** For every survey question, identify which research objective it serves. Delete any question that does not map to an objective.
- **Do use the same scale direction throughout.** If 1 is negative and 5 is positive for one question, maintain that direction for all scale questions. Inconsistent direction causes errors.
- **Do include "other (please specify)" for categorical questions where your list might be incomplete.** This captures responses you did not anticipate and reveals gaps in your assumptions.
- **Do place sensitive or demographic questions at the end.** Respondents who see demographic questions first may pattern their answers differently. Keep demographics for the final section.
- **Do pilot the survey with 3 to 5 people before launching.** Pilots catch confusing questions, broken skip logic, and questions that respondents interpret differently than intended.
- **Do specify time periods in behavioral questions.** "How often do you use X?" is vague. "In the past 30 days, how many times did you use X?" is measurable.
- **Do balance your scale anchors.** A 1-to-5 scale should have 2 positive, 1 neutral, and 2 negative points, not 3 positive and 2 negative.
- **Do include an attention check question in longer surveys.** A question with an obvious correct answer (e.g., "For quality control, please select option 3") catches respondents who are answering randomly.
- **Do write the analysis plan before finalizing the survey.** If you cannot describe how you will analyze each question before launching, you will not be able to analyze it after.

---

## Donts

- **Dont ask leading questions.** Any question that implies a preferred answer will bias your data. Read every question from the perspective of a skeptical respondent.
- **Dont use double-barreled questions.** One question, one concept. If "and" or "or" appears in a question, it is probably double-barreled.
- **Dont use jargon or acronyms without definition.** What is obvious to your team may be unfamiliar to respondents. Define all technical terms or avoid them.
- **Dont make every question required.** Forcing responses on every question causes respondents to enter random answers rather than skip irrelevant questions. Make only the most critical questions required.
- **Dont use grid/matrix questions for more than 7 items.** Longer matrices cause response fatigue and straight-line answering (checking the same column for every item).
- **Dont mix scale directions.** Reversing scale direction (1 = positive for one question, 1 = negative for another) causes errors that contaminate the data.
- **Dont launch without a pilot.** Every survey has at least one question that respondents misinterpret. Find it before launching to 500 people, not after.
- **Dont ask for information you already have.** If you have customer records with company size and industry, do not ask those questions again in the survey. It wastes respondent time and signals poor preparation.
- **Dont write the survey before writing the analysis plan.** If you cannot specify how you will analyze the data, you will end up with data you cannot use.
- **Dont use a 4-point scale without good reason.** Forced-choice scales without a neutral midpoint artificially eliminate genuine "neutral" responses and generate data that looks more opinionated than reality.

---

## Ideal Inputs

### Required
```
1. RESEARCH OBJECTIVES
   The 3 to 5 specific questions this survey needs to answer.
   Each stated as a research question, not a survey question.

2. TARGET RESPONDENTS
   Who will take this survey?
   What are their key characteristics?
   How will they be recruited or accessed?

3. KEY TOPICS OR DIMENSIONS TO COVER
   The subject areas or constructs you need to measure.
   Examples: satisfaction with specific features, purchase intent,
   current workflow behaviors, awareness of alternatives.

4. DESIRED SURVEY LENGTH
   Maximum time respondents should spend: 3 minutes, 5 minutes, 10 minutes?
   This constrains the number of questions.

5. HOW THE DATA WILL BE USED
   What decisions or actions will this data inform?
   What format will findings be presented in?
```

### Optional but Valuable
```
6. EXISTING QUESTIONS OR VALIDATED SCALES
   Are there specific questions or scales (e.g., SUS, NPS, CSAT)
   that should be included for benchmarking or consistency?

7. PRIOR SURVEY DATA
   Have you run similar surveys before?
   Are there trend questions that must be maintained for comparability?

8. SEGMENTS TO COMPARE
   Will you need to compare results across segments (e.g., SMB vs. enterprise)?
   This affects sampling and question design.

9. PLATFORM
   Which survey platform will be used? (Typeform, SurveyMonkey, Qualtrics, etc.)
   Platform capabilities affect skip logic complexity.

10. INCENTIVE AND DISTRIBUTION PLAN
    How will respondents be recruited?
    Will there be an incentive?
    What is the target response count?
```

### Example of a Strong Input Prompt
```
Research objectives:
1. What is the current awareness and consideration level of our product
   among mid-market CFOs who have not yet trialed us?
2. What are the top 3 pain points in their current AP reconciliation process?
3. What features or capabilities would most influence their decision to trial
   a new tool?
4. What price point range would they consider reasonable for this category?
Target respondents: CFOs and Controllers at US-based companies with 50 to 500 employees
currently handling AP reconciliation manually or with legacy ERP
Topics to cover: Awareness of our product, pain points in current process,
feature importance, pricing sensitivity, purchase process and stakeholders
Survey length: Under 8 minutes / under 20 questions
Data use: Input for positioning refresh and sales collateral, shared with board
Platform: Typeform
Target sample: 150 complete responses
Prior surveys: No prior data, this is first structured market research effort
```

---

## Output Format

```
1. SURVEY BRIEF
   Research objectives mapped to survey sections.
   Total question count and estimated completion time.
   Skip logic map showing branching paths.

2. COMPLETE SURVEY INSTRUMENT
   Organized into logical sections with section headers.
   For each question:
   - Question text (neutral, unbiased wording)
   - Question type (single select, multi-select, Likert, open text, etc.)
   - Response options (for closed-ended questions)
   - Required vs. optional status
   - Skip logic instructions (if applicable)

3. SKIP LOGIC DOCUMENTATION
   A clear map of branching paths:
   "If Q5 = [option X], skip to Q9.
    If Q5 = [any other option], continue to Q6."

4. SCALE DOCUMENTATION
   All scales used with anchors defined.
   Confirmation that scale direction is consistent throughout.

5. PILOT TESTING CHECKLIST
   Questions to ask pilot testers.
   What to check during pilot: timing, comprehension, skip logic, missing options.

6. ANALYSIS PLAN
   For each question or question group: how the data will be analyzed
   and what it will be used to answer.
   Cross-tabulations planned (e.g., responses by company size segment).

7. DISTRIBUTION AND SAMPLING NOTES
   Recommended sample size with rationale.
   Recruitment source and method.
   Minimum response thresholds before analysis.
```

---

## Starter Prompt

```
You are a survey research methodologist helping me design a rigorous,
unbiased survey instrument.

Research objectives: [the 3 to 5 questions this survey must answer]
Target respondents: [who will take this survey and their key characteristics]
Topics and dimensions to cover: [the subject areas to measure]
Survey length target: [maximum time or question count]
How data will be used: [decisions or actions this will inform]
Existing questions or scales to include: [any required questions for benchmarking]
Segments to compare: [any subgroups that will be analyzed separately]
Platform: [survey tool being used]
Target response count: [how many complete responses are needed]

Please produce:
1. A complete survey instrument with all questions written in neutral, unbiased language
2. Correct question type specified for each question
3. All response options for closed-ended questions, including "other (please specify)"
   where appropriate
4. Required vs. optional designation for each question
5. A skip logic map showing all branching paths
6. A scale documentation table confirming consistent direction across all scales
7. An analysis plan mapping each question to the research objective it serves
8. A pilot testing checklist
9. Distribution and sampling notes

Review every question for: leading language, double-barreled construction,
jargon, assumption embedding, and scale direction errors.
Flag and rewrite any question with these problems.
If the number of questions needed to answer all objectives exceeds the time target,
recommend which questions to cut or combine.
```

---

## Related Skills

| Use This Next | Why |
|---|---|
| `screener-questionnaire.md` | Build a screener to qualify participants before the main survey |
| `research-synthesis-report.md` | Synthesize and report survey findings |
| `nps-analysis.md` | Specific guidance for NPS survey design and analysis |
| `primary-research-plan.md` | The survey sits within a broader research plan |

| Use This Before | Why |
|---|---|
| `customer-discovery-interview.md` | Qualitative interviews should precede survey design to inform question content |
| `market-segmentation.md` | Segmentation hypotheses should inform survey segment variables |

---

## Question Type Reference

| Question Type | Best For | Max Per Survey | Analysis Method |
|---|---|---|---|
| Single select | Categorical, one answer | No limit | Frequency distribution |
| Multi-select | Categorical, multiple answers | 5 to 8 | Frequency, co-occurrence |
| 5-point Likert | Attitudes, agreement | 15 to 20 total | Mean, distribution, crosstab |
| 1 to 10 rating | NPS, likelihood, overall rating | 3 to 5 | Mean, promoter/detractor split |
| Ranking | Relative priority | 3 to 5 items | Mean rank, top-2 analysis |
| Matrix/grid | Multiple items, same scale | 2 to 3 matrices of 5 to 7 items | Mean per item, heatmap |
| Short open text | Brief facts, labels | 2 to 3 | Categorization |
| Long open text | Rich qualitative context | 1 to 2 | Thematic coding |

---

*Skill file version: 1.0 | Phase: 01 - Ideation and Market Research | Company type: Product*
