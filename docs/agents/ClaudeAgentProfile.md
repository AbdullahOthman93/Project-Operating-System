# Claude Agent Profile

> **Non-authoritative guidance.** This document defines no rule, grants no authority, and owns no concept. It orients the AI agent that works in this repository to where its obligations and process live, entirely by reference. If anything here appears to conflict with an authoritative document, that document governs and the conflict is surfaced per [../kernel/ChangeAndConflictWorkflow.md](../kernel/ChangeAndConflictWorkflow.md).

## What this agent is

Claude is an AI **participant** ([../architecture/Terminology.md](../architecture/Terminology.md)) that performs work in this repository. It engages the system through a single technology-specific execution binding, `CLAUDE.md`, together with the contents of `.claude/`. The binding holds no authority of its own; it names the contract Claude works under and nothing more ([../contracts/ContractModel.md](../contracts/ContractModel.md)).

## Where its obligations live

Claude's obligations as a working participant are defined in **one** place — the [Participant Contract](../contracts/ParticipantContract.md). This profile does not restate, extend, or reinterpret them; it points to them. The contract is the single checkable interface Claude must satisfy, and the governance those obligations derive from is reached through it ([../architecture/GovernanceModel.md](../architecture/GovernanceModel.md)).

## How it works here

Claude conducts work through the stages of [../kernel/SprintLifecycle.md](../kernel/SprintLifecycle.md) within the phase structure of [../kernel/PhaseModel.md](../kernel/PhaseModel.md), stopping at every owner-decision gate defined in [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md). It produces deliverables to the standards cataloged in [../standards/StandardsModel.md](../standards/StandardsModel.md), updates tracking artifacts only at the points and with the values the State & Tracking layer permits ([../runtime/StateModel.md](../runtime/StateModel.md)), and surfaces conflicts and defects rather than resolving them silently ([../kernel/ChangeAndConflictWorkflow.md](../kernel/ChangeAndConflictWorkflow.md)). The practical orientation for doing so is in [OperationalNotes.md](OperationalNotes.md).

## Relationship to other documents

- The interface Claude satisfies is owned by [../contracts/ParticipantContract.md](../contracts/ParticipantContract.md); its structure by [../contracts/ContractModel.md](../contracts/ContractModel.md). This profile references both and restates neither.
- The binding through which Claude participates is `CLAUDE.md` (Execution layer, [../architecture/LayerModel.md](../architecture/LayerModel.md)); it conforms to the contract above.
- Working orientation shared with any agent is in [OperationalNotes.md](OperationalNotes.md).
