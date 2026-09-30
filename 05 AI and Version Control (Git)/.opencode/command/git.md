---
description: Inspects a repository with read-only git commands and explains it. Usage: /git status
agent: git-explorer
---

Use the Git Explorer (read-only) agent: run the read-only git command requested
against `sandbox/repo1` (`git -C sandbox/repo1 <command>`), show its output, and
explain it for a beginner.

$ARGUMENTS

Allowed subcommands: status, log, diff, show, branch, ls-files, grep, rev-parse.
Never mutate anything. If the command is blocked, say so and ask for pasted output.