# docs/agents — Agent profiles and operational guidance

**Purpose:** Holds agent profiles and operational guidance for AI agents working in this repository.

**Scope:** Supplementary, non-authoritative guidance only. The formal agent interface lives exclusively in `docs/contracts/` — this directory must never restate or override it.

**Contents:**
- `ClaudeAgentProfile.md` — profile of the AI agent that works in this repository through the `CLAUDE.md` binding; points to its obligations and process, restating none.
- `OperationalNotes.md` — non-authoritative navigation aid orienting an agent to the authoritative documents that govern the work.

**Dependencies:** None as an authority. As a Supporting directory, its documents *reference* the authoritative layers for guidance — reference only, per the Dependency Model (rule 5), and conformance references per rule 7: `docs/contracts/` (source of truth for the agent interface), `docs/kernel/`, `docs/architecture/`, `docs/standards/`, and `docs/runtime/`. It also references `docs/templates/` scaffolding. No document depends on this directory.

**Related documents:**
- `docs/contracts/INDEX.md`
- `CLAUDE.md`
- `.claude/NOTES.md`
