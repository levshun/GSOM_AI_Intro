# Glossary: AI and Version Control (Git)

Simple definitions of terms used in the course, sorted alphabetically.

**.gitignore** – A file listing names/patterns (`.env`, `*.key`) that Git must never track or commit.

**add (git add)** – Stage a change so it is ready to be committed. Only staged changes go into the next commit.

**Agent (in OpenCode)** – A specialist assistant defined in an `.md` file under `.opencode/agent/`, with frontmatter and a body that is its instructions.

**AGENTS.md** – A Markdown file OpenCode reads to learn a project's rules and safety layout.

**Branch** – A parallel line of work; a pointer to a commit. `main` is the default branch; `git branch <name>` creates one.

**CATA** – A prompt recipe: C (Context), A (Action), T (Tone/format), A (Anticipate edge cases), plus a checkpoint to verify the result.

**Clone** – Make a local copy of a remote repository for the first time: `git clone <url>`.

**Commit** – A saved snapshot of the staged changes, with a message and an author.

**Commit message** – The note attached to a commit. **Conventional Commits** start with a type: `feat:`, `fix:`, `docs:`, `refactor:`, `test:`, `chore:`.

**Conflict (merge conflict)** – When two branches changed the same lines differently; Git marks the conflicting spots with `<<<<<<<`, `=======`, `>>>>>>>` and asks you to decide.

**diff (git diff)** – Shows the changes made but not yet committed (or between commits).

**HEAD** – "You are here" - the commit your working copy points to (usually the latest of the current branch).

**Least privilege** – Giving an agent only the permissions it truly needs (e.g. write-draft agents cannot run commands; the read-only `git-explorer` gets only a small inspect allowlist). Fewer permissions = smaller attack surface.

**log (git log)** – The history of commits in reverse-chronological order.

**Merge** – Joins one branch's commits into another (`git merge <branch>`, from `main`). May create a merge commit.

**Personal Access Token (PAT)** – A password-like code GitHub uses for API/HTTPS auth (starts with `ghp_` for classic). Treat it like a password; scope it to the minimum.

**Prompt injection** – Malicious instructions hidden inside data (a repository file, a README, a log line) that try to make an AI or script do something unintended. Treat repo content as *data*, never as commands to run blindly.

**Pull** – Get commits from a remote and merge them into your branch (`git pull` = fetch + merge).

**Push** – Send your commits to a remote (`git push`). Needs authentication.

**Remote** – A copy of your repository on another server (GitHub, GitLab, your machine). `git clone` starts you, `git pull`/`git push` keep syncing.

**repo (repository)** – A folder Git tracks: every change is recorded as commits. A repo is the folder plus its hidden `.git` engine.

**revert (git revert)** – A *new* commit that undoes an older commit. Safe and reversible. (Contrast: `reset --hard`, which rewrites history and is avoided here.)

**Stage / staging area** – The "to-be-committed" list. `git add` puts changes there; only staged changes go into the next commit.

**status (git status)** – Shows which files are new, modified, or staged.

**Version control** – A system that keeps every version of your files so you can compare, branch, and roll back safely.