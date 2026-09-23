# Data Analysis and Visualization - Agent Guide

This folder is the workspace for the academic course *Data Analysis and
Visualization*. It is a data-exploration project, not a software repository.

## Project layout

- `data/house_prices.csv` - the main (already clean) dataset students analyze.
- `scripts/` - Python scripts the notebook (or an agent) may generate.
- `data/plots/` - chart outputs (PNG) produced during the course.
- `data/reports/` - Markdown reports written by agents (descriptive stats, insights).

## Working rules for any assistant in this project

- The user is a learner, not an expert programmer: explain the *why* next to
  every change and keep code short, commented, and reproducible.
- Never modify `data/house_prices.csv`. Read it; write outputs to `data/plots/`
  or `data/reports/`.
- Never delete data or report files. Ask before destructive operations.
- Use a fixed `random.seed(...)` for anything generated so results are stable.
- Charts must have axis labels, a title, and units; save as PNG with white
  background so they are readable in a notebook.
- Every analysis claim must be backed by a number you can point to (mean,
  median, count, correlation). No opinion without evidence.
- Do not fetch live web data during this course; work only with the local CSV.

## Agents

- `.opencode/agent/statistician.md` - computes descriptive statistics, writes a report.
- `.opencode/agent/chartist.md` - creates matplotlib charts (may run python to save PNGs).
- `.opencode/agent/explainer.md` - turns stats + charts into a plain-language insight report.

Agent files take effect after OpenCode is restarted (configuration loads once at
startup). Reusable prompts that call these agents live in `.opencode/command/`.