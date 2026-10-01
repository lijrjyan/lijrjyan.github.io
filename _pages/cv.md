---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Education
======
**University of Wisconsin–Madison** — B.S. in Computer Science, GPA 3.885/4.0, Dean's List *(Jun 2022 – Dec 2025)*  
Coursework: Distributed Systems, Operating Systems, Databases, Computer Networks, Algorithms, Machine Learning

Experience
======
**SGLang-Omni** — Open-Source Core Contributor, Multimodal LLM Serving, supervised by Karu *(Jul 2026 – present)* · [GitHub](https://github.com/sgl-project/sglang-omni)
* Led full-duplex streaming support: maintain roadmap [#1909](https://github.com/sgl-project/sglang-omni/issues/1909), authored RFC [#2052](https://github.com/sgl-project/sglang-omni/issues/2052), designed the session architecture and implemented its core runtime ([#2035](https://github.com/sgl-project/sglang-omni/pull/2035), [#2069](https://github.com/sgl-project/sglang-omni/pull/2069), [#2070](https://github.com/sgl-project/sglang-omni/pull/2070)); drove model adaptation for Nemotron VoiceChat, MiniCPM-o, and PersonaPlex.
* Optimized the serving runtime: radix KV-cache eviction with a persistent lazy heap ([#1724](https://github.com/sgl-project/sglang-omni/pull/1724); Qwen3-TTS QPS +19%, TTFA p95 −39%) and first-audio chunk scheduling ([#1848](https://github.com/sgl-project/sglang-omni/pull/1848); TTFA p95 −24–42% at ≤8 streams, WER unchanged).
* Extended ASR serving: shared speech-to-text request/response/SSE helpers ([#1394](https://github.com/sgl-project/sglang-omni/pull/1394)); translation endpoint with capability gating ([#1453](https://github.com/sgl-project/sglang-omni/pull/1453)).
* Fixed correctness bugs: duplicate repetition penalties ([#2005](https://github.com/sgl-project/sglang-omni/pull/2005)), Qwen3-ASR 30 s truncation ([#1176](https://github.com/sgl-project/sglang-omni/pull/1176)), Qwen3-TTS termination reasons ([#1185](https://github.com/sgl-project/sglang-omni/pull/1185)).

**UW–Madison** — Capstone Project, advised by Space Science and Engineering Center *(Aug – Dec 2025)*
* Built an AIOps incident-diagnosis agent (LangGraph, FastAPI/SSE) with hybrid-retrieval RAG (nDCG@10 +42%) and replay-based evaluation.

Publications
======
* **InfraBench: Evaluating Infrastructure Agents Across Layers, Lifecycle, and Risk.** *HotInfra 2026.* [arXiv](https://arxiv.org/abs/2608.11234)
* **Harbor Adapters and Harbor-Index.** *NeurIPS 2026 (Poster).* [arXiv](https://arxiv.org/abs/2609.04298)
* **Beyond Static Policies: Exploring Dynamic Policy Selection for Single-Thread Performance Optimization.** *IEEE Computer Architecture Letters.* [arXiv](https://arxiv.org/abs/2605.05471)

Skills
======
* **Languages:** Java, Python, Go, SQL, TypeScript, JavaScript, Bash
* **Backend & Web:** Spring Boot, Django, FastAPI, React, Flowable
* **Data & Messaging:** PostgreSQL, Redis, Kafka, RabbitMQ, MQTT, Qdrant, pgvector, FAISS
* **Cloud & Infra:** AWS (Lambda, S3, SQS, DynamoDB, Step Functions), Kubernetes, Terraform, Docker, Linux
* **AI & ML:** PyTorch, Hugging Face Transformers, vLLM, SGLang, verl, OpenRLHF, LLaMA-Factory, LangGraph
