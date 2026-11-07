# ADR-002 — Federated and Short-Lived Identity

- **Status:** Accepted
- **Decision:** Federate workforce identities from the authoritative enterprise provider and issue short-lived workload credentials through the cloud identity plane.
- **Drivers:** Lifecycle control, least privilege, auditability, credential reduction, separation of duties.
- **Alternatives:** Cloud-local users; shared accounts; long-lived service keys.
- **Consequences:** Central lifecycle and stronger control; dependency on federation, attributes, policy quality, and break-glass design.
- **Controls:** Strong authentication, device posture, time-bounded elevation, role/resource policy, monitored emergency identities, credential scanning.
