# Authoritative Document Template

> **Non-authoritative scaffolding.** This template defines no rule and owns no concept. It reproduces, as a fill-in skeleton, the document structure required by [../standards/DocumentationStandard.md](../standards/DocumentationStandard.md). Every bracketed `<...>` value is **illustrative** and must be replaced. If this template ever diverges from the Documentation Standard, the Standard governs.

**Use for:** a new authoritative document in the Governance, Process, State & Tracking, Knowledge (standards), or Contracts layers.

**Structure owned by:** [../standards/DocumentationStandard.md](../standards/DocumentationStandard.md) (§ Document structure, § Conventions). **Conformance is checked** at the Validation gate via [../standards/ValidationStandard.md](../standards/ValidationStandard.md).

Copy the skeleton below into the new document's location (all `docs/` subdirectories are one level under `docs/`, so `../<dir>/<file>` links resolve unchanged) and replace every bracketed value:

```md
# <DocumentTitle — PascalCase concept name>

## Purpose

<What this document defines. If it owns a concept, include the single-home declaration here (e.g., "this is the only place X is defined").>

## Scope

<What is in scope and what is out; name where each out-of-scope concern lives.>

## <Owned content — replace with one or more sections>

<The section(s) defining what this document owns: rules, stages, schema, terms, or catalog. For anything defined elsewhere, link the owning document rather than restating it.>

## Responsibilities

<What this document alone answers for.>

## Relationship to other documents

<How this document relates to the documents it references, as resolvable links.>
```
