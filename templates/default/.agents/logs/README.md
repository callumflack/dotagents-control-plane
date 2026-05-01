# Agent Logs

Use `.agents/logs/` for session orientation notes.

Logs preserve what the agent was trying to do, what decisions were made, what checks mattered, and where the next agent should resume. They are not commit ledgers, changelogs, or proof of what shipped. Git remains the source of truth for commits, diffs, and exact file history.

## When To Write

Write or update a log when:

- a work session ends;
- a plan or audit is created;
- a resolver, gate, skill, or router changes;
- a durable artifact or active-work pointer changes;
- current work state changes.

## Create Vs Update

Update the current session note when:

- fixing review findings in the same slice;
- running extra checks;
- making small cleanup before the same commit;
- applying reviewer or skill feedback without changing scope.

Create a new session note when:

- starting a new product slice;
- changing router, resolver, gate, skill, or log doctrine;
- changing active-work pointers;
- making a separate commit-worthy decision.

Do not write a receipt for:

- typo-only fixes;
- pure formatting after checks;
- transient investigation with no durable change.

Default log target: the newest `.agents/logs/*execution*.md` for the active slice.

## Closeout

If the work produced a reusable lesson, capture it in `history/solutions/<slug>.md`.

## Shape

Each log should include:

- session intent;
- branch/worktree;
- touched surfaces;
- checks/probes run;
- decisions made;
- unresolved questions;
- next pointer.

## Boundaries

Do not:

- put live rules in logs;
- read logs before router/resolvers unless reconstructing prior work;
- treat logs as source of truth over `.agents/active-work.md`, resolvers, gates, skills, or docs.
