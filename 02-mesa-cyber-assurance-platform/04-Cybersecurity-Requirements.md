# 04 — Threat-Informed Cybersecurity Requirements

## Requirement quality rule

Each requirement uses a unique ID, accountable owner, rationale, allocation, verification method, and upstream/downstream trace. “Secure” without a measurable condition is not acceptable.

| ID | Requirement | Allocation | Verification |
|---|---|---|---|
| CYR-001 | The system shall associate every registered critical asset with an owner, mission thread, boundary, and criticality. | Architecture Registry | Inspection/query |
| CYR-002 | The system shall evaluate access using subject, device/workload, resource, purpose, environment, and current risk attributes. | Policy Plane | Test |
| CYR-003 | The system shall deny access when required policy attributes are unavailable or invalid. | Policy Plane | Negative test |
| CYR-004 | The system shall record policy decision, enforcement result, subject, resource, purpose, and correlation ID for protected actions. | Audit Service | Test/inspection |
| CYR-005 | The system shall cryptographically verify evidence-package integrity and source identity before acceptance. | Ingestion Gateway | Test |
| CYR-006 | The system shall quarantine evidence that fails schema, marking, integrity, or replay validation. | Ingestion Gateway | Fault injection |
| CYR-007 | The system shall preserve source, collection time, transfer path, transformation history, and reviewer state for each evidence record. | Evidence Catalog | Inspection |
| CYR-008 | The system shall flag evidence when its validity period expires or its generating configuration changes. | Evidence Service | Test |
| CYR-009 | The system shall map common-control providers to consumers, validation terms, and authorization dependencies. | Control Service | Inspection |
| CYR-010 | The system shall notify affected owners when an inherited control or common service changes status. | Event/Workflow Service | Test |
| CYR-011 | The system shall support store-and-forward collection for disconnected periods of at least 72 hours. | Enclave Collector | Demonstration |
| CYR-012 | The system shall reconcile duplicate and out-of-order records using immutable IDs, sequence metadata, and idempotent processing. | Ingestion/Event Services | Test |
| CYR-013 | The system shall maintain versioned interface and event contracts with compatibility checks. | Integration Services | Analysis/test |
| CYR-014 | The system shall trace each priority risk through threat, requirement, architecture allocation, control, test, evidence, finding, and decision. | Traceability Service | Inspection |
| CYR-015 | The system shall prevent automated workflows from accepting residual risk or approving authorization. | Decision Service | Negative test |
| CYR-016 | The system shall expose evidence freshness, coverage, and confidence separately from control implementation status. | Analytics Service | Demonstration |
| CYR-017 | The system shall isolate collector compromise from embedded mission execution and central management services. | Collector/Gateway | Analysis/test |
| CYR-018 | The system shall support revocation of a supplier or workload identity without changing embedded mission configuration. | Identity/Policy Plane | Test |
| CYR-019 | The system shall apply retention and disposition rules based on evidence type and handling metadata. | Data Governance | Inspection/test |
| CYR-020 | The system shall continue read-only access to the last validated risk baseline during loss of a noncritical integration. | Experience/Cache | Resilience test |

## Nonfunctional constraints

- **Availability:** 99.9% monthly for central decision-support services; collectors do not affect mission execution.
- **Recovery:** central RTO 4 hours and RPO 15 minutes for authoritative platform data; local queues reconcile after recovery.
- **Performance:** 95th percentile interactive query under 3 seconds for portfolio views up to the sizing baseline.
- **Scalability baseline:** 100,000 assets, 5 million evidence metadata records, and 2,000 events/second burst.
- **Audit retention:** defined by organizational policy; the example does not prescribe a real retention period.
- **Accessibility:** user interfaces target WCAG 2.2 AA where applicable.

## Tailoring note

These are architecture-level example requirements. A real program would derive protection needs from mission loss scenarios, system categorization, threat intelligence, safety constraints, acquisition strategy, and applicable policy.
