# Process Model

## Purpose

Defines how the Process layer is organized: what a workflow is, what the layer contains, and how its documents relate to the Governance layer above and the layers below. This is the **only** place the structure of the Process layer is defined.

## Scope

Process organization only. The rules that workflows operationalize — decision rights, approval gates, principles — are defined in the Governance layer and are referenced here, never restated ([../architecture/DesignPrinciples.md](../architecture/DesignPrinciples.md), P2). Process adds **procedure**: the ordered steps by which work demonstrably satisfies those rules. Process never defines which tool executes a step; that belongs to the Contracts and Execution layers ([../architecture/LayerModel.md](../architecture/LayerModel.md)).

## What a workflow is

A **workflow** is an ordered, repeatable procedure with:

- a defined **trigger** — the condition under which the workflow starts;
- defined **participant responsibilities** — who does what, within the decision rights of [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md);
- defined **exit conditions** — expressed against the approval gates defined in [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md), never as gates of the workflow's own invention.

A workflow may not weaken, extend, or reinterpret a governance rule. Where a workflow and a governance document appear to conflict, the conflict is handled per [ChangeAndConflictWorkflow.md](ChangeAndConflictWorkflow.md).

## Process catalog

| Document | Procedure owned |
|---|---|
| [SprintLifecycle.md](SprintLifecycle.md) | The lifecycle of a sprint, from definition through promotion |
| [PhaseModel.md](PhaseModel.md) | How phases are composed of sprints, and phase entry/exit |
| [ChangeAndConflictWorkflow.md](ChangeAndConflictWorkflow.md) | Amendment of authoritative documents; surfacing and resolving conflicts |
| [ProjectAdoptionWorkflow.md](ProjectAdoptionWorkflow.md) | Project Adoption — the establishing transition that brings a project into a Project Governance Relationship |

New workflows are added only on demonstrated need ([../architecture/DesignPrinciples.md](../architecture/DesignPrinciples.md), P9) and enter this catalog through the sprint lifecycle like any other work.

## Responsibilities

- Define what qualifies as a workflow and the structure of the Process layer.
- Maintain the single catalog of process documents.

## Relationship to other documents

- Operates entirely within the rules of the Governance layer; every gate and decision right cited in this layer is defined in [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md).
- Uses the canonical vocabulary of [../architecture/Terminology.md](../architecture/Terminology.md) (sprint, phase, promotion, participant, owner).
- Per [../architecture/DependencyModel.md](../architecture/DependencyModel.md), the State & Tracking layer and reusable standards depend on this layer; nothing in this layer depends on them.
