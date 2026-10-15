H.E.R.
Human Episodic Reasoning // The Human Experience Runtime

H.E.R. is an independently developed musical instrument and sovereign runtime engineered to bridge natural creative intent and technical execution.

H.E.R. (spoken phonetically as "HER") began as Goal 2: following hospital recovery, build an independent, voice-synthesized musical instrument that could restore an essential connection with music where intuitive pathways had been disrupted. Rooted in 35 years of systems software engineering and 25 years of global enterprise IT infrastructure leadership (including Citigroup Canada, GE, and Macquarie Group), the program enforces strict architectural rigor, deterministic state recovery, and physical hardware sovereignty.

The objective is music.

Everything else in H.E.R. exists to make that objective possible.

H.E.R. allows a performer to express musical intent naturally — in terms of genre, era, energy, atmosphere, artists, sounds, transitions, and other human concepts — and turns that intent into structured, technically executable preparation for performance.

The human artist remains the absolute authority. H.E.R. handles the technical complexity required to support the creative decision.
From Instinct to Executable Music

People do not experience music as database queries, mathematical vectors, or relational schemas.

A DJ might say:

    “I need to have 1 hour of House music, mainly from current billboard and top 90s House available in my collection, purposed for an intimate gig, with Elvis vocal samples, and 80s synth-pop samples.”

That statement contains intent, context, memory, emotion, timing, and an idea of how the music should feel.

H.E.R. is engineered as a rapid episodic reasoning translator. It decodes natural human expression into empirical acoustic evidence from the local music collection, evaluates harmonic and phrase compatibility in milliseconds, and outputs a performance-ready transition plan — all while protecting the artist’s natural groove and live "swing."

Human Intent (Voice / Abstract Vibe)
  ↓
Acoustic & Semantic Evidence Acquisition (Pedalboard C++ / DSP / CLAP)
  ↓
Episodic & Harmonic Reasoning (Camelot Wheel / 32-Beat Phrase Lock)
  ↓
Phase 1: Performance Preparation (Vendor-Neutral USB Cue Export)
  ↓
Human Live Performance
  ↓
Observed Artistic Interventions (Manual EQs, Delayed Drops, Loop Shifts)
  ↓
Episodic Event Frame (EEF) Generation
  ↓
Deterministic Event Sourcing (event_log.jsonl)
  ↓
Phase 2: Enriched Memory & Improved Future Recommendations

The objective is not to replace artistic judgement or create an algorithmic "auto-DJ." It is to make the instrument increasingly responsive to the unique style of the particular artist using it.

See Phase 1 and Phase 2 and Purpose and Origin.
The Four-Stage Epistemic Processing Pipeline

To maintain strict epistemic integrity, H.E.R. enforces a hard separation between empirical evidence and downstream interpretation:

┌──────────────────────────┬──────────────────────────┬──────────────────────────┬──────────────────────────┐
│    STAGE 1: INGESTION    │  STAGE 2: CLASSIFICATION │    STAGE 3: RETRIEVAL    │    STAGE 4: REASONING    │
│    INGESTION RETAINS     │ CLASSIFICATION INTERPRETS│    RETRIEVAL SELECTS     │    REASONING DECIDES     │
│  Spotify Pedalboard C++  │  Librosa & Essentia DSP  │ 512-D CLAP Vector Space  │    Musical Reasoning     │
│         Engine           │                          │                          │       Engine (MRE)       │
├──────────────────────────┼──────────────────────────┼──────────────────────────┼──────────────────────────┤
│ • Ingests raw local      │ • Measures empirical     │ • Embeds tracks onto     │ • Validates Camelot      │
│   WAVE/audio files       │   BPM & tempo grid       │   unit hypersphere       │   wheel key transitions  │
│ • Memory-safe O(1)       │ • Evaluates Krumhansl-   │ • Sub-millisecond SIMD   │ • Aligns 32-beat phrase  │
│   streaming decoding     │   Schmuckler profiles    │   dot-product matching   │   boundaries             │
│ • Extracts stable        │ • Computes LUFS          │ • Selects candidates     │ • Evaluates harmonic     │
│   uncompressed PCM       │   integrated loudness    │   via sonic texture      │   tension & energy arcs  │
│ • Retains raw file truth │ • Strict No-Invention:   │ • Zero manual metadata   │ • Outputs structured     │
│   without alteration     │   refuses to guess keys  │   tagging required       │   transition plans       │
└──────────────────────────┴──────────────────────────┴──────────────────────────┴──────────────────────────┘

    Stage 1 (Ingestion Retains): Spotify Pedalboard C++ JUCE streaming decoders ingest raw WAVE audio directly from disk, extracting uncompressed PCM float arrays at 4x real-time without alteration.
    Stage 2 (Classification Interprets): Librosa and Essentia extract dynamic BPM curves, beat onset envelopes, and chromagrams. Under the strict No-Invention Rule, H.E.R. explicitly refuses to invent Camelot keys or tempos when confidence falls below operational thresholds (0.82).
    Stage 3 (Retrieval Selects): Contrastive Language-Audio Pre-training (CLAP) maps natural text prompts and audio waveforms onto a shared 512-dimensional unit hypersphere, enabling sub-millisecond nearest-neighbor discovery across catalog tracks via SIMD dot-product scoring.
    Stage 4 (Reasoning Decides): The Musical Reasoning Engine (MRE) evaluates harmonic compatibility across Camelot Wheel rules (e.g., matching 8A minor rhythms with compatible 8B major hooks) and locks transition transients to 32-beat phrase boundaries.

For details on the demonstration, see Phase 1 Proof of Concept.
Why the Engineering Became This Complex

Building the instrument exposed an architectural challenge larger than signal processing alone.

A responsive musical collaborator must retain state, preserve context, retrieve the right information instantly, reason over it, manage local computational resources, and remain resilient when individual subsystems fail.

That reality led H.E.R. into rigorous systems engineering:

    Persistent, deterministic state reduction
    Single-pass event-sourced reconstruction
    Local filesystem knowledge retrieval
    Distributed Core/Edge physical computation
    Workload containment and sand-boxing
    Automated startup security gates (V2.07d audited)
    Evidence-driven testing and qualification
    Structured, durable engineering handoffs

These systems are not the purpose of H.E.R.

They are the scaffolding required to build it.
Sovereign by Design

H.E.R. is engineered to operate 100% locally on privately controlled silicon with zero external cloud dependencies.

[ PRIMARY STUDIO INTERFACE ]
         │ (Loopback / Local UI)
         ▼
[ DELL CORE AUTHORITY ] ── (Dedicated Physical Subnet: 10.99.0.0/24) ── [ MSI EDGE WORKER ]
• State Reducer Engine              Encrypted SSH Tunnel (TCP/22)        • GPU Acceleration
• event_log.jsonl                                                        • Heavy Neural Inference
• HER_LIVE_STATE.md                                                      • Sandboxed Runtime
• Live Obsidian API (:8765)                                              • Default-Deny Policy
• Default-Deny Firewall

    Core Node (State Authority): Manages authoritative state, transactional logs (event_log.jsonl), canonical markdown records (HER_LIVE_STATE.md), the read-only Live Obsidian Retrieval API (:8765), and local orchestration.
    Edge Node (Execution Worker): Dedicated physical host providing GPU compute and Vulkan-accelerated execution within secure sandboxed runtimes.
    Secure Sovereign Transport: Inter-node communication traverses an isolated physical Ethernet plane over an encrypted, key-authenticated SSH tunnel (TCP/22). Physical LAN and external WAN routes are blocked by default.

The public architecture intentionally describes these containment boundaries without publishing private network addresses, host credentials, personal records, or environment-specific telemetry.

See Architecture Overview.
Public and Private Development Surfaces

H.E.R. is published as a curated public engineering project following over a year of active daily development.

The public repository (jfc-candada/HER) is the project's maintained public engineering surface: it presents the program, systems architecture, demonstrated capabilities, methodology, and development direction in a format suitable for independent peer review, board briefings, and technical collaboration.

The broader private development environment retains the deeper forensic engineering record, including complete source code, raw mathematical formulations, operational telemetry, qualification experiments, and working-state material that is not appropriate for public release.

The distinction is deliberate.

Publicly published does not mean newly created. It represents the public release boundary of an already mature program of work.

    For an explicit breakdown of what is disclosed publicly versus what is retained within the sovereign private development environment, see the Public Release Boundary (also available at docs/program/public-release-boundary.md).

Repository Structure & Navigation

The public repository is structured into four curated documentation surfaces mirroring the project's engineering methodology:

jfc-candada/HER
├── README.md                                    # Root system charter, pipeline & reading directory
├── PUBLIC_RELEASE_BOUNDARY.md                   # Disclosure boundaries & IP containment policy
└── docs/
    ├── architecture/
    │   └── overview.md                          # Core/Edge topology, containment & signal path
    ├── methodology/
    │   ├── continuity-and-handoffs.md           # Retaining context across distributed sessions
    │   ├── development-method.md                # Experimental progression & qualification gates
    │   ├── knowledge-and-development-surfaces.md# Live Obsidian Vault integration & markdown state
    │   └── qualification-and-evidence.md        # Empirical testing standards & acceptance criteria
    ├── music/
    │   └── phase-1-poc.md                       # Musical proving ground, Camelot flow & Exploding Drop
    └── program/
        ├── phase-1-and-phase-2.md               # Preparation vs. live performance loopback strategy
        ├── public-release-boundary.md           # Secondary copy of public disclosure boundary
        └── purpose-and-origin.md                # Hospital recovery, Goal 2 & the instrument mandate

Curated Reading Paths

    Executive & Strategic Overview:
        Purpose and Origin — Hospital recovery genesis, Goal 2, and the musical mandate.
        Phase 1 and Phase 2 — Preparation workflow vs. live performance loopback learning.
        Public Release Boundary — Black-box disclosure model and intellectual property containment.

    Systems Architecture & Containment:
        Architecture Overview — Distributed Core/Edge hardware containment and sovereign transport.
        Phase 1 Proof of Concept — Empirical signal analysis, 512-D vector matching, and the 32-beat phrase lock.

    Engineering Governance & Living Knowledge:
        Development Method — Succession of experiments, evidence-driven promotion, and tooling.
        Knowledge and Development Surfaces — Local markdown state, Live Obsidian API, and external collaboration surfaces.
        Continuity and Handoffs — Avoiding context degradation across distributed human/AI sessions.
        Qualification and Evidence — Empirical evidence standards, firewall validation, and smoke tests.

Engineering Principles

    State is the product, not the graph.
    Durable state is treated as a reconstructable, single-pass system product (event_log.jsonl → state_reducer.py → HER_LIVE_STATE.md) rather than an opaque, mutating graph database prone to corruption and synchronization drift.
    Containment first, optimization second.
    Hardware execution, GPU workloads, and local inference models are strictly constrained within isolated network and filesystem boundaries before performance tuning begins.
    Evidence before promotion.
    A successful demonstration is not a qualified component. All subsystems must pass automated verification gates before promotion into the active baseline.
    Human authority remains external to the model.
    H.E.R. reasons, recommends, and stages complexity, but never acquires the authority to dictate artistic decisions or override the performer.
    Local-first means zero cloud dependency.
    The entire creative workflow, audio processing chain, and reasoning engine must remain fully functional without external internet connectivity.

Development Method & Living Knowledge

H.E.R. is developed against a durable local knowledge environment rather than transient, isolated AI chat sessions.

Development notes, handoffs, qualification records, architectural decisions, and active work queues are maintained as structured, human-readable markdown files. Appropriate material is curated and synchronized into this repository as the maintained software and documentation surface.

The local H.E.R. runtime queries this knowledge via the Live Obsidian Vault API bound to loopback, providing instant contextual awareness without re-indexing latency. This repository provides the corresponding durable collaboration surface for external engineering, version control, and tools such as Codex.

The result is deliberate continuity across human engineering, local reasoning, and repository history without treating any single model session as the system of record.

See:

    Development Method
    Continuity and Handoffs
    Knowledge and Development Surfaces
    Qualification and Evidence

Current Program State

H.E.R. is currently executing its master HER 4.03c Baseline, with core infrastructural foundations verified:

    Verified Operational Baseline:
        Core dual-node system smoke testing and inter-node SSH RPC
        Spotify Pedalboard uncompressed WAVE audio decoding
        Librosa and Essentia DSP feature extraction
        Local GPU execution and Vulkan compute acceleration
        V2.07d security closure and automated startup firewall gates
        Real-time Live Obsidian filesystem retrieval API (:8765)
        512-dimensional CLAP semantic vector space projection
        Phase 1 performance preparation and safe USB cue export (protecting Engine DJ m.db database integrity)
    Active Development Milestone (M3 Convergence):
        Fine-tuning local model prompt constraints for 100% schema compliance on transition plans
        Validating the end-to-end vertical slice from voice prompt ingestion to hardware staging
        Developing the Phase 2 live set observation loop and Episodic Event Frame (EEF) recording pipeline

H.E.R. remains an active engineering program. Architecture and implementation continue to evolve as real-world performance evidence feeds back into the design.
The Purpose Remains Simple

Build the instrument.
Make the music.
