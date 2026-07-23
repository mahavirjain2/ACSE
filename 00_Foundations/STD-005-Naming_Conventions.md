# Naming Conventions

**Document ID:** STD-005  
**Title:** Enterprise Naming Conventions Standard  
**Version:** 1.0.0  
**Status:** Approved (Baseline)  
**Layer:** Foundation  
**Owner:** Chief Enterprise Architect  
**Dependencies:** STD-001, STD-002, STD-003, STD-004  

---

# Executive Summary

This standard establishes the naming conventions for all artifacts within the AI Compliance Studio Enterprise (ACSE) repository and platform.

Consistent naming improves readability, discoverability, traceability, automation, and governance. These conventions apply to documentation, source code, APIs, databases, cloud resources, AI assets, infrastructure, and operational artifacts.

---

# Objectives

This standard aims to:

* Establish a common naming language across the platform.
* Eliminate ambiguity.
* Improve searchability and discoverability.
* Support automation and Infrastructure as Code (IaC).
* Ensure consistency across engineering teams.
* Simplify onboarding for contributors.

---

# General Principles

Names shall be:

* Descriptive
* Concise
* Consistent
* Stable
* Human-readable
* Machine-friendly

Avoid:

* Personal names
* Project nicknames
* Environment-specific terms where unnecessary
* Temporary identifiers
* Ambiguous abbreviations

---

# Document Naming

Document names shall use **Pascal Case** with underscores.

**Examples**

```text id="o3y5e8"
Product_Vision.md
Enterprise_Architecture.md
Threat_Model.md
Risk_Register.md
API_Design_Standards.md
```

Do not include:

* Version numbers
* Dates
* Draft indicators

These belong in document metadata and Git history.

---

# Folder Naming

Folders shall use the predefined repository structure.

Examples:

```text id="pc2jmu"
03_Architecture
09_Security
11_DevOps
17_Templates
```

Do not create ad hoc top-level folders.

---

# Document Identifiers

Every major specification shall have a unique identifier.

Examples:

```text id="7z3w1b"
STD-001
PRD-001
BUS-001
ARC-001
DAT-001
API-001
UIX-001
AI-001
SEC-001
CMP-001
OPS-001
ADR-001
```

Identifiers are immutable and must never be reused.

---

# Business Capability Naming

Business capabilities should use noun-based names.

Examples:

* AI Inventory
* Risk Management
* Policy Management
* Assessment Management
* Evidence Collection
* Audit Management
* Model Registry

Avoid action-oriented names such as "Manage Inventory."

---

# Service Naming

Microservices shall use clear business-aligned names.

Examples:

* Inventory Service
* Risk Service
* Policy Service
* Evidence Service
* Notification Service
* Identity Service

Avoid technology-specific names such as:

* BackendService1
* AIApp
* MicroserviceX

---

# API Naming

REST APIs should follow resource-oriented conventions.

Examples:

```text id="qumjlwm"
/api/v1/models
/api/v1/policies
/api/v1/assessments
/api/v1/evidence
/api/v1/users
```

Guidelines:

* Use plural nouns.
* Use lowercase.
* Separate words with hyphens where necessary.
* Avoid verbs in resource paths.

---

# Database Naming

## Tables

Use singular Pascal Case.

Examples:

```text id="hmp8f0"
Model
Risk
Assessment
Evidence
Policy
Control
```

## Columns

Use Pascal Case.

Examples:

```text id="cwy6vh"
ModelId
CreatedDate
OwnerId
Status
RiskLevel
```

## Primary Keys

```text id="avjlwm"
ModelId
RiskId
PolicyId
```

## Foreign Keys

Reference the parent entity.

Examples:

```text id="lpb5bn"
ModelId
OwnerId
PolicyId
```

---

# Event Naming

Events should represent completed business actions.

Examples:

* ModelRegistered
* RiskAssessed
* PolicyApproved
* AssessmentCompleted
* EvidenceSubmitted
* ReviewCompleted

Avoid command-style names.

---

# AI Asset Naming

AI assets should follow a consistent hierarchy.

Examples:

```text id="k0w2xa"
Prompt
Agent
Model
KnowledgeBase
Evaluation
Guardrail
Workflow
```

Examples:

* VendorRiskAgent
* ComplianceCopilot
* PolicyReviewPrompt
* RiskAssessmentWorkflow

---

# Cloud Resource Naming

Recommended pattern:

```text id="x1t0jc"
<application>-<service>-<environment>-<region>
```

Example:

```text id="3l56ys"
acse-api-prod-eastus
acse-db-prod-eastus
acse-storage-dev-eastus
```

Environment values:

* dev
* test
* stage
* prod

---

# Infrastructure as Code

Infrastructure modules should reflect business purpose.

Examples:

* network
* identity
* database
* monitoring
* storage
* ai-platform

Avoid generic names such as:

* module1
* infrastructure2

---

# Security Artifact Naming

Examples:

* Threat_Model_ACSE.md
* Zero_Trust_Architecture.md
* Security_Control_Catalog.md
* Identity_Architecture.md

Security artifacts should clearly communicate their purpose.

---

# Architecture Decision Records

Naming convention:

```text id="5jlwmq"
ADR-001
ADR-002
ADR-003
```

File names:

```text id="n1ifec"
ADR-001_Microservices_Architecture.md
ADR-002_PostgreSQL_Selection.md
ADR-003_Policy_As_Code.md
```

---

# Diagram Naming

Diagram filenames should describe the view.

Examples:

* System_Context.svg
* Domain_Model.svg
* Deployment_Diagram.svg
* AI_Workflow.svg
* Risk_Assessment_Process.svg

---

# Branch Naming

Recommended Git branch format:

```text id="5r2vdn"
feature/ai-inventory
feature/risk-engine
bugfix/api-validation
hotfix/security-patch
docs/std-005
```

---

# Naming Anti-Patterns

Avoid:

* Temp
* Final
* New
* Latest
* Test1
* Sample2
* Demo
* Copy
* V2
* MyService

Names should remain meaningful throughout the lifecycle of the project.

---

# Success Criteria

This standard is successful when:

* Artifacts are easily identifiable.
* Naming is consistent across the repository.
* Automation scripts can rely on predictable patterns.
* Teams use a shared vocabulary.
* The repository remains understandable as it scales.

---

# Revision History

| Version | Date      | Description                                    |
| ------- | --------- | ---------------------------------------------- |
| 1.0.0   | July 2026 | Initial enterprise naming convention standard. |
