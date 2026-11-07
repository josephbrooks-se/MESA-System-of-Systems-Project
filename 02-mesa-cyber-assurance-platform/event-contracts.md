# Event Contracts

## Envelope

Every event contains:

| Field | Rule |
|---|---|
| `eventId` | Globally unique and immutable |
| `eventType` | Namespaced and versioned |
| `occurredAt` | Source observation time |
| `publishedAt` | Producer publication time |
| `producer` | Authenticated workload identifier |
| `subjectId` | Stable affected entity identifier |
| `sequence` | Source-scoped ordering metadata where available |
| `correlationId` | Mission/workflow trace identifier |
| `markings` | Handling and access metadata |
| `schemaVersion` | Contract version |
| `payloadDigest` | Integrity digest of canonical payload |

## `security.finding.v1`

Publishes a new or updated source finding. Consumers must be idempotent by `eventId` and reconcile by source finding ID plus source version. Required payload fields: finding ID, asset/configuration ID, observed time, severity source, status, evidence references, and source confidence.

## `evidence.status-changed.v1`

Indicates accepted, quarantined, expired, superseded, or revoked evidence. Consumers recalculate only claims that reference the evidence or its generating configuration.

## `control.provider-status.v1`

Indicates a common/hybrid control or provider authorization status change. Payload includes provider, control allocation, effective time, reason, known limitations, evidence references, and affected service. Consumers query the dependency graph rather than trusting a producer-supplied consumer list.

## Failure handling

- Reject unrecognized major schema versions.
- Route malformed, unauthorized, or unverifiable events to quarantine.
- Retry transient failures with bounded exponential backoff.
- Send exhausted messages to a dead-letter queue with owner and alert.
- Reconcile after partitions; never infer success from message delivery alone.
- Preserve original and transformed payload digests in provenance.
