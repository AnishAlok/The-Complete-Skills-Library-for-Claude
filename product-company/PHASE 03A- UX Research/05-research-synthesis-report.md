# research-synthesis-report.md

> **Skill:** Produces a complete research synthesis report that transforms raw data from any qualitative research method into structured findings, prioritized insights, and actionable design or strategy recommendations.

---

## TLDR

This skill helps you answer: *"What do we now know from this research, how confident are we, and what should we do about it?"* It produces a synthesis report that moves from raw data to themes to insights to recommendations, with appropriate confidence levels and direct connection to design or product decisions.

---

## Topic Explanation

### Synthesis vs. Analysis vs. Summary

These three activities are often conflated but are distinct:

**Summary:** Recounting what each participant said. "Participant 3 said they found the navigation confusing." This is raw data, not synthesis.

**Analysis:** Identifying patterns within the data. "7 of 10 participants hesitated at the navigation menu before finding their target." This is observation of frequency.

**Synthesis:** Interpreting the meaning of patterns and connecting them to decisions. "The navigation menu labels use internal product terminology that does not match the words users use to describe their goals. This is likely the cause of hesitation and should be redesigned using users' own language." This is insight.

The synthesis report contains all three, progressing from the data layer to the insight layer to the recommendation layer.

### Thematic Analysis

Thematic analysis (Braun and Clarke) is the foundational method for qualitative data synthesis. The process:

1. **Familiarization:** Read all raw data (transcripts, notes, recordings). Start noticing patterns.
2. **Coding:** Tag every meaningful unit of data with a descriptor. A code is a label applied to a segment of data that captures its meaning.
3. **Theme generation:** Group codes into broader themes that represent a pattern across the data.
4. **Theme review:** Ensure themes are internally coherent and externally distinct.
5. **Theme definition:** Write a clear definition of each theme and what it means.
6. **Reporting:** Write the synthesis connecting themes to implications.

### Confidence Levels

Not all findings carry equal confidence. The synthesis report should be explicit about the strength of evidence behind each finding.

**High confidence:** Pattern observed consistently across most or all participants. Multiple data points (different sources, different session moments) converge on the same finding.

**Medium confidence:** Pattern observed in several participants but not all. Some variation or counterexamples exist. May reflect segment-specific behavior.

**Low confidence:** Pattern observed in a few participants or a single strong signal. Warrants further investigation rather than immediate action.

### Severity Rating for Usability Issues

For usability research specifically, findings should be severity-rated to guide prioritization:

**Critical (Severity 4):** Prevents task completion. Affects most or all users. Must fix before launch.
**Serious (Severity 3):** Causes significant difficulty or errors. Affects many users. Should fix before launch.
**Moderate (Severity 2):** Causes some difficulty but users can work around it. Consider fixing.
**Minor (Severity 1):** Small friction or aesthetic issue. Fix if time permits.

---

## When to Use This Skill

Use when:
- A qualitative research study (interviews, usability tests, contextual inquiry, diary studies) is complete and raw data needs to be transformed into findings
- Multiple researchers' notes need to be integrated into a single coherent report
- Stakeholders need findings in a format suitable for a presentation or design review
- A research repository entry needs a synthesis document

Do NOT use when:
- Raw data collection is not yet complete
- The output needed is a quantitative data analysis rather than qualitative synthesis

---

## Dos

- **Do move from data to themes to insights to recommendations.** Each layer builds on the previous. Do not jump from quotes to recommendations without the interpretive layer in between.
- **Do include verbatim participant quotes as evidence.** Quotes ground the synthesis in actual participant language and make the report credible to stakeholders.
- **Do separate findings from recommendations.** Findings describe what was observed. Recommendations describe what to do about it. Keep them distinct so stakeholders can engage with one without the other.
- **Do explicitly state what the research did not find.** Null findings (hypotheses that were not confirmed) are as strategically valuable as positive findings.
- **Do rate the confidence level of each finding.** A single participant anecdote and a pattern from 8 participants deserve different weight.
- **Do connect each recommendation to a specific finding.** Recommendations without a finding basis are opinions. Recommendations supported by a specific finding are evidence-based.

---

## Donts

- **Dont include every observation in the report.** Ruthless prioritization is a synthesis skill. Include observations that reveal something actionable or important. Omit observations that are interesting but not actionable.
- **Dont over-quote.** Quotes are evidence, not the finding itself. One strong quote per finding is usually sufficient. Multiple quotes making the same point do not add strength.
- **Dont write the report for an audience of researchers.** The primary audience is designers and product managers who need to act on the findings. Write for action, not for methodological completeness.
- **Dont present all findings as equally important.** Severity and confidence ratings are what allow stakeholders to triage.

---

## Ideal Inputs

```
1. RAW DATA
   Interview transcripts, session notes, observation notes, recordings.
   Organized by session or participant.

2. THE RESEARCH QUESTIONS FROM THE PLAN
   The questions the research was designed to answer.
   These structure the synthesis.

3. THE DESIGN DECISIONS BEING INFORMED
   The specific decisions stakeholders need to make.
   These structure the recommendations.

4. THE AUDIENCE FOR THE REPORT
   Who will read this? Product team, design team, leadership?
   This determines depth, format, and emphasis.

5. PRIOR FINDINGS TO BUILD ON (if applicable)
   Any prior research on the same topic that this study extends or contradicts.
```

---

## Output Format

```
1. REPORT HEADER
   Study title, date, researcher(s), method, participant count,
   session dates, report version.

2. EXECUTIVE SUMMARY (half page)
   The most important findings in 3 to 5 sentences.
   The single highest-priority recommended action.
   Confidence level of the overall findings.

3. METHODOLOGY SUMMARY
   What was studied, how, with whom, when.
   Any methodological limitations that affect interpretation.

4. PARTICIPANT OVERVIEW
   Anonymized participant profiles showing the range of the sample.
   Any notable sample characteristics.

5. FINDINGS BY THEME
   For each theme (3 to 7 themes):
   - Theme statement (one clear sentence)
   - Supporting observations with frequency ("7 of 10 participants...")
   - Illustrative verbatim quotes (1 to 2 per theme)
   - Confidence level: High / Medium / Low
   - Severity rating (for usability findings): Critical / Serious / Moderate / Minor

6. NULL FINDINGS
   Hypotheses that were tested and not supported.
   What was expected and what was found instead.

7. RECOMMENDATIONS
   For each finding:
   - The finding it responds to
   - The recommended action
   - Priority: Immediate / Near-term / Backlog
   - Owner or team responsible

8. OPEN QUESTIONS
   Questions this research raised but did not answer.
   Recommended follow-on research.

9. APPENDIX
   Full participant quotes by theme.
   Raw observation data (optional).
   Affinity map or synthesis artifacts.
```

---

## Starter Prompt

```
You are a UX research analyst helping me synthesize research findings into
an actionable report.

Raw data: [paste session notes, transcripts, or describe the data you have]
Research questions from the plan: [the questions the study was designed to answer]
Design decisions being informed: [specific decisions stakeholders need to make]
Participant count and method: [how many participants, what method]
Audience for the report: [who will read and act on this]
Prior relevant findings: [any prior research this builds on or contradicts]

Please produce a complete research synthesis report including:
1. Executive summary (3 to 5 sentences, top priority action)
2. Methodology summary with limitations noted
3. Anonymized participant overview
4. Findings organized by theme, each with supporting observations,
   illustrative quotes, confidence level, and severity rating
5. Null findings section for hypotheses not supported
6. Recommendations linked to specific findings with priority levels
7. Open questions and recommended follow-on research

Move from data to themes to insights to recommendations, not from quotes
directly to recommendations.
Separate findings from recommendations throughout.
```

---

## Related Skills

| Use This Next | Why |
|---|---|
| `insight-repository.md` | Tag and store individual insights for long-term retrieval |
| `affinity-mapping.md` | Use affinity mapping as a synthesis method to build themes |
| `research-brief.md` | Distill the synthesis into a stakeholder-facing brief |
| `executive-briefing.md` | Create a leadership-ready summary of key findings |

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
