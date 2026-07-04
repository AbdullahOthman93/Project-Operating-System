# Terminology

## Purpose

Defines the canonical vocabulary of the Project Operating System. Every document in this repository uses these terms with exactly these meanings. This is the **only** place terms are defined; no other document may redefine them.

## Scope

Term definitions only. Where a concept has a fuller authoritative treatment elsewhere (a principle, a layer, a mechanism), the entry here gives the short canonical meaning and points to the owning document rather than restating its content.

## Terms

**Agent** — an AI participant working under the system. Bound by the agent contract in the Contracts layer; guided (non-bindingly) by agent guidance material.

**Approval gate** — an explicit checkpoint that work must pass before advancing. Gates are defined in [GovernanceModel.md](GovernanceModel.md).

**Architecture version** — the approved, versioned whole formed by the governance documents. Changes to it are governed by the amendment procedure in [GovernanceModel.md](GovernanceModel.md).

**Authoritative document** — a document whose content is binding within its layer's responsibility. Authority classes are defined in [LayerModel.md](LayerModel.md).

**Baseline** — an approved repository state that subsequent work builds on and must not silently alter.

**Contract** — a formal, checkable interface a participant must satisfy; defined in the Contracts layer ([LayerModel.md](LayerModel.md)).

**Execution binding** — a technology-specific artifact that connects a participant or tool to the system (for example, an agent configuration file). Bindings conform to contracts and hold no authority of their own.

**Governance document** — one of the authoritative documents in the Governance layer (this directory).

**Layer** — a logical unit of the architecture with a single bounded responsibility and an authority class; defined in [LayerModel.md](LayerModel.md).

**Owner** — the holder of final approval authority for a project; defined in [GovernanceModel.md](GovernanceModel.md).

**Participant** — any human or AI actor performing work under the system.

**Phase** — a major stage of a project, composed of sprints.

**Principle** — a named, durable rule of judgement; the canonical set lives in [DesignPrinciples.md](DesignPrinciples.md) and principles are cited by their identifiers (P1–P10).

**Process** — the Process layer: workflows and phase gates ([LayerModel.md](LayerModel.md)).

**Promotion** — the act of recording an approved state transition in the permanent record; part of the gate sequence in [GovernanceModel.md](GovernanceModel.md).

**Self-hosting** — the arrangement in which this repository is itself governed by the framework it defines; stated in [Mission.md](Mission.md).

**Sprint** — the smallest approved, explicitly scoped unit of work; it passes the gates in [GovernanceModel.md](GovernanceModel.md) as a whole.

**State record** — a live tracking artifact reflecting current, transient project status. State records are never a permanent record and never live in documentation of the State & Tracking layer.

**Supporting document** — a document that assists participants but binds nothing; see authority classes in [LayerModel.md](LayerModel.md).

## Responsibilities

- Provide the single canonical definition of every shared term.
- Point each term to the document that owns its fuller treatment, where one exists.

## Relationship to other governance documents

Every governance document uses this vocabulary. Entries here deliberately stay short and defer to [DesignPrinciples.md](DesignPrinciples.md), [LayerModel.md](LayerModel.md), [DependencyModel.md](DependencyModel.md), and [GovernanceModel.md](GovernanceModel.md) for full treatment, per Single Source of Truth (P2).
