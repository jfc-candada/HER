# Phase 1 Music Intelligence POC

## Purpose

The Phase 1 proof of concept demonstrates a complete path from a natural-language musical request to structured performance preparation using a real local music collection.

It is intentionally concrete.

The system does not need to understand music in the abstract. It needs to process actual audio, preserve measurable evidence, apply musical constraints and produce something a performer can use.

## Processing path

```text
Natural-language request
        ↓
Performance intent
        ↓
Local track retrieval
        ↓
WAVE decoding
        ↓
DSP feature extraction
        ↓
Rhythm reasoning
        ↓
Harmony reasoning
        ↓
CLAP semantic representation
        ↓
Similarity evaluation
        ↓
Phrasing / transition constraints
        ↓
Cue plan
        ↓
CSV / performance export
```

## Audio processing

HER establishes an explicit audio boundary between source files and musical reasoning.

The current worker pipeline:

1. decodes source audio;
2. extracts DSP features;
3. derives rhythm context;
4. derives harmonic context;
5. preserves raw evidence separately from downstream reasoning;
6. produces a canonical Music Intelligence state.

The primary decoder path uses Spotify Pedalboard. A compatibility fallback is retained for unsupported containers/codecs.

## DSP and reasoning

The system separates measurement from interpretation.

Examples of measured evidence include:

- detected BPM
- musical key
- key confidence
- spectral and temporal features

Reasoning then operates on that evidence.

For rhythm, HER can identify relationships such as double-time and half-time candidates rather than simply replacing the detected BPM.

For harmony, the system evaluates key and mode evidence and derives compatible-key relationships when the evidence supports them.

This separation supports the project's broader rule:

> **Evidence is retained before interpretation is applied.**

## Semantic audio representation

The Phase 1 design uses CLAP embeddings to represent tracks in a high-dimensional semantic space.

The current working corpus contains **1,626 local tracks**, represented using **512-dimensional vectors**.

L2 normalization permits cosine similarity to be evaluated through normalized vector dot products.

This provides a computational representation of relationships that may not be explicitly encoded in the source metadata.

## Musical constraints

Semantic similarity is not sufficient to produce a useful DJ transition.

HER therefore combines semantic evidence with musical constraints including:

- harmonic compatibility
- BPM relationships
- phrasing boundaries
- transition context
- creative intent

The goal is an explainable transition decision rather than an opaque nearest-neighbour result.

## Example request

A representative Phase 1 request asks for approximately an hour of House music, weighted toward current and 1990s material, suited to an intimate setting, with Elvis vocal material and 1980s synth-pop elements.

HER's intended response is not simply a playlist.

It is a structured plan describing:

- selected tracks
- relevant cue locations
- transition relationships
- harmonic compatibility
- phrase alignment
- supporting reasoning
- exportable performance data

## Output boundary

Phase 1 produces standalone performance material rather than modifying the native DJ database.

This is deliberate.

The instrument should be able to generate useful output without becoming dependent on, or risking corruption of, the performer's existing production database.

## What the POC proves

The Phase 1 work demonstrates that the program can connect:

**human musical intent → real audio → measurable evidence → computational reasoning → performance preparation.**

That is the foundation on which Phase 2 builds.
