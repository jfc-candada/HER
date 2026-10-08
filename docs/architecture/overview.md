# HER Architecture Overview

HER's architecture exists to support the musical objective.

It is not the objective itself.

The system separates authoritative state and orchestration from delegated computation, while preserving human authority over creative decisions.

## Logical layers

At a high level:

```text
                         HUMAN ARTIST
                              │
                     creative direction
                              │
                              ▼
                     PERFORMANCE INTENT
                              │
                              ▼
                     HER CORE / AUTHORITY
                 ┌────────────┼────────────┐
                 │            │            │
              State       Retrieval    Orchestration
                 │            │            │
                 └────────────┼────────────┘
                              │
                     Models / Reasoning
                              │
                              ▼
                       EDGE COMPUTATION
                              │
                              ▼
                       Audio / Workloads
```

The exact implementation can change while these responsibilities remain separated.

## Core

The Core is responsible for program-level authority and durable state.

Its responsibilities include:

- orchestration
- state reduction
- knowledge retrieval
- policy and boundary enforcement
- coordination of delegated computation

The Core does not need to perform every expensive computation itself.

## Edge

Edge resources provide delegated computational capacity.

Typical workloads include:

- local model inference
- GPU-assisted computation
- specialized media processing

Edge resources are workers, not owners of HER's authoritative state.

This permits computational hardware to change without redefining the program.

## Knowledge and retrieval

HER maintains durable working knowledge outside any individual model context.

A live read-only knowledge interface has been developed around the local Obsidian workspace.

The important architectural property is the boundary:

- the knowledge source remains authoritative;
- retrieval selects relevant material;
- the model reasons over selected evidence;
- the model does not become the owner of the knowledge.

## State

HER treats state as a first-class product.

The project has explored event-based state capture and deterministic reduction so that current state can be reconstructed from recorded observations rather than depending on conversational memory.

The architectural objective is reproducibility and inspectability.

## Audio intelligence

Audio intelligence is a distinct computational layer.

It begins with source audio and progresses through:

- decoding
- DSP feature extraction
- rhythm analysis
- harmonic analysis
- semantic representation
- retrieval
- musical reasoning

This keeps empirical audio measurements separate from higher-level interpretation.

## Authority boundary

The system follows:

> **INGESTION RETAINS. CLASSIFICATION INTERPRETS. RETRIEVAL SELECTS. LLM REASONS.**

This means a model's capability does not automatically grant it authority over:

- durable knowledge
- system state
- security policy
- execution
- creative decisions

## Local-first operation

HER is designed around local/private execution.

The public repository documents the architectural principles without publishing private network topology, host addresses, personal vault contents or operational secrets.
