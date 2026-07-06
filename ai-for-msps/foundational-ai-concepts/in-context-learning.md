---
description: >-
  In-context learning — how large language models learn a task from a few
  examples in the prompt, with no retraining — explained for MSP operators, with
  a link to the 2020 GPT-3 paper.
---

# In-Context Learning

### Summary

**In-context learning** is the ability of a [[Large Language Models|large language model]] to perform a new task purely from instructions or examples placed in its prompt — with **no gradient updates and no retraining**. Named and demonstrated in the 2020 GPT-3 paper, it comes in three flavors: **zero-shot** (just an instruction), **one-shot** (one worked example), and **few-shot** (a handful of examples). It is the reason you can "teach" ChatGPT a format or a classification rule just by showing it a couple of samples in your message. In-context learning is also the practical foundation of **prompt engineering**.

### In plain terms

Before GPT-3, adapting a model to a task meant **fine-tuning** — collecting thousands of labeled examples and retraining a copy of the model (the [[BERT]] / [[Pretraining and Fine-Tuning]] approach). GPT-3 showed a different path: describe the task in plain language, optionally give a few examples, and the model just does it.

* **Zero-shot:** *"Classify this ticket as billing, technical, or sales: …"* — instruction only.
* **One-shot:** the instruction plus a single solved example.
* **Few-shot:** the instruction plus several solved examples the model pattern-matches against.

Nothing about the model changes — the "learning" happens entirely within the single prompt and is forgotten afterward. GPT-3 found that this ability improves dramatically as models get larger: bigger models are far better few-shot learners.

### Why it matters for MSPs

* **It is why AI tools are configurable without code.** When a PSA/RMM feature lets you steer AI behavior with a "prompt" or "instructions" box, you are using in-context learning. No data-science team required.
* **It shapes what you paste into the prompt — and the privacy stakes.** Because the model learns from what is in the prompt, staff naturally paste real client data (tickets, logs, configs) to get better answers. That is exactly the exposure the [Data Handling & Privacy](../ai-security/data-handling-and-privacy.md) and [Governance & Acceptable Use](../ai-security/ai-governance-and-acceptable-use-policies/) pages address.
* **It has real limits.** In-context learning is bounded by the model's **context window** (how much text it can consider at once) and is inconsistent — the same few examples can yield slightly different results, reinforcing the [human-in-the-loop verification](../ai-in-the-msp-stack/what-it-cant-do-yet.md) principle.
* **It is a cheaper first step than fine-tuning.** Before paying to fine-tune a model on your data, a well-crafted few-shot prompt often gets most of the way there — a useful cost lever for [implementation and ROI](../ai-in-the-msp-stack/where-it-shows-up/implementation-and-roi.md).

### Related concepts

[[Large Language Models]] · [[Pretraining and Fine-Tuning]] · [[Transformer Architecture]] · [[RLHF and Alignment]]

**In the MSP KB:** [Data Handling & Privacy](../ai-security/data-handling-and-privacy.md) · [AI vs. Automation](../ai-in-the-msp-stack/ai-vs.-automation.md)

### Contradictions & debates

* **In-context learning vs. fine-tuning.** This is the head-to-head with the [[BERT]] lineage. GPT-3 explicitly lists the downsides of fine-tuning — it needs task-specific datasets of thousands to tens of thousands of examples, and models can exploit spurious correlations in that data — and offers in-context learning as an alternative that needs neither. BERT's paradigm assumes the opposite: that fine-tuning per task is *the* way to reach state-of-the-art quality. In practice both survive; teams fine-tune when they have data and need consistency, and prompt when they need flexibility and speed.
* **Is it really "learning"?** The GPT-3 paper is careful with the term, and later researchers debate whether the model is genuinely *learning* the task or merely *retrieving and recombining* patterns already absorbed during pretraining. For MSP purposes the practical takeaway is the same: outputs are pattern-driven and must be verified.

### Source paper

Brown et al. (2020), *Language Models are Few-Shot Learners* — [https://arxiv.org/pdf/2005.14165](https://arxiv.org/pdf/2005.14165)

***

**Key terms**: _in-context learning_, _zero-shot_, _one-shot_, _few-shot_, _prompt engineering_, _context window_.
