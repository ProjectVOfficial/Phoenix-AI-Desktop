# Feature Overview

Phoenix AI Desktop is an evolving local-first AI environment. Availability varies by release, and experimental features may change before a stable public source release.

## Core desktop assistant

Phoenix provides a desktop interface for conversational AI with support for local-first workflows and multiple model backends.

## Local model support

Phoenix is designed to work with local inference systems and locally hosted models. Model routing and fallback behavior may vary by build.

## Persistent memory

Phoenix includes long-term memory capabilities intended to preserve useful project and conversational context across sessions.

Memory data is local/user-controlled and should never be committed to this repository.

## Project and document knowledge

Phoenix can work with project files, documents, PDFs, and workspace context to support longer-running tasks.

## Voice

Phoenix includes voice-oriented capabilities such as speech input and spoken responses where enabled and supported by the local environment.

## Tools and scripts

Phoenix can use tools and execute approved workflows. Permission controls are an important part of the design: higher-impact actions should remain gated according to the configured operating mode.

## Cortex and continuity

Phoenix development includes a persistent reasoning/continuity layer intended to track decisions, outcomes, unresolved questions, project state, and knowledge gaps over time.

## Controlled curiosity

Research and curiosity workflows are designed to let Phoenix identify useful questions or research opportunities while preserving user control over execution.

## Model Council

Phoenix can incorporate multiple models into a structured reasoning workflow so that different model perspectives can be compared before producing a result or taking an approved action.

## Project V integrations

Phoenix is designed to interoperate with other Project V applications where appropriate, including monitoring, security, analysis, and research-oriented tools.

## Live Execution Console and operational observability

Phoenix includes a real-time **Execution Console** for structured operational telemetry. The console is designed to show what Phoenix is doing without exposing private chain-of-thought.

Visible runtime events can include:

- ReAct task start, completion, and cancellation
- Project and tool command execution
- Approval-required states and approval boundaries
- Command output and verification results
- Memory/Hindsight preflight and retrieval stages
- Cortex continuity lookups
- Model Council start/completion and assessment count
- Safe-boundary cancellation behavior
- Subsystem readiness for Memory, Hindsight, Dream Lab, and Cortex
- Timestamped Phoenix Activity Ledger entries

The console also provides live refresh, auto-scroll, copy/clear controls, task inspection, and recent-activity history.

Model Council telemetry is advisory only and does not independently authorize actions. Permission policy remains authoritative for execution.

## Experimental capabilities

Some capabilities are research-stage and may not be present in every distributed build. Release notes are the authoritative source for what is included in a particular executable.
