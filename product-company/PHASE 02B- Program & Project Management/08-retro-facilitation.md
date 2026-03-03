# retro-facilitation.md

> **Skill:** Produces a retrospective facilitation guide with format options, facilitation script, output template, and action item tracking for agile team retrospectives.

---

## TLDR

A well-facilitated retrospective is the primary mechanism for continuous team improvement. This skill produces a facilitation guide covering format selection, time allocation, facilitation script, output documentation, and action item tracking. Used by Scrum Masters, PMs, or team leads facilitating sprint or project retrospectives.

---

## Topic Explanation

### The Prime Directive

Norm Kerth's retrospective prime directive should be read at the start of every retro: "Regardless of what we discover, we understand and truly believe that everyone did the best job they could, given what they knew at the time, their skills and abilities, the resources available, and the situation at hand."

This framing removes blame and makes honest reflection possible. Without it, retros devolve into complaint sessions or diplomatic avoidance.

### Retrospective Format Options

**Start / Stop / Continue:** Simple. Good for teams new to retros. Covers: what should we start doing? What should we stop? What should we keep? Works best for operational topics.

**Four L's (Liked / Learned / Lacked / Longed For):** More reflective. Good for end-of-project or mid-project check-ins. Uncovers learning and aspirations.

**Mad / Sad / Glad:** Emotionally accessible. Good for teams experiencing tension or stress. Opens up feelings that more analytical formats miss.

**Sailboat / Speed Boat:** Visual metaphor. Wind (what propels us), Anchors (what holds us back), Rocks (risks ahead), Sun (the goal). Good for visual thinkers and creating shared direction.

**5 Whys on a specific incident:** Root cause analysis format for addressing a specific process failure. Good when a particular problem needs deep diagnosis.

Choose the format based on the team's current situation, not habit. A team dealing with burnout needs a different format than a team whose last sprint went well.

### Action Item Quality

The most common retrospective failure is generating action items that are vague, unowned, and never completed. Quality action items are:
- Specific: "Write a testing checklist for API integrations" not "improve testing"
- Owned: One named person responsible
- Time-bound: A due date, not "soon"
- Reviewed: Checked at the next retrospective for completion

---

## Output Format

```
1. RETRO FACILITATION GUIDE

   FORMAT: [selected format with rationale]
   DURATION: [total time]
   PARTICIPANTS: [who attends]

2. PRE-RETRO SETUP
   Room or virtual tool setup.
   Prime directive display.
   Anonymous input mechanism if needed.
   Previous action item review.

3. FACILITATION SCRIPT

   OPENING (5 minutes)
   - Read prime directive
   - State the purpose and format
   - Set working agreements

   DATA GATHERING PHASE ([time] minutes)
   - Individual reflection: each person adds their items silently
   - Format-specific prompts

   GROUPING AND DISCUSSION PHASE ([time] minutes)
   - Group similar items
   - Vote or dot-prioritize to surface top items
   - Discussion: dig into top items with time limits per topic

   ACTION ITEM PHASE ([time] minutes)
   - Identify 2 to 4 specific, owned, time-bound action items
   - Review format: what good looks like

   CLOSE (5 minutes)
   - ROTI (Return on Time Invested) quick rating
   - Thank the team

4. RETROSPECTIVE OUTPUT DOCUMENT
   Date, sprint, attendees, facilitator.
   Format used.
   All items generated organized by category.
   Themes identified from discussion.
   Top 2 to 4 action items: description / owner / due date.
   Previous action items: status (completed / in progress / dropped).

5. ACTION ITEM TRACKER
   Running log across retros:
   Item / Owner / Created in sprint / Due / Status
```

---

## Starter Prompt

```
You are facilitating a sprint or project retrospective.

Team context: [the team and any relevant context about the sprint or project]
Current team situation: [any specific issues or tensions to be aware of]
Format preference: [specific format or ask for recommendation]
Time available: [total retro duration]
Previous action items: [any outstanding items from prior retros]

Produce a complete facilitation guide including:
1. Format recommendation with rationale for this team's situation
2. Time-boxed facilitation script
3. Facilitation prompts for each phase
4. Output document template
5. Action item quality criteria

Include the prime directive and opening working agreements.
Flag any facilitation trap specific to this team's context.
```

---

*Skill file version: 1.0 | Phase: 04 - Program and Project Management | Company type: Product*
