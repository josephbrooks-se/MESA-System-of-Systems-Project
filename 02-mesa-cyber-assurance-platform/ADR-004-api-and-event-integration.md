# ADR-004 — Governed APIs and Events

- **Status:** Accepted
- **Decision:** Use APIs for commands and authoritative queries; use events for state changes, findings, and asynchronous workflow.
- **Drivers:** Tool diversity, traceability, resilience, loose coupling, monitoring tempo.
- **Alternatives:** Point-to-point files only; shared database; synchronous APIs only.
- **Consequences:** Better decoupling and responsiveness; event ordering, duplication, versioning, and observability must be engineered.
- **Controls:** Contract registry, semantic versioning, idempotency, immutable IDs, replay protection, DLQ, reconciliation, compatibility tests.
