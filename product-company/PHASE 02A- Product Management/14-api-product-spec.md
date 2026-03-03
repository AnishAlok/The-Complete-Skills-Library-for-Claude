# api-product-spec.md

> **Skill:** Produces an API product specification documenting endpoints, authentication, data models, versioning strategy, rate limits, error handling, and developer experience requirements for an externally facing API product.

---

## TLDR

An API product spec defines what a public or partner-facing API must do, how it should behave, and what the developer experience must be like. It bridges the product perspective (who uses this, why, what outcomes they need) and the technical perspective (endpoints, authentication, data models, error handling). Used when building or redesigning a public API as a product.

---

## Topic Explanation

### The API as a Product

An API is a product whose users are developers. The same product thinking that applies to end-user products applies to APIs: who are the developers building with it, what are they trying to accomplish, what friction makes their experience bad, and what would make them succeed faster.

The most common API product failure is designing around the data model rather than the developer's use case. "Here is our user object with all 47 fields" is an API designed from inside out. "Here is the endpoint that returns everything a developer needs to display a user profile in one call" is an API designed from the developer's perspective.

### Core API Product Decisions

**REST vs. GraphQL vs. gRPC:** REST is the most widely understood. GraphQL gives developers control over the data shape and reduces over-fetching. gRPC is best for high-performance internal or mobile API use. The choice depends on developer audience, data complexity, and performance requirements.

**Versioning strategy:** How breaking changes are handled. URL versioning (/v1/, /v2/) is most visible but messier. Header versioning is cleaner but less discoverable. The strategy must be defined before the first public release.

**Authentication:** API keys are simplest. OAuth 2.0 is standard for user-data APIs. Both may be needed for different use cases.

**Rate limiting:** Critical for protecting the service and enabling fair use. Rate limits must be communicated clearly in the API response headers.

---

## Output Format

```
1. API PRODUCT OVERVIEW
   What this API is for and who uses it.
   Primary developer use cases.
   Design philosophy and principles.

2. AUTHENTICATION
   Authentication method(s) supported.
   How developers obtain credentials.
   Security requirements.

3. BASE URL AND VERSIONING
   Base URL structure.
   Versioning strategy and deprecation policy.

4. ENDPOINTS
   For each endpoint:
   - Method and path
   - Description and use case
   - Request: parameters, headers, body schema
   - Response: schema, example
   - Error responses: codes and messages
   - Rate limit: requests per window

5. DATA MODELS
   Core objects and their fields.
   Field descriptions and types.
   Required vs. optional fields.
   Relationships between objects.

6. ERROR HANDLING
   Standard error response format.
   Error code taxonomy with descriptions and recommended developer responses.

7. RATE LIMITS AND QUOTAS
   Rate limit by tier.
   How limits are communicated (headers).
   Behavior when limits are exceeded.

8. PAGINATION
   Pagination strategy: cursor, offset, or page-based.
   Consistent pagination across all list endpoints.

9. WEBHOOKS (if applicable)
   Event types available.
   Payload format.
   Security: signature verification.
   Retry policy.

10. DEVELOPER EXPERIENCE REQUIREMENTS
    Documentation requirements.
    SDK requirements.
    Sandbox/test environment.
    Example applications.

11. SLAs AND RELIABILITY
    Uptime commitments.
    Latency requirements.
    Deprecation and change communication policy.
```

---

## Starter Prompt

```
You are a product manager writing an API product specification.

API purpose: [what this API enables developers to do]
Primary developer use cases: [the top 3 to 5 things developers will build]
Authentication approach: [API keys / OAuth / both]
Core data objects: [the main resources in this API]
Key endpoints needed: [the operations developers need to perform]
Versioning strategy: [how breaking changes will be handled]
Rate limiting approach: [how usage will be managed]

Produce a complete API product spec covering all sections.
Design endpoints around developer use cases, not around internal data models.
For each error code, specify what the developer should do in response.
```

---

*Skill file version: 1.0 | Phase: 02 - Product Management | Company type: Product*
