---
layout: post
title: "Building a RAG Pipeline with LangChain"
date: 2026-03-02
categories: [AI, LangChain]
tags: [RAG, vectors, embeddings]
---

## Introduction
Hi!

## Patterns
* Sequential
* Parallel
* Evaluator-Optimizer

## Pattern Considerations
Understanding workflows vs. autonomous agents
- Latency
- Cost/Token usage
- Reliability

## Questions
* Can a single agent handle this task effectively? If yes, don't use workflows at all.
* Does the task have clear sequential dependencies? Use sequential workflows.
* Can subtasks be processed independently and simultaneously, and would faster completion help? Consider parallel workflows.
* Does quality improve meaningfully with iterative refinement? Consider evaluator-optimizer patterns.

# Conclusion
