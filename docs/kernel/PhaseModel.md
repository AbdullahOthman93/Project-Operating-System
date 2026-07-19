# Phase Model

## Purpose

Defines how phases are composed of sprints and how a phase is entered, gated, and closed. This is the **only** place phase composition and phase gating are defined.

## Scope

Phase-level ordering and gating only. What a phase *is* is defined in [../architecture/Terminology.md](../architecture/Terminology.md); the lifecycle of the sprints inside a phase is defined in [SprintLifecycle.md](SprintLifecycle.md); the approving authority at every gate is defined in [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md).

## Composition rules

- A phase is an owner-approved sequence of sprints serving one stated objective, recorded in the execution plan.
- Sprints within a phase are numbered `<phase>.<n>` and run **sequentially**: exactly one sprint is active at a time, and a sprint begins only after its predecessor's closeout is complete ([SprintLifecycle.md](SprintLifecycle.md)).
- Sprints are defined incrementally ([../architecture/DesignPrinciples.md](../architecture/DesignPrinciples.md), P7, P9): a phase does not require all of its sprints to be designed up front; undesigned sprints are recorded as pending definition.

## Phase entry

A phase opens when:

1. the previous phase, if any, has been closed; and
2. the owner has approved the phase's objective and its place in the execution plan (Scope gate, [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md)).

## Phase exit

A phase closes when:

1. every sprint in the phase has completed closeout, and no sprint remains pending definition within the phase's approved objective;
2. the owner approves phase closure (Approval gate); and
3. the phase transition is promoted into the permanent changelog (Promotion), and the execution plan and live state record are updated — following the same atomic closeout discipline as [SprintLifecycle.md](SprintLifecycle.md), stage 7, **including publication of the phase-closure change set to the official repository and verification of that publication**. No subsequent phase begins until that publication is verified; a failed or unverifiable publication stops execution and is surfaced to the owner, exactly as at sprint closeout.

A phase is never closed implicitly by starting the next one.

## Responsibilities

- Define how sprints compose into phases and the entry/exit conditions of a phase.
- Define the promotion of phase transitions into the permanent record.

## Relationship to other documents

- Operationalizes the gates of [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md) at phase granularity.
- Structured per [ProcessModel.md](ProcessModel.md); delegates all sprint-level procedure to [SprintLifecycle.md](SprintLifecycle.md).
- Terms (phase, sprint, promotion, owner) are defined in [../architecture/Terminology.md](../architecture/Terminology.md).
