# Measurement Record — <Work Unit ID>

> **Template — not a record.** Copy this file to create a per–Work Unit measurement record; do not record measurements in the template itself. This is a State & Tracking schema, not authority: a measurement record states what was observed and creates no decision right, gate, or precedence ([../StateModel.md](../StateModel.md)).
>
> **Placement.** A Work Unit uses this template during measurement capture. The **completed or preserved** record is historical project evidence and is kept in [`docs/knowledge/`](../../knowledge/INDEX.md) — not under `docs/runtime/measurements/`, which holds only this template/schema and runtime-oriented guidance.
>
> **Governing measurement method (referenced, not duplicated).** The measurement baseline and its metric definitions are owned by the Stage 6 measurement baseline in [../../knowledge/Stage6ValidationOptimizationStrategy.md](../../knowledge/Stage6ValidationOptimizationStrategy.md) (§4); the telemetry-boundary rule — agent-observable / host-observable / derived analysis, and the NOT AVAILABLE state — is owned by [../../standards/AIEngineeringStandard.md](../../standards/AIEngineeringStandard.md) (Requirement 10). This template applies those and restates neither in full.
>
> **Recording rules (preserved from the canonical method).**
> - The Agent records only what it can reliably observe (agent-observable).
> - The Host supplies measurements that only the Host can reliably measure (host-observable); the Agent does not assert them.
> - **NOT AVAILABLE** is a valid measurement state.
> - **NOT AVAILABLE** is never converted to zero, estimated, inferred, or silently omitted.
> - **QAE** is not fabricated, nor calculated, without an approved analytical basis; absent one, record it as NOT AVAILABLE.

## Identity

- **Work Unit ID:**
- **Task Class:**
- **Repository:**
- **Branch:**
- **Baseline HEAD:**
- **Final HEAD:**

## Outcome

- **Outcome Quality:**
- **Correctness:**
- **Scope Deviation:**
- **Evidence Completeness:**

## Execution

- **Model:**
- **Effort:**
- **Context State:**
- **Context Events:**
- **Human Intervention:**

## Verification

- **Required:**
- **Executed:**
- **Iterations:**
- **Failures:**
- **Skips / Pre-existing Failures:**

## Rework

- **Rework Count:**

## Delivery

- **Commit:**
- **Push:**
- **Remote Verification:**
- **Final Working Tree:**

## Host Measurements

*Host-observable only. Where the host does not reliably supply a value, record NOT AVAILABLE — never zero, an estimate, or an inferred value.*

- **Duration:**
- **Tokens:**
- **Cost:**

## QAE

- **QAE:** *(Not fabricated and not calculated without an approved analytical basis; otherwise NOT AVAILABLE.)*

## Evidence

- **Evidence references:**
