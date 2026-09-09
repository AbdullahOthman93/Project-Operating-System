# Stage 6 — Validation & Optimization Strategy

- **Stage:** 6.1 — Validation & Optimization Strategy
- **Status:** APPROVED — READY FOR CONTROLLED STAGE 6 EXECUTION
- **Approved by:** Project Owner (PASS with minor correction, applied)
- **Nature:** Strategy definition only. Creates no Work Unit, sprint, phase, gate, or roadmap entry; authorizes no Stage 6 execution.

> **Owner-approved strategy record.** This defines *how* Stage 6 will validate and optimize the AI Engineering Standard and Claude Code integration model in real project operation, strictly from Stage 5 evidence, and has been reviewed and approved by the Project Owner. It defines no rule and grants no authority; it uses the existing gates of [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md) and the checkable requirements of [../standards/AIEngineeringStandard.md](../standards/AIEngineeringStandard.md). Approval of this strategy does **not** start Stage 6 execution: the execution-entry conditions in §13 remain owner-controlled. Where it appears to conflict with an authoritative document, that document governs and the conflict is surfaced per [../kernel/ChangeAndConflictWorkflow.md](../kernel/ChangeAndConflictWorkflow.md).

## 1. Stage 6 objective

Validate and optimize the AI Engineering Standard and Claude Code integration model as exercised in real project operation, answering: did the operating model produce the intended **quality**; were **governance controls** effective; were **Work Units** appropriately bounded; was **context management** effective; was **verification** sufficient; was **human review** appropriately placed; was **Git/delivery** discipline effective; where did **unnecessary effort** occur; what **quantitative measurements** are now required; and what should be **optimized without weakening governance**. The optimization target is **quality-adjusted efficiency** (outcome relative to effort/context/model/tools/rework), never token reduction.

The concrete validation targets are the **ten checkable conformance requirements** of [../standards/AIEngineeringStandard.md](../standards/AIEngineeringStandard.md) (task classification; minimum-sufficient context; model routing; effort routing; planning; scope; parallelization; single-purpose sessions; verification-before-complete; evidence) plus the economy bar of [../standards/WorkEconomyStandard.md](../standards/WorkEconomyStandard.md).

## 2. Stage 5 baseline

Primary source: the promoted [PilotEvidenceConsolidation.md](PilotEvidenceConsolidation.md) (Stage 5.5, owner-approved). Originating evidence referenced there, not duplicated here:

- **Pilot A — FMFSLA, WU-5.3A-01:** a promoted documentation-reconciliation Work Unit (commit `4ee945b`, `HEAD==origin/main`), under a POS adoption-by-reference binding; demonstrated scope discipline and full Git completion.
- **Pilot B — School ERP, WU-5.3B-01:** an owner-**CLOSED** reverse-engineering trace with strong evidence traceability (file:line anchors, fact/inference/unknown separation), held in the git-ignored legacy tree.

Baseline limits carried forward (Stage 5 §9): **no quantitative measurements** were captured (C1); the Pilot A **WU-to-commit linkage** is conversation-recorded, not repository-stated (C2); the sample is **n=2 Work Units of deliberately different types**. Stage 5 history is not rewritten and no missing evidence is invented.

## 3. Validation dimensions

| Dim | Validates | Primary owner reference |
|---|---|---|
| A. Quality | Final outcome meets Work Unit completion criteria | Scope/Approval gate ([../architecture/GovernanceModel.md](../architecture/GovernanceModel.md)) |
| B. Correctness | Factual/technical correctness of AI output | Verification req. 9 ([../standards/AIEngineeringStandard.md](../standards/AIEngineeringStandard.md)) |
| C. Scope | Adherence to approved Work Unit boundaries | Scope gate; req. 6 |
| D. Verification | Verification sufficient and effective for task risk | req. 9; [../standards/ValidationStandard.md](../standards/ValidationStandard.md) |
| E. Evidence | Evidence quality and traceability | req. 10 |
| F. Human control | Review, approval, promotion boundaries preserved | Approval/Promotion gates; [../contracts/ParticipantContract.md](../contracts/ParticipantContract.md) |
| G. Context | Size, relevance, session discipline, unnecessary exploration | req. 2, 8; [../standards/WorkEconomyStandard.md](../standards/WorkEconomyStandard.md) |
| H. Model/effort routing | Choices appropriate to complexity/risk where observable | req. 3, 4 |
| I. Rework | Avoidable rework measured | Work Economy Standard |
| J. Intervention | Meaningful human intervention measured | Participant Contract (faithful reporting) |
| K. Delivery | Commit/push/completion discipline where applicable | [../standards/VersionControlStandard.md](../standards/VersionControlStandard.md) |
| L. Quality-adjusted efficiency | Outcome vs effort/context/model/tools/rework | Work Economy Standard |

Each dimension is checked **against** its owning document; none is restated or redefined here.

## 4. Measurement baseline (minimal)

Deliberately small — only measurements that materially improve decision quality; no telemetry is assumed to exist that does not.

| Metric | Measures | Why it matters | Observable from | Reliable? | Mandatory? |
|---|---|---|---|---|---|
| Work Unit outcome quality | Deliverable vs completion criteria | Core of quality-adjusted efficiency | Owner review record / gate result | Yes (inspection) | Mandatory |
| Scope deviations | Changes outside approved scope | Governance effectiveness | Diff vs Work Unit scope | Yes (inspection) | Mandatory |
| Defects found in review | Correctness/quality issues at Approval | Verification effectiveness | Owner review notes | Yes | Mandatory |
| Rework count | Redo cycles after review | Avoidable-effort signal | Review→revision iterations | Yes (countable) | Mandatory |
| Human-intervention count/type | Owner corrections/redirects | Human-control load | Conversation/gate record | Partial (needs discipline to log) | Mandatory |
| Verification iterations | Passes to reach acceptable state | Verification proportionality | Execution record | Partial | Optional |
| Model / effort selection | Routing choice per Work Unit | Routing-appropriateness (H) | Recorded at Work Unit start | Yes if recorded | Optional |
| Context resets/compactions | Session-hygiene events | Context discipline (G) | Observable only if noted | Weak (not reliably captured) | Optional |
| Tool-call pattern | Volume/shape of tool use | Unnecessary-exploration signal | Session record where available | Weak | Optional |
| Work Unit duration | Elapsed working time | Effort proxy | Commit timestamps / session bounds | Partial (coarse) | Optional |
| Unnecessary-exploration time | Effort not advancing the Work Unit | Efficiency leak | Inference from session record | Weak (inferential) | Optional |

Recording is **lightweight and captured at the Work Unit's own gates** (start = classification + routing; Validation = defects/verification; Approval = intervention/rework/outcome), adding no new gate. Metrics marked *weak* are used qualitatively only and never manufactured.

## 5. C1 treatment — quantitative baseline

C1 (baselines never measured) is treated as a **Stage 6 validation/optimization concern**, not a pilot failure. Treatment: adopt the **mandatory** subset in §4 as the standing measurement baseline, captured per Work Unit at existing gates; treat *optional/weak* metrics as best-effort qualitative signals. The baseline must be **owner-ratified** before it governs any controlled comparison. This does not over-engineer telemetry and assumes no unavailable instrumentation.

## 6. C2 treatment — FMFSLA Work Unit traceability

Current evidence: FMFSLA commit `4ee945b` is verifiable; its identity **as** POS `WU-5.3A-01` is conversation-recorded, not a repository string. Missing: an in-repository link between the Work Unit identifier and its evidence/commit.

**Proposed Stage 6 traceability convention (not existing POS policy):** where Git promotion is applicable, the Work Unit ID should be referenced in the associated evidence and/or commit metadata when established by the approved Work Unit procedure. This is a **Stage 6 proposal for validation**, not a mandatory POS-wide policy: it does **not** modify [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md), [../contracts/ParticipantContract.md](../contracts/ParticipantContract.md), or [../standards/VersionControlStandard.md](../standards/VersionControlStandard.md), and it does **not** retrospectively alter FMFSLA commit `4ee945b` (promoted history is immutable). **Classification: a process/documentation convention, not a code or tooling concern**; whether to adopt it is owner-decided during Stage 6. The three levels are kept distinct: *existing POS requirements* (unchanged), *this Stage 6 proposed convention*, and *the pilot observation* that School ERP's WU-5.3B-01 artifact already references its own ID while FMFSLA's did not.

## 7. Validation method

Prefer **controlled comparison within one task class** where justified by evidence: e.g. baseline vs optimized Work Unit; measured intervention/verification/rework before vs after a single deliberate change to context discipline or Work Unit sizing. Constraints: comparisons are only drawn within a comparable task class (Stage 5's two Work Units are **not** mutually comparable — different types); no experiment is prescribed that the evidence does not justify; and **no experiment is created or executed in this strategy step**. Each comparison is itself a scoped Work Unit under the normal gates.

## 8. Optimization principles

Preserve **quality-adjusted efficiency**.

- **Safe optimization** — improves efficiency while preserving quality and governance: tighter minimum-sufficient context, right-sized Work Units, appropriate (not maximal) model/effort routing, reuse of proven verification patterns, concise evidence that stays complete.
- **Unsafe optimization** — reduces controls/evidence merely to save time or tokens: bypassing a gate, removing human approval, cutting verification below acceptable quality, weakening scope control, suppressing or thinning evidence, encouraging autonomous authority, prioritizing token reduction over outcome, or embedding hidden architectural decisions.

Any candidate that is unsafe by this test is rejected regardless of efficiency gain.

## 9. Optimization candidates

| Candidate | Classification | Basis |
|---|---|---|
| Work Unit sizing | **Evidence-supported** | Both pilots' bounded WUs succeeded; sizing is directly observable and drove clean outcomes |
| Evidence capture / traceability convention | **Evidence-supported** | School ERP's anchored artifact worked well; C2 shows the FMFSLA gap — a concrete, evidenced lever |
| Verification patterns | **Evidence-supported** | School ERP §16 verification and FMFSLA's doc reconciliation both show proportional verification working |
| Context economy (minimum-sufficient) | **Plausible** | Consistent with Work Economy Standard and observed scoping, but not quantitatively measured in Stage 5 |
| Session lifecycle discipline | **Plausible** | Single-purpose sessions align with req. 8; no measured Stage 5 signal |
| `CLAUDE.md` context economy | **Plausible** | FMFSLA/School ERP each run their own CLAUDE.md; no measured comparison exists |
| Model routing | **Unknown** | Routing choices not recorded in Stage 5 evidence |
| Effort routing | **Unknown** | Not recorded |
| Skills / Subagents / MCP / Hooks / Permissions | **Unknown** | None exercised in the pilots; no evidence — and none to be introduced here |
| Prompt structure | **Unknown** | Not measured |
| Git completion discipline | **Evidence-supported (retain, not change)** | Worked in FMFSLA; a control to preserve, not optimize away |

No implementation change is recommended; candidates are for owner-authorized controlled validation only.

## 10. Governance / gate mapping

Stage 6 introduces **no new gate**. Every Stage 6 activity is a scoped unit of work under the existing four gates of [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md):

`Scope → Validation → Approval → Promotion`

- **Scope:** each validation/optimization Work Unit is owner-approved before work begins (req. 6; Participant Contract obligation 1).
- **Validation:** measurements and conformance checks run at the Validation gate ([../standards/ValidationStandard.md](../standards/ValidationStandard.md)); a failure is a surfaced defect, never a silent fix.
- **Approval:** the owner reviews outcome, evidence, and metrics; no self-approval.
- **Promotion:** verified publication per [../standards/VersionControlStandard.md](../standards/VersionControlStandard.md) where the Work Unit produces tracked changes.

The AI Operational Control sequence remains a **subordinate operating aid**, never a competing gate ([../architecture/AIGovernanceExtension.md](../architecture/AIGovernanceExtension.md)).

## 11. Evidence limitations

- Sample is **n=2** Work Units of different types → limited generalization; no within-class comparison exists yet.
- **No quantitative Stage 5 data** → routing/context/efficiency dimensions (H, G, L) start from qualitative-only evidence.
- Pilot A WU linkage is **conversation-recorded** (C2).
- Some §4 metrics are **weakly observable** (context resets, exploration time, tool-call patterns) and are qualitative-only.
- POS holds no Stage 5 program records; the pilot evidence lives in originating repositories, referenced not duplicated.

## 12. Proposed Stage 6 operating sequence

Subordinate to POS; **not** a second roadmap and **not** executed here:

`Baseline → Measure → Validate → Analyze → Optimize → Re-measure → Review → Approve → Promote`

Each pass is a single owner-approved, scoped Work Unit through the four gates: fix a baseline (with the §4 mandatory metrics), make **one** safe change, re-measure within the same task class, and let the owner review/approve/promote. No pass may weaken a control (per §8).

## 13. Readiness for controlled Stage 6 execution

**APPROVED — READY FOR CONTROLLED STAGE 6 EXECUTION.**

The strategy is approved by the Project Owner as the basis for controlled Stage 6 execution. Approval does **not** start execution; two explicit **execution-entry conditions** remain owner-controlled and must be resolved **before** the first controlled Work Unit runs (each small, and owner-decided — neither is a governance gate, and no new POS gate is created):

- (S6-C1) **Owner-ratify the minimal measurement baseline** (§4 mandatory subset) so controlled comparisons rest on an agreed metric set.
- (S6-C2) **Owner-select the first comparable task class and its baseline Work Unit** for within-class comparison (§7), since Stage 5's two Work Units are not mutually comparable.

The proposed traceability convention (§6) and any POS-side program reference remain owner-decided and require no code change. This record creates no Work Unit and authorizes no execution; S6-C1 and S6-C2 are **not** claimed as executed.

## Relationship to other documents

- Structured as a Knowledge-layer project record ([../architecture/LayerModel.md](../architecture/LayerModel.md)), alongside [PilotEvidenceConsolidation.md](PilotEvidenceConsolidation.md) and [SelfHostingRelationshipReconciliation.md](SelfHostingRelationshipReconciliation.md).
- Validates against the checkable requirements of [../standards/AIEngineeringStandard.md](../standards/AIEngineeringStandard.md) and [../standards/WorkEconomyStandard.md](../standards/WorkEconomyStandard.md); uses the gates of [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md); defines none of its own.
- **Indexing:** per [../standards/DocumentationStandard.md](../standards/DocumentationStandard.md) and the `docs/knowledge/` convention (every record is listed), the minimum `docs/knowledge/INDEX.md` Contents entry for this record is added as part of this owner-approved promotion.
