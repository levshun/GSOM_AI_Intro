---
description: Computes descriptive statistics and writes a report. Usage: /describe file=data/house_prices.csv group=city
agent: statistician
---

Load the dataset at the given path, compute descriptive statistics for all
numeric columns and a grouped summary by the named column, then save a
beginner-friendly Markdown report to `data/reports/descriptive_stats.md`.

$ARGUMENTS

Report must include: count/mean/median/min/max/std, whether each column is
skewed, the grouped numbers, and a short "How to read this" section. Never edit
the CSV and never invent numbers.