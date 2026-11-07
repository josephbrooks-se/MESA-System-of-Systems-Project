# 10 — Verification and Validation

## Verification philosophy

Verification asks whether the architecture and implementation satisfy specified requirements. Validation asks whether the resulting capability supports the mission outcome under realistic operating and failure conditions.

## Methods

| Method | Best used for | Example |
|---|---|---|
| Inspection | Traceability, configurations, records | Evidence contains provenance fields |
| Analysis | Mission impact, attack paths, capacity | Common-service failure affects boundaries |
| Demonstration | Workflow and usability | Reviewer builds decision brief |
| Test | Enforceable behavior | Missing attribute causes access denial |
| Exercise | Multi-party operational response | Compromised supplier identity is revoked |

## Test layers

1. **Contract:** API/event schema, compatibility, negative input, replay behavior.
2. **Component:** policy, provenance, mapping, workflow, and audit functions.
3. **Integration:** source adapters, identity, event broker, evidence store, A&A export.
4. **Security:** authorization bypass, privilege boundaries, secrets, supply chain, logging.
5. **Resilience:** dependency outage, partition, duplicate/out-of-order events, recovery.
6. **Mission thread:** realistic end-to-end scenarios with accountable users.
7. **Operational:** monitoring, incident response, backup restoration, sustainment handoff.

## Evidence acceptance

Evidence must be relevant to the claim, attributable to a known source, tied to the tested configuration, protected from undetected modification, within its validity period, reproducible or independently reviewable, and explicit about limitations.

## Independent assessment

The architecture owner may prepare evidence but should not be the sole approver of high-consequence claims. Separation of duties is enforced for control implementation, assessment, and risk acceptance where required.

See `verification/cyber-test-plan.md`, `verification/threat-scenarios.md`, and `verification/verification-crosswalk.csv`.
