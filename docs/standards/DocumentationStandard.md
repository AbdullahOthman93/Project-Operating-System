# Documentation Standard

## Purpose

Defines the required structure, naming, and conventions of authoritative documents. This is the **only** place documentation conventions are defined.

## Scope

Form only. What a document may contain is governed by its layer ([../architecture/LayerModel.md](../architecture/LayerModel.md)) and the dependency rules ([../architecture/DependencyModel.md](../architecture/DependencyModel.md)); this standard governs how conforming documents are structured and named.

## Document structure

Every authoritative document contains, in order:

1. **Title** — a single top-level heading naming the document.
2. **Purpose** — what the document defines, including its single-home declaration (below) where it owns a concept.
3. **Scope** — what is in and out, naming where the out-of-scope concerns live.
4. **Owned content** — the sections defining what the document owns (rules, stages, schemas, terms, or catalog).
5. **Responsibilities** — what the document alone answers for.
6. **Relationships** — how it relates to the documents it references.

## Conventions

- **Single-home declaration.** A document that owns a concept states so explicitly ("this is the **only** place X is defined"). Exactly one document may declare ownership of any concept.
- **Reference form.** Dependencies are expressed as links to the owning document, resolvable as written from the referencing document's location.
- **Binding notes.** Project-specific facts (concrete file names, the identity of the owner, the tool in use) appear only in a clearly marked binding section (for example, "In this repository"), keeping the body reusable (P10, [../architecture/DesignPrinciples.md](../architecture/DesignPrinciples.md)).
- **Illustrative values.** Any example value in a document that could be mistaken for live state is explicitly marked illustrative.
- **Naming.** Document files are named in PascalCase after the concept they own; every documentation directory carries an `INDEX.md` stating the directory's purpose, scope, contents, dependencies, and related documents.
- **Technology-agnostic language.** Outside binding notes and the Execution layer, documents name no specific language, framework, vendor, or tool (P3 — this convention is the checkable form of that principle, which remains defined in [../architecture/DesignPrinciples.md](../architecture/DesignPrinciples.md)).

## Responsibilities

- Define the structure every authoritative document must exhibit and the conventions that keep documents reusable and checkable.

## Relationship to other documents

- Gives checkable form to principles defined in [../architecture/DesignPrinciples.md](../architecture/DesignPrinciples.md) (P2, P3, P10) without restating them.
- Conformance to this standard is verified through [ValidationStandard.md](ValidationStandard.md) at the validation stage of [../kernel/SprintLifecycle.md](../kernel/SprintLifecycle.md).
