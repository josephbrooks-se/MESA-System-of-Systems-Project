# 04 — Interfaces and Information Exchanges

| ID | Exchange | Producer | Consumer | Pattern | Authority |
|---|---|---|---|---|---|
| IF-001 | Architecture baseline | SoS Architecture | Cyber, Cloud | API + event | SoS Architecture |
| IF-002 | Requirement/control allocation | SoS/Cyber | All | API + event | Owning domain |
| IF-003 | Workload and dependency state | Cloud Migration | SoS, Cyber | API + event | Cloud Migration |
| IF-004 | Threat/finding/assurance status | Cyber Assurance | SoS, Cloud | API + event | Cyber Assurance |
| IF-005 | Migration and cutover state | Cloud Migration | SoS, Cyber | API + event | Cloud Migration |
| IF-006 | Verification evidence | All sources | Cyber catalog, SoS trace | API/event/reference | Source for native result; catalog for review state |
| IF-007 | Architecture/risk/cutover decision | Human authority via owning system | Affected systems | API + event | Designated authority |
| IF-008 | Trace query | SoS Architecture | All | API | SoS trace graph |

## Contract requirements

Each exchange defines identity, authorization, purpose, schema, semantics, version, authoritative source, latency, throughput, error, retry, timeout, idempotency, ordering, replay, reconciliation, markings, retention, monitoring, and evidence.

## Interoperability rule

An event announces a change; consumers query the authoritative API when they need complete current state. Event delivery alone is not proof that the business action completed.
