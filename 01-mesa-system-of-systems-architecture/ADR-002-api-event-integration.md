# ADR-002 — API and Event Integration

- **Status:** Accepted
- **Decision:** Use REST APIs for authoritative commands/queries and signed events for state changes and asynchronous workflow.
- **Drivers:** Loose coupling, responsiveness, traceability, independent scaling.
- **Consequences:** Versioning, idempotency, ordering, replay, dead-letter, and reconciliation must be engineered.
