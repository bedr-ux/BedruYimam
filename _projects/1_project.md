---
layout: page
title: Amharic Tokenization Benchmark
description: Quantifying the 9.6x cross-lingual Token Tax and byte-fallback collapse across 9 LLMs on FLORES-200.
importance: 1
category: research
github: https://github.com/bedr-ux/Amharic-Tokenization-Benchmark
---

An empirical benchmark evaluating subword fragmentation, fertility ratios, characters per token (CPT), and UTF-8 byte-fallback across standard, multilingual, and Amharic-specialized LLM tokenizers on FLORES-200.

### Key Highlights
- **The 9.6x Penalty:** English-centric LLMs (Llama 3, Mistral) produce up to 9.6x token fragmentation compared to English text, driving inference latency and API cost through the roof.
- **Byte-Fallback Collapse:** 3-byte UTF-8 Ge'ez characters are decomposed into isolated byte tokens, degrading attention spans and context windows.
- **Model Comparisons:** Evaluated Llama 3 (8B/70B), Mistral NeMo, Gemma 2, Aya 23, Qwen 2.5, DeepSeek-V2, and native Amharic tokenizers.

[View GitHub Repository](https://github.com/bedr-ux/Amharic-Tokenization-Benchmark){: .btn .btn-sm .z-depth-0}
