# Participant Contract

## Purpose

Defines the formal, checkable obligations of any participant — human or AI — performing work under the system. This is the **only** place participant obligations are defined.

## Scope

Obligations in a participant's **working capacity** only. Decision rights, including the owner's approval authority, are defined in [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md) and are not granted, limited, or restated here; an owner performing work is bound by this contract like any participant, and an owner approving work is exercising rights defined there. Tool adapters are mechanisms, not participants, and fall outside this contract ([ContractModel.md](ContractModel.md)).

## Obligations

A conforming participant:

1. **Works only in approved scope.** Performs work only within an approved, explicitly scoped unit of work, satisfying the Scope gate as defined in [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md); scope changes are requested, never assumed.
2. **Never self-promotes.** Does not approve its own work or advance it past any gate; stops at every owner-decision point and waits (gates as defined in [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md)).
3. **Follows the process.** Conducts work through the stages of [../kernel/SprintLifecycle.md](../kernel/SprintLifecycle.md) and [../kernel/PhaseModel.md](../kernel/PhaseModel.md), including completing an interrupted closeout before any new work.
4. **Surfaces conflicts and defects.** Reports conflicts, defects, and validation failures per [../kernel/ChangeAndConflictWorkflow.md](../kernel/ChangeAndConflictWorkflow.md); never resolves, ignores, or works around them silently.
5. **Conforms to standards.** Produces deliverables that satisfy the standards cataloged in [../standards/StandardsModel.md](../standards/StandardsModel.md), verified per [../standards/ValidationStandard.md](../standards/ValidationStandard.md).
6. **Respects state discipline.** Updates tracking artifacts only at kernel-prescribed points, writing only values valid under the schemas of the State & Tracking layer ([../runtime/StateModel.md](../runtime/StateModel.md) and its catalog).
7. **Reports faithfully.** Reports created and changed artifacts, validation results including failures, and repository status accurately and completely; omission and misstatement are defects.

References to kernel and runtime documents above are conformance references under [../architecture/DependencyModel.md](../architecture/DependencyModel.md), rule 7; this contract's authority derives from the Governance layer and the standards it binds to.

## Bindings

A participant that operates through a technology-specific binding is additionally bound as follows: the binding conforms to this contract, holds no authority of its own, and never extends or reinterprets it; any conflict between the binding and this contract is a defect surfaced per [../kernel/ChangeAndConflictWorkflow.md](../kernel/ChangeAndConflictWorkflow.md). A participant without a binding satisfies this clause trivially.

## In this repository

The bindings currently governed by this contract are `CLAUDE.md` and the contents of `.claude/`. The binding is project-specific; the contract is not.

## Responsibilities

- Provide the single checkable interface every working participant must satisfy.
- Keep participant obligations bound by reference to their owning documents.

## Relationship to other documents

- Structured per [ContractModel.md](ContractModel.md); derives authority from [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md) and the standards catalog per [../architecture/DependencyModel.md](../architecture/DependencyModel.md).
- The term *participant* is defined in [../architecture/Terminology.md](../architecture/Terminology.md); execution bindings conform to this contract and are otherwise governed by the Execution layer rules of [../architecture/LayerModel.md](../architecture/LayerModel.md).
