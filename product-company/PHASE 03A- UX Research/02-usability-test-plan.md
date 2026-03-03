# usability-test-plan.md

> **Skill:** Produces a detailed usability test plan including task design, scenario writing, success metrics, session logistics, and analysis framework for moderated or unmoderated usability testing.

---

## TLDR

This skill helps you answer: *"Can users actually accomplish what we need them to accomplish with this design, and where do they get stuck?"* It produces a structured usability test plan with task scenarios, success and failure criteria, measurable metrics, session logistics, and an analysis framework. Used before a moderated or unmoderated usability test to ensure the test is rigorous and produces actionable findings.

---

## Topic Explanation

### What a Usability Test Is (and Is Not)

A usability test is a method for evaluating a product or prototype by observing representative users attempting to complete real tasks. It is not:

- A demo (you are not showing users how the product works)
- A focus group (you are not asking for opinions)
- A training session (you are not teaching users how to use the product)
- A preference test (you are not asking which design they like better)

The core activity is observation: watching what users actually do when they try to accomplish a task, not what they say they would do.

### The Five Usability Dimensions (Nielsen)

Jakob Nielsen's five quality components of usability provide the measurement framework for a well-designed usability test:

**Learnability:** How easy is it for first-time users to accomplish basic tasks?
**Efficiency:** Once learned, how quickly can users complete tasks?
**Memorability:** When returning after a break, how easily is proficiency restored?
**Errors:** How many errors do users make, how severe are they, and how easily can they recover?
**Satisfaction:** How pleasant is the experience?

Most usability tests focus primarily on learnability and errors. Include efficiency and satisfaction only when those dimensions are explicitly relevant to a design decision.

### Task Design: The Most Critical Skill

Task design is what most separates rigorous usability tests from useless ones.

**Good tasks:**
- Describe a realistic scenario, not an instruction to find a feature
- Have a clear, verifiable completion state
- Do not contain the words used to label the interface elements
- Are based on real user goals, not UI terminology

Bad task: "Click on the 'Reports' tab and create a new compliance report."
(This is a navigation instruction, uses UI labels, and tells the user exactly what to do.)

Good task: "You need to give your accountant a summary of tip credit calculations for last month. Please do that."
(This is a realistic goal, uses the user's language, and has a clear completion state without prescribing the path.)

### Sample Size for Usability Testing

Nielsen's research established that 5 participants uncover approximately 85% of usability problems in moderated testing with a homogeneous user population. This guidance has been widely replicated and is the foundation of lean usability testing.

Practical guidance:
- Moderated, homogeneous population: 5 to 8 participants
- Moderated, 2 distinct user types: 5 per type (10 total)
- Unmoderated quantitative: 20 to 50 participants per condition
- Benchmark study requiring statistical comparison: 50+ per condition

The "5 is enough" guidance applies to finding problems. It does not apply to measuring task completion rates with statistical confidence, which requires larger samples.

### Moderated vs. Unmoderated Testing

**Moderated:** A facilitator guides participants through tasks in real time. Allows probing, follow-up questions, and observation of non-verbal behavior. Higher fidelity. More resource-intensive. Required for complex tasks, early-stage prototypes, and when participants may need clarification.

**Unmoderated:** Participants complete tasks independently via a testing platform (UserTesting, Maze, Lookback). Higher scale, lower cost, faster turnaround. Best for testing clear, discrete tasks on higher-fidelity designs. Cannot probe or adapt in real time.

---

## When to Use This Skill

Use when:
- A specific design or prototype needs to be tested before development or release
- A redesign is complete and needs validation before launch
- Post-launch, a specific flow is producing high drop-off or support volume
- Comparing two or more design alternatives for a specific task

Do NOT use when:
- No prototype or product exists yet (do generative research first)
- The goal is to understand user needs rather than evaluate a design (use contextual inquiry or interviews)
- The test would require more than 90 minutes per participant (split into multiple sessions)

---

## Dos

- **Do write tasks as scenarios, not instructions.** Frame the user's goal, not the steps to achieve it.
- **Do define success criteria before the sessions begin.** What does task completion look like? What counts as a failure? What counts as partial success?
- **Do include a think-aloud protocol.** Ask participants to narrate their thoughts as they work. This is the richest source of qualitative data in usability testing.
- **Do run a pilot session.** The first session with a real participant almost always reveals task wording problems. Run one pilot before your data collection sessions.
- **Do measure time on task.** Even if efficiency is not the primary metric, time on task is a useful indicator of friction and enables before/after comparison.
- **Do distinguish between critical and minor issues.** A severity rating framework applied during analysis prevents every finding from getting equal weight.

---

## Donts

- **Dont use UI labels in task descriptions.** If the task mentions the button or tab name, you are testing recognition, not usability.
- **Dont help participants during tasks.** If a participant is struggling, the struggle is the data. Note it and resist the urge to assist.
- **Dont recruit participants who know your product too well.** Existing power users have adapted to your current design. They will not represent new users or users with normal exposure.
- **Dont test more than 5 to 7 tasks per session.** More than that causes fatigue and reduces data quality in later tasks.
- **Dont include leading tasks.** Tasks should not imply that a feature is easy, obvious, or expected. Neutral language throughout.

---

## Ideal Inputs

```
1. THE DESIGN TO BE TESTED
   What prototype, mockup, or live product will participants interact with?
   What is the fidelity level?

2. THE USER TASKS TO TEST
   What flows or features are in scope?
   What are users trying to accomplish with these flows?

3. THE DESIGN QUESTIONS TO ANSWER
   What specific issues or hypotheses does this test address?

4. TARGET USER TYPE
   Who should participate?
   What experience, role, or behavioral criteria define them?

5. MODERATED OR UNMODERATED
   Is this moderated (real-time facilitation) or unmoderated (self-guided)?
   What drives that choice?

6. TIMELINE AND LOGISTICS
   When do sessions need to run?
   In-person, remote, or either?
   Session length budget.
```

---

## Output Format

```
1. TEST PLAN HEADER
   Study name, date, lead, design being tested, method (moderated/unmoderated).

2. RESEARCH QUESTIONS
   The specific usability questions this test will answer.

3. PARTICIPANT CRITERIA
   Inclusion/exclusion criteria, sample size, segment breakdown.

4. TASK LIST WITH SCENARIOS
   For each task (5 to 7 maximum):
   - Scenario context (1 to 2 sentences)
   - Task statement (what the participant is asked to do)
   - Success criteria (what completion looks like)
   - Failure criteria (what non-completion looks like)
   - Time-on-task target (if efficiency is being measured)
   - Observation focus (what to watch for)

5. METRICS AND MEASUREMENT
   Task completion rate per task.
   Error rate per task.
   Time on task per task.
   Satisfaction scale (post-task and post-session).
   Severity rating scale for issues found.

6. SESSION STRUCTURE
   Introduction (consent, think-aloud briefing).
   Warm-up questions.
   Task sequence.
   Post-session interview questions.
   Total session length with time allocation per section.

7. MATERIALS REQUIRED
   Prototype or product state required.
   Testing environment setup.
   Recording and consent setup.
   Any supporting materials participants need.

8. ANALYSIS FRAMEWORK
   How issues will be identified and logged.
   Severity rating criteria.
   How findings will be prioritized.
   Deliverable format and timeline.
```

---

## Starter Prompt

```
You are a UX research specialist helping me design a rigorous usability test plan.

Design to be tested: [prototype, mockup, or live product and fidelity level]
User tasks in scope: [the flows or features being tested]
Design questions to answer: [specific usability questions or hypotheses]
Target user type: [participant criteria]
Method: [moderated / unmoderated and rationale]
Session length budget: [maximum time per participant]
Timeline: [when sessions need to run]

Please produce a complete usability test plan including:
1. Research questions mapped to design decisions
2. Participant criteria with sample size justification
3. Task scenarios written as realistic goals, not instructions, with success and failure criteria
4. Metrics and measurement approach
5. Session structure with time allocations
6. Materials requirements list
7. Analysis framework with severity rating criteria

Review every task scenario and flag any that use UI labels,
contain implicit instructions, or lack a verifiable completion state.
```

---

## Related Skills

| Use This Next | Why |
|---|---|
| `usability-test-script.md` | Write the moderator script for the sessions |
| `screener-questionnaire.md` | Build the participant screener |
| `research-synthesis-report.md` | Document findings after sessions complete |
| `heuristic-evaluation.md` | Complement usability testing with an expert review |

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
