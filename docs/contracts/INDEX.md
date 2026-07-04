# docs/contracts — Formal execution and agent contracts

**Purpose:** Holds the formal, checkable interfaces that execution participants must satisfy — the Execution Contract (for tool adapters) and the Agent Interaction Contract (for AI agents). This is the single source of truth for those interfaces.

**Scope:** Formal contract definitions only. `docs/agents/` may reference these contracts but must never restate or duplicate their requirements.

**Contents (to be populated in later sprints):**
- Execution Contract
- Agent Interaction Contract

**Dependencies:** `docs/architecture/` (approval gates), `docs/standards/` (contract requirements derive from standards).

**Related documents:**
- `docs/agents/INDEX.md`
- `tools/` — adapters implementing these contracts
- `.claude/` and `CLAUDE.md` — execution bindings governed by the Agent Interaction Contract
