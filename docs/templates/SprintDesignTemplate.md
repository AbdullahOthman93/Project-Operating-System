# Sprint Design Template

> **Non-authoritative scaffolding.** This template defines no rule. It provides a fill-in skeleton for the sprint design produced at Definition (stage 1) of [../kernel/SprintLifecycle.md](../kernel/SprintLifecycle.md), whose required contents that document owns. Every bracketed `<...>` value is **illustrative** and must be replaced. If this template ever diverges from the Sprint Lifecycle, that document governs.

**Use for:** the design submitted to the owner for the Scope gate before a sprint is implemented.

**Required contents owned by:** [../kernel/SprintLifecycle.md](../kernel/SprintLifecycle.md) (stage 1). Declared dependencies must validate against [../architecture/DependencyModel.md](../architecture/DependencyModel.md); the design is not implemented before it is owner-approved (Scope gate).

Copy the skeleton below and replace every bracketed value:

```md
# Sprint <phase>.<n> — <Approved Sprint Name>

## Objective

<The single outcome this sprint exists to achieve.>

## Scope

**In scope:** <what this sprint will produce.>
**Out of scope:** <what it will not, naming where that work lives.>

## Deliverables

<The concrete artifacts to be created or changed.>

## Dependencies

<The documents/sprints this sprint depends on, as references that validate against the Dependency Model.>

## Success criteria

<How a correct result is recognized — the conditions checked at the Validation gate.>

## Completion criteria

<What must be true for closeout to proceed.>

## Risks

<The risks to this sprint and their mitigations.>

## Expected impact on subsequent sprints

<How this sprint's result affects the sprints that follow.>
```
