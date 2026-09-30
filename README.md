# Project V // Phoenix AI Desktop

**Phoenix AI Desktop** is Project V's local-first desktop AI assistant for Windows. It is designed to keep models, memory, tools, files, and automation under the user's control while supporting persistent context, voice interaction, research, and permission-gated actions.

> **Repository status:** Private · Binary distribution only · Source code intentionally withheld during the current development and Phoenix Unbound research cycle.

## What Phoenix is

Phoenix is a desktop AI environment built around the idea that a personal assistant should be able to work locally, remember useful context over time, use tools, inspect project files, and help complete real work without requiring every workflow to live in the cloud.

Current Phoenix development includes capabilities such as:

- Local-first model execution and multi-model routing
- Persistent long-term memory and retrieval
- Voice input and spoken responses
- Document, PDF, and project knowledge workflows
- Workspaces and project continuity
- Tool and script execution with permission controls
- Controlled research and curiosity workflows
- Model Council / multi-model reasoning workflows
- Local system integrations and diagnostics
- Portable/local storage options
- Project V ecosystem integrations
- Live Execution Console with operational telemetry, approval visibility, safe cancellation events, Memory/Hindsight and Cortex stages, Model Council activity, and a persistent Phoenix Activity Ledger

## Live Execution Console

Phoenix includes a dedicated **Execution Console** for live operational observability. It exposes structured runtime telemetry while Phoenix works without exposing private chain-of-thought.

The console can surface ReAct task starts and completions, project/tool commands, approval boundaries, command output, Memory/Hindsight preflight, Cortex continuity lookups, Model Council activity, cancellation requests, safe-boundary termination, and verification results.

Operator-facing controls include a continuous live stream, auto-scroll, manual refresh, copy/clear controls, task inspection, subsystem readiness indicators, and a timestamped **Phoenix Activity Ledger** for recent intelligence activity.

The purpose of this interface is transparency: operators can see what Phoenix is doing, what required approval, what completed, what was cancelled, and what supporting subsystems participated in the run.

## Repository policy

This repository is currently used for **validated Phoenix executable releases and documentation only**.

The application source code is not being published here yet. The source may be added after the Phoenix Unbound research phase and a stable source-release baseline have been completed.

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

Phoenix can work with local files, tools, scripts, models, memory, and system integrations. Treat release binaries and configuration data as security-sensitive.

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
