# Changelog

All notable repository-distributed Phoenix releases should be recorded here.

The repository is currently in binary-distribution mode, so this changelog tracks packaged application releases rather than public source commits.

## Unreleased

### 0.15.0a7 — Execution Console validation tail

- 0.15.0a6 retained as the known-good autonomous-repair regression baseline
- autonomous TypeScript repair exam completed successfully: repair, typecheck, build, and tests passed
- latest successful repair run completed normally in 8/12 actions with 3 tests passed and 0 failed
- 0.15.0a7 Execution Console patch prepared on top of the a6 baseline
- source-side type validation for the a7 patch completed with zero TypeScript errors before local install
- remaining local validation: apply/install patch, typecheck, startup smoke test, harmless ReAct telemetry run, and final production-baseline freeze
- after the Phoenix 0.15 baseline is frozen, begin **Project V // Mnemosyne 0.1 — Fork + API Compatibility**

## 0.15.0a — 2026-09-29

**Integrated baseline**
- Phoenix Intelligence Core integrated into the desktop application
- Permission-controlled PowerShell, Command Prompt, and Bash tooling
- Working Directory / project-aware ReAct workflows
- Persistent Memory, Hindsight, and Cortex integration
- Model Council and knowledge-gap workflows
- Passive, Controlled, and Autonomous Curiosity foundations
- Ollama and KoboldCpp local-model routing
- Phoenix Vision and Live Voice integration
- Toolsmith, Skill Forge, and Evolution subsystem surfaces
- Project V ecosystem integration, including Phoenix ↔ Watchtower context

**Added**
- Request-scoped **Stop Thinking** control
- Escape-key cancellation while Phoenix is thinking
- Safe cancellation across Chat, ReAct/planner, Model Council, Hindsight reflection, local generation, and local vision
- Clean `cancelled` task state handling
- Safe-boundary cancellation that preserves completed tool observations
- Live Voice use of the same cancellation path

**Changed**
- Cancelled ReAct tasks clear pending approval/question state
- Cancelled Cortex tasks end cleanly instead of remaining active
- Completed Decision Ledger/tool observations remain preserved
- Cancelled tasks do not queue normal post-success Cortex review
- Operator-triggered KoboldCpp cancellation does not restart generation through Ollama fallback

**Validated**
- TypeScript typecheck: zero errors for the 0.15.0a phase
- ordinary model-generation cancellation
- Escape cancellation
- ReAct/planner cancellation
- safe-boundary tool behavior
- Live Voice interruption
- Memory, Hindsight, Cortex, Toolsmith, Skill Forge, and Evolution availability

## Earlier development

Earlier 0.x milestones established Phoenix's local model support, memory, workspaces, voice, system controls, alerts, tray/security work, Script Runner, Working Directory/PID context, SQLite memory, ReAct, Vision, proactive agency/protocols, Watchtower pairing, KoboldCpp routing, Hindsight, Cortex, Model Council, and Curiosity foundations.
