# H.E.R.
## Human Episodic Reasoning // The Human Experience Runtime

H.E.R. is an independently developed musical instrument and sovereign runtime intended to bridge natural creative intent and the technical work required to prepare and support music performance.

The objective is music.

Everything else in H.E.R. exists to make that objective possible.

H.E.R. began as Goal 2: following hospital recovery, build an independent, voice-synthesized musical instrument that could restore an essential connection with music where intuitive pathways had been disrupted. The instrument is designed to let a performer express intent in human terms — genre, era, energy, atmosphere, artists, sounds, transitions and context — and translate that intent into structured preparation for performance.

The performer remains the artistic authority. H.E.R. is intended to handle technical complexity, provide evidence-based reasoning and stage useful choices without replacing the human decision.

## From instinct to structured musical preparation

People do not experience music as database queries, mathematical vectors or relational schemas. A DJ might ask for an hour of House music drawn from a particular collection, combining current tracks with 1990s House, and shaped for a specific room, mood or set.

That request contains intent and context that must be interpreted against the actual music available to the performer.

H.E.R.'s intended processing path is:

```text
Natural creative intent (including voice)
        ↓
Intent interpretation and constraints
        ↓
Local music acquisition and audio ingestion
        ↓
Measured acoustic and musical evidence
        ↓
Semantic representation and retrieval
        ↓
Harmonic, rhythmic and phrase reasoning
        ↓
Structured transition and cue preparation
        ↓
Human performance and artistic decisions
        ↓
Observation and episodic learning (Phase 2)
```

The objective is not an algorithmic auto-DJ. It is an instrument that can become more responsive to the individual performer's methods and preferences while leaving creative authority with that performer.

## Phase 1: a substantive musical proof of concept

Phase 1 established a musical proving ground beyond BPM detection or isolated audio-feature evaluation.

The documented proof of concept exercised a processing path across a local collection reported as 1,626 tracks:

1. **Intent and retrieval** — translate a musical request into constraints and retrieve relevant material from the local collection.
2. **Audio ingestion** — decode local WAVE/audio files, with Pedalboard identified as the primary decoding path and a compatibility fallback.
3. **Signal analysis** — extract and assess measurable audio features using Librosa and Essentia, including tempo/rhythm and harmonic information.
4. **Musical interpretation** — evaluate tempo relationships, key and mode, confidence, harmonic compatibility and phrase relationships.
5. **Semantic representation** — generate 512-dimensional CLAP representations for text/audio similarity and candidate discovery.
6. **Selection and reasoning** — combine retrieved candidates with musical, harmonic and phrase constraints to reason about transitions.
7. **Structured delivery** — produce machine-readable, schema-oriented and JSON-based representations alongside cue/transition preparation and performance-oriented exports.

This is important because the POC exercised a connected musical workflow: **intent → ingestion → measurement → representation → retrieval → reasoning → structured output**. The schema and JSON work is part of that delivery path, not an incidental BPM-analysis result.

The POC documentation describes the demonstrated workflow and its evidence. It does not, by itself, qualify every subsystem for production use or establish that the wider HER runtime is fully integrated.

See [Phase 1 Proof of Concept](docs/music/phase-1-poc.md) and [Phase 1 and Phase 2](docs/program/phase-1-and-phase-2.md).

## The wider system: Core, Edge and delivery

The musical POC exposed a larger systems-engineering problem. A complete instrument must not only analyse tracks; it must retain authoritative state, preserve context, ingest and validate structured information, retrieve relevant knowledge, coordinate work, communicate with delegated compute, and deliver dependable outputs to the performer.

The architecture separates authority from execution:

- **Core** is intended to own authoritative state, orchestration, policy, retrieval and the coordination of work.
- **Edge** provides delegated compute for workloads such as local model inference and GPU-accelerated processing. Edge execution does not make Edge the authority for HER state.
- **The performer** remains the authority for artistic decisions.
- **Evidence and qualification** determine whether a capability is ready to be relied upon; a design or successful demonstration is not automatically an accepted operational component.

The wider Core and delivery programme includes work at different levels of maturity. Areas of design and development include:

- ingestion of structured events and subsystem observations into Core;
- schema and JSON contract definition, validation and version compatibility;
- durable state capture and deterministic reconstruction;
- retrieval and delivery of relevant context to the right workstream or consumer;
- Core-to-Edge communication and delegated workload handling;
- orchestration, policy and execution boundaries;
- evidence capture, handoffs and acceptance criteria;
- integration of musical reasoning and structured performance outputs;
- the later live-performance observation and Episodic Event Frame (EEF) learning loop.

These are not all completed merely because the Phase 1 musical path has been demonstrated. Some have design records, experiments or partial implementations; the extent of end-to-end integration and operational qualification remains subject to evidence and acceptance.

See [Architecture Overview](docs/architecture/overview.md), [Development Method](docs/methodology/development-method.md) and [Qualification and Evidence](docs/methodology/qualification-and-evidence.md).

## Four areas of musical processing

The musical processing model can be understood as four cooperating areas. The descriptions below express the system's functional model; they should not be read as a claim that every stage is currently production-qualified.

| Area | Responsibility | Examples |
|---|---|---|
| **Ingestion** | Acquire audio while preserving source material and provenance | Local WAVE/audio decoding, PCM data |
| **Classification** | Derive measurable acoustic and musical evidence | Tempo, rhythm, chroma, key/mode estimates, loudness and confidence |
| **Retrieval** | Find relevant tracks and musical material | Local collection search, CLAP semantic representations and similarity |
| **Reasoning** | Evaluate musical relationships and prepare choices | Harmonic compatibility, tempo relationships, phrase alignment, transition and cue plans |

The separation between measurement and interpretation is deliberate. An estimate, confidence value or inferred relationship should not be represented as raw source truth. Where evidence is insufficient, the system should preserve uncertainty rather than invent a result.

## Phase 2: learning from performance

Phase 1 concentrates on preparation: interpreting intent, finding music, analysing it and producing structured material that can support a performance.

Phase 2 extends the system into the live performance context. The intended loop observes human interventions — for example, timing changes, EQ adjustments, delayed drops or loop changes — and represents relevant observations as Episodic Event Frames (EEFs). Those records can contribute to persistent memory and future recommendations.

This learning loop is a development objective, not a claim that a complete live observation and recommendation pipeline is already operational.

The human performer remains in control throughout. Observation is intended to improve assistance, not to transfer artistic authority to the system.

## Sovereignty and containment principles

H.E.R. is designed around local control of its creative workflow, data and compute. Its architecture distinguishes the Core authority host from delegated Edge compute and treats network, filesystem and workload containment as engineering requirements.

The design intent is to avoid dependence on external cloud services for the core creative workflow. Specific isolation, firewall, transport and startup controls must be described according to their implementation and verification evidence; an architectural boundary or security design is not, by itself, proof that every runtime path is secured.

The public architecture intentionally avoids publishing private network addresses, host credentials, personal records, proprietary implementation details or environment-specific telemetry.

See [Architecture Overview](docs/architecture/overview.md) and [Public Release Boundary](docs/program/public-release-boundary.md).

## Development method and evidence

H.E.R. is developed through successive experiments, durable engineering records, explicit workstream boundaries and evidence-based promotion.

The project distinguishes the following states:

- **Designed** — the requirement, architecture or intended behaviour is documented.
- **POC-demonstrated** — a capability has been exercised in a proof-of-concept context under recorded conditions.
- **Implemented** — an implementation exists in the relevant development surface.
- **Tested** — defined tests or experiments have been executed and their results recorded.
- **Integration in development** — components or contracts are being connected, with end-to-end acceptance still outstanding.
- **Operationally qualified** — the defined acceptance conditions have been met and supported by appropriate evidence.

These states are not interchangeable. A successful experiment does not establish production readiness; a source file does not establish runtime integration; and a design statement does not establish implementation.

Development notes, architectural decisions, handoffs, qualification records and work queues are maintained as durable, human-readable project knowledge. Repository history and test evidence support continuity across human and AI-assisted engineering sessions; no single chat session is treated as the system of record.

See:

- [Development Method](docs/methodology/development-method.md)
- [Continuity and Handoffs](docs/methodology/continuity-and-handoffs.md)
- [Knowledge and Development Surfaces](docs/methodology/knowledge-and-development-surfaces.md)
- [Qualification and Evidence](docs/methodology/qualification-and-evidence.md)

## Current program state

H.E.R. is an active engineering programme. The Phase 1 musical proof of concept provides substantive evidence for a connected audio-to-musical-preparation workflow, including ingestion, DSP, rhythm and harmonic analysis, semantic representation, retrieval, reasoning, schema-oriented structured output and performance preparation.

The complete H.E.R. instrument is still under development.

The remaining programme is broader than the Phase 2 live-learning loop. It includes the Core ingestion and state model, contract and schema integration, retrieval/context delivery, orchestration and policy, Core-to-Edge coordination, integration of the musical capabilities, and evidence-backed acceptance of the resulting end-to-end system.

Current public documentation does not establish a defensible completion date for that wider programme. A time-to-completion estimate should follow a reconciled inventory of remaining work, dependencies, integration boundaries and acceptance evidence — not be inferred from the existence of the POC or from milestone labels alone.

## Public and private development surfaces

The public repository, [jfc-candada/HER](https://github.com/jfc-candada/HER), is the curated public engineering surface. It presents the instrument's purpose, architecture, demonstrated capabilities, methodology and development direction for peer review and technical collaboration.

The broader private development environment retains proprietary implementation details, differentiated mathematical formulations, detailed operational topology, private test evidence, forensic records and environment-specific working material.

The distinction is deliberate. Public documentation should explain what H.E.R. is, what it has demonstrated and how the programme is structured without unnecessarily disclosing the proprietary mechanisms or private operational record.

See [Public Release Boundary](docs/program/public-release-boundary.md).

## Repository navigation

```text
HER/
├── README.md
└── docs/
    ├── architecture/
    │   └── overview.md
    ├── methodology/
    │   ├── continuity-and-handoffs.md
    │   ├── development-method.md
    │   ├── knowledge-and-development-surfaces.md
    │   └── qualification-and-evidence.md
    ├── music/
    │   └── phase-1-poc.md
    └── program/
        ├── phase-1-and-phase-2.md
        ├── public-release-boundary.md
        └── purpose-and-origin.md
```

## Engineering principles

1. **The objective is the instrument.** Infrastructure exists to support music creation and performance.
2. **The performer retains authority.** H.E.R. can reason, recommend and prepare; artistic decisions remain human.
3. **Evidence precedes interpretation.** Measured facts, estimates, confidence and reasoning must remain distinguishable.
4. **State must be durable and reconstructable.** State ownership, event capture and recovery are explicit architectural concerns.
5. **Containment precedes optimization.** Compute, network and filesystem boundaries must be established and verified.
6. **Demonstration is not qualification.** Capabilities are promoted only when their defined acceptance evidence supports that status.
7. **Continuity is an engineering requirement.** Decisions, evidence and workstream state belong in durable project records, not solely in transient conversations.

## The purpose remains simple

**Build the instrument.  
Make the music.**
