# SoS Threat and Failure Scenarios

| ID | Scenario | Effect | Treatment |
|---|---|---|---|
| TS-SOS-01 | False architecture baseline event | Consumers act on unapproved design | Signed producer identity, baseline status, query authority |
| TS-SOS-02 | Interface contract breaking change | Cyber/cloud integrations fail | Versioning, consumer inventory, compatibility tests, parallel transition |
| TS-SOS-03 | Trace graph tampering | Impact/evidence relationships become false | Protected change, provenance, audit, independent verification |
| TS-SOS-04 | Duplicate/out-of-order event | Stale state overwrites current state | Idempotency, source version, ordering/reconciliation |
| TS-SOS-05 | Compromised workload identity | Unauthorized cross-system changes | Short-lived identity, resource/action policy, revocation, monitoring |
| TS-SOS-06 | SoS service unavailable | Baseline changes and impact queries stop | Read-only approved baseline, queued events, recovery |
| TS-SOS-07 | Cyber Assurance unavailable | New risk decisions lack evidence | Pause risk/authorization approvals; preserve current conditions |
| TS-SOS-08 | Cloud Migration unavailable | Migration/cutover execution stops | Safe stop, source retention, status reconciliation |
| TS-SOS-09 | Evidence reference becomes stale/revoked | Assurance claims no longer valid | Freshness, invalidation event, reopened decisions |
| TS-SOS-10 | Human authority spoofed | Unsafe baseline/risk/cutover decision | Strong identity, separation of duties, signed decision record |
