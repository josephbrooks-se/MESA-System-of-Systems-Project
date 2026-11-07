# ADR-001 — Hybrid Governed Deployment

- **Status:** Accepted for the reference architecture
- **Decision:** Use central governance services with site adapters and segregated enclave collectors.
- **Drivers:** Multiple boundaries, disconnected operations, source authority, evidence consistency, mission continuity.
- **Alternatives:** Centralize all data; leave all functions federated; deploy identical full stacks in every enclave.
- **Consequences:** Better dependency visibility and consistent policy; higher adapter, reconciliation, and lifecycle complexity.
- **Controls:** Canonical contracts, explicit source ownership, store-and-forward, conflict rules, integration SLOs.
- **Revisit when:** transfer policy, connectivity, classification, scale, or mission latency assumptions materially change.
