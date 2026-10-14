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
- **BM25 Dominance:** Sparse lexical retrieval (BM25Okapi) outperforms pure dense semantic embeddings by **+25.3% Hit@3** due to sparse Ge'ez pre-training in standard embedding models.
- **Hybrid RRF Synergy:** Reciprocal Rank Fusion combines the lexical precision of BM25 with dense semantic search, yielding the highest overall Hit@3 and MRR.
- **Rigorous Evaluation:** Tested against the Dagim QA dataset using Hit@k, MRR, Mean Cosine Similarity, and Token Cost metrics.

[View GitHub Repository](https://github.com/bedr-ux/Amharic-LLM-RAG-Benchmark){: .btn .btn-sm .z-depth-0}
