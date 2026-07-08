# ProjectAdoptionWorkflow

## Purpose

Defines the canonical workflow of **Project Adoption** — the establishing transition that brings a project into a Project Governance Relationship. This is the **only** place the adoption workflow is defined. It operationalizes the concept owned by [../architecture/ProjectGovernanceRelationship.md](../architecture/ProjectGovernanceRelationship.md); it adds procedure, never concept.

## Scope

Ordering and procedure only. What the Project Governance Relationship, the origin baseline, and the origin conditions *are* is defined in [../architecture/ProjectGovernanceRelationship.md](../architecture/ProjectGovernanceRelationship.md); the authority of each gate is defined in [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md); the schema by which the relationship and this transition are recorded is owned by the State & Tracking layer. This workflow expresses its exit conditions against the **existing** approval gates and defines **no gate of its own** ([ProcessModel.md](ProcessModel.md)). Relationship transitions other than establishment (for example, closure) are out of scope and are added only on demonstrated need ([../architecture/DesignPrinciples.md](../architecture/DesignPrinciples.md), P9).

## Trigger

A project is to be brought under governance: a candidate project exists (with or without prior content) and a prospective owner intends to govern it. Adoption runs **once** per relationship, before any phase or sprint runs on that project.

## Participant responsibilities

Within the decision rights of [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md): a participant proposes and carries out the establishment and reports it; the owner alone approves each gate. No participant promotes its own work past a gate.

## Stages

1. **Proposal.** The proposer states: the project to adopt; the prospective owner; the architecture to bind; the proposed **origin baseline**; and its **origin condition** — *greenfield* (empty or minimal origin) or *brownfield* (pre-existing content), the latter with the origin baseline's declared **conformance posture**. Submitted to the owner; no establishment is finalized before approval (Scope gate, [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md)).

2. **Scope approval.** Upon owner approval, the adoption is a scoped unit of work: the owner has accepted the proposed origin baseline as the trusted origin — an acceptance of an origin, not implementation under the architecture ([../architecture/ProjectGovernanceRelationship.md](../architecture/ProjectGovernanceRelationship.md)) — together with the declared origin condition and conformance posture.

3. **Establishment.** Within approved scope, the relationship's constituents are bound — owner, approved architecture, and origin baseline — and the origin baseline is fixed as the trusted origin from which the project's permanent record proceeds. For a greenfield origin the baseline is empty or minimal; for a brownfield origin it is the pre-existing content accepted as-is with its recorded conformance posture. Prior history is not retroactively passed through the gates: governance is prospective ([../architecture/ProjectGovernanceRelationship.md](../architecture/ProjectGovernanceRelationship.md)).

4. **Validation.** Before reporting, the establishment is validated against the governance documents and against this workflow: the origin baseline is well-formed and unambiguous; the origin condition and any conformance posture are recorded accurately and not concealed; references resolve; and nothing claims retroactive validation of pre-existing work. A failure is a defect surfaced per [ChangeAndConflictWorkflow.md](ChangeAndConflictWorkflow.md). This satisfies the Validation gate.

5. **Reporting.** The participant reports the established relationship, the origin baseline and its conformance posture, and the validation summary. The participant does not approve or promote its own work.

6. **Approval.** The owner reviews the report (Approval gate). Rejection returns the work to Establishment within approved scope; approval authorizes promotion.

7. **Promotion.** The establishing transition is promoted into the permanent record ([../architecture/GovernanceModel.md](../architecture/GovernanceModel.md)). From this point the relationship is established and all subsequent work on the project proceeds under forward gating — phases per [PhaseModel.md](PhaseModel.md) and sprints per [SprintLifecycle.md](SprintLifecycle.md). Any conformance shortfall recorded at a brownfield origin is discharged by later governed sprints, not by adoption.

## Conformance references

The representation of the relationship and of this establishing transition in the live and permanent records conforms to the schemas of the State & Tracking layer ([../runtime/StateModel.md](../runtime/StateModel.md) and its catalog). These are conformance references under [../architecture/DependencyModel.md](../architecture/DependencyModel.md), rule 7; this workflow's authority derives from the Governance layer.

## In this repository

The inaugural Project Governance Relationship is this repository itself, established at the framework's genesis under a greenfield origin condition ([../architecture/Mission.md](../architecture/Mission.md)). That historical establishment predates this workflow; the workflow itself is project-independent.

## Responsibilities

- Define the stages and ordering of the Project Adoption workflow and its trigger.
- Express adoption's exit conditions against the existing approval gates, introducing none of its own.

## Relationship to other documents

- Operationalizes the concept of [../architecture/ProjectGovernanceRelationship.md](../architecture/ProjectGovernanceRelationship.md) and the four gates of [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md); defines neither.
- Structured per [ProcessModel.md](ProcessModel.md); establishes the relationship within which [PhaseModel.md](PhaseModel.md) and [SprintLifecycle.md](SprintLifecycle.md) subsequently operate.
- Scope changes and detected conflicts during adoption follow [ChangeAndConflictWorkflow.md](ChangeAndConflictWorkflow.md).
