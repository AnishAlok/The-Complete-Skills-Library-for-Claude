# dependency-mapping.md

> **Skill:** Produces a cross-team dependency map that identifies which teams depend on which other teams to deliver their planned work, with timelines, owners, and risk flags.

---

## TLDR

Dependency mapping surfaces the cross-team dependencies that can derail a plan: Team A cannot ship until Team B delivers X, which depends on Team C completing Y. This skill produces a structured dependency document that makes implicit dependencies explicit, assigns owners, and flags the critical path risks before planning begins.

---

## Topic Explanation

### Why Dependencies Kill Plans

Undiscovered dependencies are among the top causes of missed delivery timelines. When a team discovers mid-quarter that their work depends on another team's output that was not planned, they face three choices: slip the timeline, descope, or request an unplanned investment from the other team. All three are bad. Dependency mapping before planning prevents this.

### Types of Dependencies

**Technical dependencies:** Team A's feature requires an API or service owned by Team B.
**Design dependencies:** Multiple teams need the same design system component that does not yet exist.
**Data dependencies:** A feature requires data produced by a pipeline owned by another team.
**Compliance/legal dependencies:** A feature requires legal or compliance review that must happen in sequence.
**External dependencies:** A vendor, partner, or customer must deliver something before work can proceed.

### Critical Path Analysis

The critical path is the sequence of dependent tasks that determines the minimum total delivery time. A delay in any critical path item delays the final delivery. Non-critical-path items have "float": they can be delayed without affecting total delivery time.

Dependency mapping produces the information needed for critical path analysis. Identify the longest chain of dependencies and flag it as the critical path.

---

## Output Format

```
1. DEPENDENCY MAP HEADER
   Teams included, planning period, date, owner.

2. DEPENDENCY REGISTRY
   For each dependency:
   - ID
   - Dependent team (who needs the deliverable)
   - Dependency team (who must provide it)
   - Deliverable description
   - Needed by date
   - Committed delivery date
   - Status: Confirmed / Pending / At-risk / Blocked
   - Owner at dependency team
   - Risk level: High / Medium / Low

3. DEPENDENCY DIAGRAM
   Visual or text-based representation showing dependency chains.
   Critical path highlighted.

4. CRITICAL PATH ANALYSIS
   The sequence of dependencies that determines the minimum delivery timeline.
   Items on the critical path flagged.
   Float available for non-critical items.

5. AT-RISK DEPENDENCIES
   Dependencies flagged as at-risk or unconfirmed.
   Why they are at risk.
   Mitigation options.

6. ACTIONS REQUIRED
   Conversations that must happen.
   Commitments that must be obtained.
   Owner and deadline for each.

7. ESCALATION LOG
   Dependencies that could not be resolved at the team level.
   Escalation path and status.
```

---

## Starter Prompt

```
You are a product manager mapping cross-team dependencies for a planning cycle.

Teams involved: [list of teams and what each is building]
Planning period: [quarter or time period]
Known dependencies: [cross-team dependencies already identified]
External dependencies: [vendor, partner, or customer dependencies]
Delivery deadlines: [key dates that must be met]

Produce a complete dependency map including registry, critical path analysis,
and at-risk dependency escalation plan.
```

---

*Skill file version: 1.0 | Phase: 02 - Product Management | Company type: Product*
