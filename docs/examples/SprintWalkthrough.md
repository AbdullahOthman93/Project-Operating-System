# Sprint Walkthrough — a real sprint, end to end

> **Non-authoritative worked example.** This document defines no rule and owns no concept. It illustrates how the framework governed one real, already-closed sprint in this repository, so a reader can see the process in action. Every governing rule is owned elsewhere and linked, never restated. Where this example appears to differ from an authoritative document, that document governs.
>
> **This is a historical illustration, not live status.** It describes Sprint 2.1 as it was completed. The live pointer is `PROJECT_STATE.md`; the permanent record is [../knowledge/CHANGELOG.md](../knowledge/CHANGELOG.md). The facts cited below (files, counts, commit identifier) are drawn from that permanent record and the version-control history; they will not change, but they describe a past sprint only.

## Why this is a self-hosting example

This repository is the first project governed by the Project Operating System — the framework operates on its own development. So the clearest worked example is not a fabricated project but a sprint this repository actually ran. This walkthrough follows **Sprint 2.1 — Templates Foundation**, the first sprint of Phase 2, chosen because it is closed, small, and typical.

The authoritative workflow it followed is [../kernel/SprintLifecycle.md](../kernel/SprintLifecycle.md); the practical checklist for carrying it out is [../operations/SprintExecutionRunbook.md](../operations/SprintExecutionRunbook.md). Read those for the definitions — this document only shows what happened at each stage.

## The sprint, stage by stage

The stages, their order, and their gates are owned by [../kernel/SprintLifecycle.md](../kernel/SprintLifecycle.md) and [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md). What follows is what Sprint 2.1 did within them.

| Stage (defined in `SprintLifecycle.md`) | What happened in Sprint 2.1 |
|---|---|
| Definition | A design was produced for four document templates and submitted for the Scope gate. During review the owner asked whether a Specification template belonged; it was reassessed against Create on Need (P9) and the four-template scope was confirmed, with Specification, ADR, and Standard templates deferred. |
| Activation | On design approval, the sprint became the current sprint in the live state record (`PROJECT_STATE.md`) and its row was marked `Active` in `ExecutionPlan.md`. |
| Implementation | Only the approved deliverables were produced in `docs/templates/`: `AuthoritativeDocumentTemplate.md`, `SprintDesignTemplate.md`, `ChangelogEntryTemplate.md`, and `DirectoryIndexTemplate.md`, plus the directory's `INDEX.md`. The deferred templates were not created. |
| Validation | The result was checked against the [../standards/ValidationStandard.md](../standards/ValidationStandard.md) checklist — cross-references, dependency direction (templates reference their owning documents only, per [../architecture/DependencyModel.md](../architecture/DependencyModel.md) rule 5), and no duplicated definitions (P2). No defect was found. |
| Reporting | The implementing participant reported created files, the validation summary, and repository status, and did not self-approve. |
| Approval | The owner approved the report, authorizing closeout. |
| Closeout (atomic) | The four closeout artifacts were updated as one change set — see below. |

## What closeout touched

The closeout sequence is owned by [../kernel/SprintLifecycle.md](../kernel/SprintLifecycle.md) (stage 7). For Sprint 2.1 the atomic change set was:

- `ExecutionPlan.md` — Sprint 2.1 row marked `Completed`.
- `PROJECT_STATE.md` — updated to show 2.1 completed and to point at the next expected sprint.
- [../knowledge/CHANGELOG.md](../knowledge/CHANGELOG.md) — the Sprint 2.1 promotion entry added (its permanent record; the schema is owned by [../runtime/StateModel.md](../runtime/StateModel.md)).
- Version control — one dedicated change set per [../standards/VersionControlStandard.md](../standards/VersionControlStandard.md).

The resulting commit is recorded in history as `c754f59` ("Sprint 2.1 — Templates Foundation"), **8 files changed, 148 insertions and 8 deletions** — the sprint's four templates and INDEX update together with its three closeout records. These figures are a fixed historical fact drawn from the version-control record.

## What this example demonstrates

- Work happened **only inside an approved, scoped unit**, and a mid-review scope question was resolved by reassessment against a principle, not by silently widening scope.
- Nothing was **promoted implicitly**: the sprint stopped at the Scope, Validation, and Approval gates ([../architecture/GovernanceModel.md](../architecture/GovernanceModel.md)).
- The permanent record grew by **one promotion entry**, and the whole sprint is **one reversible change set**.

## Related documents

- The workflow illustrated here: [../kernel/SprintLifecycle.md](../kernel/SprintLifecycle.md); the runbook for it: [../operations/SprintExecutionRunbook.md](../operations/SprintExecutionRunbook.md).
- The permanent record this example cites: [../knowledge/CHANGELOG.md](../knowledge/CHANGELOG.md).
- Where to start as a new participant: [OnboardingGuide.md](OnboardingGuide.md).
