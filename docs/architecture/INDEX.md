# docs/architecture — Governance layer

**Purpose:** Defines the Governance layer of Architecture v1.0 — the principles, approval gates, and decision rights that constrain every other part of this repository.

**Scope:** Technology-agnostic rules only. This directory must never reference a specific language, framework, vendor, or tool.

**Contents (Sprint 1.2 — Governance Foundation):**
- `ArchitectureOverview.md` — entry point; architecture summary, logical-to-physical mapping, reading order
- `Vision.md` — the enduring end state the system exists to bring about
- `Mission.md` — what the system delivers, its boundaries, and self-hosting
- `DesignPrinciples.md` — the canonical principles (P1–P10)
- `LayerModel.md` — logical layers, responsibilities, authority classes
- `DependencyModel.md` — allowed dependency and reference rules between layers
- `GovernanceModel.md` — decision rights, approval gates, conflict resolution, amendment
- `Terminology.md` — canonical vocabulary

Start with `ArchitectureOverview.md`.

**Dependencies:** None. This is the top of the internal dependency order — nothing here depends on any other part of the repository.

**Related documents:**
- `docs/kernel/INDEX.md` — Process, which operates within the rules defined here
- `docs/contracts/INDEX.md` — contracts derive their requirements from this layer
