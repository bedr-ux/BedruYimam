---
layout: page
title: Research & Projects
permalink: /projects/
description: Research benchmarks and empirical investigations across low-resource Semitic NLP, Ethiopic LLM tokenization, retrieval architectures, parameter-efficient fine-tuning (PEFT), and dialect speech recognition.
nav: true
nav_order: 2
---

<style>
  .projects-section {
    margin-bottom: 2.5rem;
  }
  .projects-section-title {
    font-size: 1.35rem;
    font-weight: 700;
    margin-top: 2rem;
    margin-bottom: 1.25rem;
    padding-bottom: 0.5rem;
    border-bottom: 2px solid var(--global-divider-color);
    letter-spacing: -0.01em;
  }
  .research-card {
    background: var(--global-bg-color);
    border: 1px solid var(--global-divider-color);
    border-radius: 10px;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    padding: 1.35rem 1.4rem;
    transition: transform 0.2s ease, box-shadow 0.2s ease, border-color 0.2s ease;
  }
  .research-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 8px 24px rgba(0, 0, 0, 0.08);
    border-color: var(--global-theme-color);
  }
  .research-card-title {
    font-size: 1.15rem !important;
    font-weight: 700 !important;
    text-transform: none !important;
    margin-bottom: 0.5rem;
    line-height: 1.35;
  }
  .research-card-title a {
    color: var(--global-text-color) !important;
    text-decoration: none;
  }
  .research-card-title a:hover {
    color: var(--global-theme-color) !important;
  }
  .research-card-desc {
    font-size: 0.92rem;
    line-height: 1.55;
    color: var(--global-text-color-light);
    margin-bottom: 1.1rem;
    flex-grow: 1;
  }
  .research-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 0.4rem;
    margin-bottom: 1rem;
  }
  .research-tag {
    font-size: 0.74rem;
    font-weight: 600;
    padding: 0.2rem 0.65rem;
    border-radius: 20px;
    background: rgba(0, 114, 206, 0.08);
    color: var(--global-theme-color);
    border: 1px solid rgba(0, 114, 206, 0.18);
  }
  .research-card-footer {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding-top: 0.85rem;
    border-top: 1px solid var(--global-divider-color);
    font-size: 0.88rem;
  }
  .research-link-btn {
    font-weight: 600;
    color: var(--global-theme-color) !important;
    text-decoration: none !important;
  }
  .research-link-btn:hover {
    text-decoration: underline !important;
  }
  .research-github-link {
    color: var(--global-text-color-light) !important;
    font-size: 1.25rem;
    transition: color 0.15s ease;
  }
  .research-github-link:hover {
    color: var(--global-theme-color) !important;
  }
</style>

<div class="projects">

  <!-- Section 1: LLM & Semitic NLP Research -->
  <div class="projects-section">
    <h2 class="projects-section-title">
      <i class="fa-solid fa-brain mr-2"></i> Large Language Models &amp; Semitic NLP
    </h2>
    <div class="row row-cols-1 row-cols-md-2 g-4">
      {%- assign nlp_projects = site.projects | where: "category", "research" | sort: "importance" -%}
      {%- for project in nlp_projects %}
      <div class="col mb-4">
        <div class="research-card">
          <div>
            <h3 class="research-card-title">
              <a href="{{ project.url | relative_url }}">{{ project.title }}</a>
            </h3>
            
            <div class="research-tags">
              {% if project.importance == 1 %}
                <span class="research-tag">LLM Tokenization</span>
                <span class="research-tag">FLORES-200</span>
                <span class="research-tag">Token Tax</span>
              {% elsif project.importance == 2 %}
                <span class="research-tag">RAG Retrieval</span>
                <span class="research-tag">Hybrid RRF</span>
                <span class="research-tag">Dagim QA</span>
              {% elsif project.importance == 3 %}
                <span class="research-tag">LoRA / PEFT</span>
                <span class="research-tag">Qwen 2.5</span>
                <span class="research-tag">Bits-per-Character</span>
              {% elsif project.importance == 4 %}
                <span class="research-tag">WordPiece vs BPE</span>
                <span class="research-tag">Fidel Normalization</span>
                <span class="research-tag">MasakhaNEWS</span>
              {% endif %}
            </div>

            <p class="research-card-desc">{{ project.description }}</p>
          </div>

          <div class="research-card-footer">
            <a href="{{ project.url | relative_url }}" class="research-link-btn">
              Details &amp; Findings <i class="fa-solid fa-arrow-right ml-1"></i>
            </a>
            {% if project.github %}
            <a href="{{ project.github }}" target="_blank" rel="noopener noreferrer" class="research-github-link" title="Code Repository">
              <i class="fa-brands fa-github"></i>
            </a>
            {% endif %}
          </div>
        </div>
      </div>
      {%- endfor %}
    </div>
  </div>

  <!-- Section 2: Speech Recognition & Dialect AI -->
  <div class="projects-section">
    <h2 class="projects-section-title">
      <i class="fa-solid fa-microphone-lines mr-2"></i> Dialect Speech Recognition &amp; Audio AI
    </h2>
    <div class="row row-cols-1 row-cols-md-2 g-4">
      {%- assign speech_projects = site.projects | where: "category", "speech" | sort: "importance" -%}
      {%- for project in speech_projects %}
      <div class="col mb-4">
        <div class="research-card">
          <div>
            <h3 class="research-card-title">
              <a href="{{ project.url | relative_url }}">{{ project.title }}</a>
            </h3>

            <div class="research-tags">
              <span class="research-tag">OpenAI Whisper</span>
              <span class="research-tag">PEFT / LoRA</span>
              <span class="research-tag">Wollo Dialect</span>
              <span class="research-tag">Dialect ASR</span>
            </div>

            <p class="research-card-desc">{{ project.description }}</p>
          </div>

          <div class="research-card-footer">
            <a href="{{ project.url | relative_url }}" class="research-link-btn">
              Details &amp; Findings <i class="fa-solid fa-arrow-right ml-1"></i>
            </a>
            {% if project.github %}
            <a href="{{ project.github }}" target="_blank" rel="noopener noreferrer" class="research-github-link" title="Code Repository">
              <i class="fa-brands fa-github"></i>
            </a>
            {% endif %}
          </div>
        </div>
      </div>
      {%- endfor %}
    </div>
  </div>

</div>
