# Knowledge and Development Surfaces

HER is developed with a deliberate separation between the public software surface and the broader working knowledge used to build it.

## Durable working knowledge

The development environment uses a local Obsidian knowledge base as a human-readable working surface.

It is used to maintain material such as:

- development notes
- architectural decisions
- handoffs and continuity records
- testing and qualification notes
- security analysis
- risk analysis
- system and network schematics
- active investigations
- implementation queues
- references and working evidence

The purpose is continuity: important engineering state should not exist only inside an AI session or a developer's short-term context.

## Local reasoning

The local HER environment can provide appropriately selected material from this knowledge base to local language-model components.

The architectural boundary remains explicit:

**the knowledge base retains; retrieval selects; the model reasons.**

A model does not become the owner of the knowledge simply because it can access selected material.

## Repository synchronization

Repository material is synchronized from the broader development process when it is appropriate for the software project and its intended audience.

The public repository is therefore not intended to be a transcript of the complete development environment.

It is the maintained public engineering surface: enough to understand the program, inspect its architecture and demonstrated capabilities, participate in development, and evaluate its direction.

Detailed operational material, private working evidence, environment-specific records and proprietary implementation remain outside that public surface.

## Why this matters for AI-assisted engineering

This arrangement allows different tools to operate against the same disciplined body of work without making any single model session the system of record.

The local environment supports controlled, context-rich development.

The repository provides durable software history and an appropriate collaboration surface.

External engineering tools such as Codex can therefore be applied to an established project with existing context, tests, architecture, decisions and work queues rather than starting from a blank coding session.

## The development record

HER is being published after approximately one year of active development.

The public release should be understood as the public engineering surface of an already active program, not as the beginning of the program itself.
