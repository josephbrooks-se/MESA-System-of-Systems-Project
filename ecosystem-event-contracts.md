# Ecosystem Event Contracts

## Shared envelope

Every event uses the schema in `schemas/mesa-ecosystem-event.schema.json` and includes immutable event ID, namespaced event type, occurrence/publication times, authenticated producer, subject, correlation, source sequence/version where available, schema version, markings, payload digest, and data.

## Architecture events

### `mesa.architecture.baseline-approved.v1`

Producer: MESA SoS Architecture. Consumers: Cyber Assurance and Cloud Migration. Includes baseline ID/version, mission/requirement/system/interface references, decision reference, effective time, and evidence references.

### `mesa.architecture.interface-changed.v1`

Producer: MESA SoS Architecture. Consumers: registered producers/consumers. Includes interface ID, old/new version, compatibility classification, effective/retirement dates, owner, and migration plan.

## Cyber-assurance events

### `mesa.cyber.evidence-status.v1`

Producer: Cyber Assurance. Consumers: SoS Architecture and Cloud Migration. Includes evidence ID, claim references, review state, validity, limitations, configuration, and invalidation reason.

### `mesa.cyber.assurance-readiness.v1`

Producer: Cyber Assurance. Consumers: Cloud Migration and SoS Architecture. Includes subject/wave, ready/conditional/not-ready state, findings, control/evidence gaps, conditions, reviewer, and expiry.

### `mesa.cyber.risk-decision.v1`

Producer: Cyber Assurance after human decision. Consumers: affected systems. Includes risk/decision IDs, authority, treatment, conditions, expiry, and affected traces.

## Cloud-migration events

### `mesa.cloud.workload-changed.v1`

Producer: Cloud Migration. Consumers: SoS Architecture and Cyber Assurance. Includes workload ID, owner, criticality, disposition, target, dependencies, wave, configuration, and status.

### `mesa.cloud.migration-status.v1`

Producer: Cloud Migration. Consumers: SoS Architecture and Cyber Assurance. Includes workload/wave, stage/gate, progress, blockers, evidence, and next decision.

### `mesa.cloud.cutover-decision.v1`

Producer: Cloud Migration after human decision. Consumers: SoS Architecture and Cyber Assurance. Includes cutover ID, workload/wave, decision, authority, effective time, rollback deadline, conditions, and evidence.

## Processing rules

- Authenticate producer and verify signature/digest before processing.
- Reject unsupported major schema versions.
- Be idempotent by `eventId`.
- Reconcile using authoritative source version; do not use arrival order alone.
- Quarantine unverifiable, malformed, unauthorized, or conflicting events.
- Retry transient failures with bounded backoff and dead-letter exhausted events.
- Alert an accountable owner when queue age, failures, or conflicts exceed threshold.
- Query the authoritative API before a material decision if event state may be incomplete.
