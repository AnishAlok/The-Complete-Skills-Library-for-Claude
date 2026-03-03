# tracking-plan.md

> **Skill:** Produces an event tracking plan and taxonomy that defines the complete specification of product analytics events: naming conventions, event schemas, property definitions, and validation rules.

---

## TLDR

A tracking plan is the authoritative technical specification of every analytics event in a product: exact event names, property schemas with data types, when each event fires, who implements it, and the validation rules that confirm it is working correctly. It is the contract between product, engineering, and data that ensures consistent, reliable analytics instrumentation across the entire product.

---

## Topic Explanation

### Why Tracking Plans Become Critical at Scale

Small teams can manage analytics instrumentation informally. As a product grows, informal tracking creates serious problems:
- The same action is tracked with different event names in different parts of the product
- Property names are inconsistent: "user_id" in one event, "userId" in another
- Events are added without documentation; no one knows what they mean six months later
- Breaking changes to events break downstream dashboards and analyses
- Data quality issues cannot be detected without a specification to validate against

A tracking plan prevents all of these issues by establishing a formal specification that all instrumentation must conform to.

### Naming Conventions

The most widely adopted naming convention for product analytics:

**Events:** `[Object] [Action]` in title case or snake_case. "Report Exported" or "report_exported". The object is the thing being acted on; the action is what happened.
- Good: "Report Exported", "Onboarding Step Completed", "Subscription Upgraded"
- Avoid: "Click", "Page View" (too generic), "exportReportButtonClicked" (too granular)

**Properties:** snake_case. Consistent names across events where the same concept appears.
- user_id, session_id, plan_type, feature_name
- Consistent: "plan_type" everywhere, not "plan", "planType", "subscription_type" in different events

**User properties:** snake_case. Set once or updated on change.
- signup_date, company_size, plan_type, lifecycle_stage

### The Avo / Segment / Amplitude Ecosystem

Most modern analytics stacks center on a Customer Data Platform (CDP) like Segment that collects events and routes them to downstream tools. The tracking plan specification should be compatible with the team's CDP. Tools like Avo (avo.app) provide tracking plan management with type safety and auto-generated implementation code.

---

## When to Use This Skill

Use when:
- Building the initial tracking plan for a new product
- Adding a new feature area that requires new events
- Conducting an analytics audit and standardizing existing events
- Migrating to a new analytics platform

---

## Output Format

```
1. TRACKING PLAN HEADER
   Product, version, date, analytics lead, last updated.
   Analytics platform(s): Segment / Mixpanel / Amplitude / other.
   Naming convention: casing, format, principles.

2. NAMING CONVENTIONS AND STANDARDS
   Event naming: format and examples.
   Property naming: format and type standards.
   Reserved property names: properties that appear on every event.
   Prohibited patterns: what not to do with examples.

3. GLOBAL PROPERTIES (on every event)
   Properties automatically appended to every event.
   | Property | Type | Description | Example |
   | user_id | string | Authenticated user ID | "usr_abc123" |
   | session_id | string | Current session | "ses_xyz789" |
   | timestamp | ISO8601 | Event time | "2024-01-15T10:30:00Z" |
   | platform | enum | Web / iOS / Android | "web" |
   | app_version | string | Product version | "2.4.1" |

4. EVENT TAXONOMY

   Organized by product area:

   [PRODUCT AREA NAME]

   EVENT: [Event Name]
   Description: [what this event represents]
   Trigger: [exactly when this event fires]
   Frequency: [estimated fires per user per session]
   Owner: [team or engineer responsible]
   Status: [implemented / planned / deprecated]

   Properties:
   | Property | Type | Required | Enum values / format | Description |

   Example payload:
   {
     "event": "Report Exported",
     "properties": {
       "report_type": "compliance",
       "date_range_days": 30,
       "format": "pdf",
       "row_count": 1247
     }
   }

   Validation rules:
   - report_type must be one of: [compliance, payroll, tax]
   - date_range_days must be a positive integer

5. USER PROPERTIES

   | Property | Type | When set | Description | Example |

6. IDENTIFY CALLS
   When identify() is called.
   Properties sent on identify.

7. PAGE/SCREEN TRACKING
   Pages or screens tracked.
   Standard page properties.

8. DEPRECATED EVENTS
   Events that have been deprecated.
   Migration path to replacement event.
   Sunset date.

9. IMPLEMENTATION NOTES
   SDK and library to use.
   Server-side vs. client-side tracking decisions.
   Testing and QA instructions.
   How to validate events in staging.
```

---

## Starter Prompt

```
You are an analytics engineer writing a tracking plan.

Product: [name and brief description]
Analytics platform: [Segment / Mixpanel / Amplitude / other]
Product areas to cover: [the features and flows to instrument]
Events to specify: [the key events from the analytics requirements]
Naming convention: [preferred format]
Platform: [web / mobile / both]
Existing events to standardize: [any existing events that need to conform]

Produce a complete tracking plan including naming conventions,
global properties, full event taxonomy with schemas and validation rules,
user properties, and identify specification.
For each event: trigger condition, all properties with types, and example payload.
Flag any two events that appear to track the same action inconsistently.
```

---

## Related Skills

| Use This Before | Why |
|---|---|
| `analytics-requirements.md` | Requirements drive the tracking plan |

| Use This Alongside | Why |
|---|---|
| `data-dictionary.md` | Property definitions in the tracking plan feed the data dictionary |

*Skill file version: 1.0 | Phase: 06 - Data and Analytics | Company type: Product*
