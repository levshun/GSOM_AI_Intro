---
description: Writes a commit message for current changes. Usage: /commit
agent: commit-writer
---

Inspect the current change by reading the changed files in `sandbox/repo1`
(e.g. `app.py`, `notes.md`) - you cannot run git commands in this project - then
write a Conventional Commit message with a short subject and, if useful, a body
explaining the *why*.

$ARGUMENTS

Output only: the suggested commit message (subject + optional body). Never run
`git commit` yourself unless asked; never mention secrets.