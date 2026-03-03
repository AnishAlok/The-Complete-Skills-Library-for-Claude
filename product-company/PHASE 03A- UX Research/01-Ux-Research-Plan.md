# ux-research-plan.md

> **Skill:** Produces a complete UX research plan with defined goals, method selection rationale, participant criteria, timeline, and stakeholder alignment structure for any user experience research initiative.

---

## TLDR

This skill helps you answer: *"What do we need to learn about users, how will we learn it, and how do we make sure the right people are aligned before we start?"* It produces a structured UX research plan that ties research goals to product decisions, selects appropriate methods, defines participant criteria, and maps a realistic timeline. Used before any UX research initiative regardless of method.

---

## Topic Explanation

### UX Research Plan vs. Primary Research Plan

The primary research plan skill (`primary-research-plan.md`) covers market and customer research broadly. This skill is specific to UX research: research that studies how people interact with, experience, or would experience a product interface, workflow, or service. The UX research plan has additional considerations:

- **Design artifacts:** UX research often involves showing prototypes, wireframes, or live products as stimuli
- **Interaction observation:** UX research frequently involves observing task performance, not just attitudes
- **Design decision connection:** Every UX research goal should map to a specific design decision pending
- **Iterative cadence:** UX research often runs in rapid cycles tied to sprints or design reviews

### Research Goals and Design Decisions

The most important discipline in UX research planning is connecting every research goal to a specific design decision. Research without a pending decision produces insight that has nowhere to land.

Good UX research goal format: "Understand whether users can navigate from dashboard to report generation without assistance, so we can decide whether the navigation structure needs to change before Q2 release."

Bad format: "Understand user experience of reporting."

The difference is the decision clause: "so we can decide whether..." Every goal needs one.

### Choosing Between Generative and Evaluative Research

**Generative research** (discovery phase): Aimed at understanding user needs, mental models, and behaviors before or without a specific design solution. Methods: contextual inquiry, diary studies, jobs-to-be-done interviews, field studies.

**Evaluative research** (validation phase): Aimed at assessing whether a specific design solution works. Methods: usability tests, cognitive walkthroughs, expert reviews, A/B tests.

Most teams over-invest in evaluative research and under-invest in generative. The best time to do generative research is before committing to a design direction. Evaluative research after a wrong direction is expensive.

### UX Research Methods Quick Reference

| Method | Type | Sample Size | Time | Best For |
|---|---|---|---|---|
| Usability testing (moderated) | Evaluative | 5 to 8 | Days | Finding task barriers in a specific flow |
| Usability testing (unmoderated) | Evaluative | 20 to 50 | Hours | Quantifying task completion at scale |
| Contextual inquiry | Generative | 5 to 10 | Weeks | Understanding real-world work context |
| Diary study | Generative | 10 to 20 | Weeks | Longitudinal behavior and experience |
| Card sorting | Generative | 15 to 30 | Days | IA and navigation structure |
| Tree testing | Evaluative | 50 to 100 | Days | Validating navigation structure |
| Cognitive walkthrough | Evaluative | Researcher only | Hours | Identifying learnability barriers |
| Expert review / heuristic evaluation | Evaluative | 3 to 5 experts | Hours | Rapid issue identification |
| First-click testing | Evaluative | 50 to 100 | Hours | Navigation and labeling clarity |
| Concept testing | Evaluative | 8 to 15 | Days | Reactions to design concepts |
| Benchmark study | Evaluative | 20 to 50 | Weeks | Tracking UX quality over time |

---

## When to Use This Skill

Use when:
- Beginning any UX research initiative regardless of method
- A design team is starting a new product area and needs to establish a research approach
- Stakeholders need alignment on what a research effort will and will not answer
- Requesting research resources or team capacity from leadership
- Onboarding a new UX researcher to an existing product area

Do NOT use when:
- Writing the specific script or guide for a single method (use `usability-test-script.md`, `contextual-inquiry.md`, etc.)
- Synthesizing research already completed (use `research-synthesis-report.md`)
- Doing market or customer research unrelated to product design (use `primary-research-plan.md`)

---

## Dos

- **Do connect every research goal to a pending design decision.** If you cannot name the decision, reconsider whether the research is needed now.
- **Do select methods after goals, not before.** Method selection based on habit ("we always do usability tests") rather than research goal produces the wrong kind of data.
- **Do include a risk assessment.** What happens to the design timeline if research takes longer than planned? What is the minimum viable learning if the full plan cannot run?
- **Do build in a stakeholder review checkpoint.** Research plans that stakeholders have not seen before execution produce friction when findings land.
- **Do plan for analysis time.** Research plans that allocate all time to data collection and none to analysis produce raw data that never becomes insight.
- **Do specify what "done" looks like.** What artifacts will the research produce? When? For which audience?

---

## Donts

- **Dont run research to justify a decision already made.** Confirmation research is not UX research.
- **Dont recruit participants from your internal team.** Internal users have too much product knowledge and too much social motivation to be helpful.
- **Dont plan research without accounting for recruiting time.** Qualified participant recruitment takes longer than most designers expect: typically 1 to 2 weeks minimum.
- **Dont combine multiple methods into one session without careful design.** A 90-minute session that includes an interview, a usability test, and a card sort asks too much of participants and produces diluted data from each method.

---

## Ideal Inputs

```
1. PRODUCT OR FEATURE CONTEXT
   What product area, feature, or design problem is this research about?
   What is the current design state?

2. OPEN DESIGN DECISIONS
   What specific decisions are pending that research should inform?
   What are the hypotheses or uncertainties?

3. USER TYPE
   Who are the users being studied?
   What role, behavior, experience level, or context defines them?

4. CONSTRAINTS
   Timeline: when must research findings land?
   Budget: what is available for recruiting, tools, incentives?
   Team: who is available to plan, facilitate, and analyze?

5. EXISTING KNOWLEDGE
   What is already known about this user group or problem?
   What prior research exists?
```

---

## Output Format

```
1. RESEARCH PLAN HEADER
   Project title, date, version, lead researcher, product area, status.

2. CONTEXT AND BACKGROUND
   The product situation driving this research.
   Current design state: what exists vs. what is being designed.
   Prior research that informs this plan.

3. RESEARCH GOALS AND DECISION MAPPING
   For each goal (3 to 5 maximum):
   - Goal statement
   - The design decision it will inform
   - What a confirming finding looks like
   - What a disconfirming finding looks like

4. OUT OF SCOPE
   Explicit list of questions this research will NOT answer.

5. METHODOLOGY
   Selected method(s) with rationale.
   Why this method over alternatives for this goal.

6. PARTICIPANT CRITERIA
   Target user description.
   Inclusion and exclusion criteria.
   Segmentation if multiple participant types.
   Sample size with justification.

7. MATERIALS AND STIMULI
   What will participants interact with? (Prototype, live product, concept)
   Fidelity level and preparation requirements.

8. TIMELINE
   Recruiting start and end.
   Session dates.
   Analysis period.
   Findings delivery.
   Owner for each phase.

9. ROLES AND RESPONSIBILITIES
   Facilitator, note-taker, observer protocol, stakeholder involvement.

10. DELIVERABLES
    What will be produced, for whom, in what format, by when.
```

---

## Starter Prompt

```
You are a UX research strategist helping me produce a complete UX research plan.

Product or feature context: [what is being designed or investigated]
Open design decisions: [what decisions are pending that research should inform]
User type: [who will be studied and their key characteristics]
Timeline constraint: [when findings must land]
Budget and team: [resources available]
Existing knowledge: [what is already known]
Prior research: [any existing research on this area]

Please produce a complete UX research plan including:
1. Research goals mapped to specific design decisions
2. Explicit out-of-scope statement
3. Method selection with rationale and comparison to alternatives
4. Participant criteria with inclusion and exclusion criteria and sample size justification
5. Materials and stimuli requirements
6. Timeline with owners for each phase
7. Roles and responsibilities
8. Deliverables specification

For every research goal, include the design decision it serves and what both
confirming and disconfirming findings would look like.
Flag any goal where the decision is not yet clear and recommend clarifying
before research begins.
```

---

## Related Skills

| Use This Next | Why |
|---|---|
| `usability-test-plan.md` | If usability testing is selected, develop the detailed test plan |
| `screener-questionnaire.md` | Build the participant screener defined in the plan |
| `contextual-inquiry.md` | If contextual inquiry is selected, build the field protocol |
| `research-brief.md` | Distill the plan into a stakeholder-facing brief |
| `participant-consent-form.md` | Prepare consent documentation for the sessions |

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
