# Glossary: AI and the Command Line

Simple definitions of terms used in the course, sorted alphabetically.

**Agent (in OpenCode)** – A specialist assistant defined in an `.md` file under
`.opencode/agent/`, with frontmatter (description, mode, model, permissions) and a body that is its instructions.

**AGENTS.md** – A Markdown file OpenCode reads to learn a project's rules and safety layout. Every assistant in the folder sees it.

**Argument** – What a command acts on (a file or folder name), e.g. the file in `head names.txt`.

**Bash** – The most common shell (the program that reads and runs your commands). "Bash script" = a small file of bash commands.

**CATA** – A prompt recipe: C (Context), A (Action), T (Tone/format), A (Anticipate edge cases), plus a *checkpoint* to verify the result.

**Command** – An instruction the shell runs, usually `name [options] [arguments]`, e.g. `ls -la sample`.

**Current directory** – The folder the shell is working in right now; `pwd` prints it, `.` means "this folder".

**Exit code** – The number a command returns (`0` = success, non-zero = error). Scripts use it to stop early with `set -e`.

**Flag / option** – A switch that changes a command (`-l`, `--recursive`), usually starts with `-` or `--`.

**Glob / wildcard** – A pattern the shell expands, like `*.txt` ("all files ending in .txt").

**grep** – Searches text for a pattern: `grep ERROR sample/logs/app.log` shows only matching lines.

**Least privilege** – Giving an agent or command only the permissions it truly needs (e.g. inspection-only agents cannot run anything).

**Pipe (`|`)** – Feeds the output of one command into the next: `cat f | wc -l`.

**Prompt injection** – Malicious text hidden inside data (e.g. a file name or log line) that tries to make an AI or script do something unintended.

**Redirection (`>`, `<`)** – Sends a command's output to a file (`>`) or reads input from a file (`<`).

**Sandbox** – A safe, isolated scratch area where you can create and manage files without harming anything real.

**Script** – A text file of commands run as one unit; usually starts with `#!` (shebang) and is made executable.

**shebang** – The first line `#!/usr/bin/env bash` that says which shell/engine runs a script.

**Shell** – The program that reads what you type and runs it; your "command line".

**stdin / stdout / stderr** – Standard input and the two standard outputs (normal results vs errors); you can redirect any of them.

**sudo** – Runs a command with elevated privileges. In this course: **never used**.

**Variable** – A named slot in a script (`src="sample/logs"`, read back with `"$src"`).