# docs/operations — Cross-cutting operating procedures

**Purpose:** Documents day-to-day repository operating procedures that are cross-cutting and not specific to any single logical layer.

**Scope:** Practical, procedural guidance only. This directory holds no governance, process, or state authority — content here must not duplicate or override `docs/architecture/`, `docs/kernel/`, or `docs/runtime/`.

**Contents:**
- `SprintExecutionRunbook.md` — non-authoritative, reference-only checklist for carrying out a sprint end-to-end in this repository; points at the authoritative document governing each step and names the concrete artifact or tool touched, defining nothing itself.

Deferred under Create on Need (P9), pending demonstrated need beyond the runbook: standalone validation, version-control, and state-update procedures.

**Dependencies:** None as an authority. As a Supporting directory, its procedures *reference* the authoritative layers for compliance — reference only, per the Dependency Model (rule 5), and conformance references per rule 7: `docs/kernel/` (the workflows carried out), `docs/architecture/` (gates, principles, layer and dependency rules), `docs/standards/` (ValidationStandard, VersionControlStandard), and `docs/runtime/` (state schemas and the live tracking artifacts). It also references `docs/templates/` scaffolding and cross-links `docs/agents/`. No document depends on this directory.

**Related documents:**
- `docs/architecture/INDEX.md`
- `docs/kernel/INDEX.md`
