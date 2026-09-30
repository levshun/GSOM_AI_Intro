# AI and Version Control (Git)

Here you learn by doing with the AI assistant on this server (**OpenCode**): you configure Git-specialist agents as Markdown files, write prompts, run safe `git` commands, and verify the results.

## What you will learn

- What **version control / Git** is and why a "time machine for files" matters.
- The core loop: `status` → `add` → `commit` → `log`, and an everyday understanding of `HEAD`, branches and merges.
- How to ask an AI to **explain Git concepts**, **write commit messages** (Conventional Commits), and **resolve merge conflicts** - then verify the result.
- How to configure a Git/GitHub **credentials file safely** (template provided),
  and why a real token must never be committed, pasted, or printed.
- How **least privilege** applies to agents: most Git agents can only read files
  and draft (you run the commands); the one exception, `git-explorer`, gets a
  **read-only** git allowlist so it can inspect a repo live - never push/commit.
- How to **audit a repository** (secrets + hygiene) with an agent and with your own checks.
- Version-control **security habits**: secret leakage in history, `.gitignore`, and least privilege.

## Structure (4 parts = 4 academic hours)

| Part | Hour | Topic |
|------|------|-------|
| 1 | 1 | Meet Git and your Git tutor: repo/commit/HEAD, safety, agents, first commit |
| 2 | 2 | Commits and histories with AI: good messages, `git log/diff`, `.gitignore` |
| 3 | 3 | Branches and merge conflicts with AI: branches, merges, a controlled conflict |
| 4 | 4 | Remotes, credentials and auditing: safe pushes, the creds file, git-auditor, security |

## Files in this catalog

| File | Purpose |
|------|---------|
| `AI and Version Control (Git).ipynb` | The main course notebook (theory + OpenCode tasks + checkpoints). |
| `AGENTS.md` | Project rules + safety rules every assistant must follow. |
| `.opencode/agent/git-tutor.md` | Agent: explains Git concepts, writes cheat-sheets. |
| `.opencode/agent/commit-writer.md` | Agent: writes clear commit messages. |
| `.opencode/agent/conflict-resolver.md` | Agent: analyses and proposes conflict resolutions. |
| `.opencode/agent/git-auditor.md` | Agent: audits a repo for secrets and hygiene. |
| `.opencode/agent/git-explorer.md` | Agent: READ-ONLY - runs a small allowlist of `git` inspect commands (`status/log/diff/show/branch/ls-files/grep/rev-parse`) and explains them. |
| `.opencode/command/` | Reusable prompts: `/explain`, `/commit`, `/conflict`, `/audit`, `/git`. |
| `config/git_credentials.example.env` | Credentials TEMPLATE + how-to-create-a-token instructions. |
| `config/.gitignore` | Safe-ignore list (secrets, junk) for practice repos. |
| `sample/` | Read-only files used to seed practice repositories. |
| `sandbox/` | Safe local practice repositories. |
| `scripts/` | Helper scripts produced by the course. |
| `reports/` | Agent-written cheat-sheets, commit messages, plans, audits. |
| `glossary.md` | Dictionary of Git + AI terms. |
| `README.md` | This file. |

## How to use the notebook

1. Open `AI and Version Control (Git).ipynb` and run cells in order.
2. Green boxes titled **Your turn: OpenCode** contain ready-made prompts. Paste
   them into the chat, then run the **checkpoint code cells** that verify the result.
3. Every task has an offline fallback, so the course works without the assistant.
4. When you create or change agent files, **quit and restart OpenCode**.
5. All git practice happens in local repos under `sandbox/` - no network needed.
   Pushing to GitHub in Part 4 is **optional** and requires your own token.

## GitHub credentials (Part 4, optional)

`config/git_credentials.example.env` explains how to create a GitHub Personal
Access Token with minimal scope, and the notebook's `load_credentials()` helper
reads it from an **untracked** `git_credentials.env` without ever printing it.
Never paste, commit, or chat about the token. If it ever leaks, revoke it.

## Requirements

Python 3.12, `git` 2.x, pandas - all present in this environment. No API key and
no internet are required for the local part; only the optional push needs your
own GitHub credentials.