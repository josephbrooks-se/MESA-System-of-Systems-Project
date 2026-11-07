# Cloud Migration Risk Registry

## Scoring

- **Probability:** 1 Rare, 2 Unlikely, 3 Possible, 4 Likely, 5 Almost certain
- **Impact:** 1 Minimal, 2 Limited, 3 Significant, 4 Severe, 5 Mission critical
- **Exposure:** Probability × Impact
- **Priority:** Low 1–4, Moderate 5–9, High 10–16, Critical 17–25

Scores support prioritization and do not replace accountable risk judgment.

| ID | Risk statement | P | I | Exposure | Owner | Primary mitigation | Trigger/indicator | Contingency | Residual target | Status |
|---|---|---:|---:|---:|---|---|---|---|---|---|
| R-01 | If portfolio inventory is incomplete, hidden dependencies may cause failed waves or mission interruption. | 4 | 4 | 16 | Portfolio Architect | Discovery tooling, owner interviews, traffic/job analysis, dependency validation | Unknown traffic, failed rehearsal, owner dispute | Delay wave; isolate affected group; restore source | Moderate | Open |
| R-02 | If the landing zone is not ready before workloads migrate, teams may create insecure or inconsistent environments. | 3 | 5 | 15 | Platform Lead | Foundation gate, automated account baseline, conformance tests | Manual resource creation, missing logs/identity/budget | Freeze onboarding; remediate or rebuild account | Low | Open |
| R-03 | If federated identity or policy attributes are unavailable, legitimate users may be blocked or unsafe access granted. | 3 | 5 | 15 | Identity Lead | Resilient federation, fail-closed writes, tested emergency access | Authentication errors, stale attributes, policy timeout | Invoke monitored emergency access or approved read-only mode | Moderate | Open |
| R-04 | If migration data diverges from the source, the target may become an incorrect authority. | 3 | 5 | 15 | Data Owner | CDC monitoring, reconciliation, write coordination, authority record | Lag/mismatch threshold exceeded | Freeze changes; reconcile; roll back authority | Low | Open |
| R-05 | If shared platform services fail, multiple workloads may be impaired simultaneously. | 3 | 5 | 15 | Platform Service Owner | Multi-zone design, SLOs, dependency map, degraded modes, recovery | SLO breach, capacity/quota warning | Isolate failure; invoke workload contingency | Moderate | Open |
| R-06 | If workload teams lack cloud operating skills, migrated systems may be unstable or costly. | 4 | 4 | 16 | Operations Lead | Training, pairing, runbooks, game days, phased ownership acceptance | Repeated incidents, manual work, alert backlog | Extend platform support; pause wave growth | Moderate | Open |
| R-07 | If schedules force incomplete readiness gates, cutover risk may exceed mission tolerance. | 4 | 5 | 20 | Program Authority | Independent gate evidence, exception authority, visible residual risk | Failed criteria reclassified without evidence | Delay cutover; escalate mission/schedule trade | Moderate | Open |
| R-08 | If provider costs differ from assumptions, the transformation may exceed the business case. | 3 | 4 | 12 | FinOps Lead | Unit-cost model, forecasts, budgets, anomaly detection, right-sizing | Forecast variance or data-transfer surge | Replatform, reschedule, cap scaling, revise case | Moderate | Open |
| R-09 | If legacy hosting is not decommissioned, expected savings and risk reduction will not be realized. | 4 | 4 | 16 | Legacy Exit Owner | Exit gate, dependency closure, license/contract tracking | Dual-run extends beyond approved window | Fund closure team; escalate ongoing cost | Low | Open |
| R-10 | If CI/CD or IaC is compromised, malicious configurations may spread across accounts. | 2 | 5 | 10 | Product Security Lead | Protected repositories, provenance, review, signed artifacts, least-privilege pipeline | Signature/provenance failure, unexpected baseline change | Stop deployments; revoke identity; rebuild from trusted state | Moderate | Open |
| R-11 | If interface behavior changes during migration, consumers may fail despite component success. | 3 | 4 | 12 | Integration Lead | Versioned contracts, consumer tests, adapters, parallel validation | Error/latency increase, semantic mismatch | Restore prior route/version; use adapter | Moderate | Open |
| R-12 | If rollback is not rehearsed with post-cutover data, recovery may cause loss or duplication. | 3 | 5 | 15 | Cutover Lead | Full rehearsal, reversal point, reverse sync, queue reconciliation | Failed rollback step or ambiguous authority | Stop cutover; preserve source; manual reconciliation | Moderate | Open |
| R-13 | If observability is incomplete, security or reliability failures may remain undetected. | 3 | 4 | 12 | Observability Lead | Required signal contract, missing-signal alerts, protected archive | Telemetry gap or unowned alert | Limit cutover; restore signal; increase manual monitoring | Low | Open |
| R-14 | If a retained system lacks an exit trigger, temporary hybrid architecture may become permanent debt. | 4 | 3 | 12 | Portfolio Owner | Expiration, target state, cost/risk reporting, quarterly review | Retain date approaches without plan | Fund remediation/replacement or reapprove explicitly | Moderate | Open |
| R-15 | If cloud quotas/capacity are insufficient, peak demand or recovery may fail. | 3 | 4 | 12 | Reliability Lead | Capacity model, quota checks, load tests, headroom monitoring | Saturation or quota warning | Throttle noncritical work; request capacity; fail over | Low | Open |

## Risk workflow

1. Identify and link the risk to mission outcomes, workloads, dependencies, requirements, threats, waves, and evidence.
2. Validate probability, consequence, uncertainty, assumptions, and affected authority.
3. Select avoid, mitigate, transfer/share, or time-bounded acceptance.
4. Define actions, milestones, resources, triggers, contingency, and verification.
5. Review at wave gates and whenever assumptions, threats, dependencies, evidence, cost, or mission conditions change.
6. Close only when treatment is verified and the accountable authority accepts the resulting state.

## Escalation triggers

- Critical exposure or Tier 1 mission consequence
- Failed readiness/cutover/recovery criterion
- Repeated milestone miss
- Unknown or expanding dependency scope
- Evidence expiration or contradiction
- Risk owner lacks authority/resources
- Residual risk exceeds established tolerance
