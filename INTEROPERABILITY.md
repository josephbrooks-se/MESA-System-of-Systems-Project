# MESA Ecosystem Interoperability

## Interoperability objectives

1. Preserve mission-to-evidence traceability across all three systems.
2. Allow each constituent system to remain independently operable and authoritative for its domain.
3. Prevent shared-database coupling and undocumented point-to-point exchange.
4. Support disconnected, delayed, duplicated, or out-of-order updates without corrupting authority.
5. Make identity, provenance, data markings, policy, failure, and decision authority explicit.

## Canonical identifiers

| Entity | Pattern | Authority |
|---|---|---|
| Mission outcome | `MO-###` | SoS Architecture |
| Operational thread | `OT-###` | SoS Architecture |
| Requirement | `REQ-###` or domain-specific `CLR/CYR-###` | SoS Architecture/domain owner |
| Constituent system | `SYS-###` | SoS Architecture |
| Workload | `WL-SYN-###` | Cloud Migration |
| Interface | `IF-###` | SoS Architecture with producer/consumer owners |
| Control allocation | `CA-SYN-###` | Cyber Assurance |
| Threat scenario | `TS-###` | Cyber Assurance with architecture owners |
| Test | `VT-###` | Verification owner |
| Evidence | `EV-SYN-###` | Evidence Catalog; source remains authoritative |
| Risk | `R-###` | Owning risk authority |
| Decision | `DEC-###` | Designated human authority |
| Migration wave | `W#` | Cloud Migration |

## Source authority

- SoS Architecture is authoritative for approved mission/architecture baselines and trace relationships.
- Cyber Assurance is authoritative for evidence review state, control/inheritance relationships, cyber findings, and authorization-support workflow.
- Cloud Migration is authoritative for discovered workload state, migration execution, cloud configuration references, cutover status, legacy exit, and cost allocation.
- Source tools remain authoritative for native records; MESA systems store stable references and approved projections.

## Integration patterns

- Use synchronous REST for commands, authoritative lookup, and decisions needing immediate response.
- Use signed events for state changes, monitoring, long-running workflow, and dependency notification.
- Use governed file/object exchange when online integration is unavailable.
- Never integrate through direct cross-system database access.

## Common request controls

- Federated user or workload identity
- Resource/action/purpose authorization
- `X-Correlation-Id` for end-to-end trace
- `Idempotency-Key` for create/decision operations
- `If-Match` for optimistic concurrency
- Contract/schema version
- Data markings and access purpose
- Standard problem response without sensitive implementation disclosure

## Common event envelope

Every event contains immutable `eventId`, namespaced `eventType`, `occurredAt`, `publishedAt`, authenticated `producer`, `subjectId`, `correlationId`, optional sequence, schema version, markings, and payload digest.

Consumers:

- Are idempotent by event ID.
- Reconcile state using source version and authority rules.
- Tolerate bounded delay and reordering.
- Quarantine unverifiable or unsupported events.
- Use dead-letter handling and accountable alerts.
- Do not treat event delivery as proof of business completion.

## Conflict resolution

1. Identify authoritative source for the disputed field/entity.
2. Preserve both received records and provenance.
3. Reject silent last-write-wins for mission, evidence, risk, or decision state.
4. Reconcile automatically only when a deterministic approved rule exists.
5. Route unresolved conflicts to the accountable data/architecture owner.
6. Reopen downstream claims or decisions when conflict affects assurance.

## Compatibility

- Backward-compatible additive changes use the existing major version.
- Breaking changes require a new major version, consumer inventory, parallel availability, migration plan, and retirement approval.
- Schemas and examples are maintained in version control and validated in CI.

## Degraded operation

- If Cyber Assurance is unavailable, architecture and migration work may continue only within previously approved conditions; new risk acceptance cannot occur.
- If Cloud Migration is unavailable, architecture and assurance remain readable; migration execution and cutover stop safely.
- If SoS Architecture is unavailable, current approved baselines remain readable; material baseline changes and new wave approvals pause.
- If shared identity/policy is unavailable, protected writes fail closed; only explicitly approved cached/read behavior may continue.
- If event transport is unavailable, producers queue within limits and reconcile after recovery.
