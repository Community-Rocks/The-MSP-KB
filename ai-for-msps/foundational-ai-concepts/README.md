---
description: >-
  Plain-language reference pages for the foundational research concepts behind
  the AI tools in the MSP stack — transformers, attention, BERT, large language
  models, in-context learning, foundation models, and RLHF — with links to the
  original papers.
---

# Foundational AI Concepts

### Why this section exists

Elsewhere in this KB we treat AI as an **augmentation layer** and focus on how to evaluate it responsibly (see [AI in the MSP Stack](../ai-in-the-msp-stack/) and [AI Security](../ai-security/)). This section goes one layer deeper: it explains the **core research ideas** that make tools like ChatGPT, Copilot, and the "AI" features in RMM/PSA platforms work.

You do not need a machine-learning background to sell, buy, or govern these tools — but a working mental model of *why AI outputs vary*, *why models hallucinate*, and *why bigger is not automatically better* helps you separate real capability from marketing. Each page is a self-contained **entity page**: a summary, a plain-language explanation, why it matters for MSPs, related concepts, noted contradictions between the source papers, and a link to the original research.

{% hint style="info" %}
This section is **descriptive, not prescriptive**. It explains what these concepts *are* so you can understand the tools you already use — it is not a tutorial on building models.
{% endhint %}

### The five papers behind modern AI

Every mainstream AI assistant in use today descends from a short lineage of research papers. Read in order, they tell the story of how we got from spell-check to ChatGPT:

| Year | Paper | Concept it introduced | Entity page |
| ---- | ----- | --------------------- | ----------- |
| 2017 | [Attention Is All You Need](https://arxiv.org/pdf/1706.03762) | The Transformer architecture | [Transformer Architecture](transformer.md) |
| 2018 | [BERT](https://arxiv.org/pdf/1810.04805) | Bidirectional pretraining + fine-tuning | [BERT](bert.md) · [Pretraining & Fine-Tuning](pretraining-and-fine-tuning.md) |
| 2020 | [Language Models are Few-Shot Learners (GPT-3)](https://arxiv.org/pdf/2005.14165) | Scale + in-context learning | [Large Language Models](large-language-models.md) · [In-Context Learning](in-context-learning.md) |
| 2021 | [On the Opportunities and Risks of Foundation Models](https://arxiv.org/pdf/2108.07258) | The term "foundation model" | [Foundation Models](foundation-models.md) |
| 2022 | [Training LMs to Follow Instructions (InstructGPT)](https://arxiv.org/pdf/2203.02155) | Alignment via human feedback (RLHF) | [RLHF & Alignment](rlhf-and-alignment.md) |

### How the concepts connect

```
Attention ──▶ Transformer ──┬──▶ BERT (bidirectional, fine-tuned)
                            │
                            └──▶ GPT-3 / LLMs (autoregressive, in-context learning)
                                     │
                                     ├──▶ Foundation Models (the category + its risks)
                                     └──▶ RLHF / InstructGPT (aligning models to humans)
```

The [Attention Mechanism](attention-mechanism.md) is the engine; the [Transformer](transformer.md) is the machine built around it. From that same machine, two families branched: **BERT-style** models that read text bidirectionally and are *fine-tuned* per task, and **GPT-style** [large language models](large-language-models.md) that generate text left-to-right and learn tasks *in-context*. As these models grew general enough to underpin everything, the research community named the category [foundation models](foundation-models.md) — and warned about its risks. [RLHF](rlhf-and-alignment.md) was the technique that turned a raw text-predictor into a helpful assistant.

### About the `[[bracket]]` links

Related concepts on each page are written as `[[Entity Name]]` wiki-style links to signal that these pages form a small **knowledge graph**. Each bracketed name maps to a file in this folder:

| `[[Bracket]]` | File |
| ------------- | ---- |
| `[[Attention Mechanism]]` | `attention-mechanism.md` |
| `[[Transformer Architecture]]` | `transformer.md` |
| `[[BERT]]` | `bert.md` |
| `[[Pretraining and Fine-Tuning]]` | `pretraining-and-fine-tuning.md` |
| `[[Large Language Models]]` | `large-language-models.md` |
| `[[In-Context Learning]]` | `in-context-learning.md` |
| `[[Foundation Models]]` | `foundation-models.md` |
| `[[RLHF and Alignment]]` | `rlhf-and-alignment.md` |

### Where the papers disagree

These papers are a lineage, but they are not a consensus. The most useful tensions to understand:

* **Bidirectional vs. one-directional.** [BERT](bert.md) argues that reading text in both directions at once is necessary for strong language understanding and explicitly frames left-to-right-only models as limited. GPT-3 keeps the left-to-right approach and still reaches state-of-the-art results — suggesting the limitation BERT identified was not fatal.
* **Fine-tuning vs. in-context learning.** BERT's whole paradigm is *fine-tune a copy of the model for each task*. [GPT-3](large-language-models.md) pushes back, listing the downsides of fine-tuning and showing a model can often learn a task from a few examples in the prompt with **no weight updates at all**.
* **Scale vs. alignment.** GPT-3's headline is *bigger is better*. [InstructGPT](rlhf-and-alignment.md) directly complicates this: human raters preferred a **1.3B-parameter aligned model over the 175B GPT-3 — a model over 100× larger**, showing that *how* you train can beat *how big* you build.
* **Capability optimism vs. risk caution.** GPT-3 celebrates broad capability; the [foundation models](foundation-models.md) paper reframes that same generality as a concentration of risk — one flawed base model propagating its flaws to everything built on top.

Each entity page carries a **Contradictions & debates** section with the specifics.

### Start here

If you are new to the topic, read in this order: [Attention Mechanism](attention-mechanism.md) → [Transformer Architecture](transformer.md) → [Large Language Models](large-language-models.md) → [In-Context Learning](in-context-learning.md) → [RLHF and Alignment](rlhf-and-alignment.md). Then loop back to [BERT](bert.md), [Pretraining and Fine-Tuning](pretraining-and-fine-tuning.md), and [Foundation Models](foundation-models.md) for the full picture.

***

**Key terms**: _transformer_, _attention_, _large language model (LLM)_, _pretraining_, _fine-tuning_, _in-context learning_, _foundation model_, _RLHF_, _alignment_.
