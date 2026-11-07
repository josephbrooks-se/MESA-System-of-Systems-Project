# 02 — Stakeholders and System-of-Systems Context

## Stakeholders

| Stakeholder | Decision or concern | MESA-CAP support |
|---|---|---|
| Lead Cyber Architect | Architecture integrity, risk posture, disputed technical decisions | Cross-boundary views, ADRs, trade studies |
| Chief/Lead Systems Engineer | Mission threads, interfaces, requirements, technical baseline | End-to-end traceability |
| Program Manager | Mission, cost, schedule, and acquisition risk | Decision briefs and trend views |
| Authorizing Official staff | Evidence sufficiency and residual risk | SSP/SCTM evidence crosswalks |
| Control Assessor | Objective evidence and test coverage | Provenance, validity, test results |
| Product/System Security Engineer | Threats, requirements, mitigations | Threat-to-control allocation |
| Cyber Test organization | Testable claims, environments, entry/exit criteria | Cyber test plans and evidence capture |
| Platform/Enclave owner | Availability, safety, isolation, configuration | Segregated collection and change control |
| Common-control provider | Inheritance terms and service status | Provider-consumer dependency graph |
| Supplier | Contracted cyber evidence and interface assurance | Controlled evidence exchange |
| Sustainment organization | Vulnerability response and configuration drift | Monitoring and POA&M workflow |
| Data steward | Markings, retention, provenance, access | Evidence catalog governance |

## External systems

| ID | External system | Authoritative for | Integration mode |
|---|---|---|---|
| EX-01 | Requirements/MBSE repository | Requirements, functions, logical interfaces | Read API/export |
| EX-02 | A&A repository | Official authorization records | Governed API/export |
| EX-03 | Asset/CMDB/SBOM sources | Asset and component facts | API/event/file |
| EX-04 | Security scanners and SIEM | Findings and telemetry | Event/API |
| EX-05 | Test management repository | Plans, results, defects | API/file |
| EX-06 | Issue/work management | Remediation status | API/event |
| EX-07 | Identity and policy services | Identity, attributes, policy decisions | Runtime protocol/API |
| EX-08 | Supplier exchange | Contracted evidence packages | Controlled file/API |
| EX-09 | Isolated enclave collector | Approved local observations | Store-and-forward |

## Context constraints

- Direct connectivity is not assumed between all domains.
- External repositories remain systems of record; MESA-CAP records stable identifiers and provenance.
- Data release and cross-domain transfer use separately authorized mechanisms.
- Evidence access can be narrower than architecture metadata access.
- A system can consume both common and system-specific controls.

See `diagrams/01-system-context.mmd`.
