---
description: Analyses a merge conflict and proposes a safe resolution. Usage: /conflict
agent: conflict-resolver
---

Analyse the current merge conflict (see `git status` and the conflicted file),
explain it in one sentence, show each side, and propose a hand-edited resolution
plus the exact safe commands to finish. Save a plan to `reports/conflict_plan.md`.

$ARGUMENTS

Never recommend `git reset` or discarding work. The user verifies by running the
result before committing.