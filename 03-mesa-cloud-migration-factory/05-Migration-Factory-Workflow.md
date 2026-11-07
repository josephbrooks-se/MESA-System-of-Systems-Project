# 05 — Migration Factory Workflow

## Factory functions

| ID | Function | Primary output |
|---|---|---|
| MF-01 | Discover and inventory | Validated workload record |
| MF-02 | Assess and disposition | 7R decision and target pattern |
| MF-03 | Map dependencies | Migration group and sequencing constraints |
| MF-04 | Design target workload | Approved architecture and ADRs |
| MF-05 | Build environment | Automated, policy-conformant target |
| MF-06 | Migrate application and data | Reconciled target instance |
| MF-07 | Verify and rehearse | Readiness evidence and rollback confidence |
| MF-08 | Authorize cutover | Time-bounded execution decision |
| MF-09 | Cut over and validate | Accepted cloud production state |
| MF-10 | Stabilize and optimize | Operational SLO, cost, and incident baseline |
| MF-11 | Decommission source | Closed legacy cost/risk |
| MF-12 | Capture learning | Updated pattern, backlog, and roadmap |

## Stage gates

1. **Discovery complete:** ownership, inventory, dependencies, performance, data, and risk are sufficient.
2. **Disposition approved:** business and technical rationale, target state, cost range, and exceptions are accepted.
3. **Foundation ready:** required identity, network, security, observability, backup, and delivery services are operational.
4. **Build ready:** design, contracts, IaC, migration method, test plan, and runbooks are reviewed.
5. **Cutover ready:** rehearsal passes; data reconciliation, rollback, staffing, communications, and authority are confirmed.
6. **Stabilization accepted:** SLOs, security, operations, costs, recovery, and defects meet exit criteria.
7. **Legacy exit approved:** data, interfaces, records, licenses, and dependencies are closed.

## Workflow rule

No workload advances on schedule pressure alone. Gate exceptions identify mission impact, compensating action, expiration, accountable owner, and decision authority.

See `diagrams/04-migration-factory-flow.mmd`.
