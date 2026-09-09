This directory holds Claude Code execution bindings for this repository.

It is an Execution-layer artifact, not a source of truth. Everything here conforms to the Participant Contract (`docs/contracts/ParticipantContract.md`) and holds no authority of its own.

Do not add rules here — rules live in the documentation layers and bind through the contract. Any conflict between this directory and the contract is surfaced explicitly, never resolved silently.

`settings.json` is this repository's Claude Code permission boundary. It grants nothing. It denies the Git operations that would rewrite promoted history, so that a requirement already binding through the contract is enforced mechanically rather than by instruction alone; it adds no requirement of its own. It is a technical boundary, never an approval authority — a denied operation that is genuinely required is surfaced to the owner, not worked around.

`settings.local.json`, where a session creates one, is machine-local, is ignored by Git, and never enters promoted history.
