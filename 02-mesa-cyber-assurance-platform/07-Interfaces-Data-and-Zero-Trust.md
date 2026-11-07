# 07 — Interfaces, Data, and Zero Trust

## Interface strategy

Use synchronous APIs for authoritative queries, commands, and immediate policy feedback. Use events for state changes, monitoring findings, long-running workflows, and dependency notifications. Use governed file transfer where isolated or supplier environments cannot support online integration.

| ID | Interface | Pattern | Key protections |
|---|---|---|---|
| IF-01 | User to experience layer | HTTPS/API | Phishing-resistant MFA, device posture, session policy |
| IF-02 | Experience to domain services | API | Token scope, resource authorization, rate limits |
| IF-03 | Source systems to gateway | API/event | Workload identity, mTLS, schema and replay validation |
| IF-04 | Supplier evidence exchange | File/API | Approved identity, malware scan, signature, quarantine |
| IF-05 | Enclave collector export | Store-and-forward | Signed manifest, sequence, one-way/approved transfer |
| IF-06 | Platform to A&A repository | API/export | Least privilege, field mapping, reconciliation |
| IF-07 | Domain service events | Pub/sub | Topic policy, immutable event ID, integrity, DLQ |
| IF-08 | Evidence object retrieval | Resource API | Purpose/marking policy, short-lived authorization |

## Zero-trust decision model

For every protected request, the policy decision evaluates:

- **Subject:** person, service, supplier, role, clearance/eligibility attributes where applicable
- **Device/workload:** managed state, software identity, health, attestation, risk
- **Resource:** asset, evidence object, field, classification/handling metadata, criticality
- **Action and purpose:** read, modify, approve, export, mission/business purpose
- **Environment:** location, time, session risk, threat state, network path
- **Relationships:** program assignment, need-to-know, separation of duties, authorization boundary

Default behavior is deny when required attributes, policy, or trust signals are missing. Network placement is a constraint and detection layer, not authorization by itself.

## Data entities

| Entity | Selected relationships |
|---|---|
| Mission Thread | depends on Capability and Asset |
| Asset/Component | resides in Boundary; exposes Interface; has Configuration |
| Threat Scenario | targets Asset/Interface; causes Loss Event |
| Requirement | mitigates Threat; allocated to Function/Component |
| Control Allocation | implements Requirement; owned by Provider/Consumer |
| Test Case | verifies Requirement/Control Claim |
| Evidence Record | supports Test/Claim; has provenance and validity |
| Finding | affects Asset/Control; supported by Evidence |
| Risk | aggregates likelihood, consequence, confidence, and dependencies |
| Decision | resolves Risk/Trade; records authority, assumptions, and expiry |

## Evidence catalog metadata

Minimum fields include immutable ID, source ID, evidence type, asset/configuration, boundary, control/requirement claim, collection time, validity period, producer identity, transfer path, integrity digest, markings, access policy, transformation history, reviewer, review state, and supersession link.

## Data minimization

- Prefer metadata and stable source references over unnecessary copies.
- Separate sensitive evidence from general architecture metadata.
- Limit dashboards to the minimum information required for the role.
- Prevent analytics exports from bypassing source markings or resource policy.
- Apply disposition to derived data when its source is removed or expires.
