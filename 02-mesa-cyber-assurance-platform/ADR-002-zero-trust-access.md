# ADR-002 — Resource-Centric Zero-Trust Access

- **Status:** Accepted
- **Decision:** Authorize each protected action using identity, device/workload, resource, purpose, environment, relationship, and risk signals.
- **Drivers:** Sensitive evidence, supplier access, distributed hosting, insider risk, multiple programs and boundaries.
- **Alternatives:** Network-zone access; role-only access; application-local authorization.
- **Consequences:** Finer control and auditability; dependency on attribute quality, policy availability, and consistent enforcement.
- **Controls:** Default deny, phishing-resistant authentication, workload identity, policy tests, separation of duties, short-lived credentials, auditable decisions.
- **Failure posture:** Protected writes fail closed; narrowly approved read-only cached behavior may continue for a limited period.
