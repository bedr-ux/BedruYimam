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
- **Algorithm Comparison:** Evaluates WordPiece vs. Byte-Level BPE vs. Unigram across vocabulary sizes 4,000 to 32,000.
- **Orthographic Normalization:** Empirical quantification of how homophone consolidation impacts vocabulary compression, token fertility, and downstream morphosyntactic consistency.
- **Replicable Pipeline:** Complete standalone training and evaluation script utilizing Hugging Face `tokenizers`.

[View GitHub Repository](https://github.com/bedr-ux/Amharic-Sub-word-Tokenization-Algorithm-Analysis-){: .btn .btn-sm .z-depth-0}
