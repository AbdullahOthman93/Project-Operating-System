# Tracking Artifacts

## Purpose

Defines the required content and update rules of the live tracking artifacts — the documents that carry current state. This is the **only** place their schemas are defined.

## Scope

Artifact structure and update rules only. Status values must come from [StateTransitionModel.md](StateTransitionModel.md); update timing comes from the Process kernel; the artifacts themselves live at the repository root, never in this directory ([StateModel.md](StateModel.md)).

## The live state record

A single document holding the current position of the project. Required content:

1. A statement that the record is transient tracking, not a permanent record, pointing to the permanent changelog.
2. **Architecture version** — the approved version in force.
3. **Repository baseline** — the approved baseline being built upon.
4. **Governed project and origin** — the Project Governance Relationship this record tracks, its origin baseline, and the origin baseline's conformance posture ([../architecture/ProjectGovernanceRelationship.md](../architecture/ProjectGovernanceRelationship.md)).
5. **Current phase** — the open phase.
6. **Current sprint** — the sprint that is Active, or the next expected sprint marked as pending.
7. **Last completed sprint** — number, name, and approval status.

The record is overwritten in place; it never accumulates history. It is updated only at kernel-prescribed points — Activation and Closeout ([../kernel/SprintLifecycle.md](../kernel/SprintLifecycle.md), stages 2 and 7), phase transitions ([../kernel/PhaseModel.md](../kernel/PhaseModel.md)), and the establishing transition of a governance relationship ([../kernel/ProjectAdoptionWorkflow.md](../kernel/ProjectAdoptionWorkflow.md)).

## The execution plan

A single document holding the approved sequence of phases and sprints. Required content:

1. A statement that it defines order and status only, deferring live detail to the state record.
2. One table per phase, titled with the phase number and objective, with columns:
   - **Sprint** — the `<phase>.<n>` identifier ([../kernel/PhaseModel.md](../kernel/PhaseModel.md));
   - **Description** — the approved sprint name, or a placeholder while Pending Definition;
   - **Status** — a value from the sprint vocabulary of [StateTransitionModel.md](StateTransitionModel.md).

Rows are appended as sprints are added and statuses advance only along the allowed transitions. Completed rows are history and are never rewritten except by owner-approved amendment ([../kernel/ChangeAndConflictWorkflow.md](../kernel/ChangeAndConflictWorkflow.md)).

## Update rules

- Tracking artifacts are updated only as part of executing a kernel-prescribed stage — never ad hoc, never retroactively.
- Every value written must be valid under [StateTransitionModel.md](StateTransitionModel.md); writing an undefined status is a defect.
- The participant updating a tracking artifact never promotes its own work thereby; promotion authority remains with the owner ([../architecture/GovernanceModel.md](../architecture/GovernanceModel.md)).

## In this repository

The roles above bind to: live state record — `PROJECT_STATE.md`; execution plan — `ExecutionPlan.md`; permanent changelog — `docs/knowledge/CHANGELOG.md`. The binding is project-specific; the schemas are not.

## Responsibilities

- Define the checkable structure of every live tracking artifact.
- Confine repository-specific naming to the binding note above.

## Relationship to other documents

- Carries the statuses defined in [StateTransitionModel.md](StateTransitionModel.md) under the concepts of [StateModel.md](StateModel.md).
- Update points are owned by [../kernel/SprintLifecycle.md](../kernel/SprintLifecycle.md) and [../kernel/PhaseModel.md](../kernel/PhaseModel.md); authority by [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md).
