# Data Collection & Cleaning - Agent Guide

This folder is the workspace for the academic course *Data Collection &
Cleaning*. It is a data-wrangling project, not a software repository.

## Project layout

- `data/messy_customers.csv` - the messy dataset you will clean (Part 3).
- `data/sample_market.html` - a local HTML snapshot used to practise web
  collection conceptually (Part 3). Never fetch a live site during the course.
- `data/messy_products.csv` - (optional) extra messy file generated with the
  assistant in Part 1.
- `data/generated/` - synthetic datasets produced from deterministic scripts.
- `data/ai/` - datasets produced with the help of an LLM (via OpenCode).
- `data/cleaned/` - cleaned outputs, with `_clean` and `_report` suffixes.

## Working rules for any assistant in this project

- The user is a learner, not an expert programmer: explain the *why* next to
  every code change and keep code short, commented, and reproducible.
- Never modify `data/messy_customers.csv` or `data/sample_market.html` in
  place. Read them, write results to `data/cleaned/` or `data/generated/`.
- Never delete data files. Ask before destructive operations.
- Use a fixed `random.seed(...)` for anything synthetic so results are
  reproducible.
- Every cleaning step should be reported: what was wrong, what was changed,
  how many rows were affected.
- Do not call external network APIs or scrape live websites during this course.

## Agents

- `.opencode/agent/data-cleaner.md` - cleans messy tabular data, reports actions.
- `.opencode/agent/data-generator.md` - designs and writes synthetic-data scripts.
- `.opencode/agent/cleaning-reviewer.md` - reviews cleaned data and writes a report.

Agent files only take effect after OpenCode is restarted (config is loaded at
startup). See `opencode.json` / `opencode.config.json` docs or the course
notebook for details.