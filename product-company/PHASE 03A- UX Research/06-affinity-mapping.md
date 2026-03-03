# affinity-mapping.md

> **Skill:** Documents the affinity mapping process and produces a structured cluster map that organizes raw research observations into themes for synthesis, design, or strategy use.

---

## TLDR

This skill helps you answer: *"How do we take hundreds of raw observations and turn them into clear, prioritized themes we can actually act on?"* It produces an affinity map structure with cluster logic, theme labels, supporting evidence, and connection to design or product decisions. Used as a primary synthesis method after qualitative research.

---

## Topic Explanation

### What Is Affinity Mapping?

Affinity mapping (also called affinity diagramming or the KJ Method, developed by Japanese anthropologist Jiro Kawakita) is a bottom-up grouping technique used to synthesize large quantities of qualitative data into themes. The process involves writing each discrete observation on an individual note, then grouping notes by "affinity" (similarity of meaning) to reveal themes that emerge from the data rather than themes imposed on it.

The method is bottom-up by design: themes are not decided in advance and observations sorted into them. Instead, themes emerge from the clustering of observations. This is what makes affinity mapping a genuine synthesis method rather than a categorization exercise.

### The Physical vs. Digital Process

**Physical (post-it notes on a wall):** The original and still widely used method. Writing observations by hand is slower but forces more careful attention to each one. Moving physical notes and standing in front of a wall creates a different cognitive experience than moving digital cards. Many researchers believe physical affinity mapping produces richer synthesis.

**Digital (Miro, FigJam, Mural):** Faster, easier for distributed teams, and produces a digital artifact that can be shared immediately. Remote teams almost always use digital. The loss of physical embodiment is a trade-off, not a dealbreaker.

### The Levels of an Affinity Map

A fully developed affinity map has four levels:

**Level 1: Individual observations.** Raw data points extracted from research. One observation per note. Written as a specific observation, not an interpretation.
Example: "P3 opened the help documentation before starting the task."

**Level 2: Groups.** Clusters of observations that share an affinity. Named with a neutral, descriptive label.
Example: "Users seek external reference before acting."

**Level 3: Themes.** Higher-order groupings of groups. Named with an interpretive, insight-oriented label.
Example: "Users lack confidence in first-time task completion."

**Level 4: Big ideas.** The top-level synthesis that frames the entire research direction.
Example: "Onboarding does not build sufficient user confidence to enable independent action."

Most affinity maps used in product UX work go to Level 3. Level 4 is optional and powerful when presenting to leadership.

### Writing Good Observation Notes

The quality of an affinity map depends entirely on the quality of the observation notes it is built from. Good observations are:

**Specific:** "Participant clicked the back button three times before finding the report" is specific. "User was confused" is an interpretation.

**Attributed but anonymized:** "P4 said 'I don't know what this number means'" not "someone said." Knowing which participant said something allows for follow-up and cross-referencing.

**Behavioral or verbatim:** Either describe what happened or quote exactly what was said. Do not paraphrase in a way that inserts interpretation.

**Single observations:** One note, one observation. Do not combine two separate observations on the same note. This prevents them from being clustered separately.

---

## When to Use This Skill

Use when:
- Synthesizing qualitative research data from interviews, usability tests, contextual inquiry, or diary studies
- After a research sprint, as the synthesis method before writing the report
- Facilitating a cross-functional team session to build shared understanding of research data
- When research findings need to be sorted and prioritized collaboratively

Do NOT use when:
- Synthesizing quantitative data (use statistical analysis methods)
- The dataset is too small for grouping to be meaningful (fewer than 30 observations)
- You need to synthesize a specific structured dataset (a survey with fixed questions), which should be analyzed statistically

---

## Dos

- **Do write each observation before starting to group.** The impulse to cluster as you write destroys the bottom-up nature of the method. Write all notes first, then group.
- **Do write in the third person from the participant's perspective.** "Participant expects the save to happen automatically" not "we should add auto-save."
- **Do let groups form naturally before naming them.** Name a group after it has formed, not before. Pre-named groups cause you to sort observations into predetermined categories.
- **Do move notes freely.** A note that seems to belong in two places is often a sign that a theme boundary is wrong. Move things until the clusters feel natural.
- **Do invite multiple perspectives.** Affinity mapping done by one person risks one person's frame. Involving designers, PMs, and engineers in the clustering session creates shared ownership of findings.
- **Do document the map at multiple stages.** Photograph or screenshot the map before and after major regroupings. The evolution of the map is itself analytical data.

---

## Donts

- **Dont write interpretations on observation notes.** "User was confused" is an interpretation. "User clicked the back button twice and said 'wait, where am I?'" is an observation. Interpretations belong at the theme level, not the observation level.
- **Dont force every note into a group.** Some observations are outliers. Maintain an "outliers" cluster for observations that do not fit anywhere. Outliers sometimes become important later.
- **Dont let one person name all the clusters.** The language used to name themes shapes how findings are perceived. Naming should reflect the group's discussion, not one researcher's framing.
- **Dont conflate affinity mapping with prioritization.** The map reveals themes and their scale. Prioritization of what to act on is a separate step that follows the mapping.

---

## Ideal Inputs

```
1. RAW OBSERVATION NOTES
   Individual observations from research sessions.
   One observation per note, written specifically and behaviorally.
   Typically 100 to 400 observations for a 6 to 10 session study.

2. THE RESEARCH QUESTIONS
   What was being studied?
   What did the team expect or hypothesize?

3. TEAM COMPOSITION FOR THE SESSION
   Who will participate in the mapping session?
   Any roles that are important to include?

4. TOOL OR FORMAT
   Physical (wall space, post-its) or digital (Miro, FigJam, Mural)?
   If digital, which platform?

5. TIME AVAILABLE
   How long is the mapping session?
   How many observations need to be clustered?
```

---

## Output Format

```
1. SESSION SETUP GUIDE
   Preparation instructions for physical or digital setup.
   Ground rules for participants.
   Time allocation: writing phase, silent grouping, discussion, naming.

2. AFFINITY MAP STRUCTURE (the output)

   For each top-level theme:
   - Theme name (interpretive, insight-oriented label)
   - Theme statement (1 to 2 sentences summarizing what this theme means)
   - Observation count (how many notes clustered here)
   - Sub-groups within the theme (with names and note counts)
   - 3 to 5 representative observations from this theme
   - 1 to 2 verbatim participant quotes if available
   - Confidence level: High (many consistent observations) /
     Medium / Low (few or inconsistent)

3. OUTLIERS CLUSTER
   Observations that did not fit any theme.
   Note whether any outliers are strategically important even if not common.

4. MAP-TO-DECISION CONNECTIONS
   How each theme connects to a design or product decision.
   Which themes are most actionable and why.

5. PRIORITIZED THEME LIST
   Themes ranked by: frequency, severity, strategic importance.
   The criteria used for prioritization.

6. NEXT STEPS
   How the map feeds into the synthesis report.
   Any themes that require follow-on research.
```

---

## Starter Prompt

```
You are a UX research analyst facilitating an affinity mapping synthesis session.

Raw observations: [paste observation notes or describe the data you have]
Research questions: [what was being studied]
Number of participants and sessions: [scale of the dataset]
Team for the session: [who will be involved]
Format: [physical / digital platform]
Time available: [how long for the session]

Please produce:
1. A session setup guide with preparation instructions and ground rules
2. An affinity map structure organizing observations into themes,
   sub-groups, and representative examples
3. A theme statement for each theme
4. An outliers cluster
5. Map-to-decision connections for each theme
6. A prioritized theme list with ranking criteria

Write observation notes in behavioral, third-person language.
Separate observations from interpretations at every level.
Flag any theme that is large enough to warrant splitting into two separate themes.
```

---

## Related Skills

| Use This Next | Why |
|---|---|
| `research-synthesis-report.md` | The affinity map is input to the written synthesis report |
| `insight-repository.md` | Themes from the map become tagged insights in the repository |
| `user-journey-map.md` | Affinity themes often become stages or pain points on a journey map |

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
