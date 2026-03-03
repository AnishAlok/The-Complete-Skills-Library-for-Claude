# service-blueprint.md

> **Skill:** Produces a service blueprint documenting both the front-stage customer experience and the back-stage organizational processes, people, systems, and support activities that enable and constrain it.

---

## TLDR

A service blueprint extends the journey map by adding the organizational view: what happens behind the scenes to make the customer experience possible. It shows where front-stage experience and back-stage operations are misaligned, revealing the root causes of service failures and opportunities for operational improvement. Used for service design, operational redesign, and cross-functional alignment.

---

## Topic Explanation

### The Five Components of a Service Blueprint (Shostack and Bitner)

**Customer actions:** What the customer does at each step.

**Front-stage employee actions / system interactions:** What the customer-facing employee or digital interface does that the customer can see and experience.

**Line of visibility:** The boundary between what customers see and what they do not. Below this line is invisible to customers.

**Back-stage actions:** Actions by employees or systems that the customer does not directly see but that directly support the front-stage experience.

**Support processes:** Internal systems, policies, and processes that enable back-stage actions. Usually the root cause of front-stage failures.

**Physical evidence:** The tangible artifacts the customer encounters (emails, invoices, interfaces, packaging).

### Why Service Blueprints Reveal Root Causes

Most customer experience problems have their root cause below the line of visibility. A customer experiences a slow response to a support ticket (front-stage pain). The root cause may be a support escalation workflow, a ticketing system misconfiguration, or a staffing policy (back-stage or support process). The journey map captures the symptom. The service blueprint reveals the cause.

### When to Use Service Blueprints

Service blueprints are most valuable for:
- Services with significant human interaction (not just digital products)
- Experiences that span multiple channels or teams
- Post-launch operations improvement
- Redesigning a service from end to end

For purely digital products with no human-facing service component, the service blueprint collapses back toward a journey map. Use judgment about when the back-stage view adds meaningful insight.

---

## Output Format

```
1. BLUEPRINT HEADER
   Service being mapped, customer type, scenario, date, scope.

2. BLUEPRINT STRUCTURE (vertical axis: swim lanes / horizontal axis: time)

   Swim lanes from top to bottom:
   - Physical evidence (what customer sees/touches)
   - Customer actions
   --- LINE OF INTERACTION (customer meets service) ---
   - Front-stage visible contact (employee or interface actions)
   --- LINE OF VISIBILITY ---
   - Back-stage invisible contact (employee actions behind the scenes)
   --- LINE OF INTERNAL INTERACTION ---
   - Support processes (systems, policies, internal workflows)

3. FAILURE POINTS
   Moments where back-stage process failures manifest as front-stage pain.
   Evidence and frequency of each failure.

4. WAIT TIMES AND BOTTLENECKS
   Where delays occur and why.

5. CROSS-FUNCTIONAL OWNERSHIP MAP
   Which team owns each swim lane and each failure point.

6. REDESIGN OPPORTUNITIES
   Specific process or system changes that would improve the customer experience.
   Prioritized by customer impact and operational feasibility.
```

---

## Starter Prompt

```
You are a service designer building a service blueprint.

Service being mapped: [what service or customer experience]
Customer scenario: [the specific customer goal and touchpoints]
Known failure points: [where the service breaks down]
Front-stage touchpoints: [customer-facing interfaces and interactions]
Back-stage systems and teams: [the operational infrastructure that supports them]
Purpose: [operational redesign / cross-functional alignment / root cause analysis]

Produce a complete service blueprint showing all swim lanes, the lines of
interaction and visibility, failure points with root causes, and prioritized
redesign opportunities.
```

---

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
