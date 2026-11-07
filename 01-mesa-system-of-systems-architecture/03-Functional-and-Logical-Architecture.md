# 03 — Functional and Logical Architecture

## Logical functions

| ID | Function | Allocation |
|---|---|---|
| LF-01 | Define mission outcome and measures | Mission Architecture Service |
| LF-02 | Manage stakeholders, actors, boundaries, and context | Context Service |
| LF-03 | Model operational threads, states, and degraded behavior | Behavior Service |
| LF-04 | Derive, prioritize, and allocate requirements | Requirements Service |
| LF-05 | Define logical constituent systems and shared services | Logical Architecture Service |
| LF-06 | Govern interfaces and information exchanges | Interface Registry |
| LF-07 | Evaluate alternatives and architecture decisions | Trade/ADR Service |
| LF-08 | Maintain cross-domain traceability | Traceability Service |
| LF-09 | Sequence capabilities and delivery increments | Roadmap Service |
| LF-10 | Coordinate verification and evidence claims | Verification Service |
| LF-11 | Govern baselines, change, exceptions, and debt | Governance Service |
| LF-12 | Assess mission impact of constituent-system change | Dependency/Impact Service |

## Logical blocks

- Mission Architecture
- Operational Thread/Behavior Model
- Requirements and Allocation
- Constituent-System Registry
- Interface and Information-Exchange Registry
- Dependency and Impact Graph
- Traceability and Evidence Reference
- Architecture Decision and Trade Study
- Capability Roadmap and Backlog Translation
- Verification and Governance

## Architectural rule

Each logical block owns a defined information domain and exposes it through approved APIs/events. Cross-block and cross-system database access is prohibited.
