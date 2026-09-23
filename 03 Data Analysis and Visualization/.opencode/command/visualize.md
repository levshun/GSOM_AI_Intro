---
description: Creates charts for a dataset and saves them as PNG. Usage: /visualize file=data/house_prices.csv
agent: chartist
---

Load the dataset, create a small set of clear matplotlib charts that answer
interesting questions about it, and save each as PNG under `data/plots/`.

$ARGUMENTS

Recommended set: a histogram of the main numeric column, a boxplot by a
categorical column, and a scatter plot of two related numbers. Every chart must
have a title and labeled axes. Return the file names and a one-line reading of
each. Never edit the source CSV.