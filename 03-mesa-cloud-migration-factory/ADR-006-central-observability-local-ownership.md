# ADR-006 — Central Observability with Local Ownership

- **Status:** Accepted
- **Decision:** Centralize protected security/audit telemetry and portfolio visibility while workload teams own service signals, alerts, runbooks, SLOs, and first response.
- **Drivers:** Cross-account visibility, independent audit, product accountability, incident speed, reusable tooling.
- **Alternatives:** Fully central operations; independent tooling per workload; logs only without metrics/traces.
- **Consequences:** Consistent portfolio awareness and local expertise; requires canonical telemetry, routing, retention, cost controls, and responsibility boundaries.
- **Controls:** Required signal contract, protected archive, health checks, alert ownership, escalation tests, retention/lifecycle policy, telemetry-cost monitoring.
