---
description: Audits a repository for secrets and hygiene. Usage: /audit
agent: git-auditor
---

Review the current repository for leaked credentials and hygiene problems, save
your evidence-based findings to `reports/audit.md`, and return the top three
findings and a verdict.

$ARGUMENTS

Review only - do not edit files or run destructive commands.