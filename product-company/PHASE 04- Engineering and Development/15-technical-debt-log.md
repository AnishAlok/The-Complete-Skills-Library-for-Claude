# technical-debt-log.md

> **Skill:** Produces a technical debt tracking log that inventories known technical debt items, assesses their cost and risk, and provides a prioritized repayment plan.

---

## TLDR

A technical debt log is the engineering team's honest accounting of the shortcuts, outdated patterns, and accumulated complexity in the codebase that slow down development and create risk. It transforms unspoken frustration into a managed, prioritized backlog. Used to communicate debt to non-technical stakeholders, justify refactoring investment, and prevent debt from growing invisibly.

---

## Topic Explanation

### Types of Technical Debt

Ward Cunningham's original metaphor: technical debt is the extra work caused by choosing an easy solution now instead of a better approach that would take longer.

**Deliberate debt:** A conscious shortcut made to meet a deadline, with intent to fix later. Example: "We hardcoded the rate limits for now; we'll make them configurable in Q3."

**Inadvertent debt:** A bad decision made unknowingly. Not discovered until the codebase has grown around it. Example: a data model that made sense initially but does not scale.

**Bit rot:** Code that was once good but has become problematic as the surrounding system has evolved. The code itself has not changed; the context has.

**Complexity debt:** Code that works but is so complex it is nearly impossible to change safely.

### Measuring Debt Cost

Two dimensions:
**Cost to carry:** How much does this debt cost the team per sprint in slowed velocity, increased bugs, and cognitive load?
**Cost to repay:** How much engineering time is required to fix it?

High carry cost + high repay cost = highest priority debt.
Low carry cost + low repay cost = easy wins to clear.
High carry cost + low repay cost = do immediately.
Low carry cost + high repay cost = document but defer.

---

## Output Format

```
1. DEBT LOG HEADER
   Team, last updated, total estimated debt hours, velocity impact estimate.

2. DEBT SUMMARY
   Total items by priority.
   Estimated total repayment cost.
   Estimated monthly carry cost (velocity impact).
   Trend: growing / stable / shrinking.

3. DEBT INVENTORY

   For each item:
   - Debt ID
   - Title
   - Type: deliberate / inadvertent / bit rot / complexity
   - Description: what the debt is
   - Location: file(s) / service(s) affected
   - Origin: when and why it was introduced
   - Impact: how it slows development or creates risk
   - Carry cost: story points per sprint lost to this debt
   - Repay cost: estimated story points to fix
   - Priority: P1 (urgent) / P2 (high) / P3 (medium) / P4 (low)
   - Owner: team responsible
   - Status: open / in progress / resolved
   - Linked risks: any risk register items

4. PRIORITIZED REPAYMENT PLAN
   Quarter-by-quarter plan for debt repayment.
   Allocation recommendation: % of sprint capacity for debt repayment.
   Expected velocity improvement after each phase.

5. DEBT PREVENTION
   Engineering practices that prevent new debt accumulation.
   Definition of Done requirements that reduce inadvertent debt.
   Review gates for deliberate debt decisions.
```

---

## Starter Prompt

```
You are a tech lead building a technical debt log.

Team: [team name and service ownership]
Known debt items: [list of known technical debt with descriptions]
Velocity impact: [current estimate of debt's cost to team velocity]
Engineering capacity for debt: [% of sprint capacity available for repayment]
Time horizon: [how far out to plan repayment]

Produce a complete technical debt log with inventory, prioritization,
repayment plan, and debt prevention practices.
For each item calculate carry cost vs. repay cost to determine priority.
```

---

*Skill file version: 1.0 | Phase: 05 - Engineering | Company type: Product*
