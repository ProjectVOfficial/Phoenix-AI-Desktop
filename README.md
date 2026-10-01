# Project V // Phoenix AI Desktop

**Phoenix AI Desktop** is Project V's local-first desktop AI assistant and agent platform for Windows. It is designed to keep models, memory, tools, files, automation, and operational control on the user's system while supporting persistent context, voice, vision, project awareness, research, and permission-gated actions.

> **Current baseline:** Phoenix Desktop **v0.15.0a**  
> **Repository status:** Public documentation and binary-release repository · Source code intentionally withheld during the current stabilization and Phoenix Unbound research cycle.

## What Phoenix is

Phoenix is a desktop AI environment built around the idea that a personal assistant should be able to work locally, remember useful context over time, understand active projects, use tools, inspect files, run approved terminal commands, and help complete real work without requiring every workflow to live in the cloud.

The current v0.15.0a baseline integrates the **Phoenix Intelligence Core** with the rest of the desktop application.

## Current capabilities

- Local-first model execution with **Ollama** and **KoboldCpp** routing
- Automatic Ollama fallback for conversational workloads
- Persistent local memory plus optional **Hindsight** experience memory
- **Cortex** continuity, evidence, confidence, contradiction, and knowledge-gap tracking
- **Model Council** multi-model reasoning
- Bounded **ReAct** agent runtime
- Working Directory / project-aware development workflows
- Permission-controlled **PowerShell, Command Prompt, and Bash** execution
- Process inspection and bounded process monitoring
- Windows Registry and Event Log tooling
- Document, PDF, Library, and RAG workflows
- **Phoenix Vision** for local images and explicit screen captures
- Voice input, spoken responses, and Live Voice
- Passive, Controlled, and Autonomous Curiosity workflows
- Idle research with configurable budgets and permission boundaries
- Project V ecosystem integrations, including the Phoenix ↔ Watchtower bridge
- Portable/local storage options
- **Stop Thinking** safe request cancellation
- Live Execution Console and Phoenix Activity Ledger
- Toolsmith, Skill Forge, and Evolution status/integration surfaces

## Phoenix Intelligence Core

The Intelligence Core unifies reasoning, memory, tools, permissions, project context, and execution.

It provides Phoenix with a common tool layer for memory operations, project inspection, process context, shell execution, system diagnostics, Registry access, event logs, ReAct planning, Cortex continuity, Hindsight reflection, and other approved actions.

High-impact capabilities remain subordinate to Phoenix permissions, approval requirements, UAC/elevation boundaries, and destructive-action safeguards.

## Terminal and system tooling

Phoenix can run operator-approved commands through:

- **PowerShell**
- **Command Prompt / cmd.exe**
- **Bash** where available

Terminal execution captures output and participates in the same permission and activity-tracking system as other Intelligence Core tools.

Phoenix can also perform read-oriented process inspection, bounded process monitoring, Windows Event Log queries, and permission-controlled Registry operations.

## ReAct agent runtime

Phoenix can execute bounded multi-step tasks using a ReAct-style loop:

**Perceive → Plan → Choose Tool → Act → Observe → Revise**

The runtime preserves action limits, failure guards, approval points, permissions, task state, activity history, and operator interruption.

This supports workflows such as project inspection, TypeScript diagnostics, command execution, verification, and bounded repair tasks.

## Memory, Hindsight, and Cortex

Phoenix uses multiple complementary memory and continuity layers.

### Persistent local memory
Stores useful project state, operator-requested facts, preferences, task context, and session information locally.

### Hindsight
Provides optional experience-memory reflection across prior observations, attempts, failures, and successful approaches. Phoenix can manage a local Hindsight sidecar while retaining SQLite-style local memory as a fail-open fallback.

### Cortex
Tracks continuity above ordinary chat, including observations, evidence, confidence, contradictions, unresolved questions, decisions, outcomes, and knowledge gaps.

Memory, Hindsight, and Cortex provide context only. They do not grant execution authority.

## Model Council

Phoenix can consult multiple local models when a problem is uncertain, contested, or contradictory.

The Council is advisory. It does not independently authorize tools or actions, and ordinary chat does not require Council activation.

## Curiosity

Phoenix includes several bounded curiosity modes:

- **Passive Curiosity** — identifies unresolved questions and proposes investigations
- **Investigation Planner** — turns a knowledge gap into a ranked research plan
- **Controlled Curiosity** — executes an explicitly approved bounded read-only investigation
- **Autonomous Curiosity / Idle Research** — performs limited research during configured idle periods and within daily budgets

Curiosity remains subordinate to normal file, web, tool, and approval permissions.

## Vision and voice

Phoenix Vision can analyze local images and explicit screen captures using a local Ollama-compatible multimodal model.

Phoenix also supports local speech recognition, spoken responses, and Live Voice interaction.

## Stop Thinking

Phoenix v0.15.0a adds request-scoped safe cancellation.

While Phoenix is reasoning or generating, the operator can click **Stop thinking** or press **Escape**.

Cancellation applies across ordinary Chat, ReAct/planner activity, Model Council processing, Hindsight reflection, local-model generation, and local vision reasoning.

If an atomic tool action is already in progress, Phoenix allows that action to reach a safe boundary, preserves the completed observation, and prevents later reasoning/tool steps from starting.

Cancelled tasks are recorded as `cancelled`. Stop Thinking does not shut down Phoenix, Ollama, KoboldCpp, Hindsight, Cortex, Memory, or unrelated background services.

## Live Execution Console

Phoenix includes a dedicated **Execution Console** for operational observability without exposing private chain-of-thought.

Visible runtime telemetry can include:

- ReAct task starts, completions, and cancellation
- Project and tool commands
- Approval boundaries
- Command output and verification
- Memory/Hindsight stages
- Cortex continuity activity
- Model Council activity
- Stop/cancellation requests and safe-boundary termination
- subsystem readiness
- timestamped Phoenix Activity Ledger entries

The goal is operator transparency: users can see what Phoenix did, what required approval, what completed, and what was cancelled.

## Current development stage

**Known-good repair baseline: Phoenix Desktop v0.15.0a6**

The deliberately broken TypeScript autonomous-repair regression has passed on the a6 baseline: Phoenix diagnosed and repaired the target project, then completed typecheck, build, and tests successfully with **3 passed / 0 failed**, finishing normally in **8/12 actions**.

**Current development tail: Phoenix Desktop v0.15.0a7**

The a7 Execution Console patch is the current validation target. Remaining work is limited to local install/application of the patch, TypeScript validation, startup smoke testing, a harmless ReAct telemetry run, regression checks, and freezing the final Phoenix 0.15 production baseline.

After that baseline is frozen, the next planned development phase is **Project V // Mnemosyne 0.1 — Fork + API Compatibility**, validating the Project V Hindsight fork as a drop-in Phoenix memory sidecar before any Phoenix-specific memory extensions are enabled.

## Repository policy

This repository is currently used for **validated Phoenix executable releases and documentation**.

The application source code is not being published here yet. Source publication may be reconsidered after Phoenix stabilization, Phoenix Unbound research, and a stable source-release baseline.

Do not commit personal Phoenix memory, local databases, API keys, credentials, connector vaults, model files, logs, or other machine-specific data.

## Installation

For binary releases, see [Installation](docs/INSTALLATION.md).

Validated builds should be distributed through **GitHub Releases** rather than committed directly into the main repository whenever practical.

## Documentation

- [Installation](docs/INSTALLATION.md)
- [Feature Overview](docs/FEATURES.md)
- [Binary Distribution Policy](docs/BINARY-DISTRIBUTION.md)
- [Privacy & Local Data](docs/PRIVACY-AND-DATA.md)
- [Roadmap](docs/ROADMAP.md)
- [Release Process](docs/RELEASES.md)
- [Security Policy](SECURITY.md)
- [Changelog](CHANGELOG.md)

## Security

Phoenix can work with local files, tools, scripts, models, memory, terminal commands, and system integrations. Treat release binaries and configuration data as security-sensitive.

Never publish:

- API keys or tokens
- `.env` files
- connector credentials
- local memory databases
- private workspaces
- signing certificates or private keys
- user-specific logs or exported conversations

See [SECURITY.md](SECURITY.md) for reporting and release-safety guidance.

## Source availability

At this stage, **no open-source license is granted** and the Phoenix source code is not included in this repository.

Unless otherwise stated, Project V retains all rights to the software, documentation, branding, and distributed binaries.

---

**Project V Official**  
Phoenix AI Desktop
