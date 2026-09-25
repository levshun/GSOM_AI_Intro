# AI and the Command Line - Agent Guide

This folder is the workspace for the academic course *AI and the Command Line*.
It is a shell-scripting teaching project, not a software repository.

## Project layout

- `sample/` - read-only example files the course inspects (logs, names, notes).
- `sandbox/` - safe scratch area. Students and agents may create/manage files here.
- `scripts/` - bash scripts produced by the notebook or by agents.
- `reports/` - Markdown outputs written by agents (explanations, cheatsheets, reviews).

## Safety rules (apply to every assistant AND every command in this project)

- No `rm`, no `rm -rf`, no `sudo`, no `chmod 777`, no root, no deletion of files
  outside `sandbox/`. Never touch system files outside this folder.
- To "delete" something, move it to `sandbox/trash/` instead (`mv`) and say so.
- Quote every file name (`"$file"`) - spaces and `*` must never be run as code.
- Prefer safe, non-destructive commands: `ls`, `pwd`, `cat`, `head`, `wc`,
  `sort`, `uniq`, `grep`, `find` (inspection only), `mkdir -p`, `touch`, `cp`, `mv`.
- Never fetch the internet. Work only with the local `sample/` and `sandbox/`.
- A script or command suggested by an LLM is a *draft* - review it before running.
- The user is a beginner: explain the *why* as well as the *what*.

## Agents

- `.opencode/agent/shell-tutor.md` - explains commands/flags and writes safe cheatsheets.
- `.opencode/agent/script-writer.md` - writes safe, defensive bash scripts.
- `.opencode/agent/shell-reviewer.md` - reviews scripts for safety and correctness.

Agent files take effect after OpenCode is restarted (configuration loads once at
startup). Reusable prompts live in `.opencode/command/`.