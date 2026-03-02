# research-repository.md

> **Skill:** Designs and populates a structured research repository: the system for tagging, organizing, storing, and retrieving research findings so that insights are discoverable, reusable, and do not get lost between projects.

---

## TLDR

This skill helps you answer: *"How do we make sure that the research we've done is findable, usable, and builds on itself rather than being redone from scratch every time?"* It produces a repository design including a tagging taxonomy, folder structure, entry templates, retrieval protocols, and maintenance practices. Used by product teams, UX researchers, and market research functions to turn individual research projects into a compounding organizational intelligence asset.

---

## Topic Explanation

### Why Research Repositories Fail

Most product and research teams do some form of research documentation. Most of those documentation efforts eventually fail. The pattern is consistent:

A team runs a series of interviews. Notes are written up. A synthesis document is produced. It sits in a Google Drive folder. Six months later, a new team member asks "has anyone ever researched why users don't adopt feature X?" Nobody remembers. The research is technically available but practically inaccessible. New research is commissioned to answer a question that was already answered.

This pattern has a name in research practice: insight debt. Insights that were generated but are not retrievable accumulate as debt that the team must repay by re-doing research, or by making decisions without insight.

Research repositories fail for four reasons:

**No consistent tagging.** Notes are stored but not tagged in a way that makes them searchable or comparable across projects.

**No standard entry format.** Each researcher documents differently. Some write long summaries. Others write bullet points. None are structured consistently enough to extract patterns across studies.

**No maintenance ownership.** Repositories are set up enthusiastically and then nobody is assigned to maintain them. They drift into incompleteness and decay.

**No retrieval culture.** The repository is not the first thing people check before starting new research. The habit of searching the repository is never established.

A well-designed research repository solves all four problems with deliberate structure, clear ownership, and a culture of retrieval before recreation.

### What a Research Repository Contains

A research repository is not just a document storage system. It contains structured, tagged, and connected artifacts at multiple levels:

**Study level:** The full documentation of a research project. Research plan, data collection artifacts (transcripts, recordings), synthesis report, key findings.

**Insight level:** Individual insights extracted from studies and tagged independently. An insight is a discrete finding: "Restaurant operators with 3 or more locations value multi-location payroll consolidation more than compliance features." This insight can be tagged, retrieved, and connected to other insights across multiple studies.

**Participant level:** Records of research participants. Who was interviewed, when, for which study, what segment they represent. Used to avoid over-researching the same customers and to enable follow-up.

**Tag level:** The taxonomy that makes everything discoverable. Tags connect insights, studies, and participants across multiple dimensions simultaneously.

### Tagging Taxonomy Design

The tagging taxonomy is the most important design decision in a research repository. Tags must be:

**Specific enough to be useful:** "Pain point" is not a useful tag. "Onboarding pain" and "compliance pain" are useful tags because they enable comparison.

**Broad enough to scale:** A taxonomy that requires 12 tags to classify a single insight will never be maintained. Aim for 3 to 5 tags per insight.

**Consistent across contributors:** Tags that mean different things to different researchers produce a repository that cannot be compared across entries.

Standard tag dimensions for a product research repository:

- **Topic:** What the insight is about. (Onboarding, compliance, pricing, integrations, support, etc.)
- **Customer type:** Which customer segment this insight applies to. (Segment name, company size, role, etc.)
- **Research method:** How this insight was gathered. (Interview, survey, NPS, usability test, etc.)
- **Study:** Which research project this came from.
- **Date:** When the insight was generated.
- **Confidence level:** How strongly this insight is supported. (Single source / multiple sources / strongly validated)
- **Status:** Current / outdated / needs revalidation.
- **Product area:** Which product domain this insight relates to.
- **Decision type:** What kind of decision this insight informs. (Roadmap / positioning / pricing / sales enablement)

### Repository Tools

Research repositories can be built in many tools depending on team size, research volume, and budget:

**Lightweight options (0 to 10 researchers):**
Notion databases, Airtable, or a structured Google Sheets + Drive system. Good for small teams with moderate research volume.

**Mid-tier options (dedicated research functions):**
Dovetail, Aurelius, or EnjoyHQ. Purpose-built research repository tools with tagging, search, and synthesis features built in.

**Enterprise options:**
UserZoom, Ethnio, or custom Confluence-based systems for large research organizations.

The most important factor is not the tool. It is the design of the taxonomy and the discipline of consistent entry. A well-designed Notion database maintained consistently will outperform a sophisticated tool with poor taxonomy and inconsistent use.

---

## When to Use This Skill

Use when:
- A team is doing consistent research (more than 2 to 3 studies per quarter) and findings are getting lost
- New team members cannot access prior research and keep re-asking answered questions
- Multiple researchers are producing findings that nobody can compare because formats differ
- The product team is making decisions without checking what research already exists
- Building a research operations practice and needing the repository as a foundation
- Preparing for organizational growth where the research function will expand

Do NOT use when:
- You only do research occasionally and a shared folder with naming conventions is sufficient
- You need to design a specific research study (use `primary-research-plan.md`)
- You need to synthesize findings from existing data (use `desk-research-synthesis.md` or `voice-of-customer.md`)

---

## Dos

- **Do design the taxonomy before choosing the tool.** The tagging structure is the repository. The tool is just where it lives. Get the taxonomy right first.
- **Do establish a standard entry template.** Every study, insight, and participant record must follow the same format to enable cross-study comparison.
- **Do assign a repository owner.** Without a named person responsible for maintaining taxonomy consistency, quality review, and regular audits, the repository will decay.
- **Do make retrieval the first step of every research project.** Build a norm: before designing any new research, the researcher searches the repository for existing relevant insights. This is the habit that makes the repository valuable.
- **Do tag at the insight level, not just the study level.** Studies are too coarse for most retrieval needs. Individual insights, each tagged independently, are what make the repository genuinely useful.
- **Do build a participant database alongside the insight database.** Knowing who has been interviewed, when, and for which study enables better recruitment decisions and prevents over-researching the same customers.
- **Do review and prune the taxonomy quarterly.** New topics emerge. Old ones become irrelevant. A stale taxonomy produces a mistagged repository.
- **Do treat the repository as a product.** It has users (researchers and decision-makers), use cases (retrieval, synthesis, onboarding), and should be designed and maintained with the same discipline as a product.

---

## Donts

- **Dont make the entry process so burdensome that researchers skip it.** A repository that takes 45 minutes to enter a study into will not be maintained. Aim for 10 to 15 minutes per study entry, 2 to 3 minutes per insight.
- **Dont store raw transcripts without synthesis.** Raw transcripts are not findable or usable. The repository should contain synthesized insights with links to raw data, not raw data alone.
- **Dont allow free-text tagging without controlled vocabulary.** Free-text tags produce synonyms and near-synonyms ("onboarding" and "on-boarding" and "new user setup") that prevent accurate retrieval. Use a controlled tag list.
- **Dont neglect the confidence level tag.** An insight from a single interview and an insight validated across 15 interviews deserve very different weight in decision-making. Confidence level tagging makes this explicit.
- **Dont build the repository for researchers only.** The most valuable use of a research repository is when product managers, marketers, and sales leaders can search it directly. Design for their search behavior, not just researcher behavior.
- **Dont let insights go stale without flagging them.** Markets change. Customer needs evolve. An insight from 3 years ago may be actively misleading today. Build a status tag (current / review needed / outdated) and a review cadence.
- **Dont require perfection before launching.** A repository with 30 well-tagged insights is more valuable than a perfectly designed empty system. Start small, enter real insights, and improve the system based on actual use.

---

## Ideal Inputs

### Required
```
1. RESEARCH VOLUME AND TYPES
   How many studies per quarter?
   What research methods are used? (Interviews, surveys, usability tests,
   NPS, competitive research, desk research)

2. TEAM SIZE AND COMPOSITION
   How many people conduct research?
   How many people consume research insights?
   Who has time to maintain the repository?

3. PRIMARY USE CASES
   What are the most common retrieval scenarios?
   Who searches for what, and when?
   Example: "PM searching for insights about onboarding before designing a new flow."

4. EXISTING DOCUMENTATION PRACTICES
   What tools do you currently use to store research notes?
   How are studies currently documented?
   What is already working and what is not?

5. TOOL PREFERENCE OR CONSTRAINTS
   Is there a preferred tool or an existing tool in use?
   Any cost or IT constraints?
```

### Optional but Valuable
```
6. EXISTING RESEARCH BACKLOG
   How many prior studies exist that should be backfilled into the repository?
   In what condition is the existing documentation?

7. CUSTOMER SEGMENT TAXONOMY
   How do you currently segment your customers?
   The customer tags should match the company's segment definitions.

8. PRODUCT AREA TAXONOMY
   How is the product organized into areas or domains?
   Product area tags should match the team's current product structure.

9. INTEGRATION REQUIREMENTS
   Should the repository connect to other tools?
   (CRM for participant records, product analytics for behavioral data,
   Jira for connecting insights to tickets, Slack for insight alerts)

10. GOVERNANCE MODEL
    Will there be a central repository owner?
    Or will it be maintained collectively?
    What quality review process is needed?
```

### Example of a Strong Input Prompt
```
Research volume: 6 to 8 studies per quarter (mix of customer interviews,
NPS follow-ups, usability tests, and competitive research).
Team: 1 UX researcher (full time), 2 PMs who conduct ad hoc interviews,
1 CS analyst who runs VoC synthesis. Repository will be read by entire
product team (8 people) and occasionally by sales and marketing.
Primary use cases:
- PM starting a new feature: "Has anyone researched pain in the [area]?"
- Researcher planning a new study: "What do we already know about this question?"
- Leadership briefing: "What does our research say about why customers value compliance?"
- New team member onboarding: "What are the most important things we know about our customers?"
Current state: All research lives in Google Drive with inconsistent naming.
No tagging. Hard to find anything older than 3 months.
Tool preference: Would like to stay in Notion if possible. Already using it for team wiki.
Backlog: Approximately 20 studies over the past 2 years, varying documentation quality.
Customer segments: We have 4 defined segments (single-location, multi-location,
food service, and enterprise chain).
Integration: Would like Slack notification when new insights are tagged to priority topics.
```

---

## Output Format

```
1. REPOSITORY ARCHITECTURE
   Overview of the repository structure: databases and how they connect.
   Study database, insight database, participant database, tag library.
   Relationship diagram showing how entries link to each other.

2. TAGGING TAXONOMY
   Complete controlled tag vocabulary organized by dimension:
   Topic tags (hierarchical: domain > sub-domain)
   Customer type tags
   Research method tags
   Confidence level tags (with definitions for each level)
   Product area tags
   Decision type tags
   Status tags (current / review needed / outdated)
   Instructions for applying tags: how many per entry, ambiguity resolution.

3. ENTRY TEMPLATES

   Study entry template:
   Study name, date, lead researcher, method, participant count,
   research questions, key findings (summary), insights generated (links),
   full synthesis document (link), raw data location (link), status.

   Insight entry template:
   Insight statement (one sentence), supporting evidence (2 to 4 sentences),
   source study, date, participant count supporting this insight,
   all applicable tags, confidence level, status, related insights (links).

   Participant entry template:
   Participant ID (anonymized or named per consent), company, role,
   segment, studies participated in with dates, contact status,
   do-not-contact flag, notes.

4. RETRIEVAL PROTOCOL
   How to search before starting new research.
   Search strategies by use case: by topic, by segment, by recency,
   by confidence level.
   What to do when no relevant insights are found.

5. MAINTENANCE PROTOCOLS
   Weekly: new entries from completed studies and interviews.
   Monthly: status review for aging insights.
   Quarterly: taxonomy review and pruning.
   Annual: full repository audit and confidence level reassessment.

6. ONBOARDING GUIDE
   How to introduce new team members to the repository.
   The core search behaviors to establish as habits.
   Who to contact for taxonomy questions.

7. BACKFILL PLAN (if prior research exists)
   Prioritization approach for backfilling existing studies.
   Minimum viable entry standard for backfill vs. full entry.
   Time estimate for backfill effort.

8. GOVERNANCE MODEL
   Repository owner responsibilities.
   Quality review process for new entries.
   Process for proposing and approving new tags.
   Escalation path for conflicting insight classifications.
```

---

## Starter Prompt

```
You are a research operations specialist helping me design a research repository
that makes insights findable, reusable, and compounding over time.

Research volume and types: [studies per quarter and methods used]
Team composition: [who conducts research, who consumes it, who will maintain it]
Primary retrieval use cases: [the most common scenarios where someone searches the repository]
Current state: [how research is currently stored and what is not working]
Tool preference: [Notion / Airtable / Dovetail / other]
Existing backlog: [prior studies that need backfilling]
Customer segment taxonomy: [how you currently define customer segments]
Product area taxonomy: [how the product is organized into domains]
Integration needs: [connections to other tools]
Governance model: [centralized owner or collective maintenance]

Please produce:
1. A repository architecture showing the databases and their relationships
2. A complete tagging taxonomy with controlled vocabulary across all dimensions
3. Entry templates for studies, insights, and participants
4. A retrieval protocol for the most common search scenarios
5. Weekly, monthly, quarterly, and annual maintenance protocols
6. An onboarding guide for new team members
7. A backfill plan if prior research exists
8. A governance model with owner responsibilities and quality review process

Design for retrieval, not storage. The test of a good repository is not how
much it contains but how quickly a user can find what they need.
If the entry process is too complex for busy researchers to complete in 15 minutes,
recommend simplifications.
```

---

## Related Skills

| Use This Next | Why |
|---|---|
| `voice-of-customer.md` | VoC synthesis outputs populate the repository |
| `primary-research-plan.md` | New studies are planned with reference to existing repository findings |
| `research-synthesis-report.md` | Synthesis reports generate the insights entered into the repository |
| `affinity-mapping.md` | Affinity mapping produces the insight clusters entered as repository records |

| Use This Before | Why |
|---|---|
| `customer-discovery-interview.md` | Repository search should precede new interview design |
| `market-opportunity-analysis.md` | Repository search for existing market insights should precede new market analysis |

---

## Repository Tool Comparison

| Tool | Best For | Strengths | Limitations |
|---|---|---|---|
| Notion | Small to mid teams already using Notion | Flexible, linked databases, free tier | Not purpose-built, search can be slow |
| Airtable | Teams needing structured data and views | Powerful filtering, relational data | Less natural for long-form text |
| Dovetail | Dedicated research functions | Purpose-built, tagging, search, analysis | Cost, overkill for small teams |
| EnjoyHQ / Aurelius | Mid-size research teams | Research-specific features | Less widely used, integration limits |
| Google Drive + Sheets | Very small teams, low volume | Free, familiar | No relational tagging, search is weak |

---

*Skill file version: 1.0 | Phase: 01 - Ideation and Market Research | Company type: Product*
