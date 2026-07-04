# State Model

## Purpose

Defines the concepts of the State & Tracking layer: what a state record is, how live state is separated from the permanent record, and which schema documents this layer contains. This is the **only** place these concepts are defined.

## Scope

Concepts and schemas only. **Live, mutable state is never stored in this directory** — this layer defines the *shape* of state; the state itself lives in the tracking artifacts (see [TrackingArtifacts.md](TrackingArtifacts.md)). *When* state changes is procedure and belongs to the Process kernel ([../kernel/SprintLifecycle.md](../kernel/SprintLifecycle.md), [../kernel/PhaseModel.md](../kernel/PhaseModel.md)); *who* may authorize a change is defined in [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md).

## Concepts

- **State record** ([../architecture/Terminology.md](../architecture/Terminology.md)) — a live tracking artifact reflecting current, transient status. It is always overwritten in place as status changes; it is never a history.
- **Permanent record** — the promoted, append-only account of completed transitions, held in the Knowledge layer's changelog. Once promoted, an entry changes only by owner-approved amendment ([../kernel/ChangeAndConflictWorkflow.md](../kernel/ChangeAndConflictWorkflow.md)).
- **The boundary between them** — a transition leaves live state and enters the permanent record exactly once, at Promotion ([../architecture/GovernanceModel.md](../architecture/GovernanceModel.md)), executed through the closeout procedure of [../kernel/SprintLifecycle.md](../kernel/SprintLifecycle.md). Nothing is a permanent record until promoted; nothing promoted is tracked as live state afterwards.

## Layer catalog

| Document | Schema owned |
|---|---|
| [StateTransitionModel.md](StateTransitionModel.md) | Canonical status vocabulary, allowed transitions, promotion entry schema |
| [TrackingArtifacts.md](TrackingArtifacts.md) | Required content and update rules of the live tracking artifacts |

## Responsibilities

- Define the concept of state and the live/permanent boundary.
- Keep this layer free of live values: every value appearing in these documents is illustrative, never current.

## Relationship to other documents

- Operates within [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md) and the layer boundaries of [../architecture/LayerModel.md](../architecture/LayerModel.md).
- Depends on the Process kernel for every trigger: state changes happen only at kernel-prescribed stages.
- Per [../architecture/DependencyModel.md](../architecture/DependencyModel.md), project records in the Knowledge layer depend on this layer; nothing here depends on them.
