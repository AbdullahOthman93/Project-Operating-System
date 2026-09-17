# AI Engineering Standard

## Purpose

Defines the reusable, checkable engineering method for AI-assisted work under the system: how an AI-assisted task is classified, how context, model capability, and reasoning effort are selected, how sessions and planning are structured, and how AI-generated work is verified and evidenced before acceptance. This is the **only** place the AI engineering method is defined.

It defines a **method**, not authority. It creates no decision right, approval gate, precedence order, or principle, and it makes no AI output authoritative. The boundaries of AI participation — capability-is-not-authority, the human-approval boundary, and AI safety and trust — are owned by the [AI Governance Extension](../architecture/AIGovernanceExtension.md); decision rights, gates, precedence, and amendment by [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md); the durable principles by [../architecture/DesignPrinciples.md](../architecture/DesignPrinciples.md). This standard applies those within its method and restates none of them.

## Scope

The engineering conduct of AI-assisted work only — classification, context, model and effort routing, sessions, planning, parallelization, verification method, and evidence. Out of scope, with their owners: the economy-of-effort quality bar ([WorkEconomyStandard.md](WorkEconomyStandard.md)); the Validation-gate checklist ([ValidationStandard.md](ValidationStandard.md)); change-set discipline and completion ([VersionControlStandard.md](VersionControlStandard.md)); the AI human-approval boundary and safety boundaries ([../architecture/AIGovernanceExtension.md](../architecture/AIGovernanceExtension.md)); tool-specific mechanisms (supporting tool-adapter guidance, named for this repository in the binding note below). Outside that binding note, this standard names no language, framework, vendor, or tool ([DocumentationStandard.md](DocumentationStandard.md)).

Every requirement below is stated so that conformance can be determined by inspection; a requirement that could not be checked has been moved to the supporting adapter guidance and is referenced, not stated here ([StandardsModel.md](StandardsModel.md)).

## Conformance requirements

An AI-assisted task conforms to this standard when all of the following hold. Each is checkable against the task's own evidence ([../architecture/AIGovernanceExtension.md](../architecture/AIGovernanceExtension.md), *Evidence and accountability*; verified per [ValidationStandard.md](ValidationStandard.md)).

### 1. The task is classified before execution

Every meaningful AI-assisted task is assigned, before execution, a task class from: architecture, investigation, analysis, planning, implementation, refactoring, testing, verification, documentation, research, review, operations. The class is recorded in the task's evidence. Classification is what selects the remaining choices below; an unclassified task is non-conforming.

### 2. Context loaded is the minimum sufficient set

The context an AI participant is given is the minimum sufficient set for the task — enough to perform and verify it, and no unrelated material — applying the reading-footprint bar owned by [WorkEconomyStandard.md](WorkEconomyStandard.md). Checkably: the context is drawn from authoritative project artifacts and task-specific evidence; it excludes unrelated project areas, obsolete decisions, duplicated documentation, and speculative future requirements. When context priority must be resolved, authoritative constraints precede the current task, which precedes relevant architecture, which precedes relevant implementation, which precedes supporting material. A session whose context has accumulated unrelated work is reset before further work.

### 3. Model capability is routed to complexity, risk, and uncertainty

Model capability is selected from the combined assessment of task complexity, risk, and uncertainty, using the lowest capability level that reliably satisfies the required quality, verification, and safety. Capability levels are Light (simple, routine transformation), Standard (ordinary implementation, debugging, analysis), Advanced (complex implementation, difficult debugging, cross-component reasoning), and Expert (architecture, high uncertainty, high-impact system reasoning). Checkably: the highest-capability level is not selected by default, and complexity alone does not set the level — where failure would carry significant security, architecture, data, operational, financial, compliance, or production impact, risk overrides efficiency and a higher level is selected even for a small task. The selected level and its justification appear in the task's evidence.

### 4. Reasoning effort is routed to complexity, risk, and uncertainty

Reasoning effort is selected on the same combined assessment, using the lowest level that reliably produces the required result. Effort levels are Low (simple, predictable), Medium (normal engineering), High (complex, uncertain, or high-impact), and Very High (exceptional reasoning requirements). Checkably: maximum effort is not selected by default; where the consequence of failure is significant, risk overrides efficiency and a higher level is selected even for a small task. The objective is minimum *sufficient* effort, not minimum effort.

### 5. Planning precedes high-risk or complex work

Work that is architectural, complex, multi-step, high-risk, a significant refactor, or poorly understood is planned before execution; the plan identifies intent, context, constraints, approach, affected areas, verification strategy, and risks. Simple, low-risk, well-defined, reversible work may execute directly. Checkably: for any task in the planning-required set, a plan exists in the evidence before changes were made. Planning never substitutes for human approval where the [AI Governance Extension](../architecture/AIGovernanceExtension.md) human-approval boundary applies.

### 6. Execution stays within approved scope

Execution modifies only what the classified, approved task requires; speculative modification outside the task is not performed (Scope Protection, [../architecture/DesignPrinciples.md](../architecture/DesignPrinciples.md), P8, and the Scope gate of [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md)). A discovered requirement conflict, architectural issue, or scope change pauses execution and is surfaced per [../kernel/ChangeAndConflictWorkflow.md](../kernel/ChangeAndConflictWorkflow.md); it does not become work silently. Checkably: the changed artifacts fall within the approved scope, and any discovered out-of-scope need appears as a surfaced item rather than an executed change.

### 7. Parallelization requires genuine independence

Work is executed in parallel only when the parallel units are independently understandable, share no mutable state, can be independently verified, and consolidate for less cost than the benefit. Checkably: any parallelized units satisfy all four; work with sequential dependencies is executed sequentially, not parallelized to raise agent count.

### 8. Sessions have one clear purpose

An AI session carries one coherent working purpose. It is continued while the task stays coherent, context stays relevant, and continuing is more efficient than rebuilding; it is reset when the purpose changes, context is polluted, unrelated work accumulates, or independent verification is required; it ends when the task is complete and its evidence is captured. Checkably: a session does not mix unrelated tasks.

### 9. Work is verified before it is treated as complete

AI-generated output is not complete merely because the AI reports success. Verification proportional to the task's risk is performed and recorded before acceptance, drawn from: AI self-check (an initial filter only, never counted as independent verification), automated validation (preferred wherever objective validation exists), diff and repository inspection, independent verification (a separate pass, context, agent, or human review — recommended for complex, security-sensitive, architectural, or high-impact work), and human review (required wherever the [AI Governance Extension](../architecture/AIGovernanceExtension.md) human-approval boundary applies). The Validation-gate checklist itself is owned by [ValidationStandard.md](ValidationStandard.md); this requirement governs the AI verification *method* that precedes it. Checkably: completion is supported by verification evidence appropriate to the task class and risk.

### 10. Completion is evidenced

AI-assisted work leaves evidence sufficient to establish what occurred — proportional to risk, and at minimum the task definition and class, the changed artifacts, the validation results including any failures, and repository status; adding, as the task warrants, the implementation summary, tests, review findings, referenced decisions, known limitations, and commit information. This is the reporting content owed at the Reporting stage of [../kernel/SprintLifecycle.md](../kernel/SprintLifecycle.md), kept concise per [WorkEconomyStandard.md](WorkEconomyStandard.md). Checkably: the evidence is present and faithful; omission or misstatement is a defect.

Where the evidence includes measurement or telemetry, each figure carries its source. Three kinds are kept distinct and not conflated: measurement the AI participant can itself reliably observe (**agent-observable**), measurement that only the host environment can reliably supply (**host-observable**), and figures produced by combining or interpreting those (**derived analysis**). The AI participant records what it can reliably observe and does not assert host-observable measurement it cannot. Where a required measurement cannot be reliably obtained, **NOT AVAILABLE** is a valid measurement state and is recorded as such; it is never converted to zero, estimated, inferred, or silently omitted. Checkably: measurements are attributed to their source, and any unobtainable measurement appears as NOT AVAILABLE rather than a fabricated value.

## Requirements owned elsewhere (applied, not restated)

This standard operates within, and does not restate, the following. They are named so that a conforming implementation resolves each to its owner rather than to a copy here.

- **Human accountability, the human-approval boundary, capability-is-not-authority, AI safety and trust** — owned by [../architecture/AIGovernanceExtension.md](../architecture/AIGovernanceExtension.md).
- **Decision rights, approval gates, conflict precedence, amendment** — owned by [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md).
- **Durable principles** (single source of truth, technology agnosticism, scope protection, incremental and small safe changes, create on need, reusability, and the rest) — owned by [../architecture/DesignPrinciples.md](../architecture/DesignPrinciples.md).
- **The economy-of-effort quality bar** (reading footprint, re-derivation, review breadth, report length) — owned by [WorkEconomyStandard.md](WorkEconomyStandard.md).
- **The Validation-gate checklist** — owned by [ValidationStandard.md](ValidationStandard.md).
- **Change-set discipline and verified completion** (inspect → change → validate → review → commit → publish → verify) — owned by [VersionControlStandard.md](VersionControlStandard.md). This standard defines no Git behavior and no completion rule.

## Adoption and tool implementation

A project adopts this standard **by reference**, not by copying it, implementing it locally without conflicting with the system's governance, and tracing its implementation back to this standard. Tool-specific implementation belongs in supporting tool-adapter guidance (named in the binding note below); a tool mechanism implements a requirement of this standard and never redefines it. Guidance that cannot be checked by inspection is not stated as a requirement here; where such guidance is useful it lives in the adapter and is referenced.

## In this repository

The AI participant working under this standard is Claude Code, engaging through the `CLAUDE.md` binding; its tool-specific implementation of this method is the supporting [Claude Code Operating Notes](../agents/ClaudeCodeOperatingNotes.md) in `docs/agents/`. That guidance implements the requirements above through Claude Code mechanisms and holds no authority of its own. The binding is project-specific; the standard is not.

## Dispositioned questions

The following were raised during drafting and are settled here so that none remains open at adoption:

- **Numerical efficiency score** — *Not adopted in v1.0.* The economy-of-effort bar ([WorkEconomyStandard.md](WorkEconomyStandard.md)) governs by inspection; no single numerical score is introduced.
- **Formal task-risk classification (Low/Medium/High/Critical)** — *Not adopted as a mandatory scheme in v1.0.* The combined complexity–risk–uncertainty assessment in requirements 3 and 4 governs; a formal scale is not required.
- **Mandatory evidence templates per task class** — *Deferred to the tool-adapter / operational layer.* Requirement 10 sets the checkable minimum; per-class templates, if introduced, live in adapter guidance, not in this standard.
- **Separate AI context for independent verification of high-risk tasks** — *A recommended, non-mandatory practice.* Requirement 9 permits a separate pass, context, agent, or human review; none is singled out as mandatory.

## Responsibilities

- Define the checkable AI engineering method — classification, context, routing, sessions, planning, parallelization, verification, and evidence — as a reusable standard.
- Keep every requirement inspectable and keep the method subordinate to the governance boundaries and principles it applies, restating none of them.

## Relationship to other documents

- **Authorities (higher layers).** Applies the boundaries of [../architecture/AIGovernanceExtension.md](../architecture/AIGovernanceExtension.md), the gates and decision rights of [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md), and the principles of [../architecture/DesignPrinciples.md](../architecture/DesignPrinciples.md) (Governance); and runs within the stages of [../kernel/SprintLifecycle.md](../kernel/SprintLifecycle.md) and the surfacing procedure of [../kernel/ChangeAndConflictWorkflow.md](../kernel/ChangeAndConflictWorkflow.md) (Process). These are the higher-authority documents this standard depends on ([../architecture/DependencyModel.md](../architecture/DependencyModel.md)).
- **Peer standards.** Defers to [WorkEconomyStandard.md](WorkEconomyStandard.md) for the economy bar, [ValidationStandard.md](ValidationStandard.md) for the Validation-gate checklist, [VersionControlStandard.md](VersionControlStandard.md) for change-set discipline and completion, and [DocumentationStandard.md](DocumentationStandard.md) for its own form; it is cataloged in [StandardsModel.md](StandardsModel.md).
- **Lower layers (described).** Tool-specific implementation of this method lives in supporting tool-adapter guidance in the agent-guidance layer (named in the binding note below); such guidance implements the method and holds no authority.
- Conformance to this standard is verified through [ValidationStandard.md](ValidationStandard.md); violations surface per [../kernel/ChangeAndConflictWorkflow.md](../kernel/ChangeAndConflictWorkflow.md).
