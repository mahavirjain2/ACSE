# Markdown Style Guide

**Document ID:** STD-003
**Title:** Markdown Style Guide
**Version:** 1.0.0
**Status:** Approved (Baseline)
**Layer:** Foundation
**Owner:** Chief Enterprise Architect
**Dependencies:** STD-001 Documentation Standards, STD-002 Repository Structure

---

# Executive Summary

This document defines the Markdown authoring standards for the AI Compliance Studio Enterprise (ACSE) repository. The objective is to ensure that every document is consistent in structure, formatting, readability, maintainability, and AI interpretation.

These standards apply to all repository content, regardless of document type.

---

# Objectives

The Markdown standard aims to:

* Establish a consistent authoring experience.
* Improve readability for technical and business audiences.
* Support documentation website generation.
* Optimize documents for AI-assisted development.
* Minimize formatting inconsistencies across contributors.

---

# Guiding Principles

Every document shall be:

* Clear
* Consistent
* Structured
* Searchable
* Version controlled
* AI-friendly
* Human-readable

Formatting should improve understanding—not become a distraction.

---

# File Naming Standard

Use **Pascal Case** with underscores.

**Examples**

```text
Product_Vision.md
Enterprise_Architecture.md
Threat_Model.md
API_Design_Standards.md
```

Avoid:

* Spaces
* Special characters
* Version numbers in filenames
* Dates in filenames

Version history belongs inside the document and in Git.

---

# Heading Hierarchy

Use headings consistently.

```markdown
# Document Title

## Primary Section

### Subsection

#### Detail

##### Rarely Used

###### Avoid Unless Necessary
```

Rules:

* Only one H1 (`#`) per document.
* Do not skip heading levels.
* Keep headings concise and descriptive.
* Prefer noun-based headings over sentence-style headings.

---

# Paragraph Guidelines

Documents should be easy to scan.

Rules:

* One idea per paragraph.
* Avoid paragraphs longer than 8–10 lines.
* Use transition sentences between major sections.
* Define technical terminology before using abbreviations.

---

# Lists

Use unordered lists for collections.

```markdown
- Item
- Item
- Item
```

Use numbered lists only for:

* Sequential workflows
* Procedures
* Algorithms
* Checklists requiring ordered execution

---

# Tables

Use tables when comparing structured information.

Example:

| Capability    | Owner      | Status   |
| ------------- | ---------- | -------- |
| AI Inventory  | Platform   | Planned  |
| Risk Register | Governance | Approved |

Avoid tables for long narrative content.

---

# Code Blocks

Always specify the language.

````markdown
```yaml
version: 1.0
```

```json
{
  "name": "ACSE"
}
```

```sql
SELECT *
FROM AI_MODEL;
```
````

Supported languages include:

* yaml
* json
* sql
* xml
* bash
* powershell
* python
* csharp
* javascript
* typescript
* mermaid

---

# Callouts

Use callouts sparingly.

Recommended types:

> **Note** – Additional context.

> **Important** – Information that affects implementation.

> **Warning** – Potential security or operational risk.

> **Decision** – References an Architecture Decision Record (ADR).

---

# Images

Store images under:

```text
18_Assets/images/
```

Rules:

* Use SVG where possible.
* Prefer diagrams over screenshots.
* Every image must have:

  * Title
  * Caption
  * Source
  * Related document reference

---

# Mermaid Diagrams

Mermaid is the default diagram language.

Supported diagrams include:

* Flowcharts
* Sequence diagrams
* State diagrams
* Entity relationship diagrams
* Class diagrams
* Gantt charts
* Journey maps

Diagrams should be:

* Readable
* Left-to-right where practical
* Modular
* Version controlled with the document

---

# Hyperlinks

Internal references should use relative paths.

Example:

```markdown
See:
../09_Security/Security_Architecture.md
```

Avoid hardcoded absolute URLs for internal content.

---

# Terminology

Use terminology consistently.

Preferred examples:

| Preferred   | Avoid                                        |
| ----------- | -------------------------------------------- |
| AI System   | AI Application                               |
| Control     | Safeguard                                    |
| Requirement | Need                                         |
| Capability  | Feature (when describing business functions) |
| Service     | Module (unless referring to code modules)    |

The glossary in the Reference layer is the authoritative source for terminology.

---

# Writing Style

Write in an authoritative engineering style.

Use:

* "shall" for mandatory requirements.
* "should" for recommendations.
* "may" for optional behavior.

Example:

> The platform **shall** maintain an immutable audit trail for all governance decisions.

Avoid vague language such as:

* maybe
* probably
* generally
* might
* could be considered

---

# Cross-Referencing

Every major document should include references to:

* Related standards
* Architecture documents
* Security specifications
* Compliance mappings
* Relevant ADRs

Cross-references improve traceability and reduce duplication.

---

# Markdown Checklist

Before committing a document, verify:

* One H1 heading only.
* Metadata present.
* Heading hierarchy is correct.
* Code blocks specify a language.
* Tables render correctly.
* Internal links are valid.
* Terminology is consistent.
* Revision history is updated.

---

# Success Criteria

The Markdown standard is successful when:

* Documents are visually consistent.
* Contributors follow a common authoring style.
* Documentation renders correctly across supported platforms.
* AI coding assistants can reliably interpret document structure.
* Readers can quickly locate and understand information.

---

# Revision History

| Version | Date      | Description                          |
| ------- | --------- | ------------------------------------ |
| 1.0.0   | July 2026 | Initial Markdown authoring standard. |
