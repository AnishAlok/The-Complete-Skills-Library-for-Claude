# usability-test-script.md

> **Skill:** Produces a complete moderator script for usability test sessions including welcome, think-aloud briefing, task delivery, probing questions, and debrief protocol.

---

## TLDR

This skill helps you answer: *"What do I say and do during a usability test session to get honest, useful data without leading participants or accidentally coaching them?"* It produces a word-for-word moderator script that standardizes delivery across sessions while leaving room for natural conversation and follow-up probing.

---

## Topic Explanation

### The Moderator's Dilemma

The usability test moderator has two competing pressures: being warm and supportive enough that participants are comfortable and thinking aloud, while being neutral enough not to influence their behavior or signal correct answers. This tension cannot be fully resolved, only managed through deliberate script design.

The most common moderator mistakes that bias data:

**Reacting to struggles.** When a participant is confused or frustrated, every natural human instinct is to help. The moderator must suppress this instinct. Struggling is the data.

**Confirming correct paths.** Nodding, saying "good," or "that's right" when a participant navigates correctly tells them they are on track and removes the validity of subsequent navigation choices.

**Answering "am I doing this right?"** Participants ask this constantly. The correct response is always a version of "What do you think you would do in this situation?" or "What would you expect to happen there?"

**Rushing through tasks.** If the session is running long, it is tempting to skip probing and move to the next task. This loses the qualitative insight that makes moderated testing valuable over unmoderated.

### Think-Aloud Protocol

The think-aloud protocol, developed by Clayton Lewis and John Rieman and widely studied by Ericsson and Simon, asks participants to verbalize their thoughts as they work. It is the primary source of qualitative insight in usability testing.

Two versions:

**Concurrent think-aloud (CTA):** Participants narrate as they work in real time. Most common. Some researchers argue this alters natural behavior because articulating thoughts consumes cognitive bandwidth.

**Retrospective think-aloud (RTA):** Participants complete tasks silently, then review a recording and narrate their thoughts retrospectively. More ecologically valid behavior, but adds significant session time and may miss in-the-moment reasoning.

For most product usability testing, CTA is the right choice: it produces richer data per session minute than RTA and the behavioral alteration is modest.

### Probe Types

Not all follow-up questions are equal. A well-designed script includes the right probe types in the right moments:

**Elaboration probes:** "Tell me more about that." "What were you thinking there?"
Used when: Participant says something interesting but vague.

**Expectation probes:** "What did you expect to happen there?" "Is that what you expected?"
Used when: Participant completes an action without narrating their expectation.

**Confusion probes:** "I noticed you hesitated there. What was going through your mind?"
Used when: Participant pauses, backtracks, or looks uncertain.

**Completion probes:** "What would you do next?" "Do you feel like you've completed the task?"
Used when: Unclear whether the participant believes they have succeeded.

**Retrospective probes (post-task):** "Looking back at that task, was there anything confusing or unclear?"
Used after every task before moving to the next.

---

## When to Use This Skill

Use when:
- A usability test plan is complete and sessions are about to begin
- A facilitator is running sessions for the first time and needs script support
- Standardizing session delivery across multiple facilitators

Do NOT use when:
- The test plan does not yet exist (build the plan first: `usability-test-plan.md`)
- Running unmoderated tests (the moderator script is only for moderated sessions)

---

## Dos

- **Do write the welcome in first person so it reads naturally when spoken.** The script is a spoken document, not a written one.
- **Do include the exact think-aloud practice exercise.** Do not assume participants understand think-aloud from a description. Walk them through a practice task (e.g., "make a cup of coffee") before any real tasks.
- **Do script the response to "Am I doing this right?"** This question will be asked in every session. Have a standard answer ready.
- **Do include time allocations per section.** The moderator needs to know when a section is running long.
- **Do write transition language between sections.** Awkward transitions break rapport and remind participants they are in a test environment.
- **Do include a section for note-taker instructions.** The note-taker needs to know what to capture and how to signal the moderator.

---

## Donts

- **Dont script probes as leading questions.** "Did you find that confusing?" leads the answer. "What were you thinking there?" does not.
- **Dont over-script the probing sections.** Probing should feel conversational. Heavy scripting produces robotic delivery that reduces participant comfort and candor.
- **Dont include filler phrases that signal evaluation.** "Great," "perfect," "exactly right" all signal approval. Replace with neutral acknowledgments: "Thank you," "Okay," "Got it."
- **Dont forget to script the session close.** Participants appreciate a clear ending and an explanation of what happens next.

---

## Ideal Inputs

```
1. THE TASK LIST FROM THE TEST PLAN
   The task scenarios and their success criteria.

2. THE DESIGN BEING TESTED
   What participants will interact with.
   Any access or setup instructions needed.

3. SESSION LENGTH AND FORMAT
   Total time available.
   Remote or in-person.

4. SPECIFIC PROBING AREAS
   Any flows or moments in the design that are particularly important to probe.

5. POST-SESSION DEBRIEF QUESTIONS
   Any specific product or design questions to ask after tasks are complete.
```

---

## Output Format

```
1. MODERATOR REFERENCE CARD
   Session timing overview.
   Key reminders (do not help, neutral acknowledgments, "Am I doing this right?" response).

2. PRE-SESSION SETUP CHECKLIST
   Recording confirmation, prototype access, consent form, note-taker briefing.

3. WELCOME AND INTRODUCTION (verbatim, 5 minutes)
   Introduction of self and role.
   Purpose of the session (learning from the design, not testing the participant).
   Recording consent confirmation.
   Permission for observers.
   Reminder that there are no right or wrong answers.

4. THINK-ALOUD BRIEFING AND PRACTICE (verbatim, 5 minutes)
   Explanation of think-aloud protocol.
   Practice task (non-product, low-stakes).
   Coaching feedback after practice.
   Transition to product tasks.

5. TASK DELIVERY SECTION
   For each task:
   - Task intro / scenario setup (verbatim)
   - Task delivery (verbatim)
   - During-task moderator reminders (not verbatim: observations to make)
   - Standard think-aloud prompt if participant goes silent: (verbatim)
   - Post-task probe questions (verbatim)
   - Transition to next task (verbatim)

6. POST-SESSION DEBRIEF (verbatim, 10 minutes)
   Overall experience questions.
   Specific design questions.
   Comparison to current solution (if applicable).
   Any final thoughts.

7. SESSION CLOSE (verbatim, 2 minutes)
   Thank participant.
   Explain what happens next.
   Incentive confirmation.

8. NOTE-TAKER GUIDE
   What to capture: observations, quotes, errors, hesitations.
   Notation system for severity.
   How to flag moments for the moderator.
```

---

## Starter Prompt

```
You are a UX research specialist writing a usability test moderator script.

Task list: [paste tasks from the test plan with their scenarios]
Design being tested: [what participants will interact with]
Session length: [total time available]
Format: [remote / in-person]
Specific probing areas: [flows or moments requiring special attention]
Post-session debrief questions: [questions to ask after tasks complete]

Please produce a complete moderator script including:
1. A moderator reference card with key reminders
2. Pre-session setup checklist
3. Word-for-word welcome and introduction (5 minutes)
4. Think-aloud briefing with practice task (5 minutes)
5. Full task delivery section with per-task intro, during-task notes, probes, and transitions
6. Post-session debrief (10 minutes)
7. Session close script
8. Note-taker guide

Write all verbatim sections in first person as spoken language.
Use neutral acknowledgments throughout (no "great," "good," or "exactly").
Include the standard response to "Am I doing this right?" in the reference card.
Flag any probe questions that could lead the participant to a particular answer.
```

---

## Related Skills

| Use This Next | Why |
|---|---|
| `research-synthesis-report.md` | Document and analyze findings after sessions |
| `screener-questionnaire.md` | Ensure the right participants are recruited |
| `participant-consent-form.md` | Prepare consent documentation |

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
