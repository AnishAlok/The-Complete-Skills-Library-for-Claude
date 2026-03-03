# api-design-doc.md

> **Skill:** Produces API endpoint design documentation covering request/response schemas, authentication, error handling, versioning, and usage examples for internal or external APIs.

---

## TLDR

An API design document specifies the interface contract for a set of API endpoints: the URLs, methods, request parameters, response schemas, error codes, and authentication requirements. It is the contract between API producer and consumer. Written before implementation to allow parallel frontend/backend development and to enable consumer feedback before the API is built.

---

## Topic Explanation

### Design-First vs. Code-First APIs

**Code-first:** Build the implementation, then generate or write the API documentation. Fast to start. Produces APIs shaped by implementation convenience rather than consumer needs.

**Design-first:** Write the API specification, review with consumers, then implement. Slower to start. Produces APIs shaped by actual consumer needs. Enables parallel development.

For APIs that will be used by multiple consumers or exposed externally, design-first is strongly preferred. The cost of changing an API after consumers have built against it is very high.

### REST API Design Principles

**Resource-oriented:** URLs represent resources (nouns), not actions (verbs). `/users/123` not `/getUser?id=123`.

**HTTP verbs carry semantics:** GET (read, idempotent), POST (create), PUT (replace, idempotent), PATCH (partial update), DELETE (remove, idempotent).

**Status codes are meaningful:** 200 (success), 201 (created), 400 (bad request - client error), 401 (unauthorized), 403 (forbidden), 404 (not found), 409 (conflict), 422 (validation error), 429 (rate limited), 500 (server error).

**Consistent error format:** Every error response should follow the same schema so consumers can handle errors generically.

**Pagination for collections:** Never return unbounded collections. Cursor pagination is preferred for large, frequently-updated collections. Offset pagination for smaller or rarely-changing collections.

### OpenAPI Specification

The OpenAPI Specification (formerly Swagger) is the industry standard for REST API documentation. An OpenAPI YAML or JSON file can be used to auto-generate documentation, mock servers, and client SDKs. API design docs should produce or reference an OpenAPI spec.

---

## Output Format

```
1. API OVERVIEW
   Purpose of this API.
   Consumers: who uses it and for what.
   Base URL and versioning scheme.
   Authentication method.

2. AUTHENTICATION
   Method: API key / OAuth 2.0 / JWT / session.
   Where credentials are passed: header / query param.
   Token scopes (if OAuth).
   Error responses for auth failures.

3. COMMON PATTERNS
   Request/response format: JSON, encoding.
   Date/time format.
   Pagination pattern with examples.
   Standard error response schema.

4. ENDPOINTS

   For each endpoint:
   ---
   [METHOD] [PATH]
   Description: [what this endpoint does]
   Auth required: yes/no, required scope

   Path parameters:
   | Param | Type | Required | Description |

   Query parameters:
   | Param | Type | Required | Default | Description |

   Request body:
   [JSON schema with field descriptions]
   Example request body.

   Response: [HTTP status code]
   [JSON schema with field descriptions]
   Example response body.

   Error responses:
   | Status | Code | Description |

5. WEBHOOKS (if applicable)
   Event types.
   Payload schema per event.
   Delivery guarantees.
   Signature verification.

6. RATE LIMITS
   Limits by tier or endpoint.
   Headers communicating current limits.
   429 response format.

7. VERSIONING AND DEPRECATION
   How versions are specified.
   Current version.
   Deprecation timeline for previous versions.
   Breaking vs. non-breaking change policy.

8. CHANGELOG
   Changes by version.
```

---

## Starter Prompt

```
You are a senior engineer writing an API design document.

API purpose: [what this API enables consumers to do]
Consumers: [who will use this API]
Authentication method: [API key / OAuth / JWT]
Resources and operations: [the endpoints and what they do]
Pagination needs: [whether list endpoints need pagination]
Rate limiting: [limits to enforce]
Versioning strategy: [how API versions will be managed]

Produce a complete API design document with OpenAPI-style endpoint specifications.
For each endpoint: method, path, parameters, request/response schema with field
descriptions, and all error responses.
Flag any endpoint design that violates REST conventions.
Flag any response that returns an unbounded collection without pagination.
```

---

*Skill file version: 1.0 | Phase: 05 - Engineering | Company type: Product*
