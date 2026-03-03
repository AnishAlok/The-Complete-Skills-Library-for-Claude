# escalation-protocol.md

> **Skill:** Produces an escalation protocol that defines when to escalate, to whom, through what channel, with what information, and in what timeframe for project issues and risks.

---

## TLDR

An escalation protocol answers: *"When a problem exceeds my authority to resolve, who do I go to, how, and with what information?"* Without a defined protocol, escalations are ad hoc, delayed, and often reach the wrong person with incomplete context. This skill produces an escalation framework that enables fast, effective escalation while maintaining appropriate stakeholder relationships.

---

## Topic Explanation

### Why Escalations Fail

The three most common escalation failures:

**Under-escalation:** The PM absorbs a problem that exceeds their authority to resolve. They manage it as best they can, the problem grows, and by the time it is escalated it is a crisis rather than an issue.

**Over-escalation:** The PM escalates every decision to leadership, creating noise and demonstrating an inability to manage independently. This erodes credibility and creates leadership fatigue.

**Poorly framed escalation:** The right person is reached but without enough context to make a decision. "We have a problem with the API vendor" is not an escalation. "The API vendor has failed to deliver the authentication module by the committed date, which blocks the launch by 3 weeks unless we approve an emergency contract modification. I need your approval on the contract change by Thursday."

### Escalation Thresholds

Every organization needs clearly defined escalation thresholds:
- Budget variance beyond X% requires VP approval
- Schedule variance beyond Y weeks requires sponsor escalation
- Any security or compliance issue is immediately escalated to [role]
- Vendor disputes above $Z require legal involvement

Without defined thresholds, escalation decisions are made by individual judgment, which produces inconsistency and organizational anxiety.

### The Escalation Brief

Every escalation should arrive pre-packaged with four elements:
1. **Situation:** What happened or what is at risk
2. **Impact:** What is the consequence if unresolved and the timeline for that consequence
3. **Options:** What are the choices and what the PM recommends
4. **Ask:** What specific decision or action is needed from the escalation recipient

An escalation that arrives with these four elements can be acted on immediately. One that arrives without them requires a back-and-forth that consumes time neither party has.

---

## Output Format

```
1. ESCALATION PROTOCOL HEADER
   Project/program, PM, sponsor, escalation path, version, date.

2. ESCALATION MATRIX
   Columns: Issue type / Threshold / First escalation point / Secondary escalation /
   Timeframe to escalate / Channel
   
   Rows by issue type:
   - Budget variance
   - Schedule variance
   - Scope change
   - Vendor dispute
   - Resource conflict
   - Security/compliance issue
   - Stakeholder conflict
   - Technical blocker

3. ESCALATION PATH DIAGRAM
   Who escalates to whom and in what sequence.
   Bypass conditions: when to skip levels.

4. ESCALATION BRIEF TEMPLATE
   Situation: [what happened or what is at risk]
   Impact: [consequence and timeline]
   Root cause: [why this occurred]
   Options: [choices available with pros/cons]
   Recommendation: [what the PM recommends]
   Ask: [specific decision or action needed, by when]
   Supporting materials: [attached documents]

5. CHANNEL GUIDANCE
   When to use: email / Slack / direct call / formal meeting request
   Response time expectations by channel.
   How to signal urgency.

6. ESCALATION LOG TEMPLATE
   Issue ID / Date raised / Issue description / Escalated to /
   Channel / Response received / Resolution / Date closed
```

---

## Starter Prompt

```
You are a PM establishing an escalation protocol.

Project/program: [context]
Sponsor: [name and role]
Escalation path: [the hierarchy above the PM]
Types of issues likely to require escalation: [project-specific issues]
Budget and schedule authority: [PM's independent authority limits]
Organizational culture: [formal or informal escalation norms]

Produce a complete escalation protocol including escalation matrix,
escalation path, brief template, channel guidance, and log template.
Define clear thresholds for each issue type.
```

---

*Skill file version: 1.0 | Phase: 04 - Program and Project Management | Company type: Product*
