# State Transition Model

## Purpose

Defines the canonical status vocabulary for sprints and phases, the allowed transitions between statuses, and the schema of a promotion entry. This is the **only** place statuses and their transitions are defined.

## Scope

Validity only — which statuses exist, which transitions are legal, and what a well-formed promotion entry contains. The stages that *trigger* transitions are defined in [../kernel/SprintLifecycle.md](../kernel/SprintLifecycle.md) and [../kernel/PhaseModel.md](../kernel/PhaseModel.md); the authority that approves them is defined in [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md). Per Create on Need ([../architecture/DesignPrinciples.md](../architecture/DesignPrinciples.md), P9), only statuses the system has actually exercised are defined.

## Sprint statuses

| Status | Meaning |
|---|---|
| **Pending Definition** | The sprint exists in the execution plan as a placeholder; no approved design. |
| **Active** | The sprint's design is owner-approved and it is the current unit of work (entered at Activation, [../kernel/SprintLifecycle.md](../kernel/SprintLifecycle.md) stage 2). |
| **Completed** | Closeout has finished in full ([../kernel/SprintLifecycle.md](../kernel/SprintLifecycle.md) stage 7). |

**Allowed transitions:** Pending Definition → Active (upon design approval, Scope gate); Active → Completed (upon owner approval and full closeout, Approval gate + Promotion). No status is skipped and no transition runs backward: a rejected design remains Pending Definition; rejected implementation remains Active and is reworked within scope. Exactly one sprint is Active at a time ([../kernel/PhaseModel.md](../kernel/PhaseModel.md)).

## Phase statuses

| Status | Meaning |
|---|---|
| **Open** | Phase entry conditions met ([../kernel/PhaseModel.md](../kernel/PhaseModel.md)); sprints may run. |
| **Closed** | Phase exit conditions met and the closure promoted. |

**Allowed transition:** Open → Closed only. A phase is never reopened; further work under its objective requires a new owner-approved phase.

## Promotion entry schema

Every promotion entry in the permanent changelog contains, in order:

1. **Identifier** — the unit's number and approved name, as the entry heading (e.g., a sprint number and sprint name).
2. **Status** — completion statement including approval (e.g., "Completed and approved").
3. **Summary** — what the unit delivered, in terms of artifacts and their layer.
4. **Approved by** — the approving authority per [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md), and where the approval was given.

Entries are append-only, newest first. A promoted entry is never edited except by owner-approved amendment ([../kernel/ChangeAndConflictWorkflow.md](../kernel/ChangeAndConflictWorkflow.md)). All values shown in this document are illustrative, never current state.

## Responsibilities

- Provide the single vocabulary against which any status value in a tracking artifact is validated.
- Define the only legal transitions and the shape of the record each promotion produces.

## Relationship to other documents

- Statuses change only at the stages defined in [../kernel/SprintLifecycle.md](../kernel/SprintLifecycle.md) and [../kernel/PhaseModel.md](../kernel/PhaseModel.md), under the gates of [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md).
- The artifacts that carry these statuses are defined in [TrackingArtifacts.md](TrackingArtifacts.md); layer concepts in [StateModel.md](StateModel.md).
