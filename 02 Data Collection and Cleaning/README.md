# Data Collection & Cleaning

This course is **interactive**: you learn by using the AI agent that runs on this
server (**OpenCode**). You will configure assistants as Markdown files
(`AGENTS.md` and `.opencode/agent/*.md`), write and refine prompts, and analyze
the results - data tables, cleaning reports, and the agent's own behavior.

## What you will learn

- How data enters a project: **synthetic data**, **web data** (conceptually), and **existing messy files**.
- How to design a schema and generate reproducible synthetic data.
- The mechanics of web collection (HTTP, HTML, robots.txt) and why we practise on a local snapshot, never live sites.
- A systematic **cleaning** workflow: inspect, normalize, dedupe, parse, flag outliers - with numbers before and after.
- How to "hire" an AI agent: create `AGENTS.md` and `.opencode/agent/*.md` files, restart OpenCode, write a good prompt, and **verify** the result with checks (prompts are only the beginning - analysis matters).
- How to write your own new agent `.md` file and load it with a restart.
- How to combine generation -> cleaning -> validation into one little pipeline and evaluate quality quantitatively.

## Structure (4 parts = 4 academic hours)

| Part | Hour | Topic |
|------|------|-------|
| 1 | 1 | Team up with an agent: tidy data, AGENTS.md, agent `.md` files, prompt writing |
| 2 | 2 | Synthetic data with AI: schemas, generators, prompts, compare script-vs-AI output |
| 3 | 3 | Collect web data (conceptually) and clean messy data step by step |
| 4 | 4 | Pipeline + results analysis: validation, an AI review report, ethics and take-away |

## Files in this catalog

| File | Purpose |
|------|---------|
| `Data Collection & Cleaning.ipynb` | The main course notebook: theory, interactive OpenCode tasks, and checkpoints. |
| `AGENTS.md` | Project-level instructions that any assistant sees when working in this folder. |
| `.opencode/agent/data-cleaner.md` | Example agent: cleans data and reports actions. |
| `.opencode/agent/data-generator.md` | Example agent: writes synthetic-data generators. |
| `.opencode/agent/cleaning-reviewer.md` | Example agent: reviews cleaned data, writes a report. |
| `.opencode/command/make-synthetic.md` | Example reusable prompt command. |
| `data/messy_customers.csv` | The messy dataset you clean in Part 3. |
| `data/sample_market.html` | Local HTML snapshot used for the conceptual web part. |
| `data/generated/` | Deterministic synthetic outputs (scripts in the notebook). |
| `data/ai/` | Outputs created with the assistant (your task). |
| `data/cleaned/` | Cleaned outputs and reports (Part 3-4). |
| `glossary.md` | Dictionary of data + AI terms used in the course. |
| `README.md` | This file. |

## How to use the notebook

1. Open `Data Collection & Cleaning.ipynb`.
2. Run cells in order. **Markdown cells** contain theory and, in green boxes,
   *Your turn: OpenCode* tasks - a prompt to paste to your AI assistant in the
   chat panel (the same way this course was made).
3. **Checkpoint cells** verify that the expected file or result appeared, and
   analyze it. If you skip an OpenCode task, the copy also provides a
   deterministic fallback so the notebook still works offline.
4. When you create or edit agent files, **quit and restart OpenCode** - agent
   configuration is loaded only at startup.
5. The course deliberately does **not** fetch live websites: web collection is
   taught against a local HTML snapshot.

## Requirements

Python 3.12 with the preinstalled data-science stack (`pandas`, `numpy`,
`matplotlib`) plus `beautifulsoup4` (all present in this environment). No API
key and no internet are required. OpenCode itself is used only through the chat
interface on this server; no separate install is needed.
