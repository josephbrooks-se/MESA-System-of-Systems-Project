# 09 — Migration Waves

## Wave construction rules

Group workloads by dependency, shared data, business event, target pattern, risk, and team capacity. Avoid selecting waves solely by organizational ownership or application count.

## Wave sequence

### Wave 0 — Foundation

Deliver landing zone, identity, connectivity, security, observability, backup, CI/CD, IaC, FinOps, and operating procedures.

### Wave 1 — Pilot

Select two or three lower-criticality workloads that collectively exercise web access, identity, database migration, monitoring, backup, and rollback.

### Wave 2 — Shared services

Migrate or establish integration, file transfer, messaging, data catalog, shared databases where appropriate, and common operational services needed by later waves.

### Wave 3 — Business applications

Migrate moderate-complexity web, COTS, batch, and internal applications using proven patterns.

### Wave 4 — Data and analytics

Move high-volume data pipelines and analytics with explicit source authority, lineage, reconciliation, and consumer transition.

### Wave 5 — Mission-critical workloads

Use full rehearsals, performance baselines, recovery exercises, time-bounded decision authority, and coordinated rollback.

### Wave 6 — Modernize and exit

Refactor high-value workloads, retire temporary hybrid dependencies, decommission legacy hosting, and close licenses/contracts.

## Wave entry criteria

- Systems and owners confirmed
- Dependencies validated
- Target patterns approved
- Platform prerequisites available
- Migration and data methods tested
- Cutover/rollback/runbooks reviewed
- Staffing, communications, and authority assigned
- Risks and exceptions accepted

## Wave exit criteria

- Acceptance and mission-thread tests pass
- Security and operations telemetry is current
- Data is reconciled and target authority recorded
- SLOs and support model are accepted
- Cost allocation and budgets are active
- Rollback window is formally closed
- Source decommissioning tasks are funded and scheduled

Use `templates/wave-plan.csv`.
