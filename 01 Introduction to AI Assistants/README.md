# Introduction to AI Assistants

## What you will learn

By the end of the course you will be able to:

- Explain what an AI assistant is and how it differs from a traditional chatbot.
- Describe how a Large Language Model (LLM) works in simple terms (tokens, context, sampling).
- Apply prompt engineering fundamentals: prompt anatomy, few-shot, persona, chain-of-thought and iterating on prompts.
- Understand how assistants "remember" a conversation and why context is limited.
- Use key parameters such as temperature and understand what they control.
- Use AI to find, summarize and explain academic sources responsibly.
- Recognize advanced capabilities (tools, retrieval/RAG, agents), including the agent loop in action via the OpenCode assistant the course itself is built with.
- Understand the main limitations and ethical risks of AI assistants.

## Structure (4 parts = 4 academic hours)

| Part | Hour | Topic |
|------|------|-------|
| 1 | 1 | What is an AI assistant? The big picture and core concepts |
| 2 | 2 | Prompt engineering fundamentals: roles, temperature, few-shot, persona, chain-of-thought, iteration |
| 3 | 3 | Building an assistant interface: conversation and memory |
| 4 | 4 | Advanced capabilities (tools, RAG, agents), the OpenCode agent in action, academic sources, limits and ethics |

## Files in this catalog

| File | Purpose |
|------|---------|
| `Introduction to AI Assistants.ipynb` | The main course notebook. Run it cell by cell. It includes explanatory charts (tokens & cost, temperature/sampling, context-window growth, sentiment analysis) drawn with matplotlib. |
| `glossary.md` | Dictionary of key terms used in the course. |
| `README.md` | This file: course overview and instructions. |

## How to use the notebook

1. Open `Introduction to AI Assistants.ipynb` in Jupyter.
2. Run cells in order using `Shift + Enter`. Markdown cells explain the theory.
3. The notebook works **out of the box** with no internet and no API key:
   a built-in "teaching assistant" simulates a language model so every
   example is reproducible and free.
4. **Optional (Part 3):** if your teacher provides an API key, set
   `RUN_LIVE = True` in the notebook to connect a real language model.
   Leave it `False` otherwise - nothing extra needed.

## Requirements

The notebook runs entirely in the standard Python library, so it works in any
Python 3 environment with no extra packages. The optional live-model cell in
Part 3 uses the `openai` package (pre-installed in this course environment);
leave `RUN_LIVE = False` and you will not need it.