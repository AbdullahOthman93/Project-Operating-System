# Work Economy Standard

## Purpose

Defines the **economy-of-effort quality bar** for conducting governed work: how much context a participant loads, how much prior work it re-derives, how widely it reviews and verifies, and how much it reports. This is the **only** place the economy-of-effort quality bar is defined.

The bar exists to reduce unnecessary context loading, repeated analysis, and resource consumption **without** reducing engineering quality, architectural integrity, governance, or safety. Economy never licenses skipping a required check, a required gate, or required disclosure; where economy and a governing requirement appear to compete, the governing requirement wins and any doubt is surfaced per [../kernel/ChangeAndConflictWorkflow.md](../kernel/ChangeAndConflictWorkflow.md).

## Scope

The economy of a participant's working conduct and its work products only — reading footprint, re-derivation, review and verification breadth, and report length. *Which* checks the Validation gate applies is defined in [ValidationStandard.md](ValidationStandard.md); *which* gates and decision rights exist is defined in [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md); *when* stages such as reporting and validation run is defined in [../kernel/SprintLifecycle.md](../kernel/SprintLifecycle.md) and [../kernel/PhaseModel.md](../kernel/PhaseModel.md). This standard adds a **quality bar** applied to how that work is conducted; it defines no obligation, gate, stage, or check of its own, and weakens none.

## The economy bar

Work conforms to this standard when it satisfies, at minimum:

### Settled artifacts are authoritative and are not re-worked

- **Trust settled artifacts.** Approved baselines ([../architecture/Terminology.md](../architecture/Terminology.md)), the promoted permanent record ([../architecture/GovernanceModel.md](../architecture/GovernanceModel.md), Promotion), and the approved definitions of completed units of work are treated as authoritative and correct. They are not re-derived, re-verified, or second-guessed as routine.
- **Do not re-read settled work absent need.** Settled phases and units of work are not re-read unless their content is directly required to perform the current task.
- **Do not restate settled decisions.** A settled decision is not restated or summarized unless the owner explicitly requests it. Reproducing content that already has a single authoritative home is duplication and a defect (Single Source of Truth, [../architecture/DesignPrinciples.md](../architecture/DesignPrinciples.md), P2).

### Reading footprint is the minimum the task requires

- **Read only what the current task needs.** For a given sprint or task, only the minimum set of documents required to perform and validate it is read. Breadth of reading is justified by the task, not by habit.
- **Prefer repository state on recovery.** When re-establishing working context — for example, resuming work after an interruption — the repository's own state (its version-control history and current files, including the live tracking artifacts and permanent record) is the primary source of truth, consulted before any wider re-reading.

### Completed work is not repeated

- **Do not repeat completed work.** Work already completed and promoted is not redone unless verification detects an inconsistency, corruption, or other defect in it — in which case the defect is surfaced and handled per [../kernel/ChangeAndConflictWorkflow.md](../kernel/ChangeAndConflictWorkflow.md), not silently reworked.

### Review and verification are scoped to the work

- **No discretionary project-wide review.** A review spanning the whole project is not undertaken unless it is explicitly requested, or a conflict or defect of redesign scale — one whose resolution would require architecture amendment ([../architecture/GovernanceModel.md](../architecture/GovernanceModel.md), [../kernel/ChangeAndConflictWorkflow.md](../kernel/ChangeAndConflictWorkflow.md)) — has been detected.
- **Verify the affected artifacts.** When executing continuously across steps or units of work, verification targets the artifacts the current work directly affects, rather than re-validating the entire project each step.
- **Required checks are never suppressed.** This scoping governs *discretionary* breadth only. Any check a governing document specifically mandates is performed in full — in particular, when work introduces a new schema or standard, the existing corpus is validated against it exactly as [ValidationStandard.md](ValidationStandard.md) requires. Economy narrows what is done by choice, never what is required.

### Reporting is concise by default

- **Concise by default.** Progress reports are kept concise unless an expansion condition below holds.
- **Expand only on cause.** A report is expanded when, and only when: a blocker exists; a gate is not satisfied (for example, the Validation gate of [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md)); a redesign-scale conflict or defect is discovered; or the owner explicitly requests detailed reporting.
- **Concision never omits.** Concision reduces length, never required content. Faithful, complete reporting of the created and changed artifacts, the validation summary including any failures, and repository status — the report content owed at the Reporting stage of [../kernel/SprintLifecycle.md](../kernel/SprintLifecycle.md) — remains in force at all times; economy shortens how that content is expressed, never what it must include.

## In this repository

The participant working under this standard is Claude Code, engaging through the `CLAUDE.md` binding. Realized against that participant, the economy bar above is this repository's **Token Efficiency Rule**: the settled artifacts it trusts without re-derivation are the repository's **frozen** phases and decisions (the promoted `docs/knowledge/CHANGELOG.md`, approved baselines, and completed sprint and phase definitions); "re-establishing working context" is **session recovery**, for which `PROJECT_STATE.md`, `ExecutionPlan.md`, the Git history, and existing files are the primary source of truth; and "executing continuously across steps or units of work" is **Continuous Execution**. Applied automatically and without separate instruction, the rule directs Claude Code to load the least context a task needs, trust frozen work, avoid repeating completed work or reviewing project-wide absent an explicit request or a redesign-class conflict, verify only the artifacts the current work affects, and report concisely — expanding only on a blocker, a failed gate, a redesign-class issue, or an explicit request — thereby reducing token consumption while every governing check, gate, and disclosure remains fully in force. The binding is project-specific; the discipline is not.

## Responsibilities

- Define the economy-of-effort quality bar applied to reading footprint, re-derivation, review and verification breadth, and report length.
- Keep that bar subordinate to every governing requirement, so that economy never suppresses a required check, gate, or disclosure.

## Relationship to other documents

- Applies Single Source of Truth, Incremental Development, and Small Safe Changes ([../architecture/DesignPrinciples.md](../architecture/DesignPrinciples.md), P2, P7, P8) as a checkable quality bar; it restates none of them.
- Binds by reference like every standard cataloged in [StandardsModel.md](StandardsModel.md) — the gates and contracts that cite the standards catalog carry it to participants automatically; it adds no obligation of its own and is cited, never citing downward for its authority.
- Scopes the breadth at which the checks of [ValidationStandard.md](ValidationStandard.md) are applied without altering the checklist, and defers to it for every mandated check; it names no gate or stage, deferring to [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md), [../kernel/SprintLifecycle.md](../kernel/SprintLifecycle.md), and [../kernel/PhaseModel.md](../kernel/PhaseModel.md).
- Conformance to this standard is verified through [ValidationStandard.md](ValidationStandard.md); violations surface per [../kernel/ChangeAndConflictWorkflow.md](../kernel/ChangeAndConflictWorkflow.md).
