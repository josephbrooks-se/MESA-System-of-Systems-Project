# 11 — Verification and Validation

## Verification layers

| Layer | Examples |
|---|---|
| Landing zone | Account vending, guardrails, log delivery, keys, budgets, drift |
| Identity/security | Deny-by-default, privilege elevation, workload identity, secrets, threat detection |
| Network | Routes, DNS, ingress/egress, inspection, segmentation, hybrid failure |
| Application | Functional, API, event, batch, integration, accessibility, user acceptance |
| Data | Counts, digests, referential integrity, business totals, lineage, authority |
| Performance | Latency, throughput, concurrency, batch window, scale, quota |
| Resilience | Zone failure, dependency outage, backup restore, regional recovery, degraded mode |
| Operations | Metrics, logs, traces, alerts, incident routing, runbooks, patching |
| Financial | Tags, budgets, forecast, unit cost, anomaly response, resource cleanup |

## Readiness evidence

Evidence records include workload/configuration, procedure and version, execution environment, date/time, operator, result, raw evidence location, integrity, reviewer, limitations, and expiration or invalidation trigger.

## Well-Architected review

Review each production workload against operational excellence, security, reliability, performance efficiency, cost optimization, and sustainability. The review is a structured improvement conversation, not a substitute for authorization or independent assessment.

## Mission-thread validation

At least one representative thread proves the end-to-end user/mission outcome through identity, application, integration, data, monitoring, and recovery. Component tests alone do not validate the portfolio outcome.

## Exit rule

A failed or limited test can proceed only through a recorded exception identifying mission impact, compensating action, owner, expiration, and decision authority.

See `verification/verification-crosswalk.csv`, `verification/cloud-readiness-gates.md`, and `verification/test-plan.md`.
