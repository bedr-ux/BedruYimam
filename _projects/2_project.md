---
layout: page
title: Amharic LLM RAG Benchmark
description: Empirical evaluation of Dense, BM25, and Hybrid RRF retrieval for Amharic Question Answering on Dagim QA.
importance: 2
category: research
github: https://github.com/bedr-ux/Amharic-LLM-RAG-Benchmark
---

A systematic comparison of retrieval paradigms (FAISS dense cosine, BM25Okapi with Ethiopic punctuation isolation, and Reciprocal Rank Fusion) paired with compact LLMs (Qwen2.5-0.5B, Tiny-Aya-Earth, Amharic-LLaMA).

### Key Highlights
- **BM25 Dominance:** Sparse BM25 heavily outperforms generic multilingual dense models (Recall@3: 0.90 vs. 0.12).
- **ROUGE Evaluation Flaw:** Diagnosed that default `rouge_score` silently strips Ethiopic characters, creating misleading evaluation metrics.

[View GitHub Repository](https://github.com/bedr-ux/Amharic-LLM-RAG-Benchmark)
