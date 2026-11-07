# 06 — Verification, Governance, and Sustainment

## Verification strategy

- Contract tests for all producer/consumer interfaces
- Model consistency and traceability checks
- Mission-thread tests across all three constituent systems
- Threat, access, evidence, and decision-authority tests
- Duplicate, out-of-order, delayed, lost, and conflicting update tests
- Constituent outage, recovery, and reconciliation exercises
- Architecture change-impact and regression verification

## Decision rights

| Decision | Accountable authority |
|---|---|
| Mission outcome and priority | Mission owner |
| SoS architecture baseline | Lead/chief systems architect with governance board |
| Cyber control/evidence assessment | Lead cyber architect/assessor roles |
| Residual-risk acceptance | Designated risk/authorization authority |
| Migration wave and cutover | Program/cutover authority |
| Data authority and lifecycle | Data owner/steward |
| Production change | Change authority with system owner |

## Governance cadence

- Weekly: interface, dependency, finding, migration, and evidence triage
- Monthly: architecture baseline, ADR, risk, exception, and roadmap review
- Quarterly: mission measures, resilience, cost, technical debt, and sustainment review
- Release/cutover: traceability, verification, rollback, operations, and decision gate
- Trigger-based: major mission, threat, provider, interface, boundary, or authority change

## Sustainment

Maintain versioned models, contracts, ADRs, test evidence, risk/exception expiry, dependency health, monitoring triggers, cost ownership, reusable patterns, skills, and succession. Reuse is permitted only after validating pattern assumptions against the new mission context.
