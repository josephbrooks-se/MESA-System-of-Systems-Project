# 12 — Governance and Sustainment

## Decision rights

| Decision | Accountable role | Required consultation |
|---|---|---|
| Mission/risk priority | Program leadership | Mission owner, lead engineers, cyber |
| Architecture baseline | Chief/Lead Systems Engineer | Lead Cyber Architect, owners, operators |
| Cyber architecture exception | Lead Cyber Architect | SSE, safety, program, assessor |
| Control implementation claim | Control owner | Engineer, assessor |
| Assessment conclusion | Independent assessor | Owner, cyber architect |
| Residual-risk acceptance | Designated authority | Program, cyber, mission, legal/policy as applicable |
| Data access policy | Data owner/steward | Security, privacy, program |
| Production change | Change authority | Architecture, security, operations |

## Architecture governance rhythm

- Weekly: interface, threat, finding, and evidence-quality triage.
- Monthly: architecture decision and dependency review.
- Quarterly: mission-thread risk, control inheritance, and monitoring effectiveness review.
- Release gate: requirements, threat model, ADRs, test evidence, rollback, and residual limitations.
- Annual or trigger-based: boundary, categorization, recovery, and authorization strategy reassessment.

## Configuration and change management

Every significant change identifies affected assets, interfaces, requirements, controls, tests, evidence, monitoring, and authorizations. Emergency changes are time-bounded, logged, retrospectively reviewed, and verified.

## Metrics

- Critical-asset traceability coverage
- Evidence freshness and rejected/quarantined rate
- Requirements with passing verification
- Findings by mission impact and age
- Inherited controls with current provider evidence
- Decisions reopened by architecture or threat change
- Mean time to identify dependent boundaries
- Recovery and reconciliation exercise results

## Sustainment risks

- Adapter proliferation: mitigate with canonical contracts and lifecycle ownership.
- Policy drift: version, test, approve, and monitor policy changes.
- Dashboard confidence inflation: show data quality and uncertainty with posture.
- Evidence accumulation: apply retention, disposition, deduplication, and source-reference rules.
- Knowledge concentration: maintain ADRs, runbooks, mentoring, and architecture reviews.

## Reusable-practice goal

The architecture team maintains patterns for control inheritance, evidence sufficiency, isolated collection, API/event security, residual-risk decisions, and verification. Teams may reuse patterns only after validating their assumptions against the new mission context.
