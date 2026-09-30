# Feature Overview

Phoenix AI Desktop is a local-first AI assistant and agent platform. The current integrated baseline is **v0.15.0a**.

## Intelligence Core

Phoenix Intelligence Core connects reasoning, memory, project context, tools, permissions, and execution through one bounded runtime.

Current tool families include:

- persistent memory search/save/reflection
- project and working-directory inspection
- process attach/status/monitor/modules/detach
- Script Runner
- PowerShell
- Command Prompt
- Bash where available
- Windows Registry read/write
- Windows Event Log / system-log queries
- model, Cortex, and research workflows

High-impact tools remain permission gated.

## Local model runtime

Phoenix supports:

- **Ollama** for Chat, ReAct, Vision, embeddings, RAG, and specialist models
- **KoboldCpp** for local GGUF Chat and ReAct workloads
- optional automatic fallback from KoboldCpp to Ollama when the selected runtime is unavailable

## ReAct agent

Phoenix can perform bounded multi-step work using a perceive/plan/act/observe/revise loop.

The runtime preserves:

- hard action budgets
- failure guards
- permission checks
- approval boundaries
- task state
- activity history
- operator interruption

## Terminal integration

Permission-controlled terminal tooling includes:

- PowerShell
- cmd.exe
- Bash where available

Phoenix captures command output and can use it during project diagnostics, builds, verification, and approved repair tasks.

## Persistent memory

Phoenix maintains local persistent memory for useful project context, operator-requested facts, preferences, decisions, and session continuity.

## Hindsight

Hindsight provides optional experience-memory reflection across prior observations, attempts, failures, and successful approaches.

Phoenix can manage a local Hindsight sidecar and retain normal local memory as a fail-open fallback.

## Cortex

Cortex adds structured continuity for:

- observations
- evidence
- confidence
- contradictions
- outcomes
- decisions
- unresolved questions
- knowledge gaps

## Model Council

Phoenix can consult several installed local models for uncertain or contradictory problems.

Council results are advisory and do not override execution policy.

## Knowledge Gap Map and Curiosity

Phoenix can explicitly represent unresolved knowledge gaps and turn them into bounded investigations.

Curiosity modes include:

- Passive Curiosity
- Investigation Planner
- Controlled Curiosity
- Autonomous Curiosity / Idle Research

Idle research is constrained by configurable thresholds, per-day investigation limits, time budgets, relevance scoring, and the ordinary Phoenix permission model.

## Vision

Phoenix Vision supports local image analysis and explicit screen captures through a locally hosted multimodal model.

## Voice

Phoenix supports local speech recognition, spoken responses, Live Voice, and request interruption during the thinking phase.

## Stop Thinking

v0.15.0a introduces safe request-scoped cancellation through **Stop thinking** and **Escape**.

Cancellation covers Chat, ReAct/planner reasoning, Model Council, Hindsight reflection, local generation, and local vision reasoning.

Already-started atomic tool actions are allowed to complete to a safe boundary before later reasoning is cancelled.

## Process intelligence

Phoenix can attach context to an explicit PID and perform read-oriented inspection including:

- CPU and memory snapshot
- handles and threads
- executable metadata
- network connections
- loaded modules
- bounded monitoring

## Project and document knowledge

Phoenix supports project/workspace context, documents, PDFs, Library/RAG workflows, and semantic retrieval.

## Phoenix ↔ Watchtower

Phoenix can receive structured Project V // Watchtower context for conversational follow-up and related analysis.

## Live Execution Console

The Execution Console surfaces operational telemetry without exposing private chain-of-thought.

It can show:

- ReAct lifecycle events
- command/tool execution
- approvals
- command output
- Memory/Hindsight stages
- Cortex activity
- Model Council activity
- cancellation and safe-stop events
- verification results
- Phoenix Activity Ledger history

## Toolsmith, Skill Forge, and Evolution

Current Phoenix builds retain these intelligence-development subsystem surfaces alongside Memory, Hindsight, and Cortex.

## Permissions and safety

Phoenix's core rule is that context does not equal authority.

Memory, Hindsight, Cortex, Model Council, and Curiosity cannot independently grant permission to execute higher-impact actions.

Tool permissions, approval requirements, UAC/elevation boundaries, destructive-action controls, and protocol safeguards remain authoritative.

## Current status

The v0.15.0a feature baseline is integrated. Current work focuses on regression stability, ReAct/planner reliability, autonomous TypeScript repair validation, and freezing a known-good production baseline.
