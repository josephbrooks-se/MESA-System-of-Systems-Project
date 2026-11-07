# MESA Ecosystem Block Definition Diagram

## Purpose

This SysML-inspired Block Definition Diagram defines the three constituent systems, their principal parts, and their system-of-systems relationships. Mermaid class notation is used because GitHub renders it natively.

```mermaid
classDiagram
  direction TB

  class MESA_Ecosystem {
    <<system of systems>>
    +missionOutcomeId
    +architectureBaselineId
    +ecosystemVersion
    +coordinateArchitecture()
    +coordinateMigration()
    +coordinateAssurance()
    +governDecisions()
  }

  class MESA_SoS_Architecture {
    <<constituent system>>
    +MissionArchitectureService
    +OperationalThreadService
    +RequirementsService
    +LogicalArchitectureService
    +InterfaceRegistry
    +TraceabilityService
    +RoadmapService
    +ArchitectureDecisionService
  }

  class MESA_Cyber_Assurance_Platform {
    <<constituent system>>
    +ThreatRiskService
    +ControlAllocationService
    +InheritanceService
    +EvidenceCatalog
    +AuthorizationWorkflow
    +POAMService
    +ContinuousMonitoring
  }

  class MESA_Cloud_Migration_Factory {
    <<constituent system>>
    +PortfolioDiscoveryService
    +AssessmentService
    +LandingZonePlatform
    +MigrationWaveService
    +DataMigrationService
    +CutoverRollbackService
    +LegacyExitService
    +FinOpsService
  }

  class Shared_Identity_Policy {
    <<shared service>>
    +FederatedIdentity
    +WorkloadIdentity
    +PolicyDecision
    +PolicyEnforcement
  }

  class Shared_Integration_Evidence {
    <<shared service>>
    +APIContractRegistry
    +EventBroker
    +SchemaRegistry
    +EvidenceProvenance
    +ProtectedAudit
  }

  MESA_Ecosystem *-- MESA_SoS_Architecture : mission architecture
  MESA_Ecosystem *-- MESA_Cyber_Assurance_Platform : cyber assurance
  MESA_Ecosystem *-- MESA_Cloud_Migration_Factory : cloud transformation
  MESA_Ecosystem *-- Shared_Identity_Policy : common trust plane
  MESA_Ecosystem *-- Shared_Integration_Evidence : common integration plane

  MESA_SoS_Architecture --> MESA_Cyber_Assurance_Platform : ArchitectureBaseline Requirements InterfaceChanges
  MESA_Cyber_Assurance_Platform --> MESA_SoS_Architecture : Findings EvidenceStatus ResidualRisk AuthorizationDependencies
  MESA_SoS_Architecture --> MESA_Cloud_Migration_Factory : TargetArchitecture Allocations Contracts Roadmap
  MESA_Cloud_Migration_Factory --> MESA_SoS_Architecture : Inventory Dependencies MigrationState Configuration LegacyExit
  MESA_Cloud_Migration_Factory --> MESA_Cyber_Assurance_Platform : Assets Configuration TestEvidence MonitoringEvents
  MESA_Cyber_Assurance_Platform --> MESA_Cloud_Migration_Factory : ControlRequirements ReadinessGates Exceptions Decisions

  Shared_Identity_Policy ..> MESA_SoS_Architecture : protects
  Shared_Identity_Policy ..> MESA_Cyber_Assurance_Platform : protects
  Shared_Identity_Policy ..> MESA_Cloud_Migration_Factory : protects
  Shared_Integration_Evidence ..> MESA_SoS_Architecture : connects and audits
  Shared_Integration_Evidence ..> MESA_Cyber_Assurance_Platform : connects and audits
  Shared_Integration_Evidence ..> MESA_Cloud_Migration_Factory : connects and audits
```

## Block responsibilities

| Block | Owns authoritative state for | Does not own |
|---|---|---|
| MESA SoS Architecture | Mission outcomes, operational threads, requirements, functions, logical systems, architecture interfaces, baselines, ADRs | Control assessment, cloud execution, cutover authority |
| MESA Cyber Assurance Platform | Threat/risk analysis, control allocation/inheritance, evidence sufficiency, findings, authorization workflow, continuous-monitoring posture | Mission baseline approval, workload migration execution |
| MESA Cloud Migration Factory | Workload inventory, 7R assessment, landing-zone delivery, migration waves, cutover execution, legacy exit, FinOps | Mission requirement authority, residual-risk acceptance |
| Shared Identity/Policy | Federated subject/workload identities and policy decisions | Business/mission approval |
| Shared Integration/Evidence | Contract/schema registry, event transport, provenance, protected audit | Source-system business truth |

## Required interfaces

| Interface | Producer | Consumer | Pattern |
|---|---|---|---|
| Architecture Baseline API/Event | SoS Architecture | Cyber Assurance, Cloud Migration | REST + signed event |
| Workload/Dependency API/Event | Cloud Migration | SoS Architecture, Cyber Assurance | REST + signed event |
| Control and Readiness API/Event | Cyber Assurance | Cloud Migration, SoS Architecture | REST + signed event |
| Evidence API/Event | All systems | Cyber Assurance catalog; authorized reviewers | REST + signed event/reference |
| Decision API/Event | Named authorities through owning system | All affected systems | Human-approved REST command + event |
| Trace Query | SoS Architecture | All systems | REST query |

## Emergent capability

No constituent system alone can provide the full outcome. The ecosystem’s emergent capability is an evidence-driven path from mission need through architecture, secure cloud transformation, verification, residual-risk decision, and lifecycle monitoring.
