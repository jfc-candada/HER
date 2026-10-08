# Qualification and Evidence

HER does not treat an impressive demonstration as sufficient evidence of operational suitability.

A component can succeed under one set of conditions and fail under another.

Qualification makes that boundary explicit.

## Capability versus qualification

A successful response establishes that a system can perform an operation under observed conditions.

Qualification asks whether it can be trusted to perform the relevant responsibility under defined conditions.

These are different questions.

## Qualification dimensions

Depending on the component, HER evaluates dimensions including:

- capability
- consistency
- context handling
- retrieval accuracy
- tool behaviour
- containment
- resource consumption
- failure behaviour
- repeatability
- integration behaviour

Not every component requires every dimension.

## Evidence

Useful evidence can include:

- executable tests
- controlled experiments
- system observations
- repository history
- reproducible failures
- qualification records
- comparative evaluations

Important conclusions should therefore be inspectable rather than dependent on a model's description of its own performance.

## Failure as data

A failed test can identify an architectural boundary.

A component that works normally but fails under resource pressure has demonstrated both a capability and a limitation.

The limitation becomes part of the engineering knowledge.

## Model selection

Models are evaluated in the context in which HER intends to use them.

Relevant factors can include:

- capability
- latency
- memory requirements
- hardware compatibility
- tool behaviour
- containment
- reliability
- integration cost

This makes model selection an engineering decision rather than a leaderboard decision.

## Promotion rule

> **Do not promote a capability because it looks convincing. Promote it when the evidence supports the responsibility being assigned to it.**
