# Mermaid Diagram Guide

**Document ID:** STD-008  
**Title:** Enterprise Mermaid Diagram Standard  
**Version:** 1.0.0  
**Status:** Approved (Baseline)  
**Layer:** Foundation  
**Owner:** Chief Enterprise Architect  
**Dependencies:** STD-001, STD-003, STD-004, STD-007  

---

# Executive Summary

This standard defines how diagrams are authored, reviewed, versioned, and maintained within the AI Compliance Studio Enterprise (ACSE) repository.

Mermaid is the primary diagram language because it is text-based, version-controlled, human-readable, and integrates seamlessly with Markdown and Git. Diagrams shall evolve alongside documentation and remain synchronized with architectural decisions and implementation changes.

---

# Objectives

This standard aims to:

* Standardize architectural visualization.
* Keep diagrams under version control.
* Improve collaboration through text-based diagrams.
* Ensure consistency across repository documentation.
* Support AI-assisted understanding of system architecture.

---

# Guiding Principles

Every diagram shall be:

* Source-controlled
* Human-readable
* Machine-readable
* Maintainable
* Consistent with related documentation
* Easy to modify through pull requests

A diagram is part of the specification, not an external attachment.

---

# Supported Diagram Types

The repository standardizes the following Mermaid diagram types.

| Diagram Type                | Primary Use                         |
| --------------------------- | ----------------------------------- |
| Flowchart                   | Process flows and workflows         |
| Sequence Diagram            | Service interactions                |
| Class Diagram               | Domain models                       |
| Entity Relationship Diagram | Data models                         |
| State Diagram               | Lifecycle modeling                  |
| Journey Diagram             | User journeys                       |
| Gantt Chart                 | Project planning                    |
| Git Graph                   | Branching and release visualization |
| Mind Map                    | Capability decomposition            |

Additional Mermaid diagram types may be adopted through an ADR.

---

# Diagram Selection Guidelines

Choose the simplest diagram that communicates the required information.

| Scenario            | Recommended Diagram         |
| ------------------- | --------------------------- |
| Business process    | Flowchart                   |
| API interaction     | Sequence Diagram            |
| Domain entities     | Class Diagram or ER Diagram |
| AI workflow         | Flowchart                   |
| Deployment topology | Flowchart                   |
| State transitions   | State Diagram               |
| User interaction    | Journey Diagram             |
| Release planning    | Gantt Chart                 |

Avoid using multiple diagram types when a single diagram communicates the concept effectively.

---

# Standard Diagram Header

Every diagram should include:

* Title
* Purpose
* Related document
* Version (when appropriate)

Example:

```markdown
### AI Risk Assessment Workflow

Purpose: Illustrates the end-to-end assessment lifecycle.

Related Document:
ARC-004 AI Risk Engine
```

---

# Flowchart Standards

Flowcharts should:

* Progress from left-to-right (`LR`) unless vertical flow is more intuitive.
* Represent decisions using diamond nodes.
* Use meaningful node labels.
* Minimize crossing lines.
* Group related activities using subgraphs where appropriate.

Example:

```
Start
  ↓
Validate Input
  ↓
Perform Risk Assessment
  ↓
Store Results
  ↓
End
```

---

# Sequence Diagram Standards

Sequence diagrams should identify:

* Actors
* Services
* External systems
* Databases
* AI components

Interactions should follow chronological order from top to bottom.

Clearly distinguish synchronous and asynchronous communications where applicable.

---

# Architecture Diagrams

Architecture diagrams should illustrate:

* System boundaries
* Trust boundaries
* Major components
* External integrations
* Data flows
* Control flows

Each architecture diagram should answer a specific architectural question rather than attempting to show the entire platform.

---

# Security Visualization

Security-relevant diagrams shall explicitly identify:

* Trust boundaries
* Identity providers
* Authentication flows
* Authorization decisions
* Encryption points
* Secrets management
* Administrative boundaries
* External dependencies

Security diagrams should support threat modeling and design reviews.

---

# AI Workflow Diagrams

AI-specific diagrams should include:

* User
* Orchestrator
* Agents
* Models
* Prompt templates
* Guardrails
* Knowledge retrieval
* Evaluation components
* Logging and monitoring
* Human review steps (where applicable)

The workflow should clearly distinguish deterministic processes from AI-driven decision points.

---

# Data Flow Visualization

Data flow diagrams should indicate:

* Data origin
* Data transformations
* Persistent storage
* External interfaces
* Sensitive data handling
* Data classification (where relevant)

Data movement across trust boundaries should be explicit.

---

# Diagram Complexity Guidelines

A single diagram should generally contain:

* No more than 20–25 primary nodes.
* Minimal line crossings.
* Logical grouping of related elements.
* Clear labels without excessive text.

If additional detail is required, decompose the design into multiple focused diagrams.

---

# Styling Guidelines

Maintain a consistent visual style across diagrams.

Recommendations:

* Use descriptive node labels.
* Avoid abbreviations unless universally understood.
* Keep label text concise.
* Align related nodes consistently.
* Use subgraphs to represent logical domains.
* Avoid excessive styling that obscures the structure.

Visual consistency is more important than decorative formatting.

---

# Versioning

Diagrams are version-controlled as part of their parent document.

When a design changes:

* Update the Mermaid source.
* Review associated ADRs.
* Confirm alignment with the architecture description.
* Update revision history where appropriate.

Diagrams shall never diverge from the documented implementation.

---

# Review Checklist

Before approving a diagram, verify:

* The correct diagram type is used.
* Labels are meaningful.
* Trust boundaries are identified where applicable.
* Components align with the accompanying text.
* No obsolete components remain.
* Diagram complexity remains manageable.
* Relationships are unambiguous.

---

# Success Criteria

This standard is successful when:

* Diagrams are understandable without verbal explanation.
* Architectural intent is communicated clearly.
* Diagrams remain synchronized with documentation.
* Security and trust boundaries are consistently represented.
* Contributors can modify diagrams using standard Markdown tooling.

---

# Revision History

| Version | Date      | Description                                  |
| ------- | --------- | -------------------------------------------- |
| 1.0.0   | July 2026 | Initial enterprise Mermaid diagram standard. |
