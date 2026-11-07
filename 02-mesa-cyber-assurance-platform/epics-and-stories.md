# Epics and Representative Stories

## EP-01 — Architecture and Boundary Registry

- **US-01:** As a lead architect, I can register assets, boundaries, interfaces, owners, and mission threads so that dependencies are explicit.
- **US-02:** As a reviewer, I can see unresolved mappings and source freshness so that I do not assume inventory completeness.

## EP-02 — Threat-Informed Requirements

- **US-03:** As a system security engineer, I can link loss scenarios to requirements and allocations so that mitigations remain mission-based.
- **US-04:** As a chief engineer, I can identify requirements without a verification method or architecture allocation.

## EP-03 — Evidence Trust and Catalog

- **US-05:** As an assessor, I can inspect source, configuration, integrity, freshness, lineage, and limitations for each evidence record.
- **US-06:** As a data steward, I can quarantine records that fail schema, marking, identity, integrity, or replay validation.

## EP-04 — Authorization Dependency Management

- **US-07:** As a control provider, I can publish a status change with evidence and limitations.
- **US-08:** As an authorization architect, I can identify consumers affected by a provider degradation.
- **US-09:** As a boundary owner, I receive an impact notification and can open a reassessment workflow.

## EP-05 — Isolated Enclave Collection

- **US-10:** As a site operator, I can package approved observations for store-and-forward without enabling an inbound central command path.
- **US-11:** As an integration owner, I can reconcile duplicates, ordering gaps, and conflicts after reconnection.

## EP-06 — Risk and Decision Support

- **US-12:** As a program leader, I can compare mitigation alternatives across mission impact, cost, schedule, and evidence confidence.
- **US-13:** As a designated authority, I can record a time-bounded decision with conditions, assumptions, and revisit triggers.

## EP-07 — Continuous Monitoring

- **US-14:** As an evidence owner, I am notified before evidence expires and when its generating configuration changes.
- **US-15:** As a cyber architect, I can see decisions reopened by threat, control-provider, configuration, or evidence changes.

## Cross-cutting acceptance criteria

Every story includes resource-level authorization, auditability, data markings, failure behavior, accessibility, telemetry, traceability, and public-safe synthetic test data.
