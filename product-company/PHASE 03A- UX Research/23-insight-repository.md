# insight-repository.md

> **Skill:** Produces a structured format and tagging system for storing, organizing, and retrieving individual research insights within a UX or product research repository.

---

## TLDR

The insight repository is the atomic layer of the research knowledge base: a structured format for storing individual insights extracted from research studies so they can be retrieved, combined, and built upon across projects. This skill produces the insight entry format, tagging taxonomy, and retrieval protocols specifically for UX and product research contexts.

---

## Topic Explanation

### The Insight vs. the Observation vs. the Finding

These three levels of research data should be stored and tagged differently:

**Observation:** A raw, specific, factual data point from a single session.
"P4 opened a new browser tab to Google 'how to calculate overtime' during the payroll task."

**Finding:** A pattern observed across multiple participants or sessions.
"6 of 8 participants needed to look up overtime calculation rules externally during the task."

**Insight:** An interpretation that connects a finding to a design or product implication.
"Users do not trust that the system's overtime calculation is correct, creating a verification behavior that signals a product credibility gap. Addressing this requires either transparent calculation logic or in-product guidance."

The insight repository should contain all three, clearly labeled, so that insights can be traced back to findings which can be traced back to observations.

### Insight Entry Format

Each insight entry in the repository should be a discrete, self-contained record with:

**Insight ID:** A unique identifier for cross-referencing.
**Insight statement:** One sentence capturing the insight.
**Observation(s) supporting it:** The specific data points.
**Source study:** Which research project produced this.
**Participants:** How many and which participant types.
**Confidence level:** High / Medium / Low based on evidence strength.
**Tags:** Topic, product area, user type, research method, decision type, status.
**Date:** When this insight was generated.
**Status:** Current / Needs revalidation / Superseded.
**Related insights:** Links to connected insights.
**Actions taken:** Any design or product decisions made based on this insight.

### Repository Taxonomy for UX Insights

UX insight repositories need a taxonomy tuned to design decision-making:

**Topic tags:** Onboarding, navigation, error handling, performance perception, trust signals, empty states, notifications, accessibility, mobile experience, etc.

**Product area tags:** Aligned with product domains or feature areas in your specific product.

**User type tags:** Novice user, expert user, admin, viewer, specific persona names.

**Research method tags:** Usability test, contextual inquiry, interview, diary study, heuristic, etc.

**Insight type tags:** Usability issue, mental model, behavioral pattern, unmet need, opportunity, design strength.

**Decision type tags:** Navigation / IA, labeling, flow design, feature prioritization, onboarding, error handling, etc.

---

## When to Use This Skill

Use when:
- Building or redesigning a UX research repository
- Onboarding a new researcher and establishing documentation standards
- Migrating insights from unstructured notes or documents into a tagged system
- The research team needs a consistent format for cross-project insight retrieval

---

## Dos

- **Do store insights atomically.** One insight per record. Compound insights that cover two separate topics should be split.
- **Do link insights to their source observations.** Traceability from insight to data is what makes insights credible to skeptical stakeholders.
- **Do track status.** Markets and products change. An insight about onboarding from 2 years ago may be superseded. Tag its status and review aging insights quarterly.
- **Do record actions taken.** The most important accountability metric for a research repository is whether insights led to product decisions. Record when they did.
- **Do use controlled vocabulary for tags.** Free-text tags create synonym problems. Use a managed tag list.

---

## Output Format

```
1. INSIGHT ENTRY TEMPLATE

   Fields (one per insight record):
   - Insight ID: [auto-generated or sequential]
   - Date: [when generated]
   - Insight statement: [one sentence capturing the insight]
   - Type: Usability issue / Mental model / Behavioral pattern /
            Unmet need / Opportunity / Design strength
   - Confidence: High / Medium / Low
   - Supporting observations: [2 to 4 specific data points]
   - Verbatim quote(s): [1 to 2 representative quotes if available]
   - Source study: [study name and link]
   - Study method: [usability test / interview / CI / etc.]
   - Participant count: [how many participants this is based on]
   - User type(s): [which user segments]
   - Topic tags: [from controlled vocabulary]
   - Product area tags: [from product taxonomy]
   - Decision type tags: [what kind of decision this informs]
   - Status: Current / Needs revalidation / Superseded
   - Related insights: [IDs of connected insights]
   - Actions taken: [any product or design decisions made based on this insight]
   - Notes: [any caveats or context]

2. TAGGING TAXONOMY
   Complete controlled vocabulary for all tag dimensions.
   Definitions for each tag.
   Guidance for applying tags to ambiguous cases.

3. RETRIEVAL PROTOCOLS
   How to search by topic, product area, and user type.
   How to filter by confidence level and recency.
   How to find insights relevant to a specific design decision.

4. MAINTENANCE CALENDAR
   Monthly: add new insights from completed studies.
   Quarterly: review insights older than 12 months for revalidation or retirement.
   Annually: full taxonomy review and pruning.

5. ONBOARDING GUIDE
   How to enter a new insight (step by step).
   How to search before starting new research.
   Who to contact with taxonomy questions.
```

---

## Starter Prompt

```
You are a research operations specialist designing an insight repository system.

Team size: [number of researchers and consumers of insights]
Research volume: [studies per quarter]
Current documentation state: [what exists and what does not]
Product areas: [the product domains that should be in the taxonomy]
User types: [the user segments the product serves]
Tool being used: [Notion / Airtable / Dovetail / other]

Produce a complete insight repository design including:
insight entry template, tagging taxonomy with controlled vocabulary,
retrieval protocols for common search scenarios,
maintenance calendar, and onboarding guide.
```

---

## Related Skills

| Use This Next | Why |
|---|---|
| `research-repository.md` | The broader repository system that the insight entries live within |
| `research-synthesis-report.md` | Synthesis reports generate the insights entered into this repository |
| `affinity-mapping.md` | Affinity mapping clusters become insights entered into the repository |

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
