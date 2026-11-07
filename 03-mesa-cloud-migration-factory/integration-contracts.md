# Integration Contract Principles

## Required contract fields

Every critical interface defines:

- Producer, consumer, owner, and authoritative source
- Purpose and mission thread
- Protocol/pattern and endpoint discovery
- Identity, authorization, encryption, and data policy
- Schema, semantics, units, valid values, and compatibility
- Frequency, latency, throughput, size, and service objectives
- Retry, timeout, idempotency, ordering, replay, and reconciliation
- Failure, degraded mode, alerting, and recovery
- Version, deprecation, testing, and change notification
- Evidence and monitoring needed for acceptance

## Cloud transition states

1. **Legacy-to-legacy:** current interface baseline.
2. **Legacy-to-cloud:** transitional hybrid contract and network path.
3. **Cloud-to-cloud:** target contract using approved platform services.
4. **Legacy removal:** consumer validation and source/interface closure.

## Anti-corruption boundary

Where legacy semantics differ from the target domain model, use a versioned adapter rather than spreading legacy formats across new services. Give the adapter an owner, tests, telemetry, retirement condition, and cost.

## Event envelope

Events include immutable ID, type, schema version, producer identity, subject, occurrence/publication times, correlation ID, sequence metadata where available, markings, and payload digest. Consumers are idempotent and tolerate bounded delay and reordering.
