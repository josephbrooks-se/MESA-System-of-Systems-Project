# ADR-005 — Segregated Embedded/OT Collectors

- **Status:** Accepted
- **Decision:** Collect only approved observations through a constrained intermediary; do not install the central management plane in embedded mission execution environments.
- **Drivers:** Safety, availability, isolation, legacy constraints, intermittent connectivity, certification and configuration control.
- **Alternatives:** Direct central agents; manual collection only; full platform deployment in each enclave.
- **Consequences:** Preserves mission isolation; reduces real-time visibility and adds reconciliation and collector assurance work.
- **Controls:** No inbound command path, least-function collector, signed manifests, local queue limits, approved transfer, integrity verification, revocable identity, compromise containment.
