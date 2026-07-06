---
description: >-
  Large language models (LLMs) — what they are, why scale matters, and where the
  "bigger is better" story breaks down — explained for MSP operators, with a
  link to the 2020 GPT-3 paper.
---

# Large Language Models

### Summary

A **large language model (LLM)** is a [Transformer Architecture](transformer.md) trained on a vast amount of text to do one deceptively simple thing: predict the next word. The 2020 paper *Language Models are Few-Shot Learners* introduced **GPT-3**, an autoregressive (left-to-right) LLM with **175 billion parameters** — roughly 10× larger than any comparable model before it. Its headline finding was that sheer scale unlocks a new ability: the model can perform many tasks it was never specifically trained for, learning them from a few examples in the prompt with **no gradient updates** (see [In-Context Learning](in-context-learning.md)). LLMs are the engine behind ChatGPT, Copilot, and most generative "AI" features now appearing in MSP tooling.

### In plain terms

An LLM is trained by covering the next word in billions of sentences and adjusting itself until its guesses are good. Do that at enormous scale and the model absorbs grammar, facts, styles, and reasoning patterns as a side effect of getting good at prediction.

GPT-3's contribution was to show what happens when you make the model *much* bigger and train it on *much* more text (hundreds of billions of words scraped largely from the web, books, and Wikipedia). Capabilities that smaller models lacked — translation, question answering, arithmetic, unscrambling words, writing news articles humans struggle to distinguish from real ones — appeared without task-specific training. GPT-3 is **decoder-only**: unlike [BERT](bert.md), it reads and writes strictly left to right, which makes it a natural text *generator*.

Importantly, the paper is candid about limits: GPT-3 sometimes only *approaches* the performance of specially fine-tuned systems, struggles on some tasks, and inherits biases and factual errors from its web training data.

### Why it matters for MSPs

* **This is what "generative AI" means.** When a tool drafts a ticket reply, summarizes a call, or writes documentation, an LLM is generating that text word by word — probabilistically. This is precisely the *probabilistic AI* the [AI vs. Automation](../ai-in-the-msp-stack/ai-vs.-automation.md) page contrasts with deterministic scripts.
* **It explains hallucination.** An LLM is optimized to produce *plausible* next words, not *true* ones. That is the mechanical reason for the "confidently wrong" answers flagged in [What It Can't Do Yet](../ai-in-the-msp-stack/what-it-cant-do-yet.md) — the model has no built-in fact-checker.
* **Scale drives cost.** 175 billion parameters is expensive to run. LLM pricing (per-token, per-seat) and latency trace back to model size, which matters when you assess [implementation and ROI](../ai-in-the-msp-stack/where-it-shows-up/implementation-and-roi.md).
* **Web-trained means data-provenance questions.** LLMs learn from scraped text of unknown licensing and accuracy — part of why [Data Handling & Privacy](../ai-security/data-handling-and-privacy.md) and vendor **no-training** guarantees deserve scrutiny.

### Related concepts

[In-Context Learning](in-context-learning.md) · [Transformer Architecture](transformer.md) · [Foundation Models](foundation-models.md) · [RLHF and Alignment](rlhf-and-alignment.md) · [BERT](bert.md)

**In the MSP KB:** [AI vs. Automation](../ai-in-the-msp-stack/ai-vs.-automation.md) · [What It Can't Do Yet](../ai-in-the-msp-stack/what-it-cant-do-yet.md)

### Contradictions & debates

* **Scale vs. alignment — the sharpest disagreement in this section.** GPT-3's thesis is that scaling up is the path to capability. The [RLHF and Alignment](rlhf-and-alignment.md) paper (InstructGPT, 2022) directly complicates it: human raters preferred the outputs of a **1.3B-parameter aligned model over the 175B GPT-3** — a model over 100× larger. Raw scale makes a model *capable*; it does not make it *helpful, honest, or harmless*. Both can be true, but the "bigger is automatically better" reading of GPT-3 does not survive InstructGPT.
* **Generation-first (GPT) vs. understanding-first (BERT).** GPT-3 keeps the left-to-right design that [BERT](bert.md) argued was a limitation — and still reaches strong, sometimes state-of-the-art results. The two lineages settled into different jobs rather than one displacing the other.
* **Capability vs. risk framing.** GPT-3 showcases broad capability; the [Foundation Models](foundation-models.md) paper (published a year later) reframes that same generality as concentrated societal risk. Same phenomenon, opposite emphasis.

### Source paper

Brown et al. (2020), *Language Models are Few-Shot Learners* — [https://arxiv.org/pdf/2005.14165](https://arxiv.org/pdf/2005.14165)

***

**Key terms**: _large language model (LLM)_, _GPT-3_, _autoregressive_, _decoder-only_, _parameters_, _next-token prediction_, _scaling_.
