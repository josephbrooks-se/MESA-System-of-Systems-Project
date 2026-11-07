# 10 — Cutover, Rollback, and Decommissioning

## Cutover principles

- Cutover is a governed mission decision, not merely a technical activity.
- The decision brief exposes current evidence, limitations, residual risk, staffing, timing, and rollback confidence.
- An independent person verifies entry criteria for Tier 1/2 workloads.
- Communication paths and decision times are rehearsed.

## Cutover sequence

1. Confirm change window, authority, staffing, contacts, and stop conditions.
2. Validate target health, identity, connectivity, capacity, security, logging, backup, and recovery.
3. Freeze or coordinate source changes.
4. Perform final data synchronization and reconciliation.
5. Shift traffic or authoritative processing using the approved technique.
6. Execute smoke, mission-thread, security, data, performance, and monitoring checks.
7. Observe the stabilization window and compare against baseline.
8. Accept, extend observation, or roll back through the named authority.

## Rollback triggers

- Mission-thread failure exceeds the approved threshold.
- Data integrity or authority cannot be demonstrated.
- Security monitoring, identity, logging, or key services are unavailable.
- Performance or error rate violates the decision threshold.
- A critical dependency behaves differently from rehearsal.
- Recovery or operational support is not functioning.

## Rollback design

Define the last responsible reversal point, data created after cutover, reverse synchronization, DNS/traffic changes, queue/event reconciliation, user communications, and evidence capture. A rollback that loses accepted transactions is not complete merely because the old application starts.

## Stabilization

Track SLOs, incidents, findings, costs, capacity, user outcomes, data quality, support volume, and unresolved migration defects. Close the rollback window only when the designated authority accepts evidence.

## Decommissioning

- Archive or dispose of data under approved policy.
- Remove interfaces, DNS, routes, identities, certificates, secrets, monitoring, backup, and jobs.
- Terminate infrastructure, support, licenses, and maintenance contracts.
- Update inventory, diagrams, authorization records, recovery plans, financial baselines, and runbooks.
- Confirm no consumer or manual workflow still depends on the source.

Use `templates/cutover-checklist.md` and `templates/rollback-plan.md`.
