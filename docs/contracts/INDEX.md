# docs/contracts — Formal participant and execution contracts

**Purpose:** Holds the formal, checkable interfaces that participants must satisfy — the Participant Contract (for human and AI participants) and, when need arises, the Execution Contract (for tool adapters). This is the single source of truth for those interfaces.

**Scope:** Formal contract definitions only. `docs/agents/` may reference these contracts but must never restate or duplicate their requirements.

**Contents (Sprint 1.6 — Contracts Foundation):**
- `ContractModel.md` — entry point; what a contract is, how bindings relate to contracts, catalog
- `ParticipantContract.md` — checkable obligations of any participant, human or AI

The Execution Contract is deferred until a tool adapter or automation exists (owner-ratified, Sprint 1.6); see `ContractModel.md`.

Start with `ContractModel.md`.

**Dependencies:** `docs/architecture/` (approval gates), `docs/standards/` (contract requirements derive from standards).

**Related documents:**
- `docs/agents/INDEX.md`
- `tools/` — adapters implementing these contracts
- `.claude/` and `CLAUDE.md` — execution bindings governed by the Participant Contract
