# ethnographic-research.md

> **Skill:** Designs and documents ethnographic field study protocols, observation frameworks, and contextual inquiry guides for understanding how people work, live, and behave in their natural environment.

---

## TLDR

This skill helps you answer: *"What do people actually do in their real context, as opposed to what they say they do when interviewed?"* It produces a field study protocol, observation guide, contextual inquiry framework, and synthesis structure for ethnographic and naturalistic research. Used when the gap between stated behavior and actual behavior is strategically important, when context shapes behavior in ways interviews cannot capture, or when you need to discover problems people do not yet know they have.

---

## Topic Explanation

### What Is Ethnographic Research?

Ethnographic research is a qualitative methodology originating in anthropology, in which a researcher immerses themselves in the natural environment of the people being studied to observe and understand behavior, culture, and context firsthand. In product and market research, it is adapted into field studies and contextual inquiries where researchers observe users or customers in their real work or life environments rather than in a lab or interview room.

The defining characteristic of ethnographic research is naturalistic observation: watching what people actually do rather than asking them to describe or remember it. This matters because human beings are remarkably poor at accurately describing their own behavior, especially habitual behavior they do not consciously notice.

### Why Ethnographic Research Produces Different Insight Than Interviews

Interviews produce self-reported behavior. Ethnographic observation produces observed behavior. The gap between the two is often where the most important product and strategy insights live.

Classic example: When asked, office workers say they spend most of their time on productive work. Observed in their natural environment, they spend significant time on workarounds, informal communication, error recovery, and shadow systems (personal spreadsheets, sticky note systems) that they have built because the official tools do not meet their actual needs. None of this appears in interview data because people do not consciously register their workarounds as "work."

For product teams, ethnographic research is the method most likely to surface:
- Workarounds and shadow systems that signal unmet needs
- Handoffs and collaboration patterns that software rarely supports well
- Environmental and contextual factors that shape behavior in unexpected ways
- The social and organizational context of tool use (who watches, who approves, who complains)
- The difference between how a tool is designed to be used and how it is actually used

### Contextual Inquiry

Contextual inquiry (CI), developed by Karen Holtzblatt and Hugh Beyer, is a structured approach to field research designed specifically for product and software research. It is the most commonly used ethnographic method in UX and product research.

CI has four guiding principles:

**Context:** Go to the user's actual work environment. Observe during real work, not simulated work.

**Partnership:** The researcher and participant work together as master and apprentice. The participant is the expert on their own work. The researcher is the curious learner.

**Interpretation:** Share interpretations in the moment. "It looks like you went back to the spreadsheet because the tool doesn't give you what you need. Is that right?" Interpretations checked in-session are more accurate than interpretations made after.

**Focus:** Have a research focus. You are not observing everything indiscriminately. You have research questions that guide which behaviors and moments receive attention.

### Observation Frameworks

**AEIOU Framework:**
A structured observation protocol that directs attention to five categories:
- **A**ctivities: What are people doing? What goals are they trying to accomplish?
- **E**nvironments: What is the physical and organizational space like? How does it enable or constrain behavior?
- **I**nteractions: What interactions happen between people? Between people and tools?
- **O**bjects: What physical and digital objects are part of the activity? What tools, documents, devices?
- **U**sers: Who are the people involved? What roles do they play? What are their characteristics and attitudes?

**Experience Sampling:**
Participants are prompted at random intervals to record what they are doing, thinking, and feeling. This produces naturalistic data without the researcher needing to be present continuously. Useful for longitudinal studies.

**Shadowing:**
The researcher follows a participant through their full workday or a defined activity period, observing without intervening. More intensive than a contextual inquiry session. Used when the full flow of work (not just a specific task) is the research subject.

### Ethical Considerations in Ethnographic Research

Ethnographic research raises specific ethical considerations:
- Participants must give informed consent to observation
- The researcher's presence changes behavior (the observer effect). This must be acknowledged in analysis.
- Participants may reveal sensitive information or behaviors during observation that must be handled with care
- Third parties (colleagues, customers) who appear in observations may not have consented
- Data storage and privacy protections must be clearly defined before research begins

---

## When to Use This Skill

Use when:
- You need to understand how work actually happens rather than how people describe it
- You have discovered workarounds or shadow systems through interviews and want to observe them directly
- You are designing a product for a complex workflow that cannot be described accurately without observation
- The context of use is a critical factor (industrial settings, hospital environments, restaurant kitchens, field work)
- Prior interview research has produced contradictory or surprising self-reported behavior
- You are entering a market you do not know well and need to understand the full work context before building

Do NOT use when:
- The behavior in question is private and cannot be observed with consent
- The research question is primarily attitudinal (use interviews or surveys)
- Budget and timeline do not allow for field research (minimum viable ethnographic study requires meaningful time in the field)
- The participant population is geographically scattered and remote observation is not feasible
- You already have strong observational data and need quantitative validation (use `survey-design.md`)

---

## Dos

- **Do observe during real work, not a staged demonstration.** Ask to join a participant during work that would happen whether you were there or not. Staged demonstrations produce idealized behavior, not real behavior.
- **Do take notes on what you see, not what you interpret.** Observation notes should be factual and descriptive. Interpretation belongs in a separate column or section. "Participant opened a new spreadsheet and copied data from the tool" is an observation. "Participant finds the tool insufficient" is an interpretation.
- **Do share interpretations in the moment.** Contextual inquiry's most powerful technique is checking your interpretation with the participant immediately. "You seem to be checking this twice. Is there a reason?" produces more accurate data than guessing later.
- **Do photograph and diagram the environment with consent.** Physical layout, tool arrangements, sticky note systems, whiteboard content, and desk organization are rich ethnographic data that field notes alone cannot capture.
- **Do note workarounds immediately when you see them.** Workarounds (participants solving problems the official tool does not solve) are the most strategically valuable ethnographic finding. Document each one with detail.
- **Do debrief with the participant after observation.** Use 15 to 20 minutes at the end to ask about specific things you observed, clarify interpretations, and ask what was not typical about today.
- **Do acknowledge the observer effect in your analysis.** Your presence changes behavior. Note when participants appeared to be performing versus when they seemed to have forgotten you were there.
- **Do produce field notes within 24 hours of each session.** Memory of observational detail degrades rapidly. Clean and expand notes the same day.

---

## Donts

- **Dont intervene during observation.** If a participant is struggling with a tool, resist the urge to help. The struggle is the data. Note it, do not solve it.
- **Dont ask too many questions during observation.** Frequent questions interrupt the natural flow of work and shift the session from observation to interview. Save most questions for the debrief.
- **Dont observe only the "happy path."** Seek out edge cases, errors, recovery behaviors, and non-standard situations. The interesting data is often in how things go wrong.
- **Dont assume your interpretation is correct.** Check every interpretation with the participant. What looks inefficient from the outside may have a logic that only makes sense in context.
- **Dont use a rigid script.** An observation session is not an interview. The guide is a focus and orientation tool, not a sequence to follow rigidly. Follow what is interesting.
- **Dont neglect the social and organizational context.** Who else is involved in this work? Who does the participant check with? What approvals are needed? Social context is as important as task behavior.
- **Dont lose the verbatim language.** When participants use specific words to describe their work, pain, or tools, capture those words exactly. Paraphrasing loses the vocabulary data.
- **Dont conduct only one session per participant type.** A single observation is a data point. Pattern recognition requires multiple sessions across multiple participants to distinguish individual idiosyncrasies from shared behavioral patterns.

---

## Ideal Inputs

### Required
```
1. RESEARCH OBJECTIVES
   What specific behaviors, workflows, or contextual factors need to be understood?
   Stated as open research questions.

2. PARTICIPANT TYPE
   Who will be observed?
   What role do they play in the work being studied?
   What are the qualification criteria?

3. WORK OR ACTIVITY TO BE OBSERVED
   What specific activity, task, or work period will be observed?
   How long does a typical instance last?

4. RESEARCH CONTEXT
   What is the physical environment where observation will take place?
   (Office, factory floor, restaurant kitchen, home, retail location)

5. PRIOR KNOWLEDGE
   What is already known about how this work is done?
   What hypotheses or surprises from prior research should be examined?
```

### Optional but Valuable
```
6. SPECIFIC BEHAVIORS TO FOCUS ON
   Are there particular moments, transitions, or behaviors
   that are highest priority to observe?

7. TOOLS OR SYSTEMS IN USE
   What tools, software, or physical objects are part of the work?
   Are there specific tools whose use is of interest?

8. STAKEHOLDERS AND ENVIRONMENT
   Who else is present during the work?
   What organizational dynamics are relevant?

9. NUMBER OF SESSIONS
   How many observation sessions are planned?
   Across how many different participants and locations?

10. REMOTE OR IN-PERSON
    Will observation be in-person or conducted remotely
    via screen share or video?
```

### Example of a Strong Input Prompt
```
Research objectives:
1. How do restaurant operators actually run their weekly payroll process end to end?
2. Where do errors, delays, and workarounds occur?
3. What systems, tools, and people are involved that we have not captured in interviews?
4. How does the physical and operational context (during service vs. before service)
   affect when and how payroll work happens?
Participant type: Independent restaurant owners or managers who currently run payroll
themselves, 1 to 3 locations, any current payroll approach
Activity to observe: The weekly payroll processing cycle from hours verification
through payment confirmation
Environment: Restaurant back-of-house office, or home if owner manages remotely
Prior knowledge: Interviews reveal 3 to 4 hours per week, spreadsheet heavy,
anxiety about tip credit compliance. We have not observed the actual process.
Specific focus: Workarounds, shadow systems, interruptions, compliance checks
Number of sessions: 6 sessions across 6 different operators
Format: In-person preferred, remote screen share if in-person not possible
```

---

## Output Format

```
1. RESEARCH PROTOCOL HEADER
   Study title, objectives, participant type, activity scope, session length,
   number of sessions planned, format (in-person / remote).

2. PARTICIPANT SCREENER
   Qualification criteria for observation participants.
   Scheduling and consent requirements.
   Pre-session instructions for participant.

3. CONSENT AND SETUP PROTOCOL
   Informed consent language for observation and recording.
   Setup instructions: recording equipment, note-taking arrangement,
   environment permission (photos, screenshots).
   Brief participant orientation script.

4. OBSERVATION FOCUS AREAS
   The 4 to 6 specific behaviors, moments, or transitions to prioritize.
   Organized using the AEIOU framework:
   Activities, Environments, Interactions, Objects, Users.

5. FIELD NOTES TEMPLATE
   Structure for capturing observations during the session:
   - Time stamp
   - Observation (factual, descriptive)
   - Interpretation (labeled separately)
   - Quote (verbatim participant language)
   - Flag (workaround / surprise / probe needed)

6. IN-SESSION PROBE QUESTIONS
   Questions to ask when specific observations require clarification.
   Written to not interrupt flow: "When you have a moment, can you tell me about...?"
   Not a sequential script, but a bank of questions to draw from.

7. POST-OBSERVATION DEBRIEF GUIDE
   15 to 20 minute debrief protocol after observation ends.
   Questions about specific things observed.
   Questions about what was typical vs. atypical about today.
   Questions about context, motivation, and history.

8. FIELD NOTES PROCESSING CHECKLIST
   Steps to complete within 24 hours of each session:
   Clean and expand raw notes
   Separate observations from interpretations
   Flag workarounds and anomalies
   Capture key quotes verbatim
   Write a 5-sentence "so what" summary

9. CROSS-SESSION SYNTHESIS TEMPLATE
   Template for comparing findings across multiple observation sessions:
   Common patterns, outliers, workarounds observed, key quotes,
   environmental factors, social dynamics.
```

---

## Starter Prompt

```
You are an ethnographic research specialist helping me design a field study
protocol and observation framework.

Research objectives: [the specific behaviors or workflows to understand]
Participant type: [who will be observed and their key characteristics]
Activity or work to observe: [what specifically will be observed]
Environment: [where the observation will take place]
Prior knowledge and hypotheses: [what is already known and what to look for]
Specific behaviors to focus on: [priority moments or transitions]
Tools or systems in use: [what tools or systems are part of the work]
Number of sessions: [how many observation sessions planned]
Format: [in-person / remote screen share]

Please produce:
1. A participant screener and consent protocol
2. An AEIOU-structured observation focus guide
3. A field notes template with separation of observation from interpretation
4. An in-session probe question bank (not a script, a set of questions to draw from)
5. A post-observation debrief guide for use at end of each session
6. A field notes processing checklist for use within 24 hours of each session
7. A cross-session synthesis template for comparing patterns across sessions

Remind me throughout to separate observation from interpretation.
Flag any sections where the observer effect is particularly likely to be
a methodological concern and suggest mitigation.
```

---

## Related Skills

| Use This Next | Why |
|---|---|
| `research-synthesis-report.md` | Synthesize findings across multiple field sessions |
| `affinity-mapping.md` | Organize observation data into themes and patterns |
| `user-journey-map.md` | Translate observed workflows into journey maps |
| `service-blueprint.md` | Document backstage processes revealed through field observation |
| `primary-research-plan.md` | Field study sits within a broader research plan |

| Use This Before | Why |
|---|---|
| `customer-discovery-interview.md` | Ethnographic observation often precedes or follows interviews |
| `jobs-to-be-done.md` | Observed workarounds reveal the jobs customers are hiring products to do |

---

## Reference Frameworks

| Framework | Use For |
|---|---|
| Contextual Inquiry (Holtzblatt and Beyer) | Structured field research method for product and software research |
| AEIOU Observation Framework | Structured categories for organizing observational notes |
| Shadowing | Following a participant through their full work period |
| Experience Sampling Method | Capturing real-time self-report data during natural behavior |
| Grounded Theory (Glaser and Strauss) | Building theory from observational data without prior hypotheses |

---

*Skill file version: 1.0 | Phase: 01 - Ideation and Market Research | Company type: Product*
