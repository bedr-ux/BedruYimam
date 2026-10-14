---
layout: page
title: Parameter-Efficient Amharic LoRA
description: LoRA adaptation of Qwen2.5-0.5B on Amharic Wikipedia; evaluated with Bits-per-Character and paired bootstrap CIs.
importance: 3
category: research
github: https://github.com/bedr-ux/Amharic-LoRA-Experiment
---

An investigation into low-rank adaptation on modest compute (single Colab Tesla T4), evaluating cross-entropy with Bits Per Character (BPC) instead of flawed per-token perplexity.

### Key Highlights
- **31.1% BPC Reduction:** LoRA on attention modules ($r=16, \alpha=32$, 4.4M trainable parameters) reduced validation loss from 2.9240 to 2.0150.
- **Metric Integrity:** Proves that token-level perplexity is statistically invalid across models with differing vocabularies; replaces it with Bits-per-Character (BPC) with 95% paired bootstrap confidence intervals.
- **Catastrophic Forgetting Audit:** Evaluated English degradation on ARC-Easy to measure cross-lingual retention during low-resource target language fine-tuning.

[View GitHub Repository](https://github.com/bedr-ux/Amharic-LoRA-Experiment){: .btn .btn-sm .z-depth-0}

