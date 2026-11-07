# Continuous Monitoring Strategy

## Objective

Detect changes that invalidate architecture assumptions, control claims, evidence, or authorization decisions, then route them according to mission impact.

| Signal | Source | Frequency | Threshold | Owner | Response |
|---|---|---|---|---|---|
| Critical asset/configuration change | CMDB/MBSE | Event plus daily reconcile | Unapproved or unmapped change | Architecture owner | Freeze affected claim; assess impact |
| Identity/policy change | ICAM/policy repo | Event | Privileged grant or policy denial regression | Security operations | Review and test; revoke if needed |
| High-risk finding | Scanner/SIEM/test | Event | Mission-adjusted high/critical | Product security | Triage within one business day |
| Evidence expiration | Evidence Catalog | Daily | Validity threshold reached | Evidence owner | Replace, justify, or mark claim limited |
| Common-control status change | Provider/A&A source | Event plus daily reconcile | Degraded, expired, or withdrawn | Authorization architect | Identify consumers and reopen risk |
| Interface contract drift | Schema registry | Build/event | Breaking or unapproved version | Integration owner | Block release or approve migration |
| Collector backlog | Collector telemetry | Hourly when connected | Queue age/volume exceeds SLO | Site operator | Restore transfer; assess evidence gap |
| Backup/recovery health | Operations platform | Daily/monthly exercise | Failed backup or recovery objective | Service owner | Correct and record resilience risk |

## Risk tiers

- **Tier 1:** mission-critical/high-consequence changes; event-driven review and immediate escalation.
- **Tier 2:** significant but bounded changes; daily correlation and time-boxed review.
- **Tier 3:** routine posture; periodic sampling and trend analysis.

## Reopen rules

Reopen a claim or decision when its generating configuration changes materially, critical evidence expires or is revoked, an inherited control/provider degrades, a new credible threat invalidates assumptions, test limitations become material, or the accepting authority's conditions expire.

## Reporting principles

Show implementation status, evidence confidence, data freshness, inherited dependency, and residual risk as separate dimensions. Missing telemetry is a visibility risk, not evidence that the system is secure.
