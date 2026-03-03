# data-dictionary.md

> **Skill:** Produces a data dictionary that defines every field, metric, and dimension in a data warehouse or analytics system with precise business definitions, calculation logic, and governance information.

---

## TLDR

A data dictionary is the authoritative reference for what every piece of data in an analytics system means: field names, business definitions, calculation logic, data types, sources, and governance rules. It prevents the most common analytics dysfunction: two analysts calculating "active users" differently because no canonical definition exists.

---

## Topic Explanation

### Why Data Dictionaries Prevent Metric Drift

Without a data dictionary, metrics drift: different teams define the same concept differently and produce conflicting numbers. "Monthly Active Users" means daily unique visitors to one team and users who completed a core action to another. Both numbers are internally consistent but they are different metrics with the same name.

A data dictionary with canonical definitions eliminates this by establishing one definition per metric that all teams use. When someone challenges a number, the dictionary is the arbiter.

### Metric Definition Quality

A good metric definition includes:
- **Business definition:** What does this metric represent in business terms?
- **Calculation:** The exact formula or SQL logic
- **Inclusions:** What is counted
- **Exclusions:** What is explicitly not counted and why
- **Edge cases:** How unusual situations are handled
- **Governance:** Who owns the definition and how changes are made

A metric definition that omits inclusions, exclusions, or edge cases will produce different results depending on the implementer's assumptions.

### Managed vs. Derived Metrics

**Managed (source-of-truth) metrics:** Defined in a central metric layer (dbt metrics, Looker LookML). Calculated consistently everywhere they appear.

**Derived metrics:** Calculated by analysts from source tables. Higher risk of inconsistency.

The data dictionary should distinguish which metrics are managed centrally and which are analyst-calculated, and where the canonical calculation lives.

---

## Output Format

```
1. DICTIONARY HEADER
   Product, data platform, version, date, analytics owner.
   How to propose changes or corrections.

2. DOMAIN SECTIONS
   Organized by business domain: Users, Revenue, Product, Marketing, etc.

3. METRIC DEFINITIONS

   For each metric:
   - Name: exact name as used in reports and dashboards
   - Alias(es): other names this metric appears under
   - Category: acquisition / activation / retention / revenue / referral
   - Business definition: what this metric measures in plain language
   - Calculation: exact formula or SQL
   - Unit: count / percentage / currency / duration
   - Inclusions: what is counted
   - Exclusions: what is explicitly not counted
   - Edge cases: how special situations are handled
   - Source table(s): where the data comes from
   - Grain: one row = one [user/event/day]
   - Update frequency: real-time / hourly / daily / weekly
   - Owner: team responsible for this metric
   - Status: active / deprecated / proposed

4. DIMENSION DEFINITIONS

   For each dimension used for segmentation:
   - Name and description
   - Values: enum list or range
   - How it is set
   - Null handling

5. EVENT DEFINITIONS
   Key analytics events with field-level definitions.
   Cross-reference to tracking plan.

6. FIELD-LEVEL DICTIONARY
   For each table column:
   - Field name, data type, description, example value, nullable.

7. CALCULATION GLOSSARY
   Common calculation patterns and conventions:
   - How rates are calculated (rate = X / Y * 100)
   - How periods are defined (month = calendar month)
   - How time zones are handled

8. CHANGE LOG
   Metric definition changes with date, change description, and author.
```

---

## Starter Prompt

```
You are a data analyst building a data dictionary.

Business domain: [what part of the business]
Metrics to define: [list of metrics with their intended meaning]
Key dimensions: [segmentation dimensions]
Source tables: [where data comes from]
Known inconsistencies: [metrics currently defined differently in different places]
Calculation conventions: [how rates, periods, time zones are handled]

Produce a complete data dictionary with precise metric definitions including
calculation logic, inclusions, exclusions, and edge cases.
Flag any metric whose definition would produce different results depending on
implementation assumptions.
```

---

*Skill file version: 1.0 | Phase: 06 - Data and Analytics | Company type: Product*
