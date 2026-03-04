# AGENTS.md

Guidelines for AI coding agents interacting with **Project Falcon**.

## Purpose

This file provides operational guidance for AI assistants (GPT, Claude,
Cursor, Copilot, etc.) working inside the Falcon repository.

Agents should read: - `falcon_agent_context.md` -
`ARCHITECTURE_FOR_AGENTS.md` before generating code or making
architectural suggestions.

------------------------------------------------------------------------

## Core Development Principles

### 1. Threads Are The Primary Primitive

All collaboration in Falcon happens in **threads**.

A thread may contain: - humans - AI agents - services - tools

Agents should design features assuming **thread-first architecture**.

------------------------------------------------------------------------

### 2. Agents Are First-Class Participants

AI agents in Falcon are not temporary assistants.

Agents have:

-   persistent identity
-   memory
-   history
-   trust relationships

Agents must behave like collaborators, not stateless request/response
tools.

------------------------------------------------------------------------

### 3. Sovereign Infrastructure

Falcon prioritizes **user sovereignty**.

Avoid designs that depend on:

-   centralized identity providers
-   single cloud vendors
-   platform lock-in

Prefer:

-   portable identity
-   cryptographic identity
-   federated or distributed infrastructure.

------------------------------------------------------------------------

### 4. Zero-Trust System Design

Falcon assumes adversarial environments.

Agents should design systems with:

-   authentication
-   service isolation
-   verification of identity
-   minimal implicit trust between services.

------------------------------------------------------------------------

## Code Generation Guidelines

When producing code for Falcon:

Prefer: - modular services - observable systems - strongly typed
interfaces - event-driven architecture - horizontally scalable designs.

Avoid: - monolithic assumptions - hard-coded trust relationships -
centralized control systems.

------------------------------------------------------------------------

## Performance Awareness

Falcon targets:

-   low latency
-   real-time collaboration
-   scalable thread processing

Agents should prioritize:

-   asynchronous processing
-   caching
-   minimal blocking operations.

------------------------------------------------------------------------

## When In Doubt

If architectural context is unclear:

1.  consult `ARCHITECTURE.md`
2.  consult `ARCHITECTURE_FOR_AGENTS.md`
3.  consult `falcon_agent_context.md`

Agents should prefer **asking for clarification rather than
hallucinating architecture**.

------------------------------------------------------------------------

## Summary

Falcon is an infrastructure project for **human-AI collaboration**.

Agents should produce solutions that support:

-   persistent agents
-   thread-native collaboration
-   decentralized infrastructure
-   sovereign identity.
