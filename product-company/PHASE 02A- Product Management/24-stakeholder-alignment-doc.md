# stakeholder-alignment-doc.md

> **Skill:** Produces a stakeholder alignment document that maps stakeholders, their interests and concerns, the decisions requiring alignment, and the communication and engagement plan needed to build and maintain cross-functional alignment.

---

## TLDR

Stakeholder alignment is not a one-time event. It is an ongoing process of understanding who needs to be aligned, on what, and through what engagement. This skill produces a structured alignment document that maps stakeholders, defines alignment goals, and plans the communication and engagement needed to keep cross-functional teams moving in the same direction.

---

## Topic Explanation

### Why Alignment Breaks Down

Alignment is not the absence of disagreement. It is shared understanding of goals, priorities, and tradeoffs, even when people disagree on specific decisions. Alignment breaks down when:
- Teams have different mental models of what the product is trying to accomplish
- Decisions are made by one team and communicated too late for others to incorporate them
- Stakeholders feel they were not consulted on decisions that affect them
- Communication is inconsistent: different stakeholders receive different information

A stakeholder alignment document prevents all four failure modes by making explicit who needs to know what, when, and through what channel.

### Stakeholder Mapping

The standard two-axis stakeholder map:
- **Power / Influence:** How much authority does this stakeholder have over the initiative?
- **Interest / Involvement:** How involved are they in or affected by the initiative?

Four quadrants:
- High power, high interest: **Key stakeholders.** Engage closely. Keep fully informed.
- High power, low interest: **Keep satisfied.** Inform regularly but do not burden with operational detail.
- Low power, high interest: **Keep informed.** May be advocates or detractors. Engage transparently.
- Low power, low interest: **Monitor.** Minimal effort required.

---

## Output Format

```
1. INITIATIVE CONTEXT
   What initiative is this alignment document for?
   Why alignment is needed now.

2. STAKEHOLDER MAP
   For each stakeholder:
   - Name and role
   - Power level: High / Medium / Low
   - Interest level: High / Medium / Low
   - Quadrant: Key / Keep satisfied / Keep informed / Monitor
   - Primary concern or interest in this initiative
   - Current alignment status: Aligned / Neutral / Misaligned / Unknown

3. DECISIONS REQUIRING ALIGNMENT
   For each key decision:
   - Decision description
   - Decision owner (who decides)
   - Stakeholders who must be consulted
   - Stakeholders who must be informed
   - Timeline for decision
   - Status: Decided / In discussion / Pending

4. CONCERNS AND OBJECTIONS
   For each stakeholder with concerns:
   - Their concern or objection
   - Root cause of the concern
   - Planned response or mitigation

5. ENGAGEMENT AND COMMUNICATION PLAN
   For each stakeholder group:
   - Communication channel and format
   - Frequency
   - Content: what they need to know
   - Owner of the communication

6. ALIGNMENT MILESTONES
   Key points where alignment must be confirmed before proceeding.
   What "confirmed alignment" looks like at each milestone.

7. ESCALATION PROTOCOL
   How unresolved misalignment will be escalated.
   Who has authority to resolve it.
   Timeline.
```

---

## Starter Prompt

```
You are a product manager building a stakeholder alignment document.

Initiative: [what you are trying to align stakeholders on]
Stakeholders: [list of people or teams who need to be aligned]
Key decisions: [the decisions that require cross-functional input or approval]
Known concerns: [any existing misalignment or objections]
Communication constraints: [meeting cadences, communication channels available]

Produce a complete stakeholder alignment document including stakeholder map,
decision inventory, concern analysis, engagement plan, and escalation protocol.
```

---

*Skill file version: 1.0 | Phase: 02 - Product Management | Company type: Product*
