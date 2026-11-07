# ADR-003 — Federated Evidence with Central Catalog

- **Status:** Accepted
- **Decision:** Keep native tools authoritative while cataloging standardized provenance and storing approved copies only when justified.
- **Drivers:** Data minimization, markings, source ownership, scale, reproducibility, review needs.
- **Alternatives:** Copy all evidence centrally; store links only; manual document packages.
- **Consequences:** Preserves authority and reduces unnecessary duplication; requires durable identifiers, connector health, and availability rules.
- **Controls:** Immutable evidence IDs, source and configuration binding, integrity digests, validity windows, transformation lineage, quarantine.
