# MESA Ecosystem Risk Registry

| ID | Risk | P | I | Owner | Mitigation | Trigger | Residual target |
|---|---|---:|---:|---|---|---|---|
| R-ECO-01 | Inconsistent identifiers/semantics prevent reliable traceability | 3 | 4 | Data/Integration Architect | Canonical IDs, schema registry, contract review | Mapping conflict | Low |
| R-ECO-02 | Architecture baseline and implemented cloud state diverge | 3 | 5 | Lead Systems Architect | Configuration events, drift/conformance review, gates | Untraced resource/change | Moderate |
| R-ECO-03 | Assurance decisions use stale or insufficient evidence | 3 | 5 | Lead Cyber Architect | Freshness, provenance, configuration binding, invalidation | Evidence expiry/change | Moderate |
| R-ECO-04 | Migration schedule pressure bypasses readiness | 4 | 5 | Program/Cutover Authority | Independent gates, explicit exception, residual-risk visibility | Failed criterion relabeled | Moderate |
| R-ECO-05 | Shared identity/integration/evidence services become single points of failure | 3 | 5 | Platform Owner | Resilience, degraded behavior, recovery, dependency mapping | SLO breach | Moderate |
| R-ECO-06 | Decision rights conflict across constituent systems | 3 | 5 | Governance Chair | Authority matrix, human scopes, signed decisions, escalation | Conflicting decisions | Low |
| R-ECO-07 | Event delay/order conflict creates inconsistent status | 3 | 4 | Integration Owner | Idempotency, source version, reconciliation, freshness display | State mismatch | Low |
| R-ECO-08 | Temporary adapters/hybrid paths become permanent debt | 4 | 3 | Architecture Owner | Owner, cost, expiry, roadmap, retirement gate | Expiry without closure | Moderate |
| R-ECO-09 | End-to-end mission thread fails despite component success | 3 | 5 | Test Lead | Cross-system system/mission-thread testing | Rehearsal failure | Low |
| R-ECO-10 | Skills/ownership gaps undermine sustainment | 4 | 4 | Operations/Engineering Leadership | Training, pairing, runbooks, product ownership, exercises | Repeated escalation/manual work | Moderate |

## Governance

Review risks at monthly ecosystem governance, each architecture/migration/authorization gate, and whenever threats, configurations, dependencies, evidence, costs, or authorities change. Acceptance is time-bounded and requires a named human authority.
