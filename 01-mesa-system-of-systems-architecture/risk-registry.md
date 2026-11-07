# SoS Architecture Risk Registry

| ID | Risk | Probability | Impact | Owner | Mitigation | Trigger | Residual target |
|---|---|---:|---:|---|---|---|---|
| R-SOS-01 | Constituent systems use inconsistent identifiers or semantics | 3 | 4 | Integration Architect | Canonical IDs, schema registry, contract review | Mapping conflict | Low |
| R-SOS-02 | Architecture baseline lags cloud/cyber implementation | 3 | 5 | Lead Systems Architect | Change events, conformance review, release gates | Untraced configuration | Moderate |
| R-SOS-03 | Interface version change breaks a consumer | 3 | 4 | Interface Owner | Compatibility tests, parallel version, consumer inventory | Contract-test failure | Low |
| R-SOS-04 | Traceability creates false confidence from stale evidence | 3 | 5 | Verification Lead | Freshness, limitations, source/config binding | Evidence expiry/change | Moderate |
| R-SOS-05 | Shared services become single points of failure | 3 | 5 | Platform Owner | Resilience, degraded behavior, dependency maps | SLO breach | Moderate |
| R-SOS-06 | Decision rights are ambiguous across systems | 3 | 5 | Governance Chair | RACI/authority matrix, signed decisions, escalation | Conflicting approvals | Low |
| R-SOS-07 | Temporary integration adapters become permanent debt | 4 | 3 | Integration Owner | Owner, cost, metrics, expiry, retirement gate | Expiry without plan | Moderate |
| R-SOS-08 | Mission thread passes components but fails end to end | 3 | 5 | Test Lead | Cross-system mission-thread testing | Integration rehearsal failure | Low |
