# Ecosystem Integration Governance

## Decision rights

| Decision | Authority |
|---|---|
| Mission outcome/priority | Mission owner |
| SoS architecture baseline and interface | Architecture governance board |
| Cyber evidence/control assessment | Cyber architecture and assessment authorities |
| Residual-risk/authorization acceptance | Designated human authority |
| Cloud migration wave/cutover/legacy exit | Program and cutover authorities |
| Canonical identifier/schema | Cross-system data/architecture owner |
| Breaking API/event change | Producer and affected consumer owners with architecture approval |

## Change process

1. Register change and affected authoritative entities.
2. Query cross-system impact.
3. Identify consumers, traces, evidence, risks, decisions, and migration effects.
4. Evaluate alternatives and compatibility.
5. Approve version/transition/rollback/retirement plan.
6. Implement in nonproduction and run contract/regression tests.
7. Release with monitoring and evidence.
8. Retire old version only after consumer validation and authority approval.

## Cadence

- Weekly interface/event/error/reconciliation review
- Monthly architecture, schema, dependency, risk, and exception review
- Quarterly mission thread, resilience, recovery, cost, and roadmap review
- Triggered review for breaking change, evidence revocation, major threat, boundary/provider change, or constituent outage
