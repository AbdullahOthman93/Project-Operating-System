# Contract Model

## Purpose

Defines what a contract is, how contracts bind, and which contracts exist. This is the **only** place the structure of the Contracts layer is defined.

## Scope

Contract organization only. The rules, procedures, schemas, and standards that contracts bind participants to are owned by their respective layers and are referenced, never restated (Single Source of Truth, [../architecture/DesignPrinciples.md](../architecture/DesignPrinciples.md), P2).

## What a contract is

A **contract** is a formal, checkable interface: the single source of truth for what a class of participants must satisfy to work under the system ([../architecture/LayerModel.md](../architecture/LayerModel.md)). A contract:

- states obligations **by reference** to the owning documents — the contract adds the binding, never the content;
- is **checkable** — conformance of a participant's conduct or a binding's text can be determined by inspection;
- is the **only** authority the Execution layer may depend on ([../architecture/DependencyModel.md](../architecture/DependencyModel.md), rule 6).

## How bindings relate to contracts

An **execution binding** ([../architecture/Terminology.md](../architecture/Terminology.md)) is a technology-specific artifact connecting a participant to the system. Bindings conform to a contract, hold no authority of their own, and never extend or reinterpret the contract. A conflict between a binding and a contract is a defect, surfaced per [../kernel/ChangeAndConflictWorkflow.md](../kernel/ChangeAndConflictWorkflow.md).

## Contracts catalog

| Document | Interface owned |
|---|---|
| [ParticipantContract.md](ParticipantContract.md) | Obligations of any participant — human or AI — working under the system |

## Deferred contracts

The **Execution Contract** (for tool adapters) is **deliberately absent**: no tool adapter or automation exists yet, and authoring it ahead of need would violate Create on Need ([../architecture/DesignPrinciples.md](../architecture/DesignPrinciples.md), P9). This deferral was owner-ratified with the Sprint 1.6 design. Boundary note: a participant is a human or AI *actor* ([../architecture/Terminology.md](../architecture/Terminology.md)); a tool adapter is a mechanism, not an actor, and is therefore not governed by the ParticipantContract. Whether future autonomous automation enters under the ParticipantContract or the Execution Contract is decided by the sprint that first introduces one.

## Responsibilities

- Define what qualifies as a contract and how bindings relate to contracts.
- Maintain the single catalog of contracts and keep deferred contracts visible.

## Relationship to other documents

- Contracts derive their requirements from the Governance layer and the standards catalog ([../standards/StandardsModel.md](../standards/StandardsModel.md)), per [../architecture/DependencyModel.md](../architecture/DependencyModel.md).
- The Execution layer conforms to the contracts cataloged here and to nothing else directly.
