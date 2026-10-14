---
layout: page
title: Subword Tokenization & Fidel Normalization
description: WordPiece vs. Byte-Level BPE vs. Unigram on MasakhaNEWS with orthographic Fidel homophone merging.
importance: 4
category: research
github: https://github.com/bedr-ux/Amharic-Sub-word-Tokenization-Algorithm-Analysis-
---

A comparative study of subword tokenization algorithms trained from scratch on MasakhaNEWS news articles, analyzing vocabulary scaling (4k–32k) and Ethiopic homophone merging (ሀ/ሐ/ኀ, ሠ/ሰ, አ/ዐ, ጸ/ፀ).

### Key Highlights
- **Algorithm Parity:** WordPiece and BPE perform identically; Unigram produces ~14% higher fragmentation.
- **Fidel Normalization:** Merging homophones and isolating punctuation reduces fertility by 8.5%.

[View GitHub Repository](https://github.com/bedr-ux/Amharic-Sub-word-Tokenization-Algorithm-Analysis-)
