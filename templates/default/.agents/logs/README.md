# Agent Logs

Use `.agents/logs/` for session receipts only.

## When To Write

Write or update a log when:

- a work session ends;
- a plan or audit is created;
- a resolver, gate, skill, or router changes;
- a durable artifact or active-work pointer changes;
- current work state changes.

## Create Vs Update

Update the current slice receipt when:

- fixing review findings in the same slice;
- running extra checks;
- making small cleanup before the same commit;
- applying reviewer or skill feedback without changing scope.

Create a new receipt when:

- starting a new product slice;
- changing router, resolver, gate, skill, or log doctrine;
- changing active-work pointers;
- making a separate commit-worthy decision.

Do not write a receipt for:

- typo-only fixes;
- pure formatting after checks;
- transient investigation with no durable change.

Default receipt target: the newest `.agents/logs/*execution*.md` for the active slice.

## Closeout

If the work produced a reusable lesson, capture it in `history/solutions/<slug>.md`.

## Shape

Each log should include:

- date;
- branch;
- changed files;
- checks run;
- decisions made;
- next pointer.

## Boundaries

Do not:

- put live rules in logs;
- read logs before router/resolvers unless reconstructing prior work;
- treat logs as source of truth over `.agents/active-work.md`, resolvers, gates, skills, or docs.
