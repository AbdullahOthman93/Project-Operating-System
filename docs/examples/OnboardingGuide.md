# Onboarding Guide — start here

> **Non-authoritative guidance.** This guide defines no rule and owns no concept. It gives a new participant — human or AI — a starting path into the Project Operating System by pointing at the documents that govern the work. It restates none of them. Where it appears to conflict with an authoritative document, that document governs.

## Who this is for

Anyone about to do work in this repository. The framework governs *how* work happens here; this guide gets you oriented and pointed at your first task. It does not replace the architecture's own entry point — that is [../architecture/ArchitectureOverview.md](../architecture/ArchitectureOverview.md), and you should read it early.

## Step 1 — Understand why the system exists

Read, in this order, the documents that carry the intent and the rules of judgement:

1. [../architecture/Vision.md](../architecture/Vision.md) and [../architecture/Mission.md](../architecture/Mission.md) — why the system exists and what it delivers.
2. [../architecture/DesignPrinciples.md](../architecture/DesignPrinciples.md) — the ten principles (P1–P10) that constrain every decision.

## Step 2 — Understand the structure

3. [../architecture/ArchitectureOverview.md](../architecture/ArchitectureOverview.md) — the authoritative orientation and the single map from logical layers to physical directories. Start here for structure and let it direct you onward.
4. [../architecture/LayerModel.md](../architecture/LayerModel.md) and [../architecture/DependencyModel.md](../architecture/DependencyModel.md) — the layers, their authority, and which may reference which.
5. [../architecture/Terminology.md](../architecture/Terminology.md) — the canonical vocabulary; consult it whenever a term is unclear.

## Step 3 — Understand your obligations

6. [../contracts/ParticipantContract.md](../contracts/ParticipantContract.md) — the single, checkable interface every working participant must satisfy. This is where your obligations live; nothing else defines them. Its structure is described in [../contracts/ContractModel.md](../contracts/ContractModel.md).
- If you are an AI agent, also read [../agents/OperationalNotes.md](../agents/OperationalNotes.md) and the profile at [../agents/ClaudeAgentProfile.md](../agents/ClaudeAgentProfile.md).

## Step 4 — Understand how work is decided and run

7. [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md) — the decision rights and the approval gates; the owner approves, and work never self-promotes.
8. [../kernel/SprintLifecycle.md](../kernel/SprintLifecycle.md) and [../kernel/PhaseModel.md](../kernel/PhaseModel.md) — how a unit of work moves from definition to promotion, and how sprints compose into phases.
9. [../kernel/ChangeAndConflictWorkflow.md](../kernel/ChangeAndConflictWorkflow.md) — how to raise an amendment or surface a conflict instead of working around it.

## Step 5 — Do your first work

- Follow the practical checklist in [../operations/SprintExecutionRunbook.md](../operations/SprintExecutionRunbook.md); it tells you which authoritative document governs each step and which artifact you touch.
- Use the skeletons in [../templates/INDEX.md](../templates/INDEX.md) for any recurring document you produce.
- Check your result against [../standards/ValidationStandard.md](../standards/ValidationStandard.md) before reporting, and record change sets per [../standards/VersionControlStandard.md](../standards/VersionControlStandard.md).

## Step 6 — See it in action

- Read [SprintWalkthrough.md](SprintWalkthrough.md) — a real, already-closed sprint followed end to end, showing every step above in one concrete pass.

## Where state lives

- The live pointer to current status is `PROJECT_STATE.md`; the static phase/sprint sequence is `ExecutionPlan.md`; the permanent record of completed work is [../knowledge/CHANGELOG.md](../knowledge/CHANGELOG.md). Read them before acting so you know where things stand.

## Related documents

- The authoritative entry point this guide leads into: [../architecture/ArchitectureOverview.md](../architecture/ArchitectureOverview.md).
- The worked example that accompanies this guide: [SprintWalkthrough.md](SprintWalkthrough.md).
