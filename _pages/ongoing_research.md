---
layout: page
title: Ongoing Research
permalink: /ongoing-research/
description: Active research initiatives, experimental benchmarks, and upcoming preprints across low-resource Semitic NLP, Ethiopic LLM tokenization, and dialect speech recognition.
nav: true
nav_order: 3
---

<style>
  .research-card {
    background: var(--global-bg-color);
    border: 1px solid var(--global-divider-color);
    border-radius: 12px;
    padding: 1.5rem;
    margin-bottom: 2rem;
    box-shadow: 0 4px 14px rgba(0, 0, 0, 0.04);
    transition: transform 0.2s ease, box-shadow 0.2s ease, border-color 0.2s ease;
  }
  .research-card:hover {
    transform: translateY(-3px);
    box-shadow: 0 8px 24px rgba(0, 0, 0, 0.09);
    border-color: var(--global-theme-color);
  }
  .research-header {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    flex-wrap: wrap;
    gap: 0.5rem;
    margin-bottom: 0.75rem;
  }
  .research-title {
    font-size: 1.3rem;
    font-weight: 700;
    margin: 0;
    color: var(--global-text-color);
  }
  .status-badge {
    font-size: 0.76rem;
    font-weight: 600;
    padding: 0.3rem 0.75rem;
    border-radius: 20px;
    letter-spacing: 0.02em;
    display: inline-flex;
    align-items: center;
    gap: 0.35rem;
  }
  .status-active {
    background: rgba(40, 167, 69, 0.12);
    color: #28a745;
    border: 1px solid rgba(40, 167, 69, 0.25);
  }
  .status-preprint {
    background: rgba(255, 193, 7, 0.15);
    color: #d39e00;
    border: 1px solid rgba(255, 193, 7, 0.3);
  }
  .status-collab {
    background: rgba(0, 123, 255, 0.12);
    color: #007bff;
    border: 1px solid rgba(0, 123, 255, 0.25);
  }
  .tag-container {
    display: flex;
    flex-wrap: wrap;
    gap: 0.4rem;
    margin: 0.85rem 0 1rem 0;
  }
  .research-tag {
    font-size: 0.74rem;
    font-weight: 600;
    padding: 0.2rem 0.65rem;
    border-radius: 15px;
    background: rgba(0, 114, 206, 0.08);
    color: var(--global-theme-color);
    border: 1px solid rgba(0, 114, 206, 0.18);
  }
  .research-body {
    font-size: 0.95rem;
    line-height: 1.6;
    color: var(--global-text-color-light);
    margin-bottom: 1rem;
  }
  .research-list {
    margin-bottom: 0.5rem;
    padding-left: 1.25rem;
    font-size: 0.93rem;
    line-height: 1.6;
  }
  .collab-banner {
    background: rgba(0, 114, 206, 0.06);
    border: 1px solid rgba(0, 114, 206, 0.2);
    border-radius: 10px;
    padding: 1.5rem;
    margin-top: 3rem;
  }
</style>

<div class="ongoing-research">

  <p class="lead" style="font-size: 1.05rem; line-height: 1.6; margin-bottom: 2rem;">
    Here is an overview of my active research projects, ongoing experimental benchmarks, and upcoming papers. My investigations center on bridging language barriers in <strong>African &amp; Semitic NLP</strong>, <strong>Ethiopic LLM tokenization efficiency</strong>, <strong>clinical RAG architectures</strong>, and <strong>dialect-robust speech technology</strong>.
  </p>

  <!-- Project 1 -->
  <div class="research-card">
    <div class="research-header">
      <h3 class="research-title">
        <i class="fa-solid fa-notes-medical text-primary mr-2"></i> Clinical RAG Assistant for Maternal &amp; Antenatal Care (ANC)
      </h3>
      <span class="status-badge status-active">
        <i class="fa-solid fa-circle" style="font-size: 0.5rem;"></i> Active Experimentation
      </span>
    </div>

    <div class="tag-container">
      <span class="research-tag">RAG Architecture</span>
      <span class="research-tag">Hybrid BM25 + FAISS</span>
      <span class="research-tag">Reciprocal Rank Fusion</span>
      <span class="research-tag">Clinical Guidelines</span>
      <span class="research-tag">Offline Edge LLMs</span>
    </div>

    <p class="research-body">
      Developing an offline-first, clinically grounded Question Answering system tailored to national Antenatal Care (ANC) guidelines for low-connectivity clinics. Evaluating hybrid retrieval against dense-only baselines to prevent semantic hallucination in critical maternal health contexts.
    </p>

    <ul class="research-list">
      <li><strong>Current Milestone:</strong> Implementing Reciprocal Rank Fusion (RRF) combining sparse lexical BM25 with dense bi-encoder embeddings to index bilingual (English &amp; Amharic) medical manuals.</li>
      <li><strong>Target Models:</strong> Local inference using quantized open-weight LLMs (Qwen2.5-0.5B, Gemma 2-2B, Aya) runnable on modest hardware.</li>
      <li><strong>Evaluation:</strong> Hit@k, Mean Reciprocal Rank (MRR), and factual precision verified against clinical case queries.</li>
    </ul>
  </div>

  <!-- Project 2 -->
  <div class="research-card">
    <div class="research-header">
      <h3 class="research-title">
        <i class="fa-solid fa-language text-info mr-2"></i> Overcoming the "Token Tax" in Ethiopic Script LLMs
      </h3>
      <span class="status-badge status-active">
        <i class="fa-solid fa-circle" style="font-size: 0.5rem;"></i> Empirical Benchmarking
      </span>
    </div>

    <div class="tag-container">
      <span class="research-tag">Subword Tokenization</span>
      <span class="research-tag">Token Tax (9.6x)</span>
      <span class="research-tag">Byte-Fallback Mitigation</span>
      <span class="research-tag">Vocabulary Surgery</span>
      <span class="research-tag">FLORES-200</span>
    </div>

    <p class="research-body">
      Investigating cross-lingual token fragmentation where English-centric models require up to 9.6x more tokens to represent equivalent Amharic text, causing context exhaustion and high inference costs.
    </p>

    <ul class="research-list">
      <li><strong>Current Milestone:</strong> Designing domain-adapted BPE and Unigram tokenizers trained on Amharic Wikipedia and news corpora with orthographic Fidel normalization.</li>
      <li><strong>Vocabulary Surgery:</strong> Injecting specialized Ge'ez script subwords into base LLM embedding layers while freezing core attention weights to preserve reasoning capabilities.</li>
      <li><strong>Key Metric:</strong> Evaluating Characters-per-Token (CPT), fertility ratio, and cross-entropy reduction on FLORES-200.</li>
    </ul>
  </div>

  <!-- Project 3 -->
  <div class="research-card">
    <div class="research-header">
      <h3 class="research-title">
        <i class="fa-solid fa-microphone-lines text-warning mr-2"></i> Parameter-Efficient ASR for Regional Amharic Dialects
      </h3>
      <span class="status-badge status-preprint">
        <i class="fa-solid fa-file-pen" style="font-size: 0.5rem;"></i> Preprint in Preparation
      </span>
    </div>

    <div class="tag-container">
      <span class="research-tag">Speech Recognition (ASR)</span>
      <span class="research-tag">OpenAI Whisper</span>
      <span class="research-tag">LoRA / PEFT</span>
      <span class="research-tag">Wollo Dialect</span>
      <span class="research-tag">Phonological Adaptation</span>
    </div>

    <p class="research-body">
      Standard speech recognition models degrade significantly when exposed to regional Ethiopian dialects. This work applies Low-Rank Adaptation (LoRA) to fine-tune OpenAI Whisper specifically for Wollo Amharic speech patterns and acoustic nuances with low computational overhead.
    </p>

    <ul class="research-list">
      <li><strong>Current Milestone:</strong> Acoustic curation and Word Error Rate (WER) / Character Error Rate (CER) benchmarking comparing zero-shot Whisper vs. PEFT adapter checkpoints.</li>
      <li><strong>Computational Efficiency:</strong> Training restricted to low-rank adapter layers on a single GPU while keeping the primary encoder-decoder backbone frozen.</li>
    </ul>
  </div>

  <!-- Project 4 -->
  <div class="research-card">
    <div class="research-header">
      <h3 class="research-title">
        <i class="fa-solid fa-chart-line text-success mr-2"></i> Bits-per-Character (BPC) Evaluation &amp; Retention in Low-Resource LoRA
      </h3>
      <span class="status-badge status-collab">
        <i class="fa-solid fa-flask" style="font-size: 0.5rem;"></i> Analysis &amp; Validation
      </span>
    </div>

    <div class="tag-container">
      <span class="research-tag">PEFT Methodology</span>
      <span class="research-tag">Bits-per-Character (BPC)</span>
      <span class="research-tag">Bootstrap CIs</span>
      <span class="research-tag">Catastrophic Forgetting</span>
      <span class="research-tag">Qwen 2.5</span>
    </div>

    <p class="research-body">
      Addressing methodological flaws in standard LLM evaluation where per-token perplexity produces skewed comparisons across tokenizers of varying vocabulary sizes. Demonstrating why Bits-per-Character (BPC) paired with 95% paired bootstrap confidence intervals provides statistically valid measurement of adaptation gains.
    </p>

    <ul class="research-list">
      <li><strong>Current Milestone:</strong> Auditing catastrophic forgetting by measuring performance drift on standard English benchmarks (ARC, MMLU) before and after Amharic domain fine-tuning.</li>
    </ul>
  </div>

  <!-- Collaboration Notice -->
  <div class="collab-banner">
    <h4 style="font-weight: 700; margin-bottom: 0.6rem;">
      <i class="fa-solid fa-handshake mr-2 text-primary"></i> Research Collaboration &amp; Compute Partnerships
    </h4>
    <p style="font-size: 0.93rem; line-height: 1.6; margin-bottom: 0.8rem;">
      I welcome collaboration with researchers, academic institutions, and organizations interested in low-resource language technologies, speech recognition for Ethiopian languages, and localized clinical AI.
    </p>
    <p style="font-size: 0.93rem; margin-bottom: 0;">
      Feel free to reach out via email at <a href="mailto:bedruy4@gmail.com"><strong>bedruy4@gmail.com</strong></a> or connect on <a href="https://scholar.google.com/citations?user=x4bGrZwAAAAJ" target="_blank" rel="noopener noreferrer"><strong>Google Scholar</strong></a>.
    </p>
  </div>

</div>
