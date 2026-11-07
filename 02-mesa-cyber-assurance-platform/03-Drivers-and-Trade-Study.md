# 03 — Drivers, Alternatives, and Trade Study

## Architecture drivers

| ID | Driver | Architectural consequence |
|---|---|---|
| D-01 | Mission continuity | Assurance system cannot be in the embedded execution path |
| D-02 | Multiple boundaries | Explicit boundary, inheritance, and dependency model |
| D-03 | Intermittent connectivity | Store-and-forward with reconciliation |
| D-04 | Evidence sensitivity | Resource-level policy, markings, and least privilege |
| D-05 | Auditability | Immutable event history and signed provenance |
| D-06 | Tool diversity | Standards-based APIs, events, and adapters |
| D-07 | Authorization tempo | Reusable evidence and continuous monitoring |
| D-08 | Supply-chain risk | Supplier identity, SBOM linkage, and evidence constraints |

## Deployment alternatives

Weights reflect this notional mission, not a universal answer. Scores range from 1 (poor) to 5 (strong).

| Criterion | Weight | Central enterprise | Federated only | Hybrid governed platform |
|---|---:|---:|---:|---:|
| Isolated-enclave compatibility | 25 | 2 | 5 | 5 |
| Evidence consistency | 20 | 5 | 2 | 4 |
| Authorization dependency visibility | 15 | 5 | 2 | 5 |
| Mission availability | 15 | 3 | 5 | 4 |
| Integration/sustainment cost | 10 | 4 | 2 | 3 |
| Data minimization | 10 | 2 | 5 | 4 |
| Incremental delivery | 5 | 3 | 3 | 5 |
| **Weighted total / 5** | **100** | **3.35** | **3.70** | **4.35** |

## Recommendation

Select the **hybrid governed platform**. Central services maintain a consistent risk, policy, and evidence model while adapters and segregated collectors respect source authority and disconnected environments.

## Key tradeoffs

- Greater integration complexity is accepted to preserve isolation and source ownership.
- Evidence is referenced when possible and copied only when policy, resilience, or review needs justify it.
- Near-real-time monitoring is used for enterprise sources; isolated domains provide risk-tiered periodic updates.
- Automation reduces review effort but cannot accept residual risk or waive evidence gaps.

## Revisit triggers

Reopen the trade when classification constraints change, a common service loses authorization, evidence volume exceeds sizing assumptions, disconnected duration exceeds 72 hours, or a new mission thread requires low-latency assurance data.
