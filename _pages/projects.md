---
title: "Projects"
permalink: /projects/
author_profile: true
---

## SGLang-Omni — Multimodal LLM Serving
*Open-source core contributor · Jul 2026 – present · Python, PyTorch, CUDA* · [GitHub](https://github.com/sgl-project/sglang-omni)

- **Full-duplex streaming.** Maintain the full-duplex roadmap ([#1909](https://github.com/sgl-project/sglang-omni/issues/1909)) and author its RFC ([#2052](https://github.com/sgl-project/sglang-omni/issues/2052)). Designed the session architecture and implemented the core runtime ([#2035](https://github.com/sgl-project/sglang-omni/pull/2035), [#2069](https://github.com/sgl-project/sglang-omni/pull/2069), [#2070](https://github.com/sgl-project/sglang-omni/pull/2070)). Drove model adaptation for Nemotron VoiceChat, MiniCPM-o, and PersonaPlex.
- **Runtime performance.** Radix KV-cache eviction with a persistent lazy heap ([#1724](https://github.com/sgl-project/sglang-omni/pull/1724)): Qwen3-TTS QPS +19%, TTFA p95 −39%. First-audio chunk scheduling ([#1848](https://github.com/sgl-project/sglang-omni/pull/1848)): TTFA p95 −24–42% at ≤8 streams with unchanged WER.
- **ASR serving.** Shared speech-to-text request/response/SSE helpers ([#1394](https://github.com/sgl-project/sglang-omni/pull/1394)); translation endpoint with capability gating ([#1453](https://github.com/sgl-project/sglang-omni/pull/1453)).
- **Correctness.** Fixed duplicate repetition penalties ([#2005](https://github.com/sgl-project/sglang-omni/pull/2005)), Qwen3-ASR 30 s truncation ([#1176](https://github.com/sgl-project/sglang-omni/pull/1176)), and Qwen3-TTS termination reasons ([#1185](https://github.com/sgl-project/sglang-omni/pull/1185)).

## AIOps Incident-Diagnosis Agent for Satellite Operations
*UW–Madison capstone, advised by SSEC · Aug – Dec 2025 · LangGraph, FastAPI, Qdrant, RabbitMQ*

- A LangGraph plan–execute–replan agent streamed over FastAPI/SSE. It calls structured tools through a policy-controlled backend that keeps model execution isolated from infrastructure credentials.
- A RAG pipeline over 2,359 outage notices, 16K+ data-object timestamps, operator manuals, and runbooks, using hybrid retrieval (dense + BM25, RRF, cross-encoder reranking): nDCG@10 +42%.
- Online and sandboxed offline-replay evaluation of tool-call effectiveness, task correctness, and risky actions.

## Enterprise Operations Platform
*Java 21, Spring Boot, PostgreSQL, Redis, Kafka, Flowable*

- Transactional-outbox event pipeline: SKIP LOCKED lease relay to Kafka plus idempotent consumers. 60K events were conserved at 11.8K events/s.
- Operations summary API over 1.15M rows: P95 dropped from 160 ms to 5 ms through cursor pagination, precomputed reads, and Redis cache-aside with single-flight.

## Serverless Media Processing Platform
*Python, AWS Lambda, S3, SQS, Step Functions, DynamoDB, Terraform*

- Signed multipart uploads to S3, with S3 events flowing through SQS into Step Functions FFmpeg workflows. Processing is idempotent under at-least-once delivery, using DynamoDB conditional writes and a DLQ.
- All infrastructure is managed in Terraform, with CloudWatch alarms on API P95, queue age, and DLQ depth.
