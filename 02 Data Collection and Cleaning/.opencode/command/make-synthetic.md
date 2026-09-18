---
description: Generates a synthetic dataset. Usage: /make-synthetic rows=200 file=data/ai/customers_ai.csv
agent: data-generator
---

Create a Python generator that builds a synthetic customer dataset and saves it
to the named file. Use `random.seed(42)` and pandas.

Schema: `customer_id, name, email, country, age, signup_date, spend`.

- `customer_id`: sequential `C0001`... format
- `name`: realistic first + last name placeholders
- `email`: matches the name (no real addresses)
- `country`: one of a small realistic list
- `age`: 18-90
- `signup_date`: recent ISO dates
- `spend`: positive dollars to two decimals

Write approximately $ARGUMENTS rows. Return schema assumptions and the first 3
rows. Never access the network.