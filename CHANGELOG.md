# Changelog

All notable repository-distributed Phoenix releases should be recorded here.

The repository is currently in binary-distribution mode, so this changelog tracks packaged application releases rather than public source commits.

## Unreleased

- Final regression and repair validation
- ReAct/planner reliability work
- Autonomous TypeScript repair exam and verification
- Production-baseline stabilization

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
