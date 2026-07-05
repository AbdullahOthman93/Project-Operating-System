# docs/templates — Document templates

**Purpose:** Holds document templates that ensure consistent structure for the recurring document types across this repository.

**Scope:** Templates only — non-authoritative structural scaffolding, not content or rules. A template reproduces the structure its owning document requires and defines nothing itself.

**Contents:**
- `AuthoritativeDocumentTemplate.md` — skeleton for a new authoritative document.
- `SprintDesignTemplate.md` — skeleton for a sprint design.
- `ChangelogEntryTemplate.md` — skeleton for a promotion (changelog) entry.
- `DirectoryIndexTemplate.md` — skeleton for a directory `INDEX.md`.

Deferred under Create on Need (P9), pending the first document of each type: Specification, ADR, and Standard templates.

**Dependencies:** None as an authority. As a Supporting directory, its templates *reference* the authoritative documents whose structure they scaffold — reference only, per the Dependency Model (rule 5): `docs/standards/` (DocumentationStandard, ValidationStandard, VersionControlStandard), `docs/kernel/` (SprintLifecycle), `docs/runtime/` (StateTransitionModel), and `docs/architecture/` (DesignPrinciples, DependencyModel). No document depends on this directory.

**Related documents:**
- `docs/standards/INDEX.md`
- `docs/kernel/INDEX.md`
- `docs/runtime/INDEX.md`
- `docs/knowledge/INDEX.md`
