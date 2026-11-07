# 02 — Portfolio Discovery and Rationalization

## Discovery objective

Create an evidence-based portfolio baseline before assigning migration waves. Application names alone are insufficient; each record must connect mission purpose, users, data, infrastructure, interfaces, owners, cost, security, performance, recovery, and lifecycle.

## Minimum inventory

| Domain | Required information |
|---|---|
| Mission | Capability, users, criticality, business events, allowable outage |
| Ownership | Mission owner, product owner, technical owner, data owner, security owner |
| Application | Technology stack, versions, support status, deployment topology, licenses |
| Infrastructure | Compute, storage, network, appliances, environments, utilization |
| Data | Types, volume, growth, authority, sensitivity, retention, residency |
| Interfaces | Producer, consumer, protocol, frequency, latency, data contract, failure behavior |
| Operations | Monitoring, backup, recovery, incidents, support hours, runbooks |
| Security | Identity, trust boundaries, privileged paths, findings, authorization dependencies |
| Financial | Hosting, license, labor, support, data-transfer, and retirement costs |
| Change | Planned releases, vendor changes, contract events, end-of-life dates |

## 7R disposition

| Strategy | Use when | Architecture concern |
|---|---|---|
| Retire | Capability is unused, duplicated, or no longer justified | Data retention and dependency removal |
| Retain | Constraint prevents current migration | Explicit owner, reason, risk, and exit trigger |
| Rehost | Fast relocation provides value without design change | Technical debt and operating cost may remain |
| Relocate | Existing virtualized/platform stack can move as a unit | Licensing, platform compatibility, and hidden coupling |
| Repurchase | SaaS/COTS replacement better meets the need | Data migration, process change, vendor dependency |
| Replatform | Managed services reduce operations without major redesign | Compatibility and behavior differences |
| Refactor | Mission value justifies cloud-native redesign | Highest complexity, testing, and transition risk |

## Scoring dimensions

Score 1–5 for mission value, cloud fit, technical health, dependency complexity, data complexity, security readiness, operational readiness, financial value, and change capacity. The score supports—not replaces—architect judgment.

## Dependency analysis

Each system must identify upstream/downstream applications, shared databases, identity, DNS, file transfers, message brokers, batch schedules, monitoring, backup, certificate, licensing, external partner, and human workflow dependencies.

Use `templates/workload-inventory.csv`, `templates/migration-assessment.csv`, and `templates/dependency-matrix.csv`.

## Discovery exit criteria

- 100% of in-scope systems have owners and approved dispositions.
- Tier 1/2 systems have validated dependency maps and current performance baselines.
- Unknown interfaces, unsupported components, and data-quality gaps are assigned owners.
- Retain decisions have expiration or reassessment triggers.
- Retirement candidates have data and dependency closure plans.
