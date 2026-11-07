# 12 — Governance, FinOps, and Sustainment

## Operating model

| Responsibility | Platform team | Product/workload team | Security/governance |
|---|---|---|---|
| Landing zone and shared products | Accountable | Consumer | Guardrail review |
| Application architecture | Consulted | Accountable | Risk/conformance review |
| Identity and resource policy | Shared | Shared | Independent monitoring |
| Observability | Standard and tooling | Signals and response | Security visibility |
| Recovery | Platform mechanisms | Workload plan and exercise | Evidence review |
| Cost | Allocation and tooling | Forecast and optimization | Policy/portfolio reporting |
| Change | Platform baseline | Workload delivery | Architecture/security gates |

## Governance cadence

- Weekly: migration-wave blockers, interfaces, risks, findings, and cost anomalies.
- Biweekly: architecture/design and platform-product review.
- Monthly: landing-zone controls, dependency health, FinOps, SLO, and exception review.
- Quarterly: roadmap, Well-Architected posture, recovery, capacity, technical debt, and legacy exit.
- Release/cutover: readiness, evidence, rollback, operations, residual risk, and authority gate.

## FinOps model

- Allocate every resource to workload, environment, owner, capability, and cost center.
- Establish budgets and anomaly thresholds before production.
- Report actual and forecast cost, unit cost, utilization, commitments, and waste.
- Include data transfer, security, observability, backup, support, and labor—not compute alone.
- Prevent migration savings from being claimed before legacy costs are closed.

## Sustainment controls

- Configuration and policy drift detection
- Patch and vulnerability lifecycle
- Certificate, key, secret, and identity lifecycle
- Backup, restore, failover, and recovery exercises
- Service quota, capacity, and dependency monitoring
- Platform-product versioning and consumer migration
- Architecture decision and exception expiration
- Data retention, lifecycle, lineage, and disposition
- Skills, runbooks, mentoring, and succession planning

## Optimization loop

Measure → compare to mission/SLO/cost baseline → identify cause → evaluate alternative → approve change → deploy through automation → verify → update architecture and evidence.
