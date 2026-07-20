# Standards Model

## Purpose

Defines what a standard is, how standards bind, and which standards exist. This is the **only** place the structure of the standards layer is defined.

## Scope

Standards organization only. The gates at which standards are enforced are defined in [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md) and exercised at the stages of [../kernel/SprintLifecycle.md](../kernel/SprintLifecycle.md); standards define the **quality bar** applied there, never the gates or the procedure themselves.

## What a standard is

A **standard** is a reusable, checkable quality requirement:

- **Reusable** — it applies across all work of its kind, in any project adopting the system; anything project-specific is confined to a marked binding note (Reusability, [../architecture/DesignPrinciples.md](../architecture/DesignPrinciples.md), P10).
- **Checkable** — conformance can be determined by inspection; a requirement that cannot be checked is guidance, and guidance belongs in supporting layers, not here.
- **Binding by reference** — gates and, once defined, contracts cite standards as requirements. A standard never restates the governance rule or schema it serves (Single Source of Truth, P2); it states what conformance to check.

## Standards catalog

| Document | Quality bar owned |
|---|---|
| [DocumentationStandard.md](DocumentationStandard.md) | Structure, naming, and conventions of authoritative documents |
| [ValidationStandard.md](ValidationStandard.md) | The canonical Validation-gate checklist |
| [VersionControlStandard.md](VersionControlStandard.md) | Change-set discipline, completion publication, and history integrity |
| [WorkEconomyStandard.md](WorkEconomyStandard.md) | The economy-of-effort quality bar — reading footprint, re-derivation, review and verification breadth, and report length |

## Deferred categories

Testing and security standards are **deliberately absent**: the repository contains no executable content, and authoring them ahead of need would violate Create on Need ([../architecture/DesignPrinciples.md](../architecture/DesignPrinciples.md), P9). This deferral was owner-ratified with the Sprint 1.5 design. They enter this catalog, through the sprint lifecycle, with the first sprint that introduces executable artifacts.

## Adding standards

A new standard enters only on demonstrated need, as an approved sprint deliverable or owner-approved amendment ([../kernel/ChangeAndConflictWorkflow.md](../kernel/ChangeAndConflictWorkflow.md)), and is added to the catalog above.

## Responsibilities

- Define what qualifies as a standard and maintain the single catalog of standards.
- Keep visible which standard categories are deferred and why.

## Relationship to other documents

- Standards enforce what the gates of [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md) require; they are applied at the validation stage of [../kernel/SprintLifecycle.md](../kernel/SprintLifecycle.md).
- Per [../architecture/DependencyModel.md](../architecture/DependencyModel.md), the Contracts layer and project records depend on this layer; nothing here depends on them.
