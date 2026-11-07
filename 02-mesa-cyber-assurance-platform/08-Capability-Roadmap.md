# 08 — Capability Roadmap

## Incremental delivery strategy

| Increment | Outcome | Principal capabilities | Exit evidence |
|---|---|---|---|
| 0 — Foundation | Agreed architecture and governance | Mission threads, data model, boundary model, ADR process, threat baseline | Approved concept and interface assumptions |
| 1 — Visibility | Trusted inventory and dependency view | Asset/boundary registry, architecture graph, source connectors, access policy | Critical assets and dependencies traced |
| 2 — Evidence | Governed evidence lifecycle | Catalog, provenance, freshness, quarantine, supplier/enclave intake | Evidence quality metrics and failure tests |
| 3 — Assurance | Requirements/control/test traceability | Threat scenarios, control allocation/inheritance, SCTM, test workflow | Priority risk thread verified end to end |
| 4 — Decision | Portfolio risk and authorization support | Residual-risk workflow, POA&M, decision briefs, dependency impacts | Decision authority accepts pilot process |
| 5 — Continuous | Risk-tiered monitoring and sustainment | Events, drift detection, reopen rules, trend analytics, recovery | Monitoring exercise and operational readiness |

## Architecture gates

- **Gate A — Mission fit:** outcome, users, constraints, and loss scenarios approved.
- **Gate B — Boundary integrity:** data flows, trust zones, identities, and external dependencies approved.
- **Gate C — Evidence readiness:** requirements are verifiable and evidence sources are credible.
- **Gate D — Authorization readiness:** gaps, inherited risk, limitations, and residual-risk decisions are explicit.
- **Gate E — Operational readiness:** monitoring, incident response, recovery, sustainment, and ownership are exercised.

## Technical debt rules

Each debt item states affected mission thread, risk exposure, accountable owner, planned retirement increment, verification needed, and the decision authority that accepted the temporary condition.

See `backlog/capability-roadmap.md`.
