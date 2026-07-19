# Version Control Standard

## Purpose

Defines the change-set discipline — and the publication that completes a unit of work — for governed work. This is the **only** place version-control conventions are defined.

## Scope

Change-set form, its publication to the official repository, and history integrity only. *When* a change set is created and published — and the progression that depends on it — is defined by the closeout procedure of [../kernel/SprintLifecycle.md](../kernel/SprintLifecycle.md) and, at phase granularity, [../kernel/PhaseModel.md](../kernel/PhaseModel.md); *who* authorizes it is defined in [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md).

## Change-set discipline

- **One sprint, one change set.** Each sprint's work — its deliverables plus its closeout records — is captured as a single dedicated change set containing that sprint's work only. Unrelated changes never share a change set (Small Safe Changes, [../architecture/DesignPrinciples.md](../architecture/DesignPrinciples.md), P8).
- **Message form.** The change-set message follows the repository's adopted message convention (named in the binding note below), identifies the unit of work by its identifier and approved name, and summarizes what was delivered and in which layer.
- **Clean completion.** At the end of closeout, the working tree is clean — nothing uncommitted, nothing untracked — and the unit's change set has been published to the official repository and its publication verified (see *Completion and publication* below). A dirty tree, or an unpublished or unverified change set, at closeout is a defect.
- **History is promoted record.** Once a change set is part of promoted history, it is never rewritten, amended in place, or removed; corrections are made by new change sets under owner-approved amendment ([../kernel/ChangeAndConflictWorkflow.md](../kernel/ChangeAndConflictWorkflow.md)).
- **Standalone amendments.** An owner-approved amendment outside any sprint is captured as its own dedicated change set, identified as an amendment in its message.

## Completion and publication

Recording a change set locally does not complete a unit of work; **publishing** it does. A unit of work — a sprint at its closeout, a phase at its closure, or a standalone amendment — is complete only once its change set has been published to the project's **official repository** and that publication has been **verified**. Until then the unit's work is not part of promoted history, and no later unit of work builds on top of it.

A conforming publication captures exactly the unit's work under the change-set discipline above, carries a conforming message, is recorded as the unit's single change set, and is confirmed received by the official repository. Verified publication is the completion criterion for every unit of work, applied automatically and without separate instruction.

*When* publication occurs, and the progression it gates — no next phase, sprint, or unit of work begins until publication is verified, and a failed or unverifiable publication stops execution and is surfaced to the owner — belong to the closeout procedure of [../kernel/SprintLifecycle.md](../kernel/SprintLifecycle.md) (stage 7) and to phase closure in [../kernel/PhaseModel.md](../kernel/PhaseModel.md). This standard defines the form of a conforming completion and the criterion that completion requires verified publication; it defines neither the procedure nor its gates ([StandardsModel.md](StandardsModel.md)).

## In this repository

The version control system in use is Git; a change set binds to a commit on the repository's primary branch (`main`), and the **official repository** is the configured `origin` remote. The adopted message convention is **Conventional Commits**. Publication is `git push` to `origin`; verification confirms `origin` has received the commit (the local branch is no longer ahead of its upstream).

Realized against Git, the completion-and-publication discipline above is this repository's **Git Completion Rule**. After a unit of work's deliverables are complete, its Validation gate has passed, and it is approved complete, Claude Code automatically: (1) reviews repository status; (2) stages all changes; (3) creates an appropriate Conventional Commit; (4) commits; (5) pushes to `origin`; (6) verifies the push succeeded; and (7) only then allows execution to continue to the next phase, sprint, or unit of work. (8) If the push fails, execution stops, the reason is reported, and the rule waits for owner action. The binding is project-specific; the discipline is not.

## Responsibilities

- Define the shape of a conforming change set, the criterion that completes a unit of work by verified publication, and the integrity rules for promoted history.

## Relationship to other documents

- Gives checkable form to the change-set and publication requirements of the closeout procedure in [../kernel/SprintLifecycle.md](../kernel/SprintLifecycle.md), stage 7, and of phase closure in [../kernel/PhaseModel.md](../kernel/PhaseModel.md), without restating either procedure.
- Conformance is verified through [ValidationStandard.md](ValidationStandard.md); violations surface per [../kernel/ChangeAndConflictWorkflow.md](../kernel/ChangeAndConflictWorkflow.md).
