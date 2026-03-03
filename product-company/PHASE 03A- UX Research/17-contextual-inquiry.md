# contextual-inquiry.md

> **Skill:** Produces a contextual inquiry field protocol and findings format for observing users in their natural work environment to understand how they actually accomplish goals with and without a product.

---

## TLDR

Contextual inquiry (CI) is a structured field research method in which a researcher visits users in their natural work environment to observe real work as it happens. The CI protocol documents the four CI principles (context, partnership, interpretation, focus), field guide, observation framework, and synthesis format. Used when understanding the real context of use is critical and self-reported data is insufficient.

---

## Topic Explanation

### The Four Contextual Inquiry Principles (Holtzblatt and Beyer)

**Context:** Conduct research where work actually happens, not in a lab. Observe real work in progress, not simulated or recalled work.

**Partnership:** Adopt a master-apprentice relationship. The user is the expert in their own work. You are the curious learner.

**Interpretation:** Share your interpretations with the user in real time. "It looks like you're going back to the spreadsheet because the tool doesn't give you what you need. Is that right?" Checking interpretations in the field produces more accurate understanding than post-hoc analysis.

**Focus:** Have research questions that guide which behaviors receive attention. CI is not passive observation. It is focused observation of specific work domains.

### What CI Reveals That Interviews Cannot

- **Workarounds:** Users often do not mention workarounds when interviewed because they do not consciously notice them. Observation makes workarounds visible.
- **Environmental factors:** The physical and organizational context of work (interruptions, collaboration patterns, tool switching) affects behavior in ways users cannot accurately describe.
- **Tacit knowledge:** Expert users perform many steps automatically and cannot articulate them. Observation captures tacit knowledge that verbal reports miss.
- **Actual vs. described workflows:** Self-reported workflows are idealized. Observed workflows reveal the real process including all the inefficiencies and deviations.

### CI Session Structure

1. **Introduction (5 to 10 minutes):** Explain the purpose, get consent, set up recording.
2. **Background interview (10 to 15 minutes):** Brief context-setting interview about role and work.
3. **Observation period (45 to 90 minutes):** Watch real work as it happens. Ask clarifying questions and share interpretations as you go.
4. **Debrief interview (15 to 20 minutes):** Discuss specific observations. Ask about what was typical or atypical.

---

## Output Format

```
1. FIELD PROTOCOL HEADER
   Research objectives, participant criteria, session length,
   focus areas, observation framework.

2. PRE-SESSION PREPARATION CHECKLIST
   Consent and recording setup.
   Background research on participant's role and context.
   Focus questions to keep in mind during observation.

3. INTRODUCTION SCRIPT (verbatim)
   CI principles explained to participant in plain language.
   Consent and recording confirmation.
   Setting up the master-apprentice dynamic.

4. BACKGROUND INTERVIEW GUIDE (15 minutes)
   Role and responsibilities.
   Typical work day.
   Tools and systems used.
   Biggest challenges.

5. OBSERVATION FIELD GUIDE
   The work activities to focus on.
   AEIOU framework applied (Activities, Environment, Interactions, Objects, Users).
   How to handle interpretation sharing during observation.
   What to note verbatim.

6. IN-SESSION PROBE BANK
   Interpretation-check probes: "It looks like you're doing X because Y. Is that right?"
   Clarification probes: "Can you tell me more about why you did that?"
   Surprise probes: "I noticed you did X. Can you walk me through what you were thinking?"

7. DEBRIEF GUIDE (15 to 20 minutes)
   Questions about specific observed moments.
   Typical vs. atypical session questions.
   Questions about workarounds observed.

8. FINDINGS FORMAT (per session)
   Work domain summary.
   Sequence model: the steps of the observed workflow.
   Artifacts observed: tools, documents, shadow systems.
   Breakdowns and workarounds.
   Key quotes verbatim.
   Interpretation notes (checked with participant or flagged for checking).

9. CROSS-SESSION SYNTHESIS
   Consolidated work models.
   Common breakdowns across participants.
   Workarounds observed with frequency.
   Design implications.
```

---

## Starter Prompt

```
You are a UX researcher designing a contextual inquiry study.

Work domain: [what type of work will be observed]
Participant type: [who will be visited and observed]
Research focus: [the specific work activities or problems to focus on]
Research questions: [what you need to understand]
Number of sessions: [how many CI visits planned]

Produce a complete CI protocol including introduction script,
background interview guide, observation field guide,
in-session probe bank, debrief guide, and per-session findings format.
```

---

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
