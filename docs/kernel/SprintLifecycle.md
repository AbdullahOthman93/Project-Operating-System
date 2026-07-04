# Sprint Lifecycle

## Purpose

Defines the canonical workflow of a sprint: the stages every sprint passes through, from definition to promotion into the permanent record. This is the **only** place the sprint lifecycle is defined.

## Scope

Ordering and procedure only. What a sprint *is* is defined in [../architecture/Terminology.md](../architecture/Terminology.md); the authority of each gate is defined in [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md); the quality criteria applied at validation belong to the reusable standards of the Knowledge layer. This workflow says *when* those criteria are applied, never what they are.

## Trigger

A phase is open (see [PhaseModel.md](PhaseModel.md)) and the previous sprint, if any, has fully completed closeout (stage 7). **A sprint never begins while a prior sprint's closeout is incomplete.**

## Stages

1. **Definition.** A sprint design is produced stating: objective, scope, deliverables, dependencies, success criteria, completion criteria, risks, and expected impact on subsequent sprints. Declared dependencies must validate against [../architecture/DependencyModel.md](../architecture/DependencyModel.md). The design is submitted to the owner; no implementation occurs before the design is approved (Scope gate, [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md)).

2. **Activation.** Upon owner approval of the definition, the sprint becomes the current sprint in the live state record.

3. **Implementation.** Only the approved deliverables are produced. Work outside the approved scope is not performed; if scope proves wrong or insufficient, the sprint definition is amended via [ChangeAndConflictWorkflow.md](ChangeAndConflictWorkflow.md) rather than silently exceeded.

4. **Validation.** Before reporting, the result is validated against the sprint's stated success criteria and against the governance documents — including cross-reference integrity, dependency validation per [../architecture/DependencyModel.md](../architecture/DependencyModel.md), and absence of duplicated definitions per Single Source of Truth ([../architecture/DesignPrinciples.md](../architecture/DesignPrinciples.md), P2). This satisfies the Validation gate.

5. **Reporting.** The implementing participant reports the created or changed artifacts, the validation summary, observations, and repository status. The participant does not approve or promote its own work.

6. **Approval.** The owner reviews the report (Approval gate). Rejection returns the sprint to Implementation within its approved scope; approval authorizes closeout.

7. **Closeout (promotion).** One atomic sequence, executed in full or not at all:
   1. The **execution plan** is updated: the sprint is marked completed and the next sprint's row is added.
   2. The **live state record** is updated to reflect the completed sprint and point at the next.
   3. The promotion entry is added to the **permanent changelog** (Promotion, [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md)).
   4. The sprint's work and its closeout records are captured as a **single dedicated change set** in version control, containing that sprint's work only.

   If closeout is interrupted, completing it takes precedence over all new work; the interruption is surfaced to the owner as a state defect.

## In this repository

The role names above bind to: live state record — `PROJECT_STATE.md`; execution plan — `ExecutionPlan.md`; permanent changelog — `docs/knowledge/CHANGELOG.md`. This binding is project-specific; the workflow itself is not.

## Responsibilities

- Define the stages and ordering every sprint follows.
- Define closeout as a single atomic procedure and the precedence of completing an interrupted closeout.

## Relationship to other documents

- Operationalizes the four gates of [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md); defines no gates of its own.
- Structured per [ProcessModel.md](ProcessModel.md); sprints compose into phases per [PhaseModel.md](PhaseModel.md).
- Scope changes and detected conflicts during a sprint follow [ChangeAndConflictWorkflow.md](ChangeAndConflictWorkflow.md).
