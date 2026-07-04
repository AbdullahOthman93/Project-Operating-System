# Dependency Model

## Purpose

Defines how the layers established in [LayerModel.md](LayerModel.md) may depend on and reference one another. This is the **only** place dependency rules are defined.

## Scope

Dependency direction and reference rules only. Layer definitions belong in [LayerModel.md](LayerModel.md); what happens when a dependency rule is violated is governed by [GovernanceModel.md](GovernanceModel.md).

## Dependency rules

1. **One direction only.** A document may depend only on documents of equal or higher authority (as classed in [LayerModel.md](LayerModel.md)). Nothing authoritative ever depends on supporting content.
2. **Governance depends on nothing.** The Governance layer is the root of the dependency order; it references nothing else in the repository as an authority.
3. **Reference, never restate.** A dependency is expressed as a reference to the owning document, applying Single Source of Truth ([DesignPrinciples.md](DesignPrinciples.md), P2). Restating a rule creates a duplicate and is a defect.
4. **No cycles.** Dependency relationships must form a directed acyclic structure. Mutual "see also" navigation links are permitted; mutual *authority* is not.
5. **Supporting content may reference anything; nothing depends on it.** Guidance, procedures, templates, and examples may cite any authoritative document, but no document may cite them as an authority.
6. **Execution depends only on Contracts.** Execution artifacts conform to Contracts and, through them, to everything above. They are never a reference target for documentation.

## Allowed dependencies by layer

| Layer | May depend on |
|---|---|
| Governance | — (root) |
| Process | Governance |
| State & Tracking | Governance, Process |
| Knowledge — standards | Governance, Process |
| Knowledge — project records | Governance, State & Tracking, standards |
| Contracts | Governance, standards |
| Execution | Contracts |
| Supporting (all) | any authoritative layer, as reference only |

## Responsibilities

- Define the binding direction of every cross-document relationship in the system.
- Provide the table against which any new document's declared dependencies are validated.

## Relationship to other governance documents

- Operates on the layers and authority classes defined in [LayerModel.md](LayerModel.md).
- Applies [DesignPrinciples.md](DesignPrinciples.md) P2 (Single Source of Truth) and P5 (Explicit Authority) as structural rules.
- Violations are surfaced and resolved through [GovernanceModel.md](GovernanceModel.md).
