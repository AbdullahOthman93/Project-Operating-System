# Design Principles

## Purpose

Defines the canonical set of principles that constrain every design, documentation, and implementation decision made under the Project Operating System. This is the **only** place principles are defined; all other documents reference principles by name and must not restate or redefine them.

## Scope

Principles only — durable rules of judgement. Enforcement mechanisms (gates, decision rights) belong in [GovernanceModel.md](GovernanceModel.md); structural rules belong in [LayerModel.md](LayerModel.md) and [DependencyModel.md](DependencyModel.md).

## The Principles

### P1 — Architecture-First Development

No work is planned, implemented, or accepted except within an approved architecture. When work reveals that the architecture is wrong or incomplete, the architecture is amended first (per [GovernanceModel.md](GovernanceModel.md)); work does not silently diverge from it.

### P2 — Single Source of Truth

Every rule, definition, and decision has exactly one authoritative home. Other documents reference that home; they never duplicate its content. Duplication is treated as a defect, because divergence between copies is inevitable.

### P3 — Technology Agnosticism

Governance, process, standards, and contracts are expressed independently of any language, framework, vendor, platform, or tool. Technology-specific detail is confined to execution bindings and adapters at the edge of the system.

### P4 — Separation of Concerns

Each layer, directory, and document has one clearly bounded responsibility (see [LayerModel.md](LayerModel.md)). Content that belongs to another responsibility is moved or referenced, never absorbed.

### P5 — Explicit Authority

Every document is either authoritative or supporting, and says which it is. Supporting material (guidance, examples, procedures, bindings) never overrides authoritative material; conflicts are surfaced, not silently resolved (see [GovernanceModel.md](GovernanceModel.md)).

### P6 — Gated Progression

Work moves through explicit approval gates. Results become permanent record only after validation and approval; nothing is promoted implicitly.

### P7 — Incremental Development

The system grows in small, complete, approved increments. Each increment leaves the repository internally consistent and usable.

### P8 — Small Safe Changes

Individual changes are kept small enough to review fully and reverse cheaply. Large outcomes are reached through sequences of small changes, not single large ones.

### P9 — Create on Need

Structure, documents, and directories are created only when there is approved content for them. Nothing is scaffolded ahead of need.

### P10 — Reusability

Governance, process, standards, and contracts are written to be reusable across any software project, not just this repository. Project-specific detail is confined to the project's own records.

## Responsibilities

- Provide the canonical name, statement, and intent of every principle.
- Serve as the reference target whenever any document invokes a principle.

## Relationship to other governance documents

- Principles serve [Vision.md](Vision.md) and [Mission.md](Mission.md).
- [LayerModel.md](LayerModel.md) and [DependencyModel.md](DependencyModel.md) apply P2, P3, P4, and P5 structurally.
- [GovernanceModel.md](GovernanceModel.md) enforces the principles through gates and decision rights (P1, P5, P6).
- Terms used here are defined in [Terminology.md](Terminology.md).
