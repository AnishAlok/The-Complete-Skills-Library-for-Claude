# launch-plan.md

> **Skill:** Produces a product launch plan with workstreams, named owners, milestones, a launch day runbook, and success metrics for coordinating a cross-functional product launch.

---

## TLDR

A launch plan is the master coordination document for bringing a product or major feature to market: every workstream, every owner, every dependency, every milestone from T-12 weeks to launch day and 30 days post. It aligns cross-functional teams, surfaces risks while there is still time to act, and ensures nothing critical is missed in the weeks before release.

---

## Topic Explanation

### Launch Tiers

Not all launches deserve the same investment. Tiering by expected impact prevents over-spending on minor releases and under-spending on major ones.

**Tier 1 (Major launch):** New product, new category, or transformational feature set. Full investment: PR, paid media, analyst briefings, sales enablement, event activation. 8 to 12 weeks of preparation minimum.

**Tier 2 (Significant launch):** Important feature or meaningful product improvement. Blog post, customer email, social assets, sales briefing, in-app announcement. 4 to 6 weeks.

**Tier 3 (Minor launch):** Incremental improvements, fixes, small additions. In-product notification, release notes, internal update. 1 to 2 weeks.

Tier decisions should be made at the beginning of the launch process, not after work has already started.

### The Launch Paradox

The team that has been building the product for six months experiences launch day as the end of a long project. Customers experience it as the beginning of something they are just learning about.

This means launch day activities must be optimized for customer discovery and initial adoption, not internal celebration. The metrics that matter are customer-facing: trial signups, demos booked, product activations. Not press mentions counted or social likes.

### Pre / During / Post Structure

**Pre-launch (T-12 to T-1 weeks):** Positioning and messaging finalized, assets created, sales trained, press embargo managed, analyst briefings completed, customer early access program run.

**Launch week (T-0):** Announcements executed in coordinated sequence, PR live, email sent, paid media activated, sales outreach begins, monitoring and rapid response for issues.

**Post-launch (T+1 to T+12 weeks):** Demand generation running, customer stories collected, metrics reviewed, iteration based on early data.

---

## Dos

- **Do assign a single named owner to every deliverable.** Joint ownership is no ownership. When something slips, one person is accountable.
- **Do run a pre-launch readiness review at T-2 weeks.** Surface problems while there is still time to fix them rather than discovering them on launch day.
- **Do write the launch day runbook before launch week.** A detailed schedule of who publishes what and when prevents chaos and missed sequencing.

---

## Donts

- **Dont let launch planning start with tactics.** "We should do a webinar" is not a launch plan. Start with objectives and audience, then derive the activities.
- **Dont declare success on launch day.** Day-one metrics are vanity. The meaningful signal is week-two and week-four adoption and retention behavior.

---

## Output Format

```
1. LAUNCH PLAN HEADER
   Product/feature, launch date, launch tier, PMM lead.
   Stakeholder list with roles: product, engineering, sales, CS, PR, demand gen, legal.

2. LAUNCH OBJECTIVES
   Primary launch metric and specific target.
   Secondary metrics with targets.
   30/60/90-day milestone targets.

3. TARGET AUDIENCE
   Primary: who the launch is aimed at with ICP details.
   Secondary: additional audiences and relevant tailored messages for each.

4. KEY MESSAGES
   The 1 to 3 messages this launch must land.
   Reference to messaging-framework.md for full approved copy.

5. WORKSTREAMS AND OWNERS

   WORKSTREAM: Product Readiness
   Owner: [name]
   Deliverables with due dates:
   - GA criteria confirmed
   - Documentation complete and reviewed
   - Support team trained with known issues documented
   - Staging environment verified

   WORKSTREAM: Positioning and Messaging
   Owner: [PMM name]
   Deliverables: positioning doc approved / messaging framework reviewed /
   all asset copy reviewed against framework

   WORKSTREAM: Sales Enablement
   Owner: [name]
   Deliverables: battlecard / demo script updated / training session completed /
   one-pager / pitch deck updated

   WORKSTREAM: Press and Analyst Relations
   Owner: [name]
   Deliverables: press release / media list / embargo managed /
   analyst briefings completed

   WORKSTREAM: Content and Creative
   Owner: [name]
   Deliverables: blog post / product video / landing page /
   social assets / screenshots / email creative

   WORKSTREAM: Email and CRM
   Owner: [name]
   Deliverables: launch email copy / audience segmentation confirmed /
   send schedule approved / test send completed

   WORKSTREAM: Customer Communications
   Owner: [name]
   Deliverables: in-app announcement / existing customer email /
   support documentation updated

   Master activity table:
   | Activity | Workstream | Owner | Due date | Status | Blockers |

6. LAUNCH TIMELINE
   T-12 weeks: [major milestones]
   T-8 weeks: [milestones]
   T-4 weeks: [milestones]
   T-2 weeks: readiness review / final checks
   T-1 week: all assets approved and staged
   Launch day: [hour-by-hour in runbook]
   T+1 week: results review
   T+4 weeks: post-launch metrics review

7. LAUNCH DAY RUNBOOK
   Hour-by-hour schedule for launch day.
   Who publishes what asset at what time and in what sequence.
   Go/no-go decision owner and criteria.
   Escalation path for launch day issues.

8. DEPENDENCIES AND RISKS
   Cross-workstream dependencies explicitly mapped.
   Top 5 risks with probability, impact, and mitigation plan.
   Open decisions that must be resolved before launch, with owners and deadlines.

9. SUCCESS METRICS AND REPORTING
   Primary metric with numeric target.
   Reporting cadence: daily for week one, weekly through day 90.
   T+7 and T+30 formal review scheduled.
```

---

## Starter Prompt

```
You are a product marketing manager writing a product launch plan.

Product/feature: [what is launching]
Launch date: [planned date or window]
Launch tier: [Tier 1 / 2 / 3]
Target audience: [who this launch is aimed at]
Key messages: [the 1 to 3 things this launch must communicate]
Teams involved: [all functions participating]
Known dependencies: [things that must happen before launch can proceed]
Primary success metric: [the one number that defines launch success]

Produce a complete launch plan covering all 9 sections.
Every deliverable must have a single named owner and specific due date.
Map all cross-workstream dependencies explicitly.
Flag every open decision that could delay or alter the launch, with a resolution deadline.
```

---

## Related Skills

| Use This Before | Why |
|---|---|
| `gtm-strategy.md` | GTM strategy defines the motion this plan executes |
| `messaging-framework.md` | Approved messaging must exist before launch assets are created |

*Skill file version: 1.0 | Phase: 08 - Product Marketing | Company type: Product*
