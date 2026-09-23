# Data Analysis and Visualization

A **4 academic hour** interactive course for students who do **not** have a
strong IT background. Everything is in English, explained in plain language with
analogies, worked examples, and code you can run.

Like the sister courses (*Introduction to AI Assistants*, *Data Collection &
Cleaning*), this one is taught in practice: you **learn by doing** with the AI
assistant that runs on this server (**OpenCode**). You configure specialist
agents as Markdown files, write prompts, run the code, and analyze the results -
both the numbers and the assistant's claims.

## What you will learn

- The classic analysis pipeline: clean data -> describe -> visualize -> explain.
- **Descriptive statistics**: central tendency, spread, grouped summaries, and
  when to trust the mean vs the median.
- **Plots and charts**: histograms, boxplots, bar charts, scatter plots - and how
  to read them and spot misleading ones.
- How to **instruct an AI** (prompts + agents) to do statistics, make charts, and
  explain the results - then **verify** its work with your own checks.
- How to configure agents in `.md` files (`AGENTS.md`, `.opencode/agent/*.md`),
  write reusable prompt commands, and analyze the outputs for real.
- Analysis ethics: correlation vs causation, evidence-based statements, honest charts.
- **Agent security & teamwork**: extra agent-to-agent interactions (peer review, chart audit, quiz me) and real-world guardrails, from least-privilege agents to prompt-injection awareness.

## Structure (4 parts = 4 academic hours)

| Part | Hour | Topic |
|------|------|-------|
| 1 | 1 | Hire your analyst team: tidy data, `AGENTS.md`, agent `.md` files, prompts, first look at the data |
| 2 | 2 | Descriptive statistics with AI: numbers, shape, groups, mean vs median |
| 3 | 3 | Plots and charts: matched chart types, honest visualization |
| 4 | 4 | Explaining results: insight report, verifying the AI's claims, ethics + agent security and teamwork |

## Files in this catalog

| File | Purpose |
|------|---------|
| `Data Analysis and Visualization.ipynb` | The main course notebook (theory + OpenCode tasks + checkpoints). |
| `AGENTS.md` | Project rules any assistant sees in this folder. |
| `.opencode/agent/statistician.md` | Agent: descriptive statistics and stats reports. |
| `.opencode/agent/chartist.md` | Agent: matplotlib charts saved as PNG. |
| `.opencode/agent/explainer.md` | Agent: plain-language insight reports. |
| `.opencode/command/describe.md` | Reusable command: run the statistician. |
| `.opencode/command/visualize.md` | Reusable command: run the chartist. |
| `data/house_prices.csv` | The clean dataset used throughout. |
| `data/plots/` | Chart outputs (students + notebook generate them). |
| `data/reports/` | Stats/insight reports (students + agents generate them). |
| `scripts/` | Helper scripts produced during the course. |
| `glossary.md` | Dictionary of data + AI terms. |
| `README.md` | This file. |

## How to use the notebook

1. Open `Data Analysis and Visualization.ipynb` and run cells in order.
2. Green boxes titled **Your turn: OpenCode** contain ready-made prompts. Paste
   them into the chat; when the agent finishes, run the **checkpoint code cells**
   that verify and analyze the result.
3. Every task has a deterministic fallback, so the notebook works fully offline.
4. When you create or change agent files, **quit and restart OpenCode** (agent
   config is loaded once at startup).
5. We never fetch live data: everything uses the local `house_prices.csv`.

## Requirements

Python 3.12 with the preinstalled data-science stack (`pandas`, `numpy`,
`matplotlib`) - all present in this environment. No API key or internet needed.
OpenCode is used through the chat interface already available on the server.