# AI and the Command Line

A **4 academic hour** interactive course for students who do **not** have a
strong IT background. Everything is in English, explained in plain language, and
**safe**: the course never deletes files, never uses `sudo`, and never touches
anything outside its own folder.

Like the sister catalogs (*Introduction to AI Assistants*, *Data Collection &
Cleaning*, *Data Analysis and Visualization*), you learn by doing with the AI
assistant on this server (**OpenCode**). You configure shell-specialist agents as
Markdown files, write prompts, run safe commands, and analyze the results.

## What you will learn

- What a **shell / command line** is and why system "power users" use it.
- How to read a command: `name [options] arguments`, flags, and the current directory.
- **File management**: `ls`, `mkdir`, `cp`, `mv`, `touch`, plus inspecting files with `head/wc/sort/uniq/grep/find` - **without deleting anything** (we move to a `trash/` folder instead).
- **Automation**: variables, pipes, redirection, loops, and writing small **Bash scripts** that back up files and run repeated tasks.
- How to **instruct an AI** to explain commands, write scripts, and review them - then **verify** the results yourself.
- How to configure a shell-agent team in `.md` files and use safe reusable commands.
- Command-line **safety and security**: spot dangerous commands, prompt injection via file names, and least privilege.

## Structure (4 parts = 4 academic hours)

| Part | Hour | Topic |
|------|------|-------|
| 1 | 1 | Meet the shell and your shell tutor: how commands work, safety rules, agents, prompts |
| 2 | 2 | File management with AI: navigate, organize, inspect - safely |
| 3 | 3 | Automating tasks with AI: variables, pipes, loops, and writing a backup script |
| 4 | 4 | Explain, review, automate responsibly: verify with numbers, security, cheat-sheet, take-away |

## Files in this catalog

| File | Purpose |
|------|---------|
| `AI and the Command Line.ipynb` | The main course notebook (theory + OpenCode tasks + checkpoints). |
| `AGENTS.md` | Project rules + safety rules every assistant must follow. |
| `.opencode/agent/shell-tutor.md` | Agent: explains commands/flags, writes cheat-sheets. |
| `.opencode/agent/script-writer.md` | Agent: writes safe, defensive Bash scripts. |
| `.opencode/agent/shell-reviewer.md` | Agent: reviews scripts for safety and correctness. |
| `.opencode/command/explain.md` | Reusable command: run the shell tutor. |
| `.opencode/command/script.md` | Reusable command: run the script writer. |
| `sample/` | Read-only example files (logs, names, notes) the course inspects. |
| `sandbox/` | Safe scratch area for creating/managing files. |
| `scripts/` | Bash scripts produced during the course. |
| `reports/` | Agent-written explanations, cheatsheets and reviews. |
| `glossary.md` | Dictionary of shell + AI terms. |
| `README.md` | This file. |

## How to use the notebook

1. Open `AI and the Command Line.ipynb` and run cells in order.
2. Green boxes titled **Your turn: OpenCode** contain ready-made prompts. Paste
   them into the chat; after the agent finishes, run the **checkpoint code cells**
   that verify and analyze the result.
3. Every task has a deterministic fallback, so the course works fully offline.
4. When you create or change agent files, **quit and restart OpenCode**.
5. The notebook runs only **safe commands** inside `sandbox/` and inspects
   `sample/` read-only. Never copy a command you do not understand into a real
   terminal.

## Requirements

Python 3.12 with a normal Bash shell (both present in this environment). No API
key or internet needed. OpenCode is used through the chat interface already
available on the server.