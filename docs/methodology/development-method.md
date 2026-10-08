# HER Development Method

HER has been developed through successive experiments rather than from a fixed architecture.

The method is deliberately evidence-driven.

## 1. Start with the human objective

Technical work is evaluated against whether it advances the musical instrument.

A technically interesting subsystem is not automatically a useful subsystem.

## 2. Experiment at the smallest useful scale

New capabilities are first tested in constrained environments.

This exposes:

- resource limitations
- integration assumptions
- model behaviour
- latency
- failure modes
- reproducibility problems

The constrained environment becomes a qualification surface rather than merely a limitation.

## 3. Separate measurement from interpretation

Where possible, HER preserves raw observations before applying reasoning.

This is particularly important in audio analysis.

Measured evidence such as BPM or key is kept distinct from interpretations such as transition suitability.

## 4. Separate capability from authority

A model may be capable of producing an answer or requesting an operation without being authorized to determine whether that operation should occur.

This separation applies to:

- knowledge
- reasoning
- orchestration
- tools
- execution
- human decisions

## 5. Preserve working state outside the model

AI sessions are not treated as the system of record.

Durable project state, working knowledge and decisions must survive changes of session, model and interface.

Obsidian, repository state, handoffs and queues are therefore part of the development method.

## 6. Use explicit handoffs and queues

Complex work is transferred through bounded state.

Handoffs preserve what matters for continuation.

Queues preserve direction.

Together they reduce context drift and prevent every new session from redefining the work.

## 7. Test claims against evidence

A model's assertion that something worked is not itself evidence that it worked.

HER uses:

- executable tests
- system observations
- qualification runs
- repository history
- reproducible failures
- explicit verification

## 8. Preserve failure as evidence

When a component fails, the useful question is not only how to make the error disappear.

The useful question is which assumption was wrong.

That evidence feeds the next architectural iteration.

## 9. Qualify before promotion

A successful demonstration establishes capability under observed conditions.

Qualification establishes whether that capability is suitable for the responsibility being assigned to it.

## 10. Repeat

The working loop is:

```text
Experiment
   ↓
Observe
   ↓
Preserve evidence
   ↓
Qualify
   ↓
Revise architecture
   ↓
Repeat
```

The purpose of the method is eventual completion of the instrument, not experimentation for its own sake.
