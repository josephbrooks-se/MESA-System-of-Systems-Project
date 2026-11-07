# 04 — Cloud Migration Architecture Requirements

| ID | Requirement | Allocation | Verification |
|---|---|---|---|
| CLR-001 | Every in-scope system shall have an approved disposition, owner, target state, and exit criteria. | Portfolio Service | Inspection |
| CLR-002 | Critical dependencies shall be validated before wave approval. | Discovery/Architecture | Inspection |
| CLR-003 | Workload resources shall be isolated by approved account, environment, network, and resource policy. | Landing Zone | Test/inspection |
| CLR-004 | Workforce access shall use federation, strong authentication, least privilege, and time-bounded elevation. | Identity Platform | Test |
| CLR-005 | Workload-to-workload access shall use authenticated identities and resource-level authorization. | Security Platform | Test |
| CLR-006 | Cloud resources shall be provisioned through reviewed, version-controlled automation except approved break-glass actions. | Platform Engineering | Inspection |
| CLR-007 | Security-relevant activity shall be centrally collected in a protected log archive. | Security/Operations | Test |
| CLR-008 | Data shall be classified, encrypted, attributable to an owner, and governed through retention and residency rules. | Data Platform | Inspection/test |
| CLR-009 | Interface contracts shall define semantics, versioning, authentication, latency, failure, replay, and reconciliation behavior. | Integration Platform | Contract test |
| CLR-010 | Tier 1/2 workloads shall demonstrate recovery objectives before production cutover. | Workload/Recovery | Exercise |
| CLR-011 | Each cutover shall define entry criteria, decision authority, rollback point, validation, and communication. | Migration Factory | Inspection/exercise |
| CLR-012 | Source environments shall remain recoverable until stabilization acceptance closes the rollback window. | Migration Factory | Inspection |
| CLR-013 | The system shall detect configuration drift from the approved infrastructure and policy baseline. | Platform/Security | Test |
| CLR-014 | Workloads shall expose standardized metrics, logs, traces, health, and business/mission indicators. | Observability | Demonstration |
| CLR-015 | Cloud costs shall be attributable to workload, environment, owner, and capability. | FinOps | Query/inspection |
| CLR-016 | Migration evidence shall preserve source, configuration, execution time, result, integrity, and reviewer. | Evidence Service | Inspection |
| CLR-017 | The cloud platform shall support controlled hybrid operation during transition. | Network/Integration | Test |
| CLR-018 | Priority mission threads shall pass functional, security, performance, resilience, and data-integrity tests after cutover. | Verification | Test |
| CLR-019 | Legacy resources shall be decommissioned after accepted stabilization unless an exception is approved. | Governance/Operations | Inspection |
| CLR-020 | Material architecture changes shall update requirements, models, ADRs, tests, evidence, and operating procedures. | Architecture Governance | Audit |

## Nonfunctional constraints

- **Availability:** targets are workload-tier specific; no single platform target is imposed on all systems.
- **Recovery:** RTO/RPO are derived from mission-impact analysis and validated through exercise.
- **Performance:** workloads must meet approved response-time, throughput, batch-window, and concurrency baselines.
- **Scalability:** load tests include expected growth, burst, service quotas, and downstream constraints.
- **Security:** missing required identity or policy attributes cause protected actions to deny by default.
- **Auditability:** privileged and production-changing actions include identity, purpose, resource, result, and correlation data.
- **Portability:** data export, configuration reconstruction, and exit dependencies are documented for critical services.
