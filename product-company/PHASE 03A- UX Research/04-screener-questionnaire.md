# screener-questionnaire.md

> **Skill:** Produces a participant screener questionnaire that identifies and qualifies research participants who match study criteria while filtering out those who do not, including routing logic and recruiter instructions.

---

## TLDR

This skill helps you answer: *"How do we make sure we talk to the right people and not waste research sessions on participants who do not represent our target users?"* It produces a screener questionnaire with qualification criteria, routing logic, and recruiter guidance for any UX or market research study.

---

## Topic Explanation

### Why Screener Design Is Strategically Critical

The screener is the most undervalued document in research planning. Poor screener design produces participants who are the wrong people, regardless of how excellent the subsequent research protocol is. The three most common screener failures:

**Over-screening:** Criteria so specific that recruiting takes months or no participants pass. Common when researchers try to replicate their ideal customer in every participant.

**Under-screening:** Criteria so loose that sessions are filled with participants who lack the experience, role, or context to produce valid data.

**Screening for answers, not criteria:** Questions that reveal the "right" answers to participants, allowing them to game the screener to qualify. This is particularly common with attitudinal screeners.

### Qualification Logic

A screener has three routing outcomes for each question:

**Must qualify (include):** Participant must have this characteristic to be in the study.
Example: Must currently use payroll software at work.

**Must disqualify (exclude):** If the participant has this characteristic, they should not be in the study.
Example: Must not work for a payroll software company (competitive intelligence risk) or must not have participated in research in the past 6 months (panel fatigue).

**Stratification (segment):** Characteristic used to sort participants into different groups for the study, rather than include or exclude them.
Example: Route participants with 1 location to Group A, participants with 2 or more locations to Group B.

### Professional Respondent Detection

Survey panels and research recruitment platforms have a chronic problem with professional respondents: people who sign up for studies to collect incentives and who know how to answer screeners to qualify. Techniques for detecting and filtering them:

**Red herring question:** Include a question with an obvious wrong answer. If the participant gets it wrong, flag them.
Example: "Which of the following is NOT a spreadsheet application? (Excel / Google Sheets / PowerPoint / Numbers)" If they choose anything other than PowerPoint, flag the response.

**Specificity trap:** Ask for specific details that a non-genuine respondent cannot fake.
Example: "What is the name of the payroll software your company currently uses?" Accept only named responses; reject "I don't know" or generic answers.

**Inconsistency detection:** Ask the same question in two different ways and compare answers.

**Recent participation filter:** "Have you participated in a paid research study in the past 3 months?" Participants who say no but have recently participated multiple times are filtering out themselves from over-researched panels.

---

## When to Use This Skill

Use when:
- Recruiting participants for any primary research study (interviews, usability tests, surveys, focus groups)
- Working with a recruitment agency and needing to provide screener criteria
- Building a self-serve screener on a form platform for inbound recruitment
- Validating that existing customers qualify for a specific study design

Do NOT use when:
- Participants are pre-identified and do not need to be screened (e.g., specific named customers invited to participate)
- The study does not have clear participant criteria (clarify the research plan first)

---

## Dos

- **Do write screener questions in lay language, not research terminology.** Screener participants have not agreed to participate yet. Complex or jargon-heavy questions create drop-off.
- **Do put disqualifying questions early.** Do not waste a participant's time by asking 10 questions before getting to the one that disqualifies them.
- **Do include at least one specificity question.** "What software do you use?" is more specific than "Do you use software?" The specificity requirement filters out non-genuine respondents.
- **Do tell the recruiter what a complete, qualified respondent looks like.** The screener is a document for the recruitment process, not just a form for participants.
- **Do randomize answer options for attitudinal questions.** Fixed order creates response bias. Randomize options so different participants see different orders.
- **Do include screening for competitive employment.** Anyone who works for a direct competitor should typically be excluded for confidentiality reasons.

---

## Donts

- **Dont reveal what answers will qualify.** "Do you regularly manage payroll for your company?" reveals that "yes" is the qualifying answer. Better: "Which of the following best describes your involvement in payroll at your company?" with multiple options.
- **Dont screen out participants who admit limitations.** Screening for only the most experienced users produces a sample that does not represent typical users.
- **Dont use leading language in demographic questions.** Avoid language that implies desirable vs. undesirable answers.
- **Dont make the screener longer than 10 to 12 questions.** Long screeners reduce completion rate and signal to genuine participants that the study will be demanding.

---

## Ideal Inputs

```
1. STUDY TYPE AND CONTEXT
   What research method is this screener for?
   What product, feature, or topic is being researched?

2. PARTICIPANT CRITERIA FROM THE RESEARCH PLAN
   Required characteristics (must have).
   Exclusion criteria (must not have).
   Segment splits (if multiple participant types).

3. PARTICIPANT SOURCE
   External recruitment panel? Existing customer list?
   Inbound form? Recruiter agency?

4. QUOTA REQUIREMENTS
   Total number of participants needed.
   Any splits by segment (e.g., 5 from each of two groups).

5. INCENTIVE AND LOGISTICS
   What incentive is being offered?
   Session format (remote/in-person) and approximate duration.
```

---

## Output Format

```
1. SCREENER HEADER
   Study code (not the real study title), session length, incentive,
   format (remote/in-person), scheduling instructions.
   Recruiter quota table.

2. INTRODUCTION TEXT
   Brief, honest description of the study purpose (without revealing the focus).
   Time required to complete the screener.
   Incentive offer.

3. SCREENER QUESTIONS
   For each question:
   - Question text
   - Answer options
   - Routing instruction: [QUALIFY] / [DISQUALIFY] / [CONTINUE] / [ROUTE TO GROUP X]

4. PROFESSIONAL RESPONDENT DETECTION QUESTIONS
   Red herring question.
   Specificity requirement question.
   Recent participation filter.

5. QUALIFIED RESPONDENT PROFILE
   A description of what a complete, qualified participant looks like.
   For recruiter reference.

6. THANK AND RELEASE LANGUAGE
   Standard decline text for disqualified participants.
   Next steps language for qualified participants.

7. DATA COLLECTION QUESTIONS (optional)
   Demographic questions for analysis purposes only (not screening).
   Placed at end, all optional.
```

---

## Starter Prompt

```
You are a research recruitment specialist designing a participant screener.

Study type and context: [what method and what product/topic]
Required participant characteristics: [must-have criteria]
Exclusion criteria: [must-not-have criteria]
Segment splits: [if multiple participant groups]
Participant source: [recruitment panel / existing customers / inbound form]
Total quota: [how many participants needed and any segment splits]
Incentive and session details: [incentive, length, format]

Please produce a complete screener questionnaire including:
1. Recruiter-facing header with quota table
2. Introduction text for participants
3. All screener questions with routing logic labeled [QUALIFY] / [DISQUALIFY] / [CONTINUE]
4. Professional respondent detection questions
5. Qualified respondent profile for recruiter reference
6. Thank and release language for disqualified participants

Do not reveal qualifying answers in the question wording.
Place disqualifying questions before time-consuming qualification questions.
Flag any criterion that may be difficult to screen for reliably and suggest alternatives.
```

---

## Related Skills

| Use This Next | Why |
|---|---|
| `participant-consent-form.md` | Prepare consent documentation for qualified participants |
| `usability-test-plan.md` | The screener criteria come from the test plan |
| `focus-group-guide.md` | Focus groups also require participant screeners |

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
