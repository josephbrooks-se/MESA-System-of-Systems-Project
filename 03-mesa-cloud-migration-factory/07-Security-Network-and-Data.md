# 07 — Security, Network, Integration, and Data

## Zero-trust access model

Every protected request evaluates subject, device/workload, resource, action, purpose, environment, relationship, and current risk. Network placement reduces exposure but never grants implicit trust.

### Workforce identity

- Federate to the authoritative identity provider.
- Require strong authentication and managed-device posture for privileged access.
- Use role-based baseline access plus resource and purpose attributes.
- Elevate privilege through approved, time-bounded workflows.
- Maintain break-glass identities offline, monitored, tested, and narrowly scoped.

### Workload identity

- Prefer short-lived, platform-issued credentials over static secrets.
- Authorize service-to-service access at the resource and action level.
- Rotate keys/secrets and prevent credentials in source or images.
- Record identity, resource, purpose, decision, and result for protected actions.

## Network architecture

- Private connectivity links legacy sites and the cloud network hub.
- Workload networks are isolated and attach through governed routing.
- Central ingress/egress, DNS, inspection, and shared endpoints reduce uncontrolled paths.
- East-west flows are explicitly modeled and minimized.
- Management traffic is separated from application and data traffic.
- Route, firewall, DNS, and certificate changes are reviewed and automated.

## Integration patterns

| Need | Preferred pattern | Key controls |
|---|---|---|
| Immediate command/query | Versioned API | Identity, authorization, quotas, timeouts |
| State-change distribution | Event | Schema, idempotency, replay, ordering rules |
| Work decoupling | Queue | DLQ, retry, visibility, poison-message handling |
| Long-running orchestration | Workflow | State, compensation, audit, timeout |
| Bulk/disconnected transfer | Governed file/object | Manifest, integrity, malware scan, reconciliation |

## Data migration

1. Identify data authority, owner, consumers, sensitivity, volume, growth, retention, and residency.
2. Profile quality and reconcile known duplicates, gaps, and invalid records.
3. Select bulk transfer, replication, change-data capture, or rebuild method.
4. Encrypt and authenticate transfer; record source, time, transformation, and digest.
5. Reconcile counts, checksums, referential integrity, semantic rules, and business totals.
6. Freeze or coordinate writes at the approved cutover point.
7. Declare the target authoritative only after acceptance and record reversal conditions.

## Data architecture

- Object storage is the durable landing and exchange layer where appropriate.
- Relational, NoSQL, cache, search, and analytics stores are selected by access pattern.
- Catalog and lineage connect source, transformation, consumer, owner, and policy.
- Lifecycle policies move or remove data according to value and retention—not age alone.
- Nonproduction data is synthetic, masked, or explicitly authorized.

See `diagrams/05-hybrid-network.mmd`, `diagrams/06-zero-trust.mmd`, and `diagrams/07-data-migration.mmd`.
