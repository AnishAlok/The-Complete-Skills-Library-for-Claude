# changelog.md

> **Skill:** Produces a structured engineering changelog from commit history, pull request titles, or release notes inputs following Keep a Changelog conventions.

---

## TLDR

A changelog is the chronological record of all notable changes to a codebase or service. This skill produces changelogs following the Keep a Changelog format: organized by version, categorized by change type, written in human-readable language rather than commit messages. Used for every versioned release and maintained as a living document throughout the software lifecycle.

---

## Topic Explanation

### Keep a Changelog Principles (keepachangelog.com)

**Changelogs are for humans, not machines.** Commit dumps are not changelogs.

**Entry categories:**
- **Added:** New features.
- **Changed:** Changes to existing functionality.
- **Deprecated:** Features that will be removed in a future version.
- **Removed:** Features removed in this version.
- **Fixed:** Bug fixes.
- **Security:** Security fixes. Always note the CVE if applicable.

**Versioning:** Use Semantic Versioning (semver.org): MAJOR.MINOR.PATCH.
- MAJOR: breaking changes
- MINOR: new functionality, backward compatible
- PATCH: bug fixes, backward compatible

**Unreleased section:** Changes not yet released live at the top under [Unreleased]. Move to a versioned section on release.

### Commit Message Quality

A changelog is only as good as the inputs. Conventional Commits format (conventionalcommits.org) produces commit messages that map directly to changelog categories:
- `feat:` → Added
- `fix:` → Fixed
- `BREAKING CHANGE:` → Changed (major version bump)
- `docs:` → typically not in changelog
- `chore:` → typically not in changelog

Teams using conventional commits can automate changelog generation.

---

## Output Format

```
# Changelog

All notable changes to this project will be documented in this file.
Format follows [Keep a Changelog](https://keepachangelog.com/).
Versioning follows [Semantic Versioning](https://semver.org/).

---

## [Unreleased]

### Added
- [New feature description]

### Changed
- [Modified behavior description]

### Fixed
- [Bug fix description]

---

## [X.Y.Z] - YYYY-MM-DD

### Added
- [Feature name]: [brief description of what was added and why] (#PR-number)

### Changed
- [Component name]: [what changed and the impact] (#PR-number)
  - Note: This is a breaking change if upgrading from X.Y to this version.

### Deprecated
- [Feature name]: will be removed in [version]. Use [alternative] instead.

### Removed
- [Feature name]: was deprecated in [version]. [Migration guidance.]

### Fixed
- [Component]: [what was broken and what was fixed] (#PR-number, fixes #issue-number)

### Security
- [CVE-XXXX-XXXX]: [description of the vulnerability and fix]

---

## [X.Y.Z-1] - YYYY-MM-DD
[Previous version entries...]

---

[Unreleased]: https://github.com/org/repo/compare/vX.Y.Z...HEAD
[X.Y.Z]: https://github.com/org/repo/compare/vX.Y.Z-1...vX.Y.Z
```

---

## Starter Prompt

```
You are an engineer generating a changelog.

Version being released: [X.Y.Z]
Release date: [YYYY-MM-DD]
Changes to document:
  Added: [list of new features]
  Changed: [list of changed behaviors]
  Deprecated: [list of deprecated features]
  Removed: [list of removed features]
  Fixed: [list of bug fixes with issue numbers]
  Security: [any security fixes with CVEs if applicable]
Breaking changes: [any breaking changes that need prominent documentation]
PR/issue references: [PR and issue numbers to link]

Produce a changelog entry in Keep a Changelog format.
Breaking changes must be prominently marked in the Changed section.
Every Security entry must include the CVE number if available.
```

---

*Skill file version: 1.0 | Phase: 05 - Engineering | Company type: Product*
