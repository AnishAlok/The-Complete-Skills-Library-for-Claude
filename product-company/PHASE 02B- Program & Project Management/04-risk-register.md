# risk-register.md

> **Skill:** Produces a risk register that identifies, scores, categorizes, assigns, and tracks mitigation plans for all known project risks.

---

## TLDR

This skill helps you answer: *"What could go wrong, how bad would it be, how likely is it, and what are we doing about it?"* A risk register is the primary tool for proactive risk management: making risks visible before they become issues, assigning ownership, and tracking the mitigation actions that reduce probability or impact. Used continuously throughout a project's lifecycle.

---

## Topic Explanation

### Risk vs. Issue

A fundamental distinction that many teams blur:

**Risk:** A potential future event that may or may not occur. Managed proactively. Tracked in the risk register.

**Issue:** A problem that has already occurred and is currently affecting the project. Managed reactively. Tracked in an issue log.

The goal of risk management is to resolve risks before they become issues. When a risk occurs, it moves from the risk register to the issue log and requires an active resolution plan rather than a mitigation plan.

### Risk Scoring

Standard risk scoring uses two dimensions:

**Probability:** How likely is this risk to occur? Typically scored 1 to 5 or 1 to 3.
1 = Unlikely (< 20%), 2 = Possible (20-40%), 3 = Likely (40-60%), 4 = Very likely (60-80%), 5 = Near certain (> 80%)

**Impact:** If this risk occurs, how severely does it affect the project? Scored against cost, schedule, scope, and quality.
1 = Negligible, 2 = Minor, 3 = Moderate, 4 = Major, 5 = Critical

**Risk score:** Probability × Impact. Produces a 1-25 scale.
- 15-25: Critical risk. Requires immediate mitigation plan.
- 8-14: High risk. Requires active monitoring and mitigation.
- 4-7: Medium risk. Mitigation plan advisable.
- 1-3: Low risk. Monitor.

### Risk Response Strategies

**Avoid:** Change the project plan to eliminate the risk entirely. Example: use a proven technology instead of an unproven one to eliminate the technology risk.

**Mitigate:** Take action to reduce probability or impact. The most common strategy.

**Transfer:** Shift the risk to a third party. Example: purchase insurance, contract with a vendor who assumes the risk.

**Accept:** Acknowledge the risk and decide to proceed without taking action. Appropriate for low-score risks where the cost of mitigation exceeds the expected cost of the risk occurring.

**Escalate:** Raise to a level with authority to decide the response. Used when the risk is outside the PM's authority to address.

---

## When to Use This Skill

Use when:
- Project planning begins (initial risk identification)
- A new phase begins (risks may change)
- A significant scope or timeline change occurs
- A trigger event occurs that changes a risk's probability or impact
- Weekly project reviews (updating status and mitigation progress)

---

## Dos

- **Do assign every risk to a named owner.** A risk without an owner is an unmanaged risk.
- **Do establish trigger events for each risk.** A trigger is an early warning indicator that the risk is about to occur. Identifying triggers enables early response.
- **Do review the risk register in every project status meeting.** Risk registers that are written at project start and never reviewed are not risk management.
- **Do capture residual risk after mitigation.** Document both the inherent risk score (before mitigation) and the residual risk score (after mitigation is applied). If residual score is still high, more mitigation is needed.
- **Do add risks discovered during execution.** A risk register that only captures initial risks is incomplete. Risks are discovered throughout the project.

---

## Donts

- **Dont list generic risks that apply to every project.** "Scope creep" and "resource availability" as generic entries add no value. Specify the particular scope creep risk and the particular resource dependency.
- **Dont conflate risk and uncertainty.** Not every unknown is a risk. A risk has a directional effect: it would damage the project if it occurred. Pure uncertainty (we do not know which direction this could go) is handled differently.
- **Dont use the risk register only to demonstrate risk awareness.** The risk register's value is in the mitigation actions it drives. If no mitigation actions are being taken, the register is decorative.

---

## Output Format

```
1. RISK REGISTER HEADER
   Project name, version, date, PM, last reviewed date.
   Risk scoring criteria used (probability and impact scales).

2. RISK SUMMARY
   Total risks by category.
   Critical and high risks count.
   Risks resolved this period.
   New risks added this period.

3. RISK REGISTER TABLE
   Columns:
   Risk ID | Category | Description | Probability (1-5) | Impact (1-5) |
   Score | Response strategy | Mitigation actions | Owner | Trigger event |
   Status | Residual score | Due date | Last updated

4. RISK DETAILS (for Critical and High risks)
   For each Critical or High risk:
   - Full risk description
   - Root cause analysis
   - Mitigation plan with specific actions and owners
   - Contingency plan (if mitigation fails, what do we do?)
   - Trigger events and monitoring approach
   - Residual risk assessment

5. RISK HEAT MAP (optional visual)
   5x5 grid: Probability (y-axis) x Impact (x-axis)
   Each risk plotted by ID.
   Color zones: green (low) / yellow (medium) / orange (high) / red (critical)

6. CLOSED RISKS LOG
   Risks that have been resolved or are no longer applicable.
   How they were resolved.

7. ESCALATED RISKS
   Risks escalated to the sponsor or steering committee.
   Decision or response received.
```

---

## Starter Prompt

```
You are a project manager building a risk register.

Project context: [what the project is doing]
Project phase: [current phase]
Key risks identified: [list of risks, as specific as possible]
Risk scoring scale: [1-3 or 1-5 for probability and impact]
Team members who own risks: [the people who can own mitigation actions]
Known trigger events: [early warning indicators if known]

Please produce a complete risk register including:
1. Risk register table with all risks scored and assigned
2. Detailed mitigation plans for all Critical and High risks
3. Contingency plans for the top 3 risks by score
4. Trigger events for each risk
5. Risk summary statistics

Make every risk description specific to this project, not generic.
For each risk, include both an inherent score and a projected residual score after mitigation.
Flag any risk with a residual score above 8 as requiring additional mitigation.
```

---

## Related Skills

| Use This Next | Why |
|---|---|
| `project-plan.md` | Risk mitigation actions feed into the project plan |
| `project-status-report.md` | Top risks are reported in every project status update |
| `escalation-protocol.md` | High-severity risks may need escalation |
| `milestone-review.md` | Risk register is reviewed at each milestone |

*Skill file version: 1.0 | Phase: 04 - Program and Project Management | Company type: Product*
