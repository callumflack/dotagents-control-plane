# Agent Tooling Gate

Done means:

- Codex-facing repo skills live under `.agents/skills/`;
- `.agents/skills/agents-kit/` exists when `.agents` control-plane behavior is being edited;
- `python3 .agents/skills/agents-kit/scripts/check-agents-kit-health.py` passes when router, resolver, gate, skill, or captured-learning structure changes;
- reusable lessons live under `history/solutions/`, not `.agents/`;
- host mirrors such as `.claude/` are tracked only when intended;
- local-only host surfaces such as `.pi/` stay ignored unless user explicitly asks;
- `skills-lock.json` matches the intended installed skill set;
- `AGENTS.md` stays short and points to `.agents/`;
- if the work produced a reusable lesson, capture it in `history/solutions/<slug>.md`;
- one-off project plans and execution evidence live in `history/`; do not create `.agents/resolvers/*` or `.agents/gates/*` for single-use work; promote only repeatable routing rules, done checks, or skills into `.agents/`;
- `git status --short --ignored` shows no accidental local-only staged files.
