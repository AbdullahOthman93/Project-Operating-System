# Layer Model

## Purpose

Defines the logical layers of the Project Operating System: what each layer is responsible for, what it must not contain, and whether it is authoritative or supporting. This is the **only** place layers are defined.

## Scope

Layer identity, responsibility, and authority class only. How layers may depend on and reference one another is defined in [DependencyModel.md](DependencyModel.md). Where each layer physically lives in this repository is mapped in [ArchitectureOverview.md](ArchitectureOverview.md).

## Authority classes

Applying the Explicit Authority principle ([DesignPrinciples.md](DesignPrinciples.md), P5), every layer is one of:

- **Authoritative** — its documents define binding rules within the layer's responsibility.
- **Supporting** — its documents assist participants but bind nothing; they must never restate or override authoritative content.

## Authoritative layers

Listed from highest authority downward.

### 1. Governance

Defines the principles, models, decision rights, and vocabulary that constrain everything else. Depends on nothing inside the repository. Contains only technology-agnostic, project-independent rules.

### 2. Process

Defines the workflow library and phase-gate definitions — how work moves from intent to accepted result. Process operates within Governance's rules. It defines the ordering and gating of work, never which tool executes a step.

### 3. State & Tracking

Defines what a valid state record is and how state transitions are governed, including promotion of completed transitions into permanent record. This layer holds concepts and schemas only; live, mutable state is never stored in its documentation.

### 4. Knowledge

The accumulated output of governed work, in two distinct forms with distinct homes:

- **Reusable standards** — the quality bar (testing, security, naming, review conventions) applied across all work. Standards enforce what approval gates require.
- **Project records** — specifications, architecture decision records, and the permanent changelog specific to one project.

Reusable material and project-specific material must never be mixed (Reusability, P10).

### 5. Contracts

Defines the formal, checkable interfaces any executing participant — tool adapter or AI agent — must satisfy to work under the system. Contracts are the single source of truth for participant obligations.

### 6. Execution

The technology-facing edge: tool adapters and agent bindings that implement the Contracts. Execution is where technology-specific detail is permitted (Technology Agnosticism, P3). Execution artifacts carry no documentation authority; they conform to Contracts, never extend them.

## Supporting layers

Supporting content assists but never binds:

- **Agent guidance** — profiles and operational notes for AI agents; the binding agent interface lives exclusively in Contracts.
- **Operating procedures** — cross-cutting day-to-day procedures not owned by any single authoritative layer.
- **Templates** — structural scaffolding for recurring document types.
- **Examples** — illustrative, worked material for onboarding.

## Responsibilities

- Provide the canonical definition, responsibility boundary, and authority class of every layer.
- Serve as the reference target whenever any document names a layer.

## Relationship to other governance documents

- Applies [DesignPrinciples.md](DesignPrinciples.md) P3, P4, P5, and P10 structurally.
- [DependencyModel.md](DependencyModel.md) defines the allowed relationships between the layers defined here.
- [GovernanceModel.md](GovernanceModel.md) uses the authority classes defined here for conflict resolution.
- Layer names are part of the canonical vocabulary in [Terminology.md](Terminology.md), which points back to this document.
