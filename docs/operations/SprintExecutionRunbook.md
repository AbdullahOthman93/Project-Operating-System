# Sprint Execution Runbook

> **Non-authoritative operating procedure.** This runbook defines no workflow, no stage, no gate, and no rule, and owns no concept. It is a practical checklist that helps a participant *carry out* the sprint workflow already defined in [../kernel/SprintLifecycle.md](../kernel/SprintLifecycle.md), pointing at the authoritative document that governs each step and naming the concrete artifact or tool touched. Where it appears to conflict with an authoritative document, that document governs and the conflict is surfaced per [../kernel/ChangeAndConflictWorkflow.md](../kernel/ChangeAndConflictWorkflow.md).

## What this runbook is for

Running a sprint touches several layers at once — the process that orders it, the gates that authorize it, the standards it is checked against, and the live artifacts it updates. No single authoritative document assembles that cross-layer sequence, because each correctly owns only its own part (Single Source of Truth, [../architecture/DesignPrinciples.md](../architecture/DesignPrinciples.md), P2). This runbook is that assembly and nothing more: it tells you *where to look* and *what you touch* at each step, never *what the rule is*.

The authoritative sequence, triggers, and exit conditions are owned by [../kernel/SprintLifecycle.md](../kernel/SprintLifecycle.md); the gates are owned by [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md). Read those for the definitions. This runbook is subordinate to both.

## Before you start

- Confirm a phase is open and any prior sprint's closeout is complete — the trigger condition in [../kernel/SprintLifecycle.md](../kernel/SprintLifecycle.md) and the phase state in [../kernel/PhaseModel.md](../kernel/PhaseModel.md). Read `PROJECT_STATE.md` (live pointer) and `ExecutionPlan.md` (static sequence) to see where things stand.
- Know your working obligations — they are defined in [../contracts/ParticipantContract.md](../contracts/ParticipantContract.md), not here.

## Stage-by-stage: where to look, what you touch

The stages, their order, and their exit conditions are defined in [../kernel/SprintLifecycle.md](../kernel/SprintLifecycle.md). For each stage below, that document governs; the right-hand notes are only the practical artifact/tool touchpoints in this repository.

| Lifecycle stage (defined in `SprintLifecycle.md`) | Governing authority to consult | What you touch here |
|---|---|---|
| Definition | Scope gate — [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md); required contents — `SprintLifecycle.md`; skeleton — [../templates/SprintDesignTemplate.md](../templates/SprintDesignTemplate.md) | The design document submitted for approval; declared dependencies checked against [../architecture/DependencyModel.md](../architecture/DependencyModel.md) |
| Activation | `SprintLifecycle.md` | `ExecutionPlan.md` (sprint row → Active) and `PROJECT_STATE.md` (current sprint), within the schemas of [../runtime/StateModel.md](../runtime/StateModel.md) |
| Implementation | Approved scope only; scope changes via [../kernel/ChangeAndConflictWorkflow.md](../kernel/ChangeAndConflictWorkflow.md) | The approved deliverables; nothing outside scope |
| Validation | The checklist owned by [../standards/ValidationStandard.md](../standards/ValidationStandard.md); satisfies the Validation gate in `GovernanceModel.md` | The deliverables under review; no state change |
| Reporting | `SprintLifecycle.md` (participant does not self-approve) | The report: created/changed artifacts, validation summary, repository status |
| Approval | Approval gate — `GovernanceModel.md` | Owner decision; you make no state change until it is given |
| Closeout (atomic) | The single atomic sequence in `SprintLifecycle.md` stage 7 | See the closeout touchpoints below |

## Closeout touchpoints

The closeout sequence and its all-or-nothing character are defined in [../kernel/SprintLifecycle.md](../kernel/SprintLifecycle.md) (stage 7); the promotion authority is in [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md). In this repository the artifacts touched, in the order that document prescribes, are:

- `ExecutionPlan.md` — mark the sprint completed (add the next sprint's row if it is not already present).
- `PROJECT_STATE.md` — reflect the completed sprint and point at the next.
- `docs/knowledge/CHANGELOG.md` — add the promotion entry (schema owned by [../runtime/StateModel.md](../runtime/StateModel.md) and its catalog; skeleton at [../templates/ChangelogEntryTemplate.md](../templates/ChangelogEntryTemplate.md)).
- Version control — capture the sprint's work and its closeout records as one dedicated change set, per [../standards/VersionControlStandard.md](../standards/VersionControlStandard.md).

If closeout is interrupted, completing it takes precedence over any new work and the interruption is surfaced as a state defect — as required by `SprintLifecycle.md`.

## Related documents

- The workflow this runbook helps carry out: [../kernel/SprintLifecycle.md](../kernel/SprintLifecycle.md); structured per [../kernel/ProcessModel.md](../kernel/ProcessModel.md).
- The layer rules that make this a non-authoritative, reference-only procedure: [../architecture/LayerModel.md](../architecture/LayerModel.md) and [../architecture/DependencyModel.md](../architecture/DependencyModel.md).
- Agent-facing orientation to the same documents: [../agents/OperationalNotes.md](../agents/OperationalNotes.md).
