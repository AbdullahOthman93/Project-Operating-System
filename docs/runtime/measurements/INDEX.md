# docs/runtime/measurements — Measurement records

**Purpose:** Holds the Measurement Record **schema/template** and runtime-oriented guidance for measurement capture, within the State & Tracking layer ([../INDEX.md](../INDEX.md), [../StateModel.md](../StateModel.md)). Consistent with that layer, this directory holds conceptual/schema material only; it does **not** hold live mutable runtime state, and it is **not** a permanent store of completed historical records. A Measurement Record states what was observed for a Work Unit and **creates no governance authority** — no decision right, gate, precedence, or principle.

**Contents:**
- `MeasurementRecordTemplate.md` — the schema/template for a Work Unit measurement record. Copy it to create a record; the template itself holds no data.

**Lifecycle.** A Work Unit **uses** the template during measurement capture. A **completed or preserved** Measurement Record is historical project evidence and belongs in [`docs/knowledge/`](../../knowledge/INDEX.md) — not here. This directory is limited to the template/schema and runtime-oriented guidance; completed records are not retained in it. None exists yet.

**Governing measurement method (canonical):** The Stage 6 measurement baseline in [../../knowledge/Stage6ValidationOptimizationStrategy.md](../../knowledge/Stage6ValidationOptimizationStrategy.md) (§4) governs which measurements are taken and how; the telemetry-boundary rule (agent-observable / host-observable / derived analysis, and the NOT AVAILABLE state) is owned by [../../standards/AIEngineeringStandard.md](../../standards/AIEngineeringStandard.md) (Requirement 10). This directory applies that method and does not redefine it.

**Dependencies:** `docs/runtime/` (State & Tracking concepts), `docs/knowledge/` and `docs/standards/` (the governing measurement method above).

**Related documents:**
- `docs/runtime/INDEX.md`
- `docs/knowledge/Stage6ValidationOptimizationStrategy.md`
- `docs/standards/AIEngineeringStandard.md`
