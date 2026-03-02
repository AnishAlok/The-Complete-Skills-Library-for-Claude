# primary-research-plan.md

> **Skill:** Produces a complete primary research plan with clearly defined objectives, methodology selection, participant criteria, timeline, and success metrics for any market or user research initiative.

---

## TLDR

This skill helps you answer: *"How do we structure a research initiative so it actually answers the questions we need answered, with the right methods, the right participants, and enough rigor to trust the results?"* It produces a full research plan document used to align stakeholders before research begins, guide execution, and ensure the output is actionable. Used by product managers, UX researchers, market researchers, and strategists before any primary research effort.

---

## Topic Explanation

### What Is a Primary Research Plan?

Primary research is research you conduct directly, gathering new data from real people rather than synthesizing existing sources. It includes interviews, surveys, usability tests, focus groups, ethnographic studies, diary studies, and experiments.

A primary research plan is the strategic document that precedes execution. It answers: why are we doing this research, what exactly do we want to learn, how will we go about learning it, who will we talk to, when will we do it, and how will we know the research succeeded?

Without a research plan, research efforts tend to drift, produce data that cannot be synthesized, or answer questions no one needed answered. The plan is what converts a vague research impulse into a structured, defensible, and useful initiative.

### Research Plan vs. Research Script

These are two distinct documents that often get conflated:

**Research plan:** The strategic document. What are we studying, why, with what methods, who are participants, what is the timeline, what decisions will the output inform? Produced before research begins, shared with stakeholders for alignment.

**Research script/guide:** The tactical document. The specific questions, tasks, or protocols used during data collection. Produced after the plan is approved.

This skill covers the plan. Scripts and guides for specific methods are covered in `usability-test-script.md`, `focus-group-guide.md`, `customer-discovery-interview.md`, and related skills.

### Research Question vs. Interview Question

One of the most common research planning mistakes is confusing the research question with the interview question.

**Research question:** What does the team need to learn? Written at a strategic level.
Example: "What are the primary barriers preventing mid-market CFOs from adopting automated AP reconciliation tools?"

**Interview question:** What you actually ask a participant.
Example: "Walk me through the last time you evaluated a new financial software tool. What was that process like?"

The research plan contains research questions. The interview guide or survey contains the participant-facing questions. They should be clearly distinguished.

### Choosing the Right Research Method

Method selection depends on four factors:

**What you need to know:**
- Attitudes, motivations, mental models: qualitative methods (interviews, focus groups)
- Behaviors and frequencies: quantitative methods (surveys, analytics)
- Both: mixed methods

**How many people you need:**
- Small sample (5 to 30): qualitative (interviews, ethnographic)
- Large sample (100+): quantitative (survey, behavioral analytics)

**How much time and budget you have:**
- Fast and cheap: survey, remote interviews
- Slower and richer: ethnographic, diary studies, in-person usability

**How exploratory vs. confirmatory the research is:**
- Exploratory (what is going on): qualitative
- Confirmatory (how much, how many): quantitative

### The Research Plan Structure

A complete research plan has eight components:

1. **Background and context:** Why is this research being done now? What is the business situation that is driving the question?
2. **Research objectives:** What specific questions need to be answered? Stated as research questions, not interview questions.
3. **Method selection:** Which method(s) will be used and why these methods over alternatives?
4. **Participant criteria:** Who will participate? What are the screener criteria?
5. **Sample size and recruitment:** How many participants, from where, and how will they be recruited?
6. **Timeline:** When will each phase happen? Planning, recruitment, data collection, analysis, synthesis, readout?
7. **Roles and responsibilities:** Who is leading, who is supporting, who are the stakeholders?
8. **Output and decisions:** What will be produced? What decisions will it inform?

---

## When to Use This Skill

Use when:
- Beginning any primary research initiative regardless of method
- Aligning multiple stakeholders on what a research effort will and will not answer
- Requesting budget or resource approval for a research initiative
- Scoping a research project to ensure it is the right size for the question
- Onboarding a new researcher or team member to a research initiative
- Documenting research methodology for future reference or peer review

Do NOT use when:
- You are writing the actual interview guide or survey (use `customer-discovery-interview.md`, `survey-design.md`, or `focus-group-guide.md`)
- You are synthesizing research that has already been completed (use `research-synthesis-report.md`)
- You are doing secondary (desk) research, not primary (use `desk-research-synthesis.md`)

---

## Dos

- **Do start with the decision the research will inform.** Research that is not connected to a specific business or product decision often produces interesting findings nobody acts on. Name the decision upfront.
- **Do write research objectives as questions, not hypotheses.** "Why do mid-market CFOs avoid automation tools?" is an objective. "CFOs avoid automation because of implementation complexity" is a hypothesis. Research objectives should be genuinely open.
- **Do select the method after defining the objective.** Method selection driven by convenience ("we always do surveys") rather than by the research question produces the wrong kind of data.
- **Do define participant criteria precisely.** Vague participant criteria ("small business owners") produces a sample with too much variance to draw useful conclusions. Be specific about industry, role, company size, behavior, and experience level.
- **Do include a plan for what happens with the output.** Every research plan should specify what format the findings will take, who will receive them, when, and what decisions they will feed.
- **Do scope the research to the question, not to your available time.** A research plan that includes too many methods or too many questions produces data that cannot be synthesized in time to be useful.
- **Do get stakeholder sign-off on the plan before beginning.** Stakeholders who are not aligned on the research objectives will question the findings later. Alignment before research begins is far more efficient than debate after.
- **Do include what the research will NOT answer.** Explicitly scoping out-of-scope questions prevents scope creep during execution and manages stakeholder expectations.

---

## Donts

- **Dont write research objectives as "we want to learn about X."** "Learn about" is too vague. Replace with specific questions: "What are the top three barriers that prevent X from doing Y?"
- **Dont select participants who are too easy to recruit rather than right for the question.** Convenience sampling (using your existing customers, your employees, your network) produces biased data that confirms what you already believe.
- **Dont plan more research than you can synthesize.** 40 interviews with no analysis plan is not rigorous research. It is data hoarding. Plan analysis capacity before committing to sample size.
- **Dont confuse research objectives with business objectives.** "Increase conversion by 15%" is a business objective. "Understand what prevents users from completing the signup flow" is a research objective.
- **Dont plan research to validate decisions already made.** Research designed to confirm a conclusion rather than discover truth wastes resources and produces false confidence.
- **Dont skip the timeline.** Research without a timeline drifts indefinitely. Even a rough timeline forces the team to confront resource and sequencing constraints before they become blocking problems.
- **Dont write the plan alone.** The research plan should be reviewed by at least one stakeholder who will use the findings and one person who will execute the research. Both perspectives improve it.
- **Dont over-specify the methods before exploring alternatives.** Write down what you need to learn first. Then evaluate which method best answers that question, rather than defaulting to the familiar method.

---

## Ideal Inputs

### Required
```
1. THE BUSINESS OR PRODUCT CONTEXT
   What is happening in the business or product that is driving this research?
   What decision or problem is prompting the need?

2. THE CORE RESEARCH QUESTION(S)
   What specifically needs to be understood?
   Stated as open questions, not hypotheses.
   Limit to 3 to 5 core questions maximum.

3. THE DECISION THIS RESEARCH WILL INFORM
   What will be decided or changed based on what the research finds?
   Who is making that decision and when do they need the input?

4. THE TARGET PARTICIPANT TYPE
   Who should be in this research?
   What are the key characteristics: industry, role, behavior, experience, demographics?

5. CONSTRAINTS
   Timeline: when do findings need to be ready?
   Budget: what resources are available?
   Team capacity: who is available to run the research?
```

### Optional but Valuable
```
6. EXISTING KNOWLEDGE
   What do you already know about this question?
   What hypotheses does the team currently hold?
   What prior research exists that this builds on?

7. METHOD PREFERENCES OR CONSTRAINTS
   Are there methods that are off the table for practical reasons?
   Are there methods the team is particularly equipped to run well?

8. STAKEHOLDER LIST
   Who needs to be aligned on the research objectives?
   Who will receive the findings and in what format?

9. RELATED RESEARCH
   Is there related research happening simultaneously that should be coordinated?
   Are there research questions that overlap with other initiatives?

10. SENSITIVITY CONSIDERATIONS
    Are there topics in this research that require special ethical consideration?
    Are participants in a vulnerable population?
    Are there confidentiality or legal considerations?
```

### Example of a Strong Input Prompt
```
Business context: We are considering building a vendor risk management module
as an adjacent product for our existing compliance automation customers.
Before committing to an 8-month build, we want to understand whether there
is genuine demand and what form it should take.
Core research questions:
1. How do our existing customers currently manage vendor risk assessments?
2. What is most painful about their current approach?
3. What would they pay for a tool that addressed the pain?
4. What features are must-have vs. nice-to-have?
Decision: Go/no-go decision on building the vendor risk module, Q1 budget planning
Participants: Heads of compliance and CFOs at our existing customers who are
responsible for vendor risk. Secondary: same roles at non-customers in our ICP.
Constraints: Findings needed in 6 weeks, budget for 15 to 20 research sessions,
one researcher available 50% of their time
Existing knowledge: 6 customers have mentioned vendor risk in support tickets.
No structured research has been done. Team hypothesizes the pain is real but unknown
whether it is a must-have or nice-to-have.
```

---

## Output Format

```
1. RESEARCH PLAN HEADER
   Project name, date, version, lead researcher, stakeholders, status.

2. BACKGROUND AND CONTEXT (half page)
   The business situation driving this research.
   What is known and unknown going into the study.
   The hypothesis or assumption the research will test or explore.

3. RESEARCH OBJECTIVES
   The 3 to 5 core research questions this study will answer.
   Stated as open questions, not hypotheses.
   Explicitly noting what is OUT OF SCOPE.

4. DECISION THIS RESEARCH WILL INFORM
   The specific decision, investment, or action that depends on findings.
   The decision-maker and the timeline for the decision.

5. METHODOLOGY
   Selected method(s) with rationale for each.
   Why this method over alternatives for this question.
   If mixed methods: how qualitative and quantitative components will work together.

6. PARTICIPANT CRITERIA
   Detailed screener criteria for all participant types.
   Inclusion criteria: what makes someone right for this study.
   Exclusion criteria: who to leave out and why.
   Segmentation: if multiple participant types, how they differ.

7. SAMPLE SIZE AND RECRUITMENT PLAN
   How many participants per segment.
   Justification for sample size (qualitative saturation logic
   or quantitative statistical power logic as applicable).
   Recruitment source and method.
   Incentive structure.

8. TIMELINE
   Phase-by-phase schedule:
   Planning and screener development
   Recruitment
   Data collection
   Analysis and synthesis
   Findings readout
   With owner for each phase.

9. ROLES AND RESPONSIBILITIES
   Lead researcher, supporting researchers, note-takers,
   recruiting coordinator, stakeholders.
   Who attends sessions vs. who receives output only.

10. OUTPUT AND DELIVERABLES
    What will be produced: report format, presentation, recording library.
    Who receives findings and when.
    How findings will feed the decision being made.

11. ETHICAL CONSIDERATIONS
    Informed consent approach.
    Data storage and privacy.
    Any sensitivity considerations for the topic or population.
```

---

## Starter Prompt

```
You are a research strategist helping me build a complete primary research plan.

Business or product context: [what is happening that is driving this research]
Core research questions: [the 3 to 5 questions that need answering, as open questions]
Decision this will inform: [what will be decided or changed based on findings,
and when does the decision-maker need the input]
Target participant type: [who should be in this research, with specific criteria]
Timeline constraint: [when do findings need to be ready]
Budget and team capacity: [resources available]
Existing knowledge: [what is already known and what hypotheses exist]
Stakeholders: [who needs to be aligned and who receives findings]
Method preferences or constraints: [any methods that are required or off the table]
Sensitivity considerations: [any ethical or confidentiality factors]

Please produce a complete primary research plan including:
1. Background and context
2. Three to five specific research objectives as open questions, plus explicit out-of-scope list
3. The specific decision this research will inform and who makes it
4. Methodology selection with rationale and comparison to alternatives
5. Detailed participant criteria including inclusion and exclusion
6. Sample size with justification and recruitment plan
7. Phase-by-phase timeline with owners
8. Roles and responsibilities
9. Output and deliverables with format and distribution plan
10. Ethical considerations

Flag immediately if the research questions are too broad to answer in the available
time and budget. Recommend scoping adjustments if needed.
If the method I have implied is not the best fit for the research question, say so
and recommend a better one.
```

---

## Related Skills

| Use This Next | Why |
|---|---|
| `customer-discovery-interview.md` | Build the interview guide for qualitative sessions in the plan |
| `survey-design.md` | Build the survey instrument for quantitative components |
| `focus-group-guide.md` | Build the moderator guide if focus groups are selected |
| `screener-questionnaire.md` | Build the participant screener defined in the plan |
| `research-synthesis-report.md` | Synthesize findings once data collection is complete |

| Use This Before | Why |
|---|---|
| `desk-research-synthesis.md` | Secondary research should be completed before designing primary research |
| `market-opportunity-analysis.md` | Market analysis may reveal gaps that primary research should fill |

---

## Reference Frameworks

| Framework | Use For |
|---|---|
| Double Diamond (Design Council) | Framing where primary research sits in the discovery process |
| Research Question Hierarchy | Distinguishing business objectives from research objectives from interview questions |
| Theoretical Saturation (Glaser and Strauss) | Determining qualitative sample size: keep recruiting until no new themes emerge |
| Mixed Methods Research (Creswell) | Structuring studies that combine qualitative and quantitative components |
| CONSORT/STROBE Reporting Standards | Rigor frameworks for quantitative and observational research planning |

---

*Skill file version: 1.0 | Phase: 01 - Ideation and Market Research | Company type: Product*
