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
- **31.1% BPC Reduction:** LoRA on attention modules ($r=16, \alpha=32$, 0.44% trainable weights) cuts Amharic BPC from 6.16 to 4.25 in 13 minutes.
- **Quantified Catastrophic Forgetting:** English BPC degrades by 18.8%, empirically establishing the cross-lingual plasticity-stability trade-off.

[View GitHub Repository](https://github.com/bedr-ux/Amharic-LoRA-Experiment)
