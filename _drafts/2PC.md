---
layout: post
title: "Building a RAG Pipeline with LangChain"
date: 2026-03-02
categories: [AI, LangChain]
tags: [RAG, vectors, embeddings]
---

## Introduction
Hi!

Picking the wrong one costs you in latency, tokens, or reliability.

Understanding workflows and agents
A fully autonomous agent decides everything: which tools to use, what order to execute tasks, and when to stop.

A workflow provides structure: it establishes overall flow, defines checkpoints, and sets boundaries for how agents operate at each step, while still allowing dynamic behaviour within these boundaries. 

A workflow pattern gives you agent intelligence within each step, and a predictable process flows across the entire task.

### Sequential Pattern
When: For executing tasks in a fixed order.

Each agent processes an input, performs its task and passes the output to the next agent in the chain.

Pros: High predictability and easy debugging. Breaks complex patterns into manageable sub-tasks.

Cons: Higher latency, token costs can compound if context grows.

### Parallel Pattern
When: For running independent tasks across agents simultaneously. 

Their individual outputs are then aggregated or synthesised by a final “coordinator agent”.

### Evaluator-Optimizer Pattern
Goal: For outputs that need iterative refinement.

This creates a feedback loop between two distinct roles: a Generator (who produces the work) and an Evaluator (who critiques it against specific rubrics). The loop continues until a quality threshold is met.

It prevents self-bias, it fails to see it’s own mistakes.

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
