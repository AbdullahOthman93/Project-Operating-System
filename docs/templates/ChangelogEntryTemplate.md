# Changelog Entry Template

> **Non-authoritative scaffolding.** This template defines no rule and no schema. It provides a fill-in skeleton for a promotion entry whose schema is owned by [../runtime/StateTransitionModel.md](../runtime/StateTransitionModel.md) (§ Promotion entry schema). Every bracketed `<...>` value is **illustrative** and must be replaced. If this template ever diverges from that schema, the schema governs.

**Use for:** the entry added to the permanent changelog at closeout (stage 7) of [../kernel/SprintLifecycle.md](../kernel/SprintLifecycle.md), upon owner approval.

**Schema owned by:** [../runtime/StateTransitionModel.md](../runtime/StateTransitionModel.md). Entries are append-only, newest first, and are never edited once promoted except by owner-approved amendment. The single change set that carries the entry conforms to [../standards/VersionControlStandard.md](../standards/VersionControlStandard.md).

Copy the skeleton below to the top of the changelog (newest first) and replace every bracketed value:

```md
## <Unit identifier — number and approved name>
- **Status:** <completion statement including approval — e.g., "Completed and approved">
- **Summary:** <what the unit delivered, in terms of artifacts and the layer they belong to>
- **Approved by:** <the approving authority, and where the approval was given>
```
