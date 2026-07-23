# AI Context Standard

**Document ID:** STD-009  
**Title:** Enterprise AI Context Standard  
**Version:** 1.0.0  
**Status:** Approved (Baseline)  
**Layer:** Foundation  
**Owner:** Chief Enterprise Architect  
**Dependencies:** STD-001, STD-003, STD-004, STD-007, STD-008  

---

# Executive Summary

This standard defines how contextual information is organized, maintained, and consumed by AI-assisted development tools within the AI Compliance Studio Enterprise (ACSE) repository.

Unlike traditional documentation, AI coding assistants require structured, concise, and authoritative context to generate consistent designs, documentation, code, tests, diagrams, and security controls. This standard establishes a single source of truth for repository context and ensures AI-generated outputs align with project architecture, governance, and engineering principles.

---

# Objectives

This standard aims to:

* Improve the accuracy of AI-generated outputs.
* Reduce hallucinations caused by missing or conflicting context.
* Ensure consistent terminology across contributors and AI tools.
* Provide reusable project knowledge for documentation and implementation.
* Enable secure and governed use of AI throughout the software development lifecycle.

---

# Guiding Principles

AI context shall be:

* Accurate
* Current
* Version-controlled
* Authoritative
* Minimal but sufficient
* Traceable to repository sources

Context files are supporting artifacts and shall never replace the primary engineering documentation.

---

# AI Context Hierarchy

Context is consumed in layers, from broad organizational guidance to implementation details.

| Layer                  | Purpose                                        |
| ---------------------- | ---------------------------------------------- |
| Repository Context     | Vision, scope, standards, terminology          |
| Domain Context         | Business capabilities and bounded contexts     |
| Architecture Context   | Components, integrations, trust boundaries     |
| Security Context       | Controls, identities, threats, guardrails      |
| Compliance Context     | Regulations, policies, evidence requirements   |
| Implementation Context | APIs, data models, workflows, coding standards |

Higher-level context takes precedence when conflicts arise.

---

# Repository Context Files

The `.ai/` directory contains AI-specific guidance.

Recommended files include:

| File          | Purpose                                 |
| ------------- | --------------------------------------- |
| `copilot.md`  | Guidance for GitHub Copilot             |
| `cursor.md`   | Guidance for Cursor                     |
| `claude.md`   | Guidance for Claude Code                |
| `codex.md`    | Guidance for Codex                      |
| `windsurf.md` | Guidance for Windsurf                   |
| `lovable.md`  | Guidance for compatible AI design tools |

These files should reference authoritative repository documents rather than duplicate their content.

---

# Context Design Principles

Effective AI context should:

* State facts, not assumptions.
* Prefer stable architectural decisions over implementation details.
* Reference standards and ADRs.
* Define project terminology explicitly.
* Avoid contradictory guidance.
* Be concise enough for efficient retrieval.

---

# Required Repository Context

Every AI context package should communicate:

* Product vision
* Repository structure
* Architectural principles
* Technology stack
* Security requirements
* Compliance objectives
* Naming conventions
* Documentation standards
* Coding standards (when available)

This information enables AI tools to produce outputs aligned with repository expectations.

---

# Context Referencing

AI context shall reference authoritative documents using document identifiers.

Example:

```text id="b41frp"
STD-001 Documentation Standards
ARC-001 Enterprise Architecture
SEC-001 Security Architecture
ADR-003 Policy-as-Code
```

Avoid copying large sections of content into context files.

---

# Context Granularity

Keep context focused.

Recommended approach:

* Repository-level guidance for global principles.
* Domain-level guidance for business capabilities.
* Feature-level guidance for implementation details.

Smaller, targeted context improves retrieval quality and reduces conflicting instructions.

---

# Security Requirements

AI context shall never include:

* Secrets
* Passwords
* API keys
* Certificates
* Access tokens
* Personally identifiable information
* Production credentials
* Confidential customer data

Sensitive information must remain outside the repository and be managed through approved secret-management solutions.

---

# Compliance Considerations

AI context should identify applicable governance requirements, including:

* AI risk classification
* Data handling expectations
* Audit evidence obligations
* Privacy considerations
* Regulatory references

This allows AI-generated outputs to incorporate governance requirements from the outset.

---

# Context Maintenance

Context shall be reviewed whenever there are changes to:

* Repository standards
* Architecture
* Security controls
* Compliance requirements
* Technology stack
* Terminology
* Major ADRs

Outdated context reduces the reliability of AI-assisted development.

---

# AI Output Validation

AI-generated artifacts should be reviewed for:

* Architectural consistency
* Security alignment
* Compliance coverage
* Terminology consistency
* Traceability to repository standards
* Technical correctness

Human review remains mandatory before implementation or publication.

---

# Governance

The Chief Enterprise Architect is accountable for:

* Repository-level AI context.
* Alignment with architectural standards.
* Consistency across AI context files.

Domain owners are responsible for maintaining context specific to their areas.

---

# Review Checklist

Before approving AI context updates, verify:

* References point to current standards.
* Terminology matches the repository glossary.
* No confidential information is included.
* Context remains concise and relevant.
* Superseded architectural decisions have been removed or clearly identified.
* Security and compliance guidance reflects current policy.

---

# Success Criteria

This standard is successful when:

* AI-generated outputs are consistent with repository standards.
* Contributors spend less time correcting AI-generated artifacts.
* Architectural terminology remains consistent.
* Security and compliance requirements are reflected in AI-assisted work.
* Context remains maintainable as the repository evolves.

---

# Revision History

| Version | Date      | Description                             |
| ------- | --------- | --------------------------------------- |
| 1.0.0   | July 2026 | Initial enterprise AI context standard. |
