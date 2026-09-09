# docs/knowledge — Knowledge layer: project records

**Purpose:** Holds project-specific knowledge records for this repository's own self-hosted development: specifications, architecture decision records, and the permanent changelog.

**Scope:** Records specific to this repository only. Reusable standards belong in `docs/standards/`, not here.

**Contents:**
- Specs — none yet
- ADRs (including ADRs governing this repository's own architecture) — none yet
- `CHANGELOG.md` — permanent record of promoted state transitions; first entry: Sprint 1.1 completion
- `SelfHostingRelationshipReconciliation.md` — permanent reconciliation and validation report: this repository as the inaugural Project Governance Relationship (Sprint 3.4)
- `ClaudeCodeIntegrationDesign.md` — project-specific integration design record for applying the Claude Code adapter to this repository under the AI Governance Extension and AI Engineering Standard; defines no rule and authorizes no implementation (added under DAI-02 — Claude Code Integration Artifacts)
- `PilotEvidenceConsolidation.md` — Stage 5.5 dual-pilot evidence consolidation and assessment (FMFSLA and School ERP); owner-approved, READY FOR STAGE 6 WITH CONDITIONS; defines no rule and references originating-project evidence rather than duplicating it
- `Stage6ValidationOptimizationStrategy.md` — Stage 6.1 validation & optimization strategy: validation dimensions, minimal measurement baseline, optimization candidates, and gate mapping; owner-approved, READY FOR CONTROLLED STAGE 6 EXECUTION; defines no rule and creates no Work Unit or gate

Internal subdivision (e.g. separate `specs/`, `adrs/`, `changelog/` folders) will be introduced incrementally as content accumulates, rather than created ahead of need.

**Dependencies:** `docs/runtime/` (source of promoted state transitions), `docs/standards/` (records must conform to standards).

**Related documents:**
- `docs/runtime/INDEX.md`
- `docs/standards/INDEX.md`
