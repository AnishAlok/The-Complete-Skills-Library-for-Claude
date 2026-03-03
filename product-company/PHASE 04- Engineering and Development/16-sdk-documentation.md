# sdk-documentation.md

> **Skill:** Produces SDK and library documentation covering installation, quick start, full API reference, code examples, error handling, and versioning for a developer-facing SDK.

---

## TLDR

SDK documentation is the primary interface between a library or SDK and the developers who use it. Good SDK docs reduce time-to-hello-world, prevent the most common misuse patterns, and build developer confidence. This skill produces complete SDK documentation following the structure of high-quality developer docs (Stripe, Twilio, AWS SDKs).

---

## Topic Explanation

### The Documentation Hierarchy

**Quick Start:** The most important section. Gets a developer to a working example in under 5 minutes. Covers: install, initialize, make first call, see result.

**Core Concepts:** The mental model a developer needs to use the SDK effectively. What are the main objects? What is the lifecycle?

**API Reference:** Complete method/function reference. Every public interface documented. Not a substitute for the quick start.

**Guides:** Task-oriented documentation for common use cases. "How to handle pagination," "How to implement webhooks."

**Examples:** Complete working code samples for the most important scenarios.

The most common SDK documentation mistake: writing only the API reference and calling it documentation. The API reference is a reference, not an introduction. Developers need the quick start and core concepts first.

### Documenting Error Handling

Every SDK should document the complete error taxonomy: what error types can be thrown, what causes them, and what the developer should do in response. An SDK that throws undocumented errors forces developers to handle them by trial and error.

---

## Output Format

```
1. README / OVERVIEW
   What the SDK does.
   Languages / platforms supported.
   Installation (one command).
   Link to full documentation.

2. QUICK START
   Prerequisites.
   Installation.
   Initialization / authentication.
   First working example (complete, copy-pasteable).
   Expected output.

3. CORE CONCEPTS
   The main objects and their relationships.
   Lifecycle: how the SDK is initialized, used, and cleaned up.
   Authentication model.
   Request/response model.
   Async model (sync / async / callback / promise).

4. INSTALLATION AND CONFIGURATION
   Package manager installation.
   Environment configuration.
   Initialization options with descriptions.
   Minimal and full configuration examples.

5. API REFERENCE
   For each public class/module:
   - Description
   For each method:
   - Signature
   - Parameters: name / type / required / description
   - Returns: type and description
   - Throws: error types
   - Code example

6. GUIDES
   One guide per common task.
   Each guide: problem statement, complete working code, explanation.

7. ERROR HANDLING
   Error class hierarchy.
   For each error type: when it occurs, properties, how to handle it.
   Retry strategy for transient errors.

8. VERSIONING AND MIGRATION
   Versioning scheme.
   Changelog link.
   Migration guides for major versions.

9. EXAMPLES REPOSITORY
   Link to examples.
   Description of each example scenario.
```

---

## Starter Prompt

```
You are a developer advocate writing SDK documentation.

SDK name and language: [e.g., Node.js SDK for PaymentAPI]
What the SDK does: [the API or service it wraps]
Public API surface: [the classes and methods to document]
Authentication: [how the SDK authenticates]
Error types: [the errors the SDK can throw]
Common use cases: [the top tasks developers will want to do]

Produce complete SDK documentation including quick start with working example,
core concepts, full API reference with examples, error handling guide,
and task-oriented guides for common use cases.
Quick start must get a developer to working code in under 5 minutes.
```

---

*Skill file version: 1.0 | Phase: 05 - Engineering | Company type: Product*
