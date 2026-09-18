# Glossary: Introduction to AI Assistants

Simple definitions of the key terms used in the course. Sorted alphabetically.

**Agent / Agentic assistant** – An assistant that can *use tools* (search the web, run code, check a calendar) to accomplish a task by itself over several steps.

**API (Application Programming Interface)** – A standardized way for a program to talk to another program. In this course, the "API" is how our Python code sends a message to a language model and receives a reply.

**Chain-of-thought (CoT)** – A prompting technique where we ask the model to reason *step by step* before giving the final answer. Improves results on math, logic and analysis, and makes the reasoning visible so mistakes can be spotted.

**Context window** – The maximum amount of text the model can consider at once. It is like a person's "short-term memory": once it is full, older parts of the conversation must be removed or summarized.

**Few-shot prompting** – Giving the model a few clear input–output examples *inside* the prompt before asking it to do the same task.

**Foundation model / LLM** – A Large Language Model: a machine-learning model that has been trained on huge amounts of text and can predict/produce natural language.

**Hallucination** – When an assistant produces a confident but false answer. It "makes things up". This is a real limitation to watch out for.

**In-context learning** – A model's ability to learn from examples given inside the current prompt, without being re-trained.

**Message roles** – Labels for each message in a conversation:
- `system`: instructions about how the assistant should behave;
- `user`: what a person wrote;
- `assistant`: what the model replied.

**Persona prompting** – A prompting technique where the system message tells the model *who it is* ("You are a patient tutor for beginners"). The persona sets the tone, vocabulary and level of detail.

**Prompt** – The text you send to the model. It usually contains instructions, context, and (optionally) examples.

**RAG (Retrieval-Augmented Generation)** – A technique where the assistant first searches a database for relevant documents and then writes an answer using them. This reduces hallucinations and grounds answers in data.

**Sampling** – The process by which the model picks the next word. Because it is random, the same prompt can produce different, yet valid, answers.

**System prompt** – The part of the prompt that sets the assistant's personality, role and rules. It is the "instruction manual" for the assistant.

**Temperature** – A number (usually 0 to 2) that controls randomness. Low temperature = focused, predictable answers; high temperature = more creative, varied answers.

**Token** – The unit of text the model reads and writes. Tokens are often small word pieces, e.g. the word "assistant" could be one or two tokens. As a rough rule, **1 token ≈ 4 characters** of English text.

**Tool / function calling** – The ability of an assistant to call external functions (a calculator, a database, a web search) and use their results.

**Zero-shot prompting** – Asking the model to do a task with *no examples* in the prompt, relying only on the instruction (as opposed to few-shot prompting, which includes examples).

## Quick reference: temperature

| Temperature | Effect | Use case |
|-------------|--------|----------|
| 0 – 0.3     | Deterministic, factual, focused | Data extraction, summarization, code |
| 0.5 – 0.8   | Balanced | General chat, explanations |
| 0.8 – 1.5+  | Creative, varied | Brainstorming, stories, ideas |