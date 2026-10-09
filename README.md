# HER

## Human Episodic Runtime

**HER is an independently developed musical instrument and runtime designed to bridge natural creative intent and technical execution.**

HER began as **Goal 2**: following hospital recovery, build an independent, voice-synthesized musical instrument that could restore a meaningful connection with music where intuitive pathways had been disrupted.

**The objective is music.**

Everything else in HER exists to make that objective possible.

HER allows a performer to express musical intent naturally — in terms of genre, era, energy, atmosphere, artists, sounds, transitions and other human concepts — and turns that intent into structured, technically executable preparation for performance.

The human artist remains the authority. HER handles the technical complexity required to support the creative decision.

## From instinct to executable music

People do not experience music as databases, vectors or relational schemas.

A DJ might say:

> “I need to have 1 hour of House music, mainly from current billboard and top 90s House available in my collection, purposed for an intimate gig, and Elvis vocal samples, and 80s synth-pop samples.”

That statement contains intent, context, memory, emotion, timing and an idea of how the music should feel.

HER is being engineered to translate that human expression into evidence from the actual music collection and then into actionable performance material.

The technical path includes:

```text
Natural-language intent
        ↓
Intent interpretation
        ↓
Local music collection
        ↓
Audio ingestion
        ↓
DSP feature extraction
        ↓
CLAP semantic representation
        ↓
Similarity / retrieval
        ↓
Harmonic and phrasing constraints
        ↓
Transition reasoning
        ↓
Cue plan
        ↓
Performance-ready export
```

## A demonstrated Phase 1

The first major vertical slice has been demonstrated against a real local music collection.

Phase 1 combines audio ingestion, DSP analysis, semantic audio representation, similarity search, harmonic rules and cue-plan generation to produce standalone performance material without modifying the DJ platform's native database.

The current audio-intelligence work maps **1,626 local tracks into 512-dimensional CLAP representations**, allowing semantic relationships between tracks to be evaluated computationally.

The system combines that information with musical constraints such as harmonic compatibility and phrasing boundaries to produce explainable transition logic.

The result is not simply a list of recommended songs. It is a generated performance plan that can be exported for use by the performer.

See [Phase 1 POC](docs/music/phase-1-poc.md).

## Phase 2: the performance loop

Phase 1 establishes that HER can move from **creative intent to executable preparation**.

The next phase closes the loop.

During performance, the artist's actual decisions become evidence:

- cue changes
- skips
- transitions
- timing decisions
- extended sections
- rejected recommendations
- other performance choices

These observations are intended to become **Episodic Event Frames (EEFs)** and enter HER's persistent event state.

That creates the next development cycle:

```text
Intent
  ↓
HER recommendation
  ↓
Human performance
  ↓
Observed artistic decision
  ↓
Episodic Event Frame
  ↓
Persistent state
  ↓
Improved future recommendation
```

The objective is not to replace artistic judgement. It is to make the instrument increasingly responsive to the particular artist using it.

See [Phase 1 and Phase 2](docs/program/phase-1-and-phase-2.md).

## Why the engineering became this complex

Building the instrument exposed a problem larger than audio processing alone.

A useful musical collaborator needs to retain state, preserve context, retrieve the right information, reason over it, operate local computational resources and remain predictable when individual components fail.

That led HER into systems engineering:

- persistent state
- event-sourced reconstruction
- local knowledge retrieval
- distributed computation
- model qualification
- tool boundaries
- workload containment
- security validation
- evidence-driven testing
- structured handoffs
- controlled development queues

These are not the purpose of HER.

**They are the scaffolding required to build it.**

## Sovereign by design

HER is designed to operate locally on privately controlled hardware.

The architecture separates authoritative state and orchestration from delegated computational workloads.

A Core node owns program state and orchestration. Edge resources provide computational capacity. Models and services operate within defined boundaries rather than becoming authorities over the system.

The public architecture intentionally describes those boundaries without publishing private network addresses, host details, personal data or operational secrets.

## Public and private development surfaces

HER is being published as an open-source project after approximately one year of active development.

The public repository is the project's **maintained public engineering surface**: it presents the program, architecture, demonstrated capabilities, methodology and development direction in a form suitable for independent review and participation.

The broader private development environment contains the deeper engineering record, including detailed implementation work, operational evidence, experiments, qualification results, working-state material and environment-specific information that is not appropriate for public release.

The distinction is deliberate.

The public project represents the maintained software and its engineering principles. The private development environment retains the deeper evidence and working material from which the public project has been developed.

**Publicly published does not mean newly created. It is the public release of an already active program of work.**

## Development knowledge and collaboration

HER is developed against a durable local knowledge environment rather than against isolated AI sessions.

Development notes, handoffs, testing and qualification records, architecture and security decisions, risk analysis, schematics and active work queues are maintained as structured working knowledge. Appropriate material is synchronized into the repository as the maintained software and documentation surface.

The local HER environment can provide selected knowledge to local language-model components under explicit retrieval and authority boundaries. The online repository provides the corresponding durable collaboration surface for external engineering and tools such as Codex.

The result is deliberate continuity across human work, local reasoning and repository history without treating any one model session as the system of record.

See [Knowledge and Development Surfaces](docs/methodology/knowledge-and-development-surfaces.md) and [Public Release Boundary](docs/program/public-release-boundary.md).

## Engineering principles

**State is the product, not the graph.**

Durable state is treated as a reconstructable system product rather than something owned by an individual model or interface.

**Containment first, optimization second.**

Capabilities are constrained before they are optimized.

**Evidence before promotion.**

A successful demonstration is not automatically a qualified component.

**Human authority remains external to the model.**

A model can reason or propose an action without acquiring authority to make that decision.

**Local-first means the creative workflow should remain useful without cloud dependency.**

## Development method

HER has been developed through successive experiments rather than from a fixed architecture.

The progression has included constrained local model experiments, audio processing, GPU execution, distributed Core/Edge architecture, persistent knowledge, live retrieval, security validation, qualification and orchestration.

The process used to develop HER has itself become part of the engineering.

Persistent working knowledge, structured handoffs, queues, repository state and evidence are used to maintain direction across development sessions.

See:

- [Development Method](docs/methodology/development-method.md)
- [Continuity and Handoffs](docs/methodology/continuity-and-handoffs.md)
- [Qualification and Evidence](docs/methodology/qualification-and-evidence.md)
- [Architecture Overview](docs/architecture/overview.md)

## Current program state

HER has established verified elements of the foundation including:

- Core system smoke testing
- WAVE audio ingestion
- DSP feature extraction
- local hardware acceleration
- security validation
- live knowledge retrieval
- semantic audio representation
- Phase 1 music-processing work

The next major development stage is the Phase 2 performance loop and the reasoning/orchestration integration required to make that loop operational.

HER remains an active engineering program. Architecture and implementation continue to evolve as evidence from implementation and performance feeds back into the design.

## The purpose remains simple

**Build the instrument.  
Make the music.**
