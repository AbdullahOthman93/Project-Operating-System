# Mission

## Purpose

Defines *what* the Project Operating System is and delivers, and the boundaries of that delivery. Where [Vision.md](Vision.md) states the end state, this document states the system's concrete purpose in service of it.

## Scope

Statement of deliverable and boundaries only. Design rationale belongs in [DesignPrinciples.md](DesignPrinciples.md); structure belongs in [ArchitectureOverview.md](ArchitectureOverview.md) and [LayerModel.md](LayerModel.md).

## The Mission

Provide a reusable, technology-agnostic operating framework that governs how software projects are planned, designed, implemented, validated, documented, and maintained — by human engineers, AI agents, or both.

The framework consists of:

- **Governance** — the authoritative principles, models, and decision rules (this directory).
- **Process** — workflows and phase gates that move work from intent to accepted result.
- **State and knowledge management** — how live progress is tracked and how completed work becomes permanent record.
- **Standards** — the reusable quality bar applied to all work.
- **Contracts** — formal interfaces that any executing participant (tool or AI agent) must satisfy.

## Boundaries

The Project Operating System:

- **Does** define how projects operate: rules, workflows, states, standards, and participant interfaces.
- **Does not** prescribe any programming language, framework, vendor, platform, or tool.
- **Does not** replace a project's own domain decisions; it governs the process by which those decisions are made and recorded.

## Self-hosting

This repository is itself the first project governed by the framework it defines. Every rule established here applies to the development of this repository, as it happens.

## Responsibilities

- Define the deliverable of the Project Operating System and its explicit boundaries.
- Anchor scope decisions: work that does not serve this Mission is out of scope for the framework.

## Relationship to other governance documents

- Derives its direction from [Vision.md](Vision.md).
- The framework components named above are structured by [LayerModel.md](LayerModel.md) and related by [DependencyModel.md](DependencyModel.md).
- [DesignPrinciples.md](DesignPrinciples.md) governs how this Mission is pursued.
- Terms used here are defined in [Terminology.md](Terminology.md).
