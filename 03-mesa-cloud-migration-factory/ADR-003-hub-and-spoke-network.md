# ADR-003 — Governed Hub-and-Spoke Hybrid Network

- **Status:** Accepted
- **Decision:** Connect legacy sites, shared services, and workload networks through a governed routing, DNS, inspection, ingress, and egress hub.
- **Drivers:** Hybrid transition, segmentation, central policy, route visibility, reusable connectivity.
- **Alternatives:** Full mesh; independent workload connections; internet-only connectivity.
- **Consequences:** Consistent governance and reduced path sprawl; hub scale, availability, and organizational coordination become critical.
- **Controls:** Multi-zone design, route automation, explicit attachments, egress policy, path telemetry, quota monitoring, failure exercises.
