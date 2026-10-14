---
layout: page
title: Amharic Tokenization Benchmark
description: Quantifying the 9.6x cross-lingual Token Tax and byte-fallback collapse across 9 LLMs on FLORES-200.
img: assets/img/publication_preview/flores_token.png
importance: 1
category: research
github: https://github.com/bedr-ux/Amharic-Tokenization-Benchmark
---

An empirical benchmark evaluating subword fragmentation, fertility ratios, characters per token (CPT), and UTF-8 byte-fallback across standard, multilingual, and Amharic-specialized LLM tokenizers on FLORES-200.

### Key Highlights
- **The 9.6x Penalty:** Standard Llama-3-8B requires ~9.6x more tokens per word for Amharic than English, collapsing to 0.91 tokens/byte (effectively single-byte fallback on 3-byte Ge'ez characters).
- **Specialization Gains:** Dedicated Amharic tokenizers (Llama-3.2-1B-Amharic) cut fertility from 11.9 to 1.75 while maintaining English efficiency.

[View GitHub Repository](https://github.com/bedr-ux/Amharic-Tokenization-Benchmark)
