# docs/kernel — Process layer

**Purpose:** Defines the Process layer — the workflow library and phase-gate definitions that govern how work moves through this repository.

**Scope:** Ordering, gating, and workflow selection only. This directory never defines what tool executes a step — that belongs in `tools/` and `docs/contracts/`.

**Contents (Sprint 1.3 — Process Kernel):**
- `ProcessModel.md` — entry point; what a workflow is, structure and catalog of this layer
- `SprintLifecycle.md` — the canonical sprint workflow, definition through atomic closeout
- `PhaseModel.md` — phase composition, entry and exit gating
- `ChangeAndConflictWorkflow.md` — amendment and conflict-surfacing procedures
- `ProjectAdoptionWorkflow.md` — the Project Adoption workflow: the establishing transition bringing a project into a Project Governance Relationship (added Sprint 3.2)

Start with `ProcessModel.md`.

**Dependencies:** `docs/architecture/` — Process operates within Governance's rules.

**Related documents:**
- `docs/architecture/INDEX.md`
- `docs/runtime/INDEX.md` — Process defines what states are valid
