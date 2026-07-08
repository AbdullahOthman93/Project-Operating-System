# ProjectGovernanceRelationship

## Purpose

Defines the **Project Governance Relationship** — the long-lived relationship under which a project is governed by the framework — together with the transition that establishes it (**Project Adoption**) and the conditions under which a project enters it. This is the **only** place these concepts are defined: the governed project, the relationship itself, when governance begins, the origin baseline, Project Adoption as the establishing transition, and the origin conditions (greenfield and brownfield).

It defines *concepts*, not procedure. How an adoption is carried out is owned by the Process layer, and how the relationship's state is recorded is owned by the State & Tracking layer; neither is defined here.

## Scope

The governing concept and its vocabulary only. This document does not define:

- the *procedure* by which a project is adopted — a workflow owned by the Process layer;
- any *state value, status, or tracking rule* for a relationship or its transitions — owned by the State & Tracking layer;
- any *approval gate, decision right, or amendment rule* — defined in [GovernanceModel.md](GovernanceModel.md);
- the *principles* the concept rests on — defined in [DesignPrinciples.md](DesignPrinciples.md).

The direction and deliverable this concept serves are defined in [Vision.md](Vision.md) and [Mission.md](Mission.md).

## The governed project and the relationship

A **governed project** is a project standing in a **Project Governance Relationship** with the framework. Governedness is a status conferred by this relationship, not a property of a project's code or contents: a project is governed when, and only when, the relationship holds.

A Project Governance Relationship consists of:

- an **owner** holding final approval authority for the project (decision rights defined in [GovernanceModel.md](GovernanceModel.md));
- an **approved architecture** the project's work is planned and accepted within (Architecture-First, [DesignPrinciples.md](DesignPrinciples.md), P1);
- an **origin baseline** (below) from which the project's permanent record proceeds;
- **forward gating** — the commitment that every subsequent state transition passes the approval gates and is promoted into the permanent record ([GovernanceModel.md](GovernanceModel.md)).

The relationship is **long-lived**: it persists across the project's whole governed life, and the transitions performed under it — including its establishment — are transitions of this one relationship.

## When governance begins

Governance begins at a single discrete event — the **point of adoption** — not gradually, and not when code first exists. Before that point a project is ungoverned; from it, every state transition is gated and recorded.

Governance is **prospective**: it governs transitions forward from the origin. It does not retroactively validate work performed before the relationship existed. Admitting a project therefore fixes a starting state and governs every move away from it, rather than passing prior history through the gates.

## The origin baseline

The **origin baseline** is the approved state fixed at the establishing transition, accepted as the **trusted origin** of the project's permanent record. It is the baseline ([Terminology.md](Terminology.md)) as it stands at the moment of adoption.

Establishing an origin baseline is an act of **acceptance of an origin**, consistent with Architecture-First ([DesignPrinciples.md](DesignPrinciples.md), P1) under the owner's determination — recorded in the permanent record — that an origin baseline is *accepted as an origin*, not *implemented under the architecture*. Fixing the origin baseline therefore does not assert that its contents were produced under the architecture, nor that they conform to current standards; it declares only where the governed permanent record begins.

An origin baseline carries a **conformance posture** — the degree to which its contents already satisfy the standards that govern future work. A posture short of full conformance is recorded, not concealed, and is discharged by subsequent gated transitions.

## Project Adoption — the establishing transition

**Project Adoption** is the transition that establishes a Project Governance Relationship: it binds an owner and an approved architecture to a project and fixes the project's origin baseline. It is the **first** transition of the relationship, not a concept standing apart from it.

Adoption is defined here as a concept only. Its *procedure* — trigger, participant responsibilities, and exit conditions expressed against the existing approval gates — is owned by the Process layer and is not defined in this document. Adoption introduces no gate of its own.

## Origin conditions — greenfield and brownfield

A project enters the relationship under one of two **origin conditions**, which are two values of a single concept, not two concepts:

- **Greenfield** — the origin baseline is empty or minimal; its conformance posture is clean by construction.
- **Brownfield** — the origin baseline encloses pre-existing content of external provenance; its conformance posture may fall short of current standards, and that shortfall is recorded for discharge by later governed work.

Greenfield is the degenerate case of brownfield in which the pre-existing content is empty. Both are established by the same adoption transition and governed by the same relationship; the only variable is the origin baseline's initial content and conformance posture.

## Responsibilities

- Provide the single canonical definition of the Project Governance Relationship, the governed project, the origin baseline, Project Adoption as the establishing transition, and the greenfield/brownfield origin conditions.
- Serve as the reference target whenever any document names these concepts.

## In this repository

The inaugural Project Governance Relationship is this repository itself, formed at the framework's genesis under a **greenfield** origin condition (self-hosting, [Mission.md](Mission.md)). This binding is project-specific; the concept is not.

## Relationship to other documents

- Serves the direction of [Vision.md](Vision.md) and the deliverable and self-hosting framing of [Mission.md](Mission.md).
- Rests on [DesignPrinciples.md](DesignPrinciples.md) — especially Architecture-First (P1) and Gated Progression (P6).
- Uses the decision rights and approval gates of [GovernanceModel.md](GovernanceModel.md); defines none of its own.
- Its terms are cataloged in [Terminology.md](Terminology.md), which points here for their fuller treatment.
- The procedure operationalizing Project Adoption (Process layer) and the state representation of the relationship (State & Tracking layer) are owned by those layers and lie outside this document.
