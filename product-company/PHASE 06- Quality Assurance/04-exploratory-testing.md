# exploratory-testing.md

> **Skill:** Produces exploratory testing session notes documenting the charter, approach, real-time observations, defects found, and follow-up session recommendations from an unscripted product investigation.

---

## TLDR

Exploratory testing is simultaneous test design and execution: the tester uses judgment and curiosity to investigate the product without a script, following interesting threads and probing for unexpected behavior. This skill produces session documentation using the Session-Based Test Management (SBTM) format: charter, notes, defects, observations, questions, and follow-up charters.

---

## Topic Explanation

### Exploratory vs. Scripted Testing

Scripted testing executes pre-defined test cases. It verifies known requirements efficiently and consistently. Its weakness: it only looks where it was told to look.

Exploratory testing applies human judgment to find what scripted tests miss: unexpected interactions, unanticipated edge cases, usability problems, and defect clusters. Its weakness: it does not provide systematic coverage that can be measured against requirements.

Both are necessary. Teams using only scripted tests miss a significant class of defects. Teams using only exploratory testing cannot demonstrate requirements coverage.

### Session-Based Test Management

A session is a fixed period of 60 to 90 minutes of uninterrupted exploratory testing with a defined charter. The charter defines the mission without specifying steps. Notes are captured in real time and reported afterward.

The three-part charter: **Explore** [what area] / **Using** [data or approach] / **To discover** [risks or behaviors targeted].

Example: "Explore the CSV import feature using malformed CSV files to discover how the system handles data errors, encoding issues, and files exceeding size limits."

### Defects vs. Observations vs. Questions

**Defects:** actual bugs that must be filed as formal defect reports. Something broke.

**Observations:** behaviors that are not bugs but are worth noting: usability friction, confusing UI text, inconsistent terminology, performance that feels slow, missing error messages. These are product improvement candidates.

**Questions:** behaviors that need clarification because it is unclear whether they are intended. "Is it intentional that deleting a draft does not ask for confirmation?"

---

## Dos

- **Do write the charter before starting.** An undirected session is wandering, not exploring.
- **Do capture notes in real time.** Observations fade quickly. Log as you go, even briefly.
- **Do separate defects, observations, and questions explicitly.** Mixing them makes the output hard to act on.
- **Do debrief within 24 hours** while context is still fresh.

---

## Output Format

```
SESSION NOTES HEADER
Session ID: [unique identifier]
Tester: [name]
Date: [date]
Duration: [actual time spent]
Product area: [feature or area tested]
Build/version: [what was tested]

CHARTER
Explore: [area or feature]
Using: [data, tools, or approach]
To discover: [risks, behaviors, or questions]

SESSION NOTES (real-time log)
[HH:MM] [What was explored and what was observed]
[HH:MM] [Interesting behavior noticed or thread followed]
[HH:MM] [What happened when that thread was pursued]

DEFECTS FOUND
For each defect:
- Title and severity
- Brief reproduction summary
- Link to full defect report filed separately

OBSERVATIONS (noteworthy, not defects)
Usability friction, confusing UI, missing error messages,
inconsistent terminology, performance concerns.

QUESTIONS RAISED
Behaviors needing product clarification.
Owner assigned to answer each.

COVERAGE NOTES
Areas explored within the charter.
Areas not reached (candidates for follow-up sessions).
Threads discovered outside the charter worth a separate session.

SESSION METRICS
Defects found by severity. Observations count. Questions raised. Charter completion %.

FOLLOW-UP SESSIONS RECOMMENDED
For each recommended follow-up:
Charter: Explore [area] Using [approach] To discover [risk]
Rationale: [what this session revealed as worth investigating further]
```

---

## Starter Prompt

```
You are a QA engineer documenting a completed exploratory testing session.

Area explored: [what was investigated]
Charter: [the Explore / Using / To discover statement]
Duration: [time spent]
Defects found: [list of issues with severity]
Observations: [behavioral notes that are not defects]
Questions raised: [behaviors needing product clarification]
Areas not reached: [scoped but not explored within this session]

Produce complete session notes in SBTM format.
Clearly distinguish defects, observations, and questions.
Include at least one recommended follow-up session charter based on what was discovered.
```

---

## Related Skills

| Use This Alongside | Why |
|---|---|
| `defect-report.md` | Defects found in exploration must be formally documented |
| `test-case-writing.md` | Observations often reveal missing test case coverage |

*Skill file version: 1.0 | Phase: 07 - Quality Assurance | Company type: Product*
