# Architecture Overview

## Purpose

The orientation document and entry point for Architecture v1.0. It summarizes how the Project Operating System is structured, maps the logical architecture to the physical repository, and directs readers to the authoritative document for each concern. It defines no rules of its own.

## Scope

Summary and navigation only. Every rule referred to here is owned by another governance document; if this overview ever appears to conflict with one of them, the owning document prevails.

## Architecture summary

The Project Operating System is organized as a set of **layers** with strictly ordered authority. Governance sits at the top and depends on nothing; every other layer operates within the rules of the layers above it. Authoritative content is separated from supporting content, and all cross-document relationships follow one dependency direction.

- The layers, their responsibilities, and their authority classes are defined in [LayerModel.md](LayerModel.md).
- The allowed dependency and reference relationships between them are defined in [DependencyModel.md](DependencyModel.md).
- Decision rights, approval gates, and change control are defined in [GovernanceModel.md](GovernanceModel.md).
- The concept of a governed project — the Project Governance Relationship and how a project is brought under governance — is defined in [ProjectGovernanceRelationship.md](ProjectGovernanceRelationship.md).
- The rules of judgement behind all of this are defined in [DesignPrinciples.md](DesignPrinciples.md).
- The canonical vocabulary is defined in [Terminology.md](Terminology.md).
- Direction and purpose are defined in [Vision.md](Vision.md) and [Mission.md](Mission.md).

## Logical-to-physical mapping

| Logical layer (see [LayerModel.md](LayerModel.md)) | Physical location |
|---|---|
| Governance | `docs/architecture/` |
| Process | `docs/kernel/` |
| State & Tracking | `docs/runtime/` |
| Knowledge — reusable standards | `docs/standards/` |
| Knowledge — project records | `docs/knowledge/` |
| Contracts | `docs/contracts/` |
| Execution | `tools/`, `.claude/`, `CLAUDE.md`, `.github/` |
| Supporting — agent guidance | `docs/agents/` |
| Supporting — operating procedures | `docs/operations/` |
| Supporting — templates | `docs/templates/` |
| Supporting — examples | `docs/examples/` |

Each `docs/` directory carries an `INDEX.md` describing its own purpose, scope, contents, and dependencies. Those index files describe individual directories; this table is the single overall map.

## Reading order

1. [Vision.md](Vision.md) and [Mission.md](Mission.md) — why the system exists and what it delivers.
2. [DesignPrinciples.md](DesignPrinciples.md) — the rules of judgement.
3. [LayerModel.md](LayerModel.md) and [DependencyModel.md](DependencyModel.md) — the structure.
4. [GovernanceModel.md](GovernanceModel.md) — how decisions and changes are made.
5. [ProjectGovernanceRelationship.md](ProjectGovernanceRelationship.md) — what it means for a project to be governed.
6. [Terminology.md](Terminology.md) — consult as needed throughout.

## Responsibilities

- Orient any reader — human or AI agent — entering the architecture.
- Own the single overall mapping between logical layers and physical repository locations.

## Relationship to other governance documents

This document references all other governance documents and is referenced by them only as an entry point. It holds no authority they do not already hold.
