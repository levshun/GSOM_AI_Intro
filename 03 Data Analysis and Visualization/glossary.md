# Glossary: Data Analysis and Visualization

Simple definitions of terms used in the course, sorted alphabetically.

**Agent (in OpenCode)** – A specialist assistant defined in an `.md` file under
`.opencode/agent/`, with frontmatter (description, mode, model, permissions) and
a body that is its instructions.

**AGENTS.md** – A Markdown file OpenCode reads to learn a project's rules and
layout. Every assistant working in that folder sees it.

**Bar chart** – Counts per category as bar heights. Good for "how many in each group".

**Boxplot** – Shows the median, the middle box (interquartile range) and outliers
of a numeric column. Good for comparing spread across groups.

**CATA** – A prompt recipe: C (Context), A (Action), T (Tone/format), A
(Anticipate edge cases). Add a *checkpoint* so you can verify the result.

**Central tendency** – A single "typical" value: **mean** (average), **median**
(middle value), **mode** (most frequent). In skewed data the median is usually smarter.

**Correlation** – Whether two numbers move together (positive: both up; negative:
one up, other down). Correlation is **not** causation.

**Descriptive statistics** – Numeric summaries of data: count, mean, median,
min/max, standard deviation, quartiles.

**Grouped summary** – Applying a summary per category (e.g. mean price per city)
with `df.groupby(...)`.

**Guardrail** – A rule or safety measure that stops an AI agent from doing
something risky (e.g. never delete files, never run destructive commands,
never send secrets).

**Histogram** – Bins a numeric column into ranges and shows how many fall in each;
reveals the shape/skew of the distribution.

**IQR (Interquartile Range)** – The middle 50% of the data (Q3 minus Q1). A small
IQR means values are tightly clustered.

**Least privilege** – Giving an agent only the permissions it truly needs (e.g.
a statistics agent cannot run bash). Fewer permissions = smaller attack surface.

**Mean** – The arithmetic average. Sensitive to outliers.

**Median** – The middle value when sorted. Robust to outliers; usually a better
"typical" for skewed data.

**Misleading chart** – A chart that hides or distorts truth (truncated axis,
missing labels, poor scale). Honest charts have labels and a true baseline.

**Outlier** – A value far outside the typical range. Report it; do not silently delete it.

**Prompt injection** – Malicious instructions hidden inside data (a web page,
a document) that trick an agent into doing something unintended. Real-world
reason to validate data and never paste secrets.

**Scatter plot** – One dot per row, x = one number, y = another. Shows the
relationship (correlation) between two variables.

**Skewed distribution** – When most values pile up on one side and a long tail
goes the other way (e.g. a few super-expensive houses). Mean is dragged by the tail.

**Standard deviation (std)** – How spread out the values are from the mean. Larger
= more variation.

**Value counts** – How often each distinct value occurs (`df["col"].value_counts()`).

**Visualization / plot** – Turning numbers into a picture so patterns become obvious.