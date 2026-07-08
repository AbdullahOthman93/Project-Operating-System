# Changelog

Permanent record of promoted state transitions. Entries are added only by Process, upon completion and approval of a sprint (Sprint 0.2 promotion rule).

## Sprint 3.1 — Project Governance Relationship Concept
- **Status:** Completed and approved
- **Summary:** Governance layer extended with the framework's fundamental concept. One new authoritative document, `docs/architecture/ProjectGovernanceRelationship.md`, defines the **Project Governance Relationship** (owner, bound architecture, origin baseline, forward gating) as the long-lived concept under which a project is governed; the **governed project** as a status conferred by that relationship; **when governance begins** (the discrete, prospective point of adoption, which never retroactively validates prior history); the **origin baseline** (accepted as the trusted origin of the permanent record, on the owner's established determination — AR-001 §5 — that a baseline is *accepted as an origin*, not *implemented under the architecture*), carrying a recorded **conformance posture**; **Project Adoption** as the establishing transition (concept only — no workflow, stage, or gate, those owned by the Process layer); and **greenfield/brownfield** as two origin conditions of one concept. `Mission.md` self-hosting framing generalized: this repository is the **inaugural** relationship under a greenfield origin condition, not the limit of applicability. `Terminology.md` gained five canonical terms (Governed project, Origin baseline, Origin condition, Project Adoption, Project Governance Relationship), each a short meaning pointing to the new owning document. `ArchitectureOverview.md` (summary bullet and reading order) and `docs/architecture/INDEX.md` updated to include the new document. No workflow, lifecycle, state schema, gate, decision right, layer, or dependency rule was introduced or changed; the versioning check confirms **Architecture remains v1.0**. Single Source of Truth preserved (concepts defined once, referenced elsewhere) and all authority references remain within the Governance layer (Dependency Model rules 1–2). Non-blocking observations surfaced to the owner: `README.md` and `docs/examples/SprintWalkthrough.md` retain "first project governed" phrasing (consistent with "inaugural", not contradictory, left unedited as out of scope); and whether `DesignPrinciples.md` P1 should carry an explicit cross-reference to the origin-baseline determination is left to the owner. First sprint of Phase 3 — Governed Project Enablement.
- **Approved by:** repository owner (implementation and closeout pre-authorized with the Sprint 3.1 implementation authorization)

## Phase 2 — Operational Enablement
- **Status:** Closed and approved
- **Summary:** Phase 2 objective achieved — Operational Enablement: the four supporting layers needed to operate the framework populated across sprints 2.1–2.4 — Templates (`docs/templates/`, 2.1), Agent Guidance (`docs/agents/`, 2.2), Operating Procedures (`docs/operations/`, 2.3), and the self-hosting Worked Example & Onboarding (`docs/examples/`, 2.4). All content is non-authoritative and reference-only: no authority was added to any supporting layer, no authoritative or Execution layer was modified, and Architecture remains v1.0. Every supporting-layer `INDEX.md` declares its reference-only sources per Dependency Model rules 5 and 7, and no document depends on any supporting layer. The worked example uses this repository's own real history rather than any fabricated project, demonstrating the framework governing itself. Deferrals remain owner-ratified under Create on Need (P9): Specification, ADR, and Standard templates; and standalone validation, version-control, and state-update procedures. Phase status transitions Open → Closed; no phase is open following closure and no Phase 3 is approved. Per the owner-ratified Stage 7.1 interpretation, the final sprint created no next sprint row.
- **Approved by:** repository owner, following authorization of the Phase 2 exit gate

## Sprint 2.4 — Self-Hosting Worked Example & Onboarding
- **Status:** Completed and approved
- **Summary:** Examples supporting layer populated: two non-authoritative documents created in `docs/examples/` — `OnboardingGuide.md` (a "start here" path leading a new participant through Vision/Mission, Design Principles, the architecture entry point, the Participant Contract, the governance gates and sprint lifecycle, and the operating runbook, entirely by reference) and `SprintWalkthrough.md` (a worked example following one real, already-closed sprint — Sprint 2.1 — Templates Foundation — end to end, drawn from the permanent record and version-control history, citing commit `c754f59`). No project or record was fabricated; the self-hosting example uses this repository's own real history, with the walkthrough explicitly marked a historical illustration and not live status. `docs/examples/INDEX.md` updated to list both documents and declare its reference-only sources across all other `docs/` areas (Dependency Model rule 5, conformance references rule 7), with no document depending on the directory. No authority introduced; no authoritative or Execution layer modified. Per the owner-ratified Stage 7.1 interpretation for the final sprint of a phase, no new sprint row was created and the live state now points to the Phase 2 exit gate only. Fourth and final sprint of Phase 2 — Operational Enablement.
- **Approved by:** repository owner (implementation and closeout pre-authorized with the Sprint 2.4 implementation authorization)

## Sprint 2.3 — Operating Procedures Foundation
- **Status:** Completed and approved
- **Summary:** Operating Procedures supporting layer populated: one non-authoritative, reference-only document created in `docs/operations/` — `SprintExecutionRunbook.md`, a practical checklist for carrying out a sprint end-to-end in this repository. For each stage it points at the authoritative document that governs it (`SprintLifecycle.md`, `GovernanceModel.md`) and names the concrete artifact or tool touched (`PROJECT_STATE.md`, `ExecutionPlan.md`, `docs/knowledge/CHANGELOG.md`, the version-control change set); it defines no workflow, stage, gate, or rule and is explicitly subordinate to the Process layer, preserving Single Source of Truth (P2) and the operations-layer scope rule that it must not duplicate or override `docs/kernel/`. `docs/operations/INDEX.md` updated to list the runbook and declare its reference-only sources across the Process, Governance, Standards, and State & Tracking layers (Dependency Model rule 5, conformance references rule 7), with no document depending on the directory. Standalone validation, version-control, and state-update procedures deferred under Create on Need (P9). No new workflow, gate, or authority introduced; no authoritative layer modified; no execution technology introduced. Third sprint of Phase 2 — Operational Enablement.
- **Approved by:** repository owner (implementation and closeout pre-authorized with the Sprint 2.3 implementation authorization)

## Sprint 2.2 — Agent Guidance Foundation
- **Status:** Completed and approved
- **Summary:** Agent Guidance supporting layer populated: two non-authoritative documents created in `docs/agents/` — `ClaudeAgentProfile.md` (profile of the AI agent that works in this repository through the `CLAUDE.md` binding) and `OperationalNotes.md` (navigation aid orienting an agent to the authoritative documents that govern the work). Both reach every obligation, gate, standard, and schema by reference to its owning document and restate none, preserving Single Source of Truth (P2); the formal agent interface remains exclusively in `docs/contracts/`. `docs/agents/INDEX.md` updated to list the two documents and to declare its reference-only sources across the Contracts, Process, Governance, Standards, and State & Tracking layers (Dependency Model rule 5, conformance references rule 7), with no document depending on the directory. No authority added to the supporting layer; no authoritative layer modified; no execution technology introduced. Second sprint of Phase 2 — Operational Enablement.
- **Approved by:** repository owner (implementation and closeout pre-authorized with the Sprint 2.2 implementation authorization)

## Sprint 2.1 — Templates Foundation
- **Status:** Completed and approved
- **Summary:** Templates supporting layer populated: four non-authoritative document templates created in `docs/templates/` (`AuthoritativeDocumentTemplate.md`, `SprintDesignTemplate.md`, `ChangelogEntryTemplate.md`, `DirectoryIndexTemplate.md`), each a fill-in skeleton that references its owning document and defines nothing itself. `docs/templates/INDEX.md` updated to list them and to declare its reference-only sources across the Standards, Process, State & Tracking, and Governance layers (Dependency Model rule 5). Specification, ADR, and Standard templates deferred under Create on Need (P9), pending the first document of each type. No authority added to the supporting layer; no execution technology introduced. First sprint of Phase 2 — Operational Enablement.
- **Approved by:** repository owner (implementation and closeout pre-authorized with the Sprint 2.1 implementation authorization)

## Phase 1 — Repository Setup
- **Status:** Closed and approved
- **Summary:** Phase 1 objective achieved — the physical repository and all six authoritative layers of Architecture v1.0 populated across sprints 1.1–1.7: repository structure (1.1), Governance (`docs/architecture/`, 1.2), Process (`docs/kernel/`, 1.3), State & Tracking (`docs/runtime/`, 1.4), Knowledge — standards (`docs/standards/`, 1.5), Contracts (`docs/contracts/`, 1.6), and Execution bindings aligned to the Contracts layer (`CLAUDE.md`, `.claude/`, `.github/`, `tools/`, 1.7). Amendments 1 and 2 incorporated. Every Dependency Model row is exercised, Single Source of Truth is preserved, no drift or open defect remains, and no authority resides in the Execution layer. Phase status transitions Open → Closed; no phase is open following closure. Deferrals (Execution Contract; testing and security standards) remain owner-ratified and recorded in their owning layers.
- **Approved by:** repository owner, following the accepted Phase 1 Gate Review (Architecture v1.0 Completion Assessment)

## Sprint 1.7 — Execution Binding Alignment
- **Status:** Completed and approved
- **Summary:** Execution layer aligned to the Contracts layer: `CLAUDE.md` and `.claude/NOTES.md` rewritten as pure rule-6 bindings naming the Participant Contract as their single governing interface; `.github/NOTES.md` and `tools/NOTES.md` reworded to state the Execution Contract deferral truthfully via `ContractModel.md`. No new files, no new capability, no automation, no Execution Contract (per approved design). The Sprint 1.6 drift finding is resolved. Architecture v1.0 is now populated end-to-end with every dependency row exercised as designed.
- **Approved by:** repository owner (implementation and closeout pre-authorized with the Sprint 1.7 design approval)

## Sprint 1.6 — Contracts Foundation
- **Status:** Completed and approved
- **Summary:** Contracts layer populated: `ContractModel.md` (what a contract is, how bindings relate to contracts, catalog) and `ParticipantContract.md` (checkable obligations of any participant, human or AI, generalized from the originally planned agent-specific contract by owner-approved evaluation) created in `docs/contracts/`; `docs/contracts/INDEX.md` updated. The Execution Contract deferred until a tool adapter or automation exists (owner-ratified). All six authoritative layers of Architecture v1.0 are now populated. Known drift: execution bindings (`CLAUDE.md`, `.claude/NOTES.md`) still name the superseded "Agent Interaction Contract" — dispositioned to Sprint 1.7 binding alignment.
- **Approved by:** repository owner (implementation and closeout pre-authorized with the updated Sprint 1.6 design approval)

## Amendment 2 — Participant Contract Naming (Terminology)
- **Status:** Completed and approved
- **Summary:** The *Agent* entry in `docs/architecture/Terminology.md` updated from "bound by the agent contract" to "bound by the participant contract", following the owner-approved generalization of the contract to all participants. Applied within the Sprint 1.6 change set. No layer, dependency rule, or decision right changed — Architecture remains v1.0.
- **Approved by:** repository owner, prior turn

## Amendment 1 — Validation References Clarification (DependencyModel)
- **Status:** Completed and approved
- **Summary:** Rule 7 added to `docs/architecture/DependencyModel.md`: validation references used solely for conformance verification do not constitute architectural dependencies; the allowed-dependencies table expresses authority dependencies only. Resolves the finding surfaced during Sprint 1.5 validation (ValidationStandard's citation of runtime schemas as check-subjects). No allowed relationship, layer, or decision right changed — Architecture remains v1.0.
- **Approved by:** repository owner, prior turn

## Sprint 1.5 — Standards Foundation
- **Status:** Completed and approved
- **Summary:** Standards layer populated: four reusable standards created in `docs/standards/` (StandardsModel, DocumentationStandard, ValidationStandard, VersionControlStandard) codifying the quality bar exercised at the Validation gate — document structure and naming, the canonical validation checklist, and change-set discipline. `docs/standards/INDEX.md` updated. Testing and security standards deferred until executable content exists (owner-ratified with the design). Existing corpus retro-validated against the new standards.
- **Approved by:** repository owner (implementation and closeout pre-authorized with the Sprint 1.5 design approval)

## Sprint 1.4 — State & Tracking Foundation
- **Status:** Completed and approved
- **Summary:** State & Tracking layer populated: three concept/schema documents created in `docs/runtime/` (StateModel, StateTransitionModel, TrackingArtifacts) defining the live/permanent record boundary, the canonical status vocabulary and allowed transitions for sprints and phases, the promotion entry schema, and the schemas and update rules of the live tracking artifacts. `docs/runtime/INDEX.md` updated to list them. No live state stored in the layer; dependencies point to Governance and Process only. Existing tracking artifacts retro-validated against the schemas and found conforming.
- **Approved by:** repository owner (implementation and closeout pre-authorized with the Sprint 1.4 design approval)

## Sprint 1.3 — Process Kernel
- **Status:** Completed and approved
- **Summary:** Process layer populated: four kernel documents created in `docs/kernel/` (ProcessModel, SprintLifecycle, PhaseModel, ChangeAndConflictWorkflow) operationalizing the Governance Foundation's gates as procedure — the atomic sprint lifecycle, phase composition and gating, and amendment/conflict-surfacing workflows. `docs/kernel/INDEX.md` updated to list them. All dependencies point to the Governance layer only, per the approved dependency model.
- **Approved by:** repository owner (implementation and closeout pre-authorized with the Sprint 1.3 design approval)

## Sprint 1.2 — Governance Foundation
- **Status:** Completed and approved
- **Summary:** Governance layer populated: eight authoritative documents created in `docs/architecture/` (Vision, Mission, DesignPrinciples P1–P10, ArchitectureOverview, LayerModel, DependencyModel, GovernanceModel, Terminology), each with a unique responsibility and single-home definitions per Single Source of Truth. `docs/architecture/INDEX.md` updated to list them. These documents are now the authoritative architectural reference; future documentation references them rather than redefining governance concepts.
- **Approved by:** repository owner, prior turn

## Sprint 1.1 — Repository Initialization
- **Status:** Completed and approved
- **Summary:** Physical repository structure initialized per Architecture v1.0 and the approved repository layout (root files, `.claude/`, `.github/`, `docs/` with ten indexed subdirectories, `tools/`). `src/` intentionally not created. All `docs/` subdirectories carry an `INDEX.md` covering Purpose, Scope, Contents, Dependencies, and Related Documents.
- **Approved by:** repository owner, prior turn
