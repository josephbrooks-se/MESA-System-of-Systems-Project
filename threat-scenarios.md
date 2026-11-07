# MESA Ecosystem Threat Scenarios

| ID | Scenario | Cross-system consequence | Coordinated treatment |
|---|---|---|---|
| TS-ECO-01 | False architecture baseline is published | Cyber/cloud act on unapproved architecture | Signed producer, baseline status, human decision, authoritative API confirmation |
| TS-ECO-02 | Cloud configuration changes without architecture update | Traceability and assurance no longer match reality | Drift/configuration events, conformance review, reopened claims |
| TS-ECO-03 | Evidence is forged, stale, or bound to wrong configuration | Unsafe risk/cutover decision | Provenance, digest/signature, configuration binding, validity, independent review |
| TS-ECO-04 | Compromised identity crosses constituent boundaries | Unauthorized architecture, assurance, or migration change | Short-lived identity, resource/action/purpose policy, separation of duties, revocation |
| TS-ECO-05 | Event replay/duplication/reordering corrupts state | Conflicting baseline, risk, or migration status | Idempotency, source version, sequence, reconciliation, quarantine |
| TS-ECO-06 | Shared identity/policy outage | Protected actions cannot be authorized | Fail-closed writes, approved cached read behavior, emergency process |
| TS-ECO-07 | Contract/schema breaking change | Constituent integration failure | Versioning, consumer inventory, compatibility tests, parallel transition |
| TS-ECO-08 | Human authority is spoofed or automated | Unsafe baseline, risk, cutover, or authorization | Strong identity, human-only scopes, signed record, independent audit |
| TS-ECO-09 | Trace graph is tampered with | Impact analysis hides affected mission elements | Protected changes, provenance, cross-source validation, audit |
| TS-ECO-10 | Constituent outage during cutover | Incomplete evidence or unsafe transition | Safe stop, source retention, bounded queue, reconciliation, authority decision |
| TS-ECO-11 | Shared integration/evidence service compromised | Broad false state or evidence exposure | Isolation, least privilege, signed sources, protected archive, recovery |
| TS-ECO-12 | Insider exports restricted evidence | Unauthorized disclosure | Purpose/resource policy, export approval, audit, data minimization |

## Required analysis

Each scenario links threatened mission assets, preconditions, path, affected interfaces/trust boundaries, mission consequence, preventive/detective/recovery controls, verification, evidence limitations, residual risk, and authority.
