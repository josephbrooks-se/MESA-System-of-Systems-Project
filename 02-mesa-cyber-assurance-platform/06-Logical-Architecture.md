# 06 — Logical Architecture

## Layers and responsibilities

| Layer | Components | Responsibility |
|---|---|---|
| Experience | Portfolio dashboard, architect workspace, assessor workspace, decision brief generator | Role-focused views and workflows |
| Domain services | Architecture Registry, Threat/Risk, Control, Evidence, Traceability, Test, POA&M, Decision | Mission and assurance business logic |
| Integration | API gateway, event broker, schema registry, adapters, transfer gateway | Contract enforcement and decoupling |
| Data | Architecture graph, relational transaction store, object evidence store, metadata catalog, audit ledger | Governed persistence and lineage |
| Security plane | ICAM, policy decision/enforcement, workload identity, key/secrets management, telemetry | Resource-level protection |
| Edge/enclave | Segregated collectors, local queue, approved export packager | Disconnected and isolated collection |
| Operations | Observability, configuration, backup/recovery, software supply-chain controls | Resilience and sustainment |

## Service boundaries

- Domain services own their data contracts; cross-service access occurs through approved APIs or events.
- Evidence binaries are separated from searchable metadata and protected by resource policy.
- The audit ledger records security-relevant actions but is not used as the transactional source of truth.
- Architecture graph relationships are derived from approved source identifiers and stewarded mappings.
- Analytics consumes governed projections; it does not change authorization state.

## Trust assumptions

1. Identity providers and key services are critical common-service dependencies.
2. A valid identity does not imply authorization to a resource.
3. Source evidence can be incomplete, stale, or compromised and must be evaluated.
4. Network zones reduce exposure but do not create implicit trust.
5. Collector output is untrusted until gateway validation completes.
6. Human approval is required for residual-risk acceptance and authorization decisions.

## High-availability posture

- Stateless services scale across failure domains.
- Transactional data uses replicated storage with tested recovery.
- Event processing is idempotent and replayable from governed retention points.
- Integrations use timeouts, circuit breakers, backpressure, and dead-letter handling.
- Last validated posture remains readable during selected dependency failures.

See `diagrams/02-logical-architecture.mmd` and `diagrams/05-hybrid-deployment.mmd`.
