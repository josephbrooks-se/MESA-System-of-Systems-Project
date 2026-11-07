# 05 — Functional and Behavioral Analysis

## Logical functions

| ID | Function | Inputs | Outputs |
|---|---|---|---|
| LF-01 | Register architecture entities | Models, assets, boundaries | Governed architecture graph |
| LF-02 | Model mission and authorization dependencies | Mission threads, services, controls | Dependency and impact paths |
| LF-03 | Analyze threats and loss scenarios | Assets, interfaces, threat intel | Risk scenarios and requirements |
| LF-04 | Tailor and allocate controls | Baselines, threats, architecture | Control responsibility records |
| LF-05 | Ingest evidence | Signed packages/events | Validated or quarantined records |
| LF-06 | Catalog evidence and provenance | Validated evidence | Searchable metadata and lineage |
| LF-07 | Evaluate assurance and risk | Requirements, tests, evidence, findings | Coverage, confidence, residual risk |
| LF-08 | Orchestrate remediation | Findings, owners, milestones | POA&M/work items/status |
| LF-09 | Support authorization decisions | SSP/SCTM/evidence/risk | Review package and decision record |
| LF-10 | Monitor change | Telemetry, configurations, dependencies | Alerts and reopened decisions |
| LF-11 | Govern access and data | Identities, attributes, markings, policy | Policy decisions and audit events |
| LF-12 | Report portfolio posture | Governed graph and metrics | Mission/risk/trend views |

## Primary operational thread: new critical finding

1. A source tool detects a finding and assigns an immutable source ID.
2. The gateway authenticates the source, validates the contract, checks replay state, and applies markings.
3. The catalog links the finding to the affected asset, configuration, boundary, mission thread, controls, and evidence.
4. The risk service evaluates exploitability, mission consequence, exposure, compensating controls, and evidence confidence.
5. Workflow routes the finding to accountable engineering and program owners.
6. A mitigation, acceptance recommendation, or request for additional evidence is recorded.
7. The decision authority receives alternatives with mission, cost, schedule, and residual-risk impacts.
8. Verification evidence closes or reduces the risk; monitoring watches for recurrence or invalidated assumptions.

## Exception behaviors

- **Duplicate event:** acknowledge but do not duplicate state; preserve audit trace.
- **Out-of-order event:** hold within reconciliation window or apply version rule; alert on unresolved conflict.
- **Unknown asset:** quarantine and route to data steward; never silently create a critical asset.
- **Stale evidence:** retain for history, mark invalid for current assurance, notify owner.
- **Policy service unavailable:** deny protected writes; allow only approved cached/read-only behavior.
- **Source compromised:** revoke identity, isolate connector, identify dependent evidence, and reopen affected decisions.

See `diagrams/04-authorization-evidence-flow.mmd`.
