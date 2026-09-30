# AI and Version Control (Git) - Agent Guide

This folder is the workspace for the academic course *AI and Version Control*.
It teaches Git (and a little about GitHub) through hands-on, safe practice inside
`sandbox/`. It is a teaching project, not a software repository.

## Project layout

- `sample/` - read-only example files used to seed practice repositories.
- `sandbox/` - safe scratch area where you create real (local, untracked) git repos.
- `scripts/` - helper scripts produced by the course or by agents.
- `reports/` - agent-written outputs (cheatsheets, commit messages, conflict plans).
- `config/` - GitHub credentials TEMPLATE (never a real token). See the file.

## Safety rules (apply to every assistant AND every command in this project)

- Work only inside `sandbox/`. Never touch files outside this folder.
- **Never commit secrets.** No API keys, tokens, `.env` files, or `git_credentials.env`. `.gitignore` must cover them.
- Prefer safe git ops: `git status`, `git log`, `git diff`, `git add`, `git commit`, `git branch`, `git merge` (local), `git revert`. Do not run `git reset --hard`, `git clean`, `git push` unless a *specific* exercise says so.
- Rules of thumb: commit small, write clear messages, review diffs before committing.
- Work with **repo-local** user identity (never set or change the global git config).
- The user is a beginner: explain the *why* as well as the *what*.
- An LLM-drafted commit message or conflict resolution is a *draft* - review it.

## Agents

- `.opencode/agent/git-tutor.md` - explains Git concepts, writes cheat-sheets.
- `.opencode/agent/commit-writer.md` - writes clear commit messages (Conventional Commits).
- `.opencode/agent/conflict-resolver.md` - analyses merge conflicts and proposes clean fixes.
- `.opencode/agent/git-auditor.md` - reviews a repo/history for secrets and hygiene.
- `.opencode/agent/git-explorer.md` - READ-ONLY: runs a *small allowlist* of git
  inspect commands (`status`, `log`, `diff`, `show`, `branch`, `ls-files`,
  `grep`, `rev-parse`) and explains them. It may NOT commit/add/merge/push.

Note on permissions: most agents here have `bash: deny` (they read files and
draft - you run the commands). `git-explorer` is the exception: it gets a
**scoped, read-only** bash allowlist so it can inspect a repo live. If your
OpenCode setup blocks even that allowlist, fall back to pasting git output.

Agent files take effect after OpenCode is restarted (loaded once at startup).
Reusable prompts live in `.opencode/command/`.