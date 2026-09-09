# ClaudeCodeIntegrationDesign

A project-specific integration design record for this repository: how the Claude Code adapter — the [Claude Code Operating Notes](../agents/ClaudeCodeOperatingNotes.md) together with the `CLAUDE.md` / `.claude/` execution bindings — is applied to the Project Operating System under the [AI Governance Extension](../architecture/AIGovernanceExtension.md) and the [AI Engineering Standard](../standards/AIEngineeringStandard.md). This is a design record, not an authoritative layer: it defines no rule, owns no governance concept, creates no gate, and references the authoritative owner for every notion it uses. It authorizes no implementation by itself — implementation proceeds only through the owner-approved units of work of [../kernel/SprintLifecycle.md](../kernel/SprintLifecycle.md) and [../kernel/PhaseModel.md](../kernel/PhaseModel.md).

Produced under the DAI-02 Claude Code Integration Artifacts authorization. It is a Knowledge-layer project record ([../architecture/LayerModel.md](../architecture/LayerModel.md)) and depends only on Governance, State & Tracking, and standards, per [../architecture/DependencyModel.md](../architecture/DependencyModel.md).

## Purpose

To record the target integration design for Claude Code in this repository: what belongs in `CLAUDE.md`, what belongs in `.claude/`, when Rules, Skills, Subagents, Hooks, MCP, and Permissions are justified, and how Claude Code remains bound to the [Participant Contract](../contracts/ParticipantContract.md) — without duplicating any POS authority.

## Scope

Design findings and recommendations for this repository's Claude Code adapter only. Decision rights, gates, precedence, layer structure, dependency rules, version-control discipline, and the phase/sprint sequence are each owned elsewhere and are referenced, never set here. This record neither defines nor schedules any Phase or Sprint; the authoritative sequence lives in [../../ExecutionPlan.md](../../ExecutionPlan.md) and the live pointer in [../../PROJECT_STATE.md](../../PROJECT_STATE.md).

## Architecture-documentation impact of this integration

This integration is **not** change-free at the documentation level, and this record states that plainly rather than claiming otherwise. Adopting the Claude Code Integration Artifacts:

- **adds an authoritative Governance-layer document** — the [AI Governance Extension](../architecture/AIGovernanceExtension.md) — to `docs/architecture/`, and correspondingly updates [../architecture/INDEX.md](../architecture/INDEX.md);
- **adds an authoritative standard** — the [AI Engineering Standard](../standards/AIEngineeringStandard.md) — to `docs/standards/`, updating [../standards/INDEX.md](../standards/INDEX.md) and the catalog in [../standards/StandardsModel.md](../standards/StandardsModel.md);
- **adds supporting agent guidance** — the [Claude Code Operating Notes](../agents/ClaudeCodeOperatingNotes.md) — to `docs/agents/`, updating [../agents/INDEX.md](../agents/INDEX.md);
- **adds this project record** to `docs/knowledge/`, updating [INDEX.md](INDEX.md).

What it does **not** do is alter the logical-to-physical map, the layer structure ([../architecture/LayerModel.md](../architecture/LayerModel.md)), the dependency rules ([../architecture/DependencyModel.md](../architecture/DependencyModel.md)), or decision rights ([../architecture/GovernanceModel.md](../architecture/GovernanceModel.md)). Because none of those change, the adoption is not a new **architecture version**; but it is not free of architecture-*documentation* change, and the earlier assertion to the contrary is corrected here. All four documents land in directories already mapped in [../architecture/ArchitectureOverview.md](../architecture/ArchitectureOverview.md); no new POS layer and no new physical-map row is introduced.

## Adapter documentation versus execution binding

A key distinction this design preserves: the Claude Code *guidance* (the [Claude Code Operating Notes](../agents/ClaudeCodeOperatingNotes.md)) is **supporting agent guidance** in `docs/agents/`, not an authoritative layer and not an execution artifact. The actual Claude Code **execution bindings** remain `CLAUDE.md` and `.claude/`, in the Execution layer. Under [../architecture/DependencyModel.md](../architecture/DependencyModel.md) rule 6, Execution depends only on Contracts; the bindings therefore conform to the [Participant Contract](../contracts/ParticipantContract.md) and to nothing else directly. The Operating Notes are used as design and conformance reference; they never become an authority on which Execution depends.

## Governing relationship

The governance-and-implementation flow the integration preserves:

- [Participant Contract](../contracts/ParticipantContract.md) governs participation → `CLAUDE.md` / `.claude/` conform to it (the only authority Execution depends on);
- [AI Governance Extension](../architecture/AIGovernanceExtension.md) owns AI authority, accountability, and human-approval boundaries;
- [AI Engineering Standard](../standards/AIEngineeringStandard.md) owns the engineering method;
- [Claude Code Operating Notes](../agents/ClaudeCodeOperatingNotes.md) translate that method into Claude Code mechanisms as supporting guidance.

This is a governance-and-implementation reading, not a dependency chain: the only authority the bindings depend on is the Participant Contract.

## Integration principles

- **No governance duplication.** Claude Code configuration must not reproduce decision rights, approval gates, precedence, or project governance rules — owned by [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md) and [AIGovernanceExtension.md](../architecture/AIGovernanceExtension.md). It operationalizes their requirements only within the existing contract and method.
- **No contract duplication.** The [Participant Contract](../contracts/ParticipantContract.md) is the single source of participant obligations; `CLAUDE.md` never becomes a second copy of it.
- **No standard duplication.** The [AI Engineering Standard](../standards/AIEngineeringStandard.md) owns the engineering principles; configuration carries only the minimum implementation detail needed to execute them.
- **Capability is not authority.** Claude Code features acquire no authority from being able to edit files, run commands, reach external systems, invoke MCP, create agents, or run hooks.
- **Minimum sufficient mechanism.** No Rule, Skill, Agent, Hook, MCP integration, or permission exception without demonstrated need (Create on Need, [../architecture/DesignPrinciples.md](../architecture/DesignPrinciples.md), P9).

## `CLAUDE.md` target

The existing `CLAUDE.md` is intentionally minimal — an execution binding, not a source of truth — and this design preserves that. It should hold only high-value, repository-wide binding information: Claude's participant role, the binding to the [Participant Contract](../contracts/ParticipantContract.md), conflict-surfacing behavior, and essential navigation pointers that are genuinely part of the binding. It should not absorb the AI Governance Extension, the AI Engineering Standard, a POS manual, a Skill catalog, transient instructions, or a duplicate of the contract. It is amended only when an actual execution-binding gap is demonstrated — not merely because guidance exists. (Any such change is a separate, owner-approved unit of work; this record does not authorize it.)

## `.claude/` target

`.claude/` is the execution-binding area and evolves incrementally. It may grow to include `rules/`, `skills/`, `agents/`, and `hooks/` subdirectories, but only as each is justified. It is not a source of governance; it implements the applicable contract and approved operating practice. `.claude/settings.json` is a permission boundary that grants nothing and denies history-rewriting Git operations already required by [../standards/VersionControlStandard.md](../standards/VersionControlStandard.md); it adds no requirement of its own.

## Mechanism strategy (design intent, not a schedule)

Each mechanism is introduced only on demonstrated need; the following records the intent and the test, not a timeline.

- **Rules** — introduce a scoped Rule only when an instruction is stable, clearly scoped, repeatedly needed, and inappropriate for `CLAUDE.md`. Rules reference the authoritative owner and never become hidden governance.
- **Skills** — the preferred mechanism for reusable procedural workflows (for example: repository-context establishment, conformance review, validation, closeout), created only once the workflow is defined and justified, each with purpose, trigger, required context, steps, output, verification, and side-effect boundaries.
- **Subagents** — for genuine context isolation or specialization; not required for ordinary implementation. Independent verification does not require a Subagent.
- **MCP** — an external trust boundary; none added to the baseline until a concrete external-system use case exists, each evaluated for value, trust, authentication, data exposure, prompt-injection risk, scope, and reversibility.
- **Hooks** — reserved for deterministic lifecycle checks with clear value; never used to invent a gate or bypass an approval boundary.
- **Permissions** — least privilege, explicit access, narrow scope, sensitive operations reviewable; technical permission is never approval authority.

## Routing, context, sessions, and verification (design intent)

Model and effort selection implement the routing principle owned by [../standards/AIEngineeringStandard.md](../standards/AIEngineeringStandard.md) — complexity, risk, and uncertainty together, lowest sufficient level, risk override permitted — without hard-coding a vendor-specific model policy into POS. Context is managed to the minimum sufficient set ([../standards/WorkEconomyStandard.md](../standards/WorkEconomyStandard.md)); sessions carry one clear purpose; verification remains proportional to risk and never equates Claude's statement of success with verified completion, against the checklist owned by [../standards/ValidationStandard.md](../standards/ValidationStandard.md).

## Git integration

Claude Code operates under this repository's existing change-set discipline and **Git Completion Rule** exactly as owned by [../standards/VersionControlStandard.md](../standards/VersionControlStandard.md): dedicated change sets, clean completion, accurate status, validation before completion, authorized commit, publication to `origin`, and verified publication as the completion criterion. The integration creates no alternative Git lifecycle and reinvents no completion rule in a Skill or Hook.

## Repository startup pattern

A Claude Code session working in this repository establishes context from the authoritative artifacts before execution, proportional to the task — typically `CLAUDE.md`, then [../../PROJECT_STATE.md](../../PROJECT_STATE.md), then [../../ExecutionPlan.md](../../ExecutionPlan.md), then the relevant governance, contract, or standard, then repository status and the task-specific files. The repository remains the primary source of truth ([../standards/WorkEconomyStandard.md](../standards/WorkEconomyStandard.md)).

## What this design does not do

- It does not authorize implementation, commit, publication, or activation of any Claude Code mechanism by itself.
- It does not create, schedule, or sequence any Phase or Sprint; the phase/sprint order is owned by [../kernel/PhaseModel.md](../kernel/PhaseModel.md) and recorded in [../../ExecutionPlan.md](../../ExecutionPlan.md).
- It does not modify POS governance, the Layer Model, the Dependency Model, or decision rights; conflicts, if any, are surfaced per [../kernel/ChangeAndConflictWorkflow.md](../kernel/ChangeAndConflictWorkflow.md).
- It does not create a second contract, a new POS layer, independent AI authority, or a competing set of approval gates.

## Relationship to other documents

- Applies the AI-participant boundaries owned by [../architecture/AIGovernanceExtension.md](../architecture/AIGovernanceExtension.md) and the method owned by [../standards/AIEngineeringStandard.md](../standards/AIEngineeringStandard.md) to a concrete tool; both remain the sole owners of what they define.
- The obligations the bindings satisfy are owned by [../contracts/ParticipantContract.md](../contracts/ParticipantContract.md); the tool guidance itself is [../agents/ClaudeCodeOperatingNotes.md](../agents/ClaudeCodeOperatingNotes.md).
- Structural placement and dependency direction follow [../architecture/LayerModel.md](../architecture/LayerModel.md) and [../architecture/DependencyModel.md](../architecture/DependencyModel.md); this record is a project record under [INDEX.md](INDEX.md).
