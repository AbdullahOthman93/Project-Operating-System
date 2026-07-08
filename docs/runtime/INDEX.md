# docs/runtime — State & Tracking layer (concepts only)

**Purpose:** Documents the State & Tracking layer concepts — what a valid state record is and how state transitions are governed.

**Scope:** Conceptual and schema documentation only. **Live, mutable runtime state must never be stored here** (Sprint 0.3, refinement 5).

**Contents (Sprint 1.4 — State & Tracking Foundation):**
- `StateModel.md` — entry point; state concepts and the live/permanent boundary
- `StateTransitionModel.md` — canonical status vocabulary, allowed transitions, promotion entry schema
- `TrackingArtifacts.md` — schemas and update rules of the live tracking artifacts

Extended in Sprint 3.3 to represent a governed project's origin baseline, establishing transition (Project Adoption), and conformance posture.

Start with `StateModel.md`.

**Dependencies:** `docs/kernel/` — Process defines what states are valid.

**Related documents:**
- `docs/kernel/INDEX.md`
- `docs/knowledge/INDEX.md` — promoted state transitions become permanent records there
