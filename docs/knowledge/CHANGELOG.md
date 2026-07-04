# Changelog

Permanent record of promoted state transitions. Entries are added only by Process, upon completion and approval of a sprint (Sprint 0.2 promotion rule).

## Sprint 1.4 — State & Tracking Foundation
- **Status:** Completed and approved
- **Summary:** State & Tracking layer populated: three concept/schema documents created in `docs/runtime/` (StateModel, StateTransitionModel, TrackingArtifacts) defining the live/permanent record boundary, the canonical status vocabulary and allowed transitions for sprints and phases, the promotion entry schema, and the schemas and update rules of the live tracking artifacts. `docs/runtime/INDEX.md` updated to list them. No live state stored in the layer; dependencies point to Governance and Process only. Existing tracking artifacts retro-validated against the schemas and found conforming.
- **Approved by:** repository owner (implementation and closeout pre-authorized with the Sprint 1.4 design approval)

## Sprint 1.3 — Process Kernel
- **Status:** Completed and approved
- **Summary:** Process layer populated: four kernel documents created in `docs/kernel/` (ProcessModel, SprintLifecycle, PhaseModel, ChangeAndConflictWorkflow) operationalizing the Governance Foundation's gates as procedure — the atomic sprint lifecycle, phase composition and gating, and amendment/conflict-surfacing workflows. `docs/kernel/INDEX.md` updated to list them. All dependencies point to the Governance layer only, per the approved dependency model.
- **Approved by:** repository owner (implementation and closeout pre-authorized with the Sprint 1.3 design approval)

## Sprint 1.2 — Governance Foundation
- **Status:** Completed and approved
- **Summary:** Governance layer populated: eight authoritative documents created in `docs/architecture/` (Vision, Mission, DesignPrinciples P1–P10, ArchitectureOverview, LayerModel, DependencyModel, GovernanceModel, Terminology), each with a unique responsibility and single-home definitions per Single Source of Truth. `docs/architecture/INDEX.md` updated to list them. These documents are now the authoritative architectural reference; future documentation references them rather than redefining governance concepts.
- **Approved by:** repository owner, prior turn

## Sprint 1.1 — Repository Initialization
- **Status:** Completed and approved
- **Summary:** Physical repository structure initialized per Architecture v1.0 and the approved repository layout (root files, `.claude/`, `.github/`, `docs/` with ten indexed subdirectories, `tools/`). `src/` intentionally not created. All `docs/` subdirectories carry an `INDEX.md` covering Purpose, Scope, Contents, Dependencies, and Related Documents.
- **Approved by:** repository owner, prior turn
