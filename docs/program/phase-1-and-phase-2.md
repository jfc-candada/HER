# Phase 1 and Phase 2

HER is being developed in two deliberately connected phases.

## Phase 1 — Preparation

Phase 1 establishes the ability to move from natural-language musical intent to a technically structured performance plan.

The workflow is:

```text
Human intent
    ↓
Intent decoding
    ↓
Local library retrieval
    ↓
WAVE ingestion
    ↓
DSP analysis
    ↓
Semantic representation
    ↓
Similarity evaluation
    ↓
Harmonic / phrasing constraints
    ↓
Transition reasoning
    ↓
Cue plan
    ↓
Vendor-neutral export
```

Phase 1 deliberately avoids modifying the DJ platform's native database. HER produces standalone performance material instead.

This establishes a clean boundary between the instrument and the performer's existing production environment.

## Phase 1 evidence

The audio-analysis vertical slice has been exercised against a local collection of **1,626 tracks**.

The processing foundation includes:

- Spotify Pedalboard for audio decoding
- Librosa-based DSP feature extraction
- rhythm relationship reasoning
- harmonic reasoning
- semantic audio representation
- local retrieval
- cue and transition planning

The repository contains the underlying implementation and qualification work rather than treating the result as a purely conceptual architecture.

## Phase 2 — Live loopback

Phase 2 adds the missing half of the instrument.

Instead of stopping when HER produces a recommendation, the system observes what the artist actually does.

Candidate observations include:

- manual cue movement
- skipped recommendations
- changed transition timing
- extended sections
- altered ordering
- other deliberate performance adjustments

These observations are intended to become **Episodic Event Frames (EEFs)**.

The EEFs enter persistent event state and become available to subsequent reasoning.

```text
HER recommendation
       ↓
Human performance
       ↓
Observed decision
       ↓
EEF
       ↓
Persistent state
       ↓
Future recommendation
```

## Why Phase 2 matters

Phase 1 can produce a technically coherent plan.

Phase 2 asks whether the instrument can become progressively more useful to its particular artist.

That is a fundamentally different capability from simply generating recommendations.

The human remains the source of artistic authority. The system learns from evidence of human choice rather than attempting to replace it.

## Completion target

Phase 2 is the next major completion milestone for the music loop.

The work already completed in Phase 1 provides the processing foundation. The remaining engineering is primarily concerned with live observation, event capture, state integration and reasoning/orchestration around those observations.
