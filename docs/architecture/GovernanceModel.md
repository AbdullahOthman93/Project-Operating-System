# Governance Model

## Purpose

Defines how decisions are made and how change is controlled under the Project Operating System: who decides, what gates work must pass, how conflicts between documents are resolved, and how the governance documents themselves are amended. This is the **only** place decision rights and approval gates are defined.

## Scope

Decision-making and change control only. The principles being enforced are defined in [DesignPrinciples.md](DesignPrinciples.md); the authority classes used for conflict resolution are defined in [LayerModel.md](LayerModel.md).

## Decision rights

- **Owner.** Every project governed by the system has an owner who holds final approval authority. In this repository, the owner is the repository owner.
- **Participants.** All other participants — human engineers and AI agents alike — propose, implement, validate, and report. They do not approve their own work, and they do not amend authoritative documents without owner approval.
- **No self-promotion.** No participant may promote its own output past an approval gate.

## Approval gates

Applying Gated Progression ([DesignPrinciples.md](DesignPrinciples.md), P6), work advances through explicit gates:

1. **Scope gate.** Work begins only against an approved, explicitly scoped unit of work (a sprint). Work outside the approved scope is not performed.
2. **Validation gate.** Before a unit of work is reported complete, it is validated against its stated completion criteria and against the governance documents.
3. **Approval gate.** The owner reviews the reported result. Only owner approval completes the unit of work.
4. **Promotion.** Upon approval, the completed transition is promoted into the permanent record (the changelog in the Knowledge layer). Nothing enters the permanent record without passing all prior gates.

## Conflict resolution

- Precedence follows the authority order in [LayerModel.md](LayerModel.md): Governance, then Process, then State & Tracking, then Knowledge, then Contracts, then Execution. Supporting content has no precedence at all.
- A conflict between documents is a **defect**, not an interpretation choice. Whoever detects it must surface it explicitly to the owner; silently resolving, ignoring, or working around a conflict is prohibited (Explicit Authority, P5).
- Until a surfaced conflict is resolved by amendment, the higher-authority document governs.

## Amending governance

- Governance documents (this directory) change only by owner-approved amendment, passing the same gates as any other work (Architecture-First, P1).
- An amendment that changes a rule must update the rule's single home and leave references intact (Single Source of Truth, P2).
- The architecture as a whole is versioned; a change to the layer structure, dependency rules, or decision rights constitutes a new architecture version and must be recorded as such in the permanent record.

## Responsibilities

- Define who may approve what, and the gates every unit of work must pass.
- Define the precedence rule for conflicts and the obligation to surface them.
- Define the amendment procedure for authoritative documents, including this one.

## Relationship to other governance documents

- Enforces [DesignPrinciples.md](DesignPrinciples.md) — especially P1, P2, P5, and P6 — through concrete mechanisms.
- Uses the authority order from [LayerModel.md](LayerModel.md) and the reference rules from [DependencyModel.md](DependencyModel.md).
- Terms used here (owner, gate, promotion, sprint) are defined in [Terminology.md](Terminology.md).
