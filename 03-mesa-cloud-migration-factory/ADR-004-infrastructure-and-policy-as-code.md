# ADR-004 — Infrastructure and Policy as Code

- **Status:** Accepted
- **Decision:** Provision cloud accounts, networks, services, guardrails, and monitoring through reviewed, version-controlled automation.
- **Drivers:** Repeatability, traceability, peer review, recovery, drift detection, scalable governance.
- **Alternatives:** Console-first administration; tickets executed manually; scripts without state/version control.
- **Consequences:** Consistent delivery and reconstruction; requires module ownership, testing, state protection, release management, and skills.
- **Controls:** Protected repositories, code review, automated tests, signed artifacts, least-privilege pipelines, drift alerts, monitored break-glass process.
