# ux-writing-guidelines.md

> **Skill:** Produces a comprehensive UX writing guidelines document covering voice and tone principles, content hierarchy rules, terminology standards, and writing patterns for product UI copy.

---

## TLDR

This skill helps you answer: *"How should we write every word in our product, and how do we make sure everyone writes it the same way?"* It produces a UX writing guidelines document that defines voice, tone, terminology, grammar standards, and content patterns for all product copy. Used to ensure consistency across a product written by multiple contributors.

---

## Topic Explanation

### Voice vs. Tone

These terms are frequently confused and should be defined distinctly in any writing guide:

**Voice** is the consistent personality of the brand in all communication. It does not change. A voice defined as "confident, direct, and human" applies to error messages, marketing copy, and legal notices alike. Voice is brand identity expressed in language.

**Tone** is how the voice adapts to context. The same confident, direct, human voice sounds different in a congratulatory success message than in a data loss warning. Tone acknowledges the user's emotional state and adjusts accordingly, while voice remains constant.

A practical way to document this distinction: "Our voice is always [X]. Our tone shifts based on context. When users are [situation], we sound [description]. When users are [situation], we sound [description]."

### The Five Principles of Effective UX Writing

**1. Clarity first.** The primary job of UI copy is to be understood. Cleverness, brand personality, and delight are all secondary to clarity. When in doubt, choose the clearer word.

**2. Specific over generic.** "An error occurred" is generic. "Your session has expired. Please sign in again to continue." is specific. Specific copy gives users the information they need to act.

**3. Action-oriented.** Button labels should describe what happens when you click, not what the button is. "Submit" describes the button. "Send application" describes what happens.

**4. User-centric language.** The product should speak about what the user can do, not what the system does. "You can export your data" not "Your data can be exported." "Save changes" not "Changes saved to server."

**5. Appropriate brevity.** UI copy should be as short as possible while remaining clear. Every unnecessary word competes with necessary words for the user's attention.

### Terminology Consistency

Inconsistent terminology is one of the most common and most damaging UX writing problems. When the same thing is called three different names in three different places ("employee," "team member," and "staff"), users develop uncertainty about whether these are the same thing or different things.

A terminology section of the writing guide should document:
- The canonical term for every key product concept
- Terms that should never be used (and what to use instead)
- Terms that are easily confused with each other and how to distinguish them
- Terms with specific technical meanings that differ from their casual meanings

---

## When to Use This Skill

Use when:
- A product is being written by multiple contributors and copy inconsistency is emerging
- A product is undergoing a rebrand or voice refresh that affects all product copy
- A new product or major feature is launching and copy standards need to be established
- Onboarding a new content designer, UX writer, or product manager who will write copy

---

## Dos

- **Do include real product examples for every guideline.** Abstract principles without examples are much less actionable. Show before/after rewrites.
- **Do document the "why" behind each principle.** Writers who understand the reasoning make better decisions in uncovered edge cases.
- **Do make the terminology section scannable.** Writers need to look up terms quickly. A table format with "Use" / "Don't use" / "Notes" columns is more useful than paragraphs.
- **Do acknowledge that tone shifts with context.** A guide that treats all UI copy as identical ignores the most nuanced and important aspect of UX writing.

---

## Donts

- **Dont write guidelines so abstract they provide no practical guidance.** "Be human" is not actionable. "Use contractions (you're, we'll, it's) rather than formal constructions (you are, we will, it is)" is actionable.
- **Dont create a guide that is longer than it needs to be.** A 50-page writing guide will not be consulted. A 10-page guide with a scannable terminology section will.
- **Dont conflate brand voice guidelines with UX writing guidelines.** Brand guidelines cover external marketing. UX writing guidelines cover product copy. They share a voice but differ in context, audience, and specific guidance.

---

## Output Format

```
1. INTRODUCTION
   Why these guidelines exist.
   Who they are for.
   How to use this document.

2. VOICE AND TONE
   Voice definition: 3 to 5 voice qualities with descriptions.
   For each quality: what it means, how it shows up in copy, what it is not.
   Tone spectrum: how tone shifts by context.
   Tone by situation table: context / emotional state / tone / example.

3. WRITING PRINCIPLES
   5 to 7 core principles with:
   - Principle name and description
   - Rationale
   - Do example (real product copy)
   - Don't example (what to avoid and why)

4. GRAMMAR AND MECHANICS
   Capitalization: sentence case vs. title case rules.
   Punctuation: Oxford comma, ellipsis, em dash usage.
   Numbers: when to write out vs. use numerals.
   Dates and times: preferred format.
   Contractions: allowed or not, in what contexts.

5. TERMINOLOGY GLOSSARY
   Table format:
   Use | Don't use | Notes
   (Canonical product terms, easily confused pairs, forbidden terms)

6. CONTENT PATTERNS BY UI ELEMENT
   Button labels: rules and examples.
   Headings and titles: rules and examples.
   Body copy and descriptions: rules and examples.
   Error messages: structure and examples (see microcopy-doc.md).
   Empty states: structure and examples.
   Confirmation dialogs: structure and examples.
   Tooltips and help text: rules and examples.
   Notifications and alerts: rules and examples.
   Success messages: rules and examples.

7. INCLUSIVE AND ACCESSIBLE LANGUAGE
   Gender-neutral language standards.
   Plain language requirements.
   Reading level target.
   Internationalization considerations.

8. REVIEW PROCESS
   How new copy gets reviewed against these guidelines.
   Who has final approval on copy.
   How to flag edge cases or request guideline updates.
```

---

## Starter Prompt

```
You are a UX writing specialist creating a comprehensive writing guidelines document.

Product type and context: [what the product is and who uses it]
Brand voice qualities: [how the brand wants to be perceived, e.g., "direct, helpful, honest"]
Audience: [who uses the product and their characteristics]
Current copy problems: [consistency issues, tone problems, or terminology confusion]
Key product terminology: [the main concepts the product uses]
Tone contexts: [the different emotional situations users encounter in the product]
Existing brand guidelines: [any brand voice guidance that should be respected]

Please produce a comprehensive UX writing guidelines document including:
1. Voice definition with 3 to 5 qualities, each with description, examples, and what it is not
2. Tone spectrum with context-by-context guidance
3. Writing principles with do/dont examples from product copy
4. Grammar and mechanics rules
5. Terminology glossary in Use / Don't use / Notes table format
6. Content patterns for all major UI elements
7. Inclusive language standards

For every principle and pattern, include a real product copy example and a rewrite example.
Make the terminology section scannable for quick reference.
```

---

## Related Skills

| Use This Next | Why |
|---|---|
| `microcopy-doc.md` | Detailed copy for specific UI elements follows these guidelines |
| `design-system-doc.md` | Writing guidelines inform content guidelines in component documentation |
| `onboarding-flow-spec.md` | Onboarding copy follows these guidelines |

*Skill file version: 1.0 | Phase: 03 - UX and Design | Company type: Product*
