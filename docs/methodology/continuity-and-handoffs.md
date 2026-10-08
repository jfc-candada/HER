# Continuity, Handoffs and Working State

HER treats continuity as an engineering problem.

AI-assisted development introduces reasoning state that can otherwise exist only inside a conversation: decisions, current hypotheses, unresolved questions, constraints and the relationship between experiments.

HER deliberately moves important working state outside the session.

## Persistent knowledge

Obsidian is used as a durable, human-readable working surface for:

- architectural decisions
- active investigations
- project context
- unresolved questions
- references
- working notes

The knowledge environment is not treated as automatically authoritative simply because it is persistent. Its contents remain subject to retrieval and validation.

## Handoffs

A handoff is a deliberate transfer of working state.

A useful handoff records:

- current objective
- completed work
- evidence
- unresolved issues
- constraints
- decisions already made
- next bounded action

This allows a new session or collaborator to continue from known state rather than reconstructing the project from conversational memory.

## Queues

Queues provide an explicit boundary around current work.

They provide:

- direction
- prioritization
- bounded scope
- recovery after interruption
- a record of unfinished work

This is especially important in AI-assisted development, where technically interesting adjacent problems can otherwise pull work away from its current objective.

## Repository state

Git preserves one class of state:

> What exists?

Working-state documentation preserves another:

> Why does it exist this way, what are we investigating, and what should happen next?

They are complementary.

## The design principle

A capable model without durable context is episodic.

Durable context without controlled retrieval is noise.

Retrieval without authority boundaries is risk.

**Continuity requires all three to be designed together.**
