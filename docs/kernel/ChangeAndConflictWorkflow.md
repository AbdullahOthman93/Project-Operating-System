# Change and Conflict Workflow

## Purpose

Defines the operational procedures for (a) amending authoritative documents and (b) surfacing and resolving conflicts between documents. This is the **only** place these procedures are defined.

## Scope

Procedure only. The *rules* being operationalized — that governance changes require owner-approved amendment, that conflicts are defects with a fixed precedence order, that architecture changes are versioned — are defined in [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md) and are not restated here.

## Conflict-surfacing procedure

Trigger: any participant detects that two documents disagree, or that a document contradicts observed repository state.

1. **Stop relying** on the conflicting content for further decisions in the current work.
2. **Report** the conflict explicitly to the owner: the documents (or document and state) involved, the specific disagreement, and which reading currently governs under the precedence order of [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md).
3. **Continue under precedence** — until resolved, the higher-authority document governs, per [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md).
4. **Resolve by amendment** — the owner either directs an amendment (below) or rules that no conflict exists. Silent resolution, in either direction, is prohibited (Explicit Authority, [../architecture/DesignPrinciples.md](../architecture/DesignPrinciples.md), P5).

## Amendment procedure

Trigger: a rule in an authoritative document must change, or an approved sprint definition must change mid-sprint.

1. **Proposal.** The proposer states: the rule (or scope item) to change, its single home per Single Source of Truth ([../architecture/DesignPrinciples.md](../architecture/DesignPrinciples.md), P2), the proposed wording, and the reason.
2. **Owner approval.** No amendment is applied without it; participants never amend authoritative content on their own authority ([../architecture/GovernanceModel.md](../architecture/GovernanceModel.md)).
3. **Application.** The change is made in the rule's single home only; references elsewhere are verified to remain valid rather than duplicated.
4. **Versioning check.** If the amendment changes layer structure, dependency rules, or decision rights, it constitutes a new architecture version per [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md) and is recorded as such.
5. **Promotion.** The approved amendment is promoted into the permanent changelog following the closeout discipline of [SprintLifecycle.md](SprintLifecycle.md), stage 7 — as part of the sprint it occurred in, or as a dedicated change set if it stands alone.

## Sprint-scope changes

A discovered need to exceed or alter an active sprint's approved scope is handled as an amendment to the sprint definition (procedure above), not by silently doing the extra work. Until approved, the original scope governs.

## Responsibilities

- Define the step-by-step procedure for surfacing conflicts and for amending authoritative content.
- Ensure every change and every conflict resolution leaves an explicit trail through the gates.

## Relationship to other documents

- Operationalizes the conflict-resolution and amendment rules of [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md); defines no precedence or decision rights of its own.
- Structured per [ProcessModel.md](ProcessModel.md); invoked from [SprintLifecycle.md](SprintLifecycle.md) whenever scope or consistency problems arise mid-sprint.
