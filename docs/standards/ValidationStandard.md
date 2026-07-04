# Validation Standard

## Purpose

Defines the canonical checklist applied at the Validation gate. This is the **only** place the validation checklist is defined.

## Scope

Checklist content only. *When* validation runs is defined in [../kernel/SprintLifecycle.md](../kernel/SprintLifecycle.md) (stage 4); *what authority* the gate carries is defined in [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md). Every check below verifies work **against** an owning document; none of the rules, schemas, or structures being checked are restated here.

## The checklist

Work is validated by confirming, at minimum:

1. **Cross-reference integrity.** Every reference in created or changed documents resolves to an existing target.
2. **Dependency direction.** Every authority reference conforms to the allowed-dependencies table in [../architecture/DependencyModel.md](../architecture/DependencyModel.md); mentions of lower layers are permitted only as scope-exclusions or descriptions, never as authority.
3. **Single home.** No concept is defined in more than one place; new content references owning documents rather than restating them (verified per the declarations required by [DocumentationStandard.md](DocumentationStandard.md)).
4. **Documentation conformance.** Created or changed documents conform to [DocumentationStandard.md](DocumentationStandard.md).
5. **Schema conformance.** Tracking artifacts and promotion entries touched by the work conform to the schemas of the State & Tracking layer ([../runtime/StateModel.md](../runtime/StateModel.md) and its catalog); status values are valid under its transition model.
6. **Scope conformance.** Only the approved deliverables were produced (Scope gate, [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md)).
7. **Retro-validation on new rules.** When work introduces a new schema or standard, the existing corpus is validated against it.

## Handling failures

A failed check is a **defect**. It is surfaced through [../kernel/ChangeAndConflictWorkflow.md](../kernel/ChangeAndConflictWorkflow.md) — never silently fixed, never absorbed by weakening the check, and never waved through. Validation is complete only when every check passes or every failure has been explicitly surfaced.

## Responsibilities

- Define the minimum checks that constitute passing the Validation gate.
- Require that check failures become surfaced defects rather than silent adjustments.

## Relationship to other documents

- Enforces what the Validation gate of [../architecture/GovernanceModel.md](../architecture/GovernanceModel.md) requires, at the stage defined by [../kernel/SprintLifecycle.md](../kernel/SprintLifecycle.md).
- Checks conformance *to* [DocumentationStandard.md](DocumentationStandard.md), the dependency table of [../architecture/DependencyModel.md](../architecture/DependencyModel.md), and the schemas of the State & Tracking layer — each remains the sole owner of what it defines.
