# Cloud Migration Test Plan

## Test campaigns

| Campaign | Purpose | Representative tests |
|---|---|---|
| Foundation | Validate landing-zone controls | Account vending, policy denial, log delivery, drift, budget, closure |
| Identity | Validate zero-trust access | Missing attribute, revoked session, privilege expiry, workload role, emergency access |
| Network | Validate paths and isolation | Routes, DNS, TLS, egress, segmentation, failover, quota |
| Application/integration | Preserve behavior | User journeys, APIs, events, queues, batch, retries, compatibility |
| Data | Preserve authority and meaning | Counts, digests, integrity, business totals, CDC lag, rollback reversal |
| Security | Validate protection/detection | Secrets, encryption, policy bypass, findings, incident routing, audit |
| Performance | Meet workload baseline | Response, throughput, concurrency, batch window, scale, downstream saturation |
| Resilience | Demonstrate recovery | Zone loss, dependency outage, restore, failover, degraded mode, regional recovery |
| Operations | Prove sustainable support | Metrics, logs, traces, alerts, runbooks, patching, support escalation |
| Financial | Prove accountability | Tags, budgets, forecast, unit cost, anomaly, idle resource cleanup |

## Entry criteria

- Approved architecture baseline, threat/failure scenarios, contracts, and test configuration
- Representative data and load approved
- Rules of engagement, safety, rollback, and evidence handling defined
- Test accounts, identities, tools, owners, and independent reviewers available

## Exit criteria

- Priority requirements have pass/fail/limited results.
- Tier-specific mission, data, security, performance, recovery, and operations thresholds are satisfied.
- Evidence is tied to the tested configuration and reviewed.
- Unresolved findings have owners, mission impact, milestones, and decision authority.
- Rehearsal demonstrates the cutover and rollback decision process.
