# Operational Notes

> **Non-authoritative guidance.** This document defines no rule, grants no authority, and owns no concept. It is a navigation aid for an agent working in this repository — it points to the authoritative documents that govern the work and never restates them. Where it appears to conflict with an authoritative document, that document governs and the conflict is surfaced per [../kernel/ChangeAndConflictWorkflow.md](../kernel/ChangeAndConflictWorkflow.md).

## How this repository is organized

Work is governed by layered documentation. The layers, their authority order, and what each may contain are defined in [../architecture/LayerModel.md](../architecture/LayerModel.md); which layer may reference which is defined in [../architecture/DependencyModel.md](../architecture/DependencyModel.md). This directory (`docs/agents/`) is a supporting layer: it may reference any authoritative layer for guidance, and nothing depends on it.

## Where to find what you need

- **Your obligations** — [../contracts/ParticipantContract.md](../contracts/ParticipantContract.md) (the single interface a working participant satisfies).
- **The gates and decision rights** — [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md); the principles behind them — [../architecture/DesignPrinciples.md](../architecture/DesignPrinciples.md).
- **The process to follow** — [../kernel/SprintLifecycle.md](../kernel/SprintLifecycle.md) and [../kernel/PhaseModel.md](../kernel/PhaseModel.md); how to raise amendments, conflicts, and defects — [../kernel/ChangeAndConflictWorkflow.md](../kernel/ChangeAndConflictWorkflow.md).
- **The quality bar** — the standards cataloged in [../standards/StandardsModel.md](../standards/StandardsModel.md), verified through [../standards/ValidationStandard.md](../standards/ValidationStandard.md).
- **State and tracking** — what the live and permanent records are, and the vocabulary and transitions they accept — [../runtime/StateModel.md](../runtime/StateModel.md) and its catalog; the permanent record itself is [../knowledge/CHANGELOG.md](../knowledge/CHANGELOG.md), the live pointer is `PROJECT_STATE.md`, and the static sequence is `ExecutionPlan.md`.
- **Reusable scaffolding** — [../templates/INDEX.md](../templates/INDEX.md) provides fill-in skeletons for recurring document types.

## Working rhythm

Read the current state before acting, work only within an approved and explicitly scoped unit, stop at every owner-decision gate, surface anything that conflicts rather than working around it, and report what changed accurately. Each of these is an obligation owned by the [Participant Contract](../contracts/ParticipantContract.md) and the documents it binds to — consult them for the authoritative wording; the summary here is orientation only.

## Relationship to other documents

- Every pointer above resolves to the document that owns the concept; this note owns none of them.
- The agent-specific counterpart to these shared notes is [ClaudeAgentProfile.md](ClaudeAgentProfile.md).
- Layer membership and permitted references for this directory are governed by [../architecture/LayerModel.md](../architecture/LayerModel.md) and [../architecture/DependencyModel.md](../architecture/DependencyModel.md).
