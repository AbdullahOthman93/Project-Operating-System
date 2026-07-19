# docs/standards — Knowledge layer: reusable standards

**Purpose:** Holds reusable engineering standards — the quality bar that applies across all work in this repository: testing, security, naming, and review conventions.

**Scope:** Reusable, stable standards only. Project-specific records (specs, ADRs, changelog) belong in `docs/knowledge/`, not here.

**Contents (Sprint 1.5 — Standards Foundation):**
- `StandardsModel.md` — entry point; what a standard is, catalog, deferred categories
- `DocumentationStandard.md` — structure, naming, and conventions of authoritative documents
- `ValidationStandard.md` — the canonical Validation-gate checklist
- `VersionControlStandard.md` — change-set discipline, completion publication, and history integrity

Testing and security standards are deferred until executable content exists (owner-ratified, Sprint 1.5); see `StandardsModel.md`.

Start with `StandardsModel.md`.

**Dependencies:** `docs/architecture/` and `docs/kernel/` — standards enforce what approval gates require.

**Related documents:**
- `docs/knowledge/INDEX.md`
- `docs/contracts/INDEX.md` — contracts must conform to these standards
