# 11 — RMF and Authorization Strategy

## Architectural intent

MESA-CAP supports a disciplined, system-life-cycle risk process. It does not automatically determine compliance or authorize a system. The official A&A repository remains authoritative.

## Prepare

- Define mission/business functions, stakeholders, risk tolerance, common services, evidence rules, and portfolio dependencies.
- Establish reusable architecture patterns, control implementation statements, and evidence schemas.

## Categorize

- Document information types, mission consequences, safety dependencies, boundary assumptions, and rationale.
- Expose disagreements and missing data; do not manufacture a category from incomplete inputs.

## Select

- Tailor controls based on threat, architecture, mission consequence, technology, and applicable policy.
- Record control origin, tailoring rationale, allocation, common/system-specific/hybrid status, and verification approach.

## Implement

- Link implementation claims to components, configurations, interfaces, owners, and evidence.
- Distinguish design intent from deployed and verified state.

## Assess

- Use claim-specific procedures and representative configurations.
- Record assessor independence, limitations, exceptions, sampling, and confidence.

## Authorize

- Present mission impact, unresolved findings, inherited dependencies, evidence limitations, alternatives, and time-bounded residual risk.
- Require designated human authority for acceptance and authorization decisions.

## Monitor

- Watch changes to threats, assets, software components, identities, control providers, configurations, findings, evidence age, and authorization dependencies.
- Reopen affected claims when change exceeds a defined threshold.

## Authorization boundary strategy

The platform is decomposed into central services, data stores, integration gateways, and enclave collectors. Boundary decisions consider administrative control, mission function, data flows, shared services, technology, and authorization responsibility—not deployment convenience alone.

## Inheritance model

Each inherited control record identifies provider, consumer, service, implementation responsibility, validation terms, evidence, service-level dependency, authorization status, failure impact, and consumer-specific responsibilities. Inheritance is a verified relationship, not a checkbox.

## Core authorization outputs

- System security plan inputs and boundary narrative
- Security control traceability matrix
- Control inheritance and responsibility matrix
- Evidence catalog and sufficiency assessment
- Findings and POA&M records
- Cyber test results and limitations
- Continuous monitoring strategy
- Residual-risk decision record

Templates in `rmf/` are intentionally generic and non-authoritative.
