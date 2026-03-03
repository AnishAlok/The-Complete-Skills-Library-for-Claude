# release-notes.md

> **Skill:** Produces release notes for internal and external audiences, translating technical changes into user-facing descriptions of what is new, what changed, and what was fixed.

---

## TLDR

Release notes bridge the changelog (technical record for engineers) and the audience (users, customers, or internal stakeholders) by translating changes into the language and perspective of the recipient. This skill produces release notes for different audiences from the same underlying changelog, ranging from developer-focused technical notes to customer-facing product updates.

---

## Topic Explanation

### Changelog vs. Release Notes

**Changelog:** Technical record. For engineers. "Fixed race condition in export job queue when concurrent requests exceed connection pool limit." Exact, technical, precise.

**Release notes:** Communication artifact. For the audience. "Export jobs now complete reliably when multiple users request exports simultaneously." Outcome-focused, user-language, no implementation details.

Both should be maintained. The changelog is the source of truth. Release notes are derived from it for specific audiences.

### Audience-Specific Release Notes

**Developer/API release notes:** Include breaking changes prominently, API changes with migration guidance, deprecation timelines. Technical but user-focused for developer audiences.

**End-user release notes:** Focus on what changed in the product experience. No technical implementation details. Written in plain language. Emphasize benefits.

**Customer success / support release notes:** Include what is new, what changed that affects support workflows, and common questions customers are likely to ask.

**Internal stakeholder release notes:** Include business context, metrics implications, and any operational changes.

---

## Output Format

```
RELEASE NOTES: [Product/Service Name] [Version]
Release date: [date]
Audience: [developers / end users / CS team / internal]

---

WHAT'S NEW IN [VERSION]

[1 to 2 sentence summary of the most significant things in this release]

NEW FEATURES
[Feature name]
[User-focused description: what you can now do and why it matters]

[Feature name]
[Description]

IMPROVEMENTS
[What improved, framed as the user benefit]

BUG FIXES
[Description of what was broken and is now fixed, in user language]
[For developer audience: link to issue numbers]

BREAKING CHANGES (for developer audiences)
[What changed that requires action]
[Migration path: what to do]
[Deadline for migration if the old version is being deprecated]

DEPRECATIONS
[What is being deprecated]
[Timeline: when it will be removed]
[What to use instead]

KNOWN ISSUES
[Any known issues in this release with workarounds]

DOCUMENTATION UPDATES
[Links to updated documentation]

QUESTIONS?
[Where to get support or ask questions]
```

---

## Starter Prompt

```
You are a technical writer producing release notes.

Version: [release version]
Audience: [developer / end user / customer success / internal]
Changelog input: [the engineering changelog or list of changes]
Breaking changes: [any breaking changes requiring action]
Deprecations: [anything being deprecated]
Known issues: [any known issues in this release]

Translate the changelog into audience-appropriate release notes.
For end-user audiences: remove technical language, emphasize benefits.
For developer audiences: include migration guidance for breaking changes.
Highlight breaking changes prominently regardless of audience.
```

---

*Skill file version: 1.0 | Phase: 05 - Engineering | Company type: Product*
