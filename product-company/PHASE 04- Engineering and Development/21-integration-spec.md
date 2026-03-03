# integration-spec.md

> **Skill:** Produces a third-party integration specification covering the integration architecture, data flow, authentication, error handling, sync/async patterns, and operational requirements.

---

## TLDR

An integration spec defines how a product connects to an external system: what data flows in what direction, how authentication works, how errors and failures are handled, and what the operational requirements are. Written before integration development begins to align on approach, surface risks, and document decisions for future maintainers.

---

## Topic Explanation

### Integration Patterns

**Synchronous (request-response):** One system makes a request and waits for a response. Simple. Creates temporal coupling: if the external system is slow, the calling system is slow.

**Asynchronous (event-driven):** One system publishes events that the other consumes. Decoupled. More complex. Better for high-volume or latency-sensitive integrations.

**Webhook:** The external system pushes events to the product when something happens. Efficient. Requires the product to expose a publicly accessible endpoint. Must handle duplicate delivery and out-of-order events.

**Polling:** The product periodically checks the external system for updates. Simple but inefficient. Use when webhooks are not available.

**Batch sync:** Data is exported from one system and imported into another on a schedule. Simple. Creates data freshness delay. Use for non-real-time requirements.

### Integration Failure Modes

**External system unavailable:** The integration must handle the external system being unreachable. Retry with exponential backoff, circuit breaker, fallback behavior.

**Authentication failure:** Tokens expire, API keys are rotated. The integration must detect auth failures and refresh credentials without requiring manual intervention.

**Rate limiting:** External APIs have rate limits. The integration must respect them, implement backoff, and queue requests appropriately.

**Schema changes:** External APIs change their response schemas. The integration must handle unexpected fields gracefully and alert when required fields go missing.

---

## Output Format

```
1. INTEGRATION OVERVIEW
   External system name and version.
   Purpose: what this integration enables.
   Direction: inbound / outbound / bidirectional.
   Pattern: synchronous / webhook / polling / batch.
   Owner team.

2. AUTHENTICATION
   Method: OAuth / API key / JWT / HMAC.
   Credential management: where stored, how rotated.
   Token refresh mechanism.
   What happens when authentication fails.

3. DATA FLOW

   For each data flow:
   - Direction: product → external / external → product
   - Trigger: when does this data flow occur?
   - Data: what is sent/received (field mapping)
   - Volume and frequency

4. API ENDPOINTS / WEBHOOK EVENTS USED
   For each endpoint or event:
   - Method/event name
   - Purpose
   - Request/payload structure
   - Response/event structure
   - Rate limits

5. DATA MAPPING
   For each entity synced:
   - Our field name → their field name
   - Data type transformation if needed
   - Fields with no mapping (explicitly ignored)

6. ERROR HANDLING
   For each error type:
   - How it is detected
   - Retry strategy (with backoff parameters)
   - When to stop retrying
   - Alert and escalation trigger
   - User-facing impact and communication

7. IDEMPOTENCY AND DEDUPLICATION
   How duplicate events/webhooks are handled.
   Idempotency key strategy.
   How out-of-order delivery is managed.

8. OPERATIONAL REQUIREMENTS
   Monitoring: what metrics are tracked for this integration.
   Alerting: what triggers an alert.
   Dependency risk: impact if the external system is unavailable.
   Testing: how the integration is tested in staging.

9. SECURITY CONSIDERATIONS
   Data sensitivity of what is transmitted.
   Webhook signature verification.
   PII handling in logs.
```

---

## Starter Prompt

```
You are a senior engineer writing an integration specification.

External system: [name and what it does]
Integration purpose: [what this integration enables]
Integration pattern: [sync / webhook / polling / batch]
Authentication method: [how we authenticate with the external system]
Data flows: [what data moves in what direction]
Error scenarios: [known failure modes to handle]
Volume: [expected request/event volume]

Produce a complete integration spec covering authentication, data flow,
data mapping, error handling with retry strategy, idempotency approach,
and operational requirements.
Flag any error scenario without a documented retry or fallback strategy.
Flag any data transmission involving PII without documented encryption.
```

---

*Skill file version: 1.0 | Phase: 05 - Engineering | Company type: Product*
