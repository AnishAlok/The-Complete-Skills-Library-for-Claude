# microcopy-doc.md

> **Skill:** Produces approved UI copy for labels, button text, error messages, empty states, tooltips, placeholder text, confirmation dialogs, and other interface text for a specific feature or product area.

---

## TLDR

Microcopy is the small-scale UI text that directly guides user action: button labels, error messages, empty states, tooltips, confirmations, and placeholder text. This skill produces approved, on-brand, specific microcopy for a defined feature area, following UX writing guidelines and accessibility standards.

---

## Topic Explanation

### Why Microcopy Is Disproportionately Important

Microcopy is often written last and given least attention. It has disproportionate impact for two reasons:

**It appears at decision moments.** Button labels, error messages, and confirmation dialogs appear exactly when users are deciding what to do next. Copy that is ambiguous, misleading, or alarming at these moments causes errors, abandonment, and support tickets.

**It is the voice of the product at its most direct.** A product's personality is most visible in how it handles errors, empty states, and confirmations. "Oops! Something went wrong." and "Unable to save. Please try again." say very different things about the product's personality and the team behind it.

### Error Message Structure

Well-written error messages have three components:
1. **What happened:** In plain language, without blaming the user.
2. **Why it happened (if useful):** Only if this helps the user resolve the issue.
3. **What to do:** A specific, actionable next step.

Bad: "Error 403. Access denied."
Good: "You don't have permission to view this report. Contact your admin to request access."

Bad: "Invalid input."
Good: "Enter your start date in MM/DD/YYYY format."

### Empty State Types

Empty states are not all the same. There are four distinct empty state situations, each requiring different copy:

**First use:** The user has just signed up and nothing is here yet. Opportunity to explain the value and guide first action. Tone: welcoming, encouraging.

**User-cleared:** The user has done something (completed all tasks, deleted all items). The emptiness is their achievement. Tone: affirming, what's next.

**No results:** A search or filter returned nothing. Give options to broaden the search or check for errors. Tone: helpful, calm.

**Error:** Something failed. Explain what happened and what to do. Tone: clear, direct, not alarming.

---

## Output Format

```
1. MICROCOPY DOCUMENT HEADER
   Feature or product area, version, writer, reviewer, date.
   Link to UX writing guidelines.

2. BUTTON AND ACTION LABELS
   For each action in the feature:
   - Action description
   - Approved label
   - Rationale (if not obvious)
   - Variants: short version for constrained contexts

3. HEADINGS AND TITLES
   Page/view headings.
   Modal and dialog titles.
   Section headings.

4. FORM LABELS AND HELPER TEXT
   For each form field:
   - Label
   - Placeholder text (sparingly; not a replacement for labels)
   - Helper/hint text
   - Validation requirements

5. ERROR MESSAGES
   For each error condition:
   - Trigger condition
   - Error message (what happened / what to do)
   - Tone note if context-specific

6. SUCCESS AND CONFIRMATION MESSAGES
   For each success condition:
   - Trigger
   - Message copy
   - Duration (if it auto-dismisses)

7. EMPTY STATES
   For each empty state type (first use, user-cleared, no results, error):
   - Heading
   - Body copy
   - Call to action label

8. TOOLTIPS AND CONTEXTUAL HELP
   For each tooltip:
   - UI element it is attached to
   - Tooltip copy (brief, specific, single-sentence)

9. CONFIRMATION DIALOGS
   For each destructive or irreversible action:
   - Dialog title
   - Body explanation
   - Confirm button label
   - Cancel button label

10. NOTIFICATIONS AND TOASTS
    For each notification type:
    - Trigger condition
    - Message copy
    - Action label (if actionable)
```

---

## Starter Prompt

```
You are a UX writer producing microcopy for a product feature.

Feature: [what feature area this copy covers]
User type: [who uses this feature]
Brand voice: [the voice qualities to express, e.g., direct, warm, professional]
Actions to label: [the actions in the feature]
Form fields: [the form fields and their purposes]
Error conditions: [the error states that can occur]
Empty state types: [which empty states need copy]
Confirmation dialogs: [destructive actions requiring confirmation]
Writing guidelines reference: [link or key principles from UX writing guidelines]

Please produce complete approved microcopy for all UI elements in this feature including:
buttons, headings, form labels, helper text, error messages, success messages,
empty states, tooltips, and confirmation dialogs.
For each error message: include what happened, why (if useful), and what to do.
For each empty state: distinguish between first-use, user-cleared, no-results, and error types.
```

---

## Related Skills

| Use This Next | Why |
|---|---|
| `ux-writing-guidelines.md` | Microcopy follows the principles and terminology in the writing guidelines |
| `design-spec.md` | Approved microcopy feeds into the component spec |
| `design-handoff-doc.md` | Microcopy doc is referenced in the engineering handoff |

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
