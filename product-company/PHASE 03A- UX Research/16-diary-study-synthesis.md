# diary-study-synthesis.md

> **Skill:** Synthesizes longitudinal diary study data into themes, behavior change patterns, and insights about how user experience and behavior evolve over time with a product.

---

## TLDR

A diary study is a longitudinal research method in which participants self-report their experiences, behaviors, and thoughts over an extended period (days to weeks). The synthesis report transforms diary entries, activity logs, and periodic surveys into patterns about how the user experience changes over time, identifying habituation, abandonment, learning curves, and emotional arcs that single-session research cannot capture.

---

## Topic Explanation

### Why Diary Studies Capture What Other Methods Miss

Most UX research methods are cross-sectional: they capture experience at a single point in time. Diary studies are longitudinal: they capture how experience changes. This reveals:

**Learning curves:** Where and when users move from confusion to competence.
**Habituation:** Which initial frustrations users learn to tolerate vs. which continue to cause friction.
**Context variability:** How use patterns vary by time of day, location, or situation.
**Workaround evolution:** How users develop and refine workarounds over time.
**Abandonment patterns:** At what point in the experience curve users disengage.

### Diary Study Design

Diary studies require careful design decisions:

**Signal types:**
- **Interval-contingent:** Participants report at fixed time intervals (e.g., end of each work day)
- **Event-contingent:** Participants report each time a specific event occurs (e.g., every time they use the product)
- **Signal-contingent:** Participants report when prompted by a random signal

**Data collection methods:**
- Text entries (open-ended)
- Photo or screen capture
- Short surveys
- Emoji or rating scales

**Participant burden:** The more frequently participants must report, the higher the drop-off rate. Balance richness with feasibility.

### Longitudinal Synthesis Challenges

Diary study synthesis is more complex than single-session synthesis because:
- Participants contribute varying numbers of entries over the study period
- Entry quality varies day-to-day within the same participant
- Patterns must be analyzed both within-participant (change over time) and across-participants (common patterns)
- Missing entries must be distinguished from "nothing to report" from "disengagement"

---

## Output Format

```
1. STUDY OVERVIEW
   Duration, participant count, daily/weekly entry rate, completion rate,
   data collection methods, date range.

2. PARTICIPANT SUMMARY
   Anonymized participant profiles.
   Entry completion rates per participant.
   Segment distribution.

3. LONGITUDINAL BEHAVIOR PATTERNS
   How usage behaviors changed from study start to end.
   Learning curve analysis: when users achieved competence milestones.
   Usage frequency trends over the study period.

4. EXPERIENCE ARC
   Emotional arc across the study period.
   Key inflection points: when positive or negative shifts occurred.
   What triggered the shifts.

5. STABLE PATTERNS
   Behaviors and attitudes that remained consistent throughout.

6. EMERGING WORKAROUNDS
   Workarounds observed and when they appeared.
   Whether workarounds stabilized or were abandoned.

7. ABANDONMENT ANALYSIS
   Participants who reduced or stopped engagement.
   At what point in the journey and what preceded it.

8. THEMES AND INSIGHTS
   Cross-participant themes from diary content.
   Confidence level for each theme.

9. RECOMMENDATIONS
   Design or product implications of the longitudinal findings.
   Specifically: onboarding, features, and retention interventions.
```

---

## Starter Prompt

```
You are a UX researcher synthesizing diary study data.

Study context: [what product and experience was studied]
Duration and participant count: [how long, how many participants]
Data available: [diary entries, periodic surveys, activity logs]
Key questions the study was designed to answer: [the research objectives]

Synthesize the diary data into longitudinal patterns covering:
learning curves, experience arc, emerging workarounds, abandonment patterns,
and cross-participant themes. Connect findings to specific product and design recommendations.
```

---

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
