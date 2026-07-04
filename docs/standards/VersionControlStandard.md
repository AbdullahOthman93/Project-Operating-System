# Version Control Standard

## Purpose

Defines the change-set discipline for governed work. This is the **only** place version-control conventions are defined.

## Scope

Change-set form and history integrity only. When a change set is created is defined by the closeout procedure of [../kernel/SprintLifecycle.md](../kernel/SprintLifecycle.md); who authorizes it is defined in [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md).

## Change-set discipline

- **One sprint, one change set.** Each sprint's work — its deliverables plus its closeout records — is captured as a single dedicated change set containing that sprint's work only. Unrelated changes never share a change set (Small Safe Changes, [../architecture/DesignPrinciples.md](../architecture/DesignPrinciples.md), P8).
- **Message form.** The change-set message begins with the unit identifier and approved name (e.g., a sprint number and sprint name — illustrative), followed by a summary of what was delivered and in which layer.
- **Clean completion.** At the end of closeout, the working tree is clean: nothing uncommitted, nothing untracked. A dirty tree at closeout is a defect.
- **History is promoted record.** Once a change set is part of promoted history, it is never rewritten, amended in place, or removed; corrections are made by new change sets under owner-approved amendment ([../kernel/ChangeAndConflictWorkflow.md](../kernel/ChangeAndConflictWorkflow.md)).
- **Standalone amendments.** An owner-approved amendment outside any sprint is captured as its own dedicated change set, identified as an amendment in its message.

## In this repository

The version control system in use is Git; a change set binds to a commit on the repository's primary branch. The binding is project-specific; the discipline is not.

## Responsibilities

- Define the shape of a conforming change set and the integrity rules for promoted history.

## Relationship to other documents

- Gives checkable form to the change-set requirements of the closeout procedure in [../kernel/SprintLifecycle.md](../kernel/SprintLifecycle.md), stage 7, without restating the procedure.
- Conformance is verified through [ValidationStandard.md](ValidationStandard.md); violations surface per [../kernel/ChangeAndConflictWorkflow.md](../kernel/ChangeAndConflictWorkflow.md).
