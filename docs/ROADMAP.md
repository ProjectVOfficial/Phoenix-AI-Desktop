# Roadmap

This roadmap is intentionally high level. It describes direction rather than promising specific release dates.

## Current production baseline

### Phoenix Desktop v0.15.0a

The integrated Intelligence Core baseline is in place, including terminal tooling, ReAct, Memory/Hindsight, Cortex, Model Council, Curiosity, local model routing, Vision, Voice, Stop Thinking, and operational telemetry.

## Current phase

### Stabilization and final validation

- Complete full regression validation against v0.15.0a
- Finish ReAct/planner reliability repair
- Run the deliberately broken TypeScript autonomous-repair exam
- Verify repair → typecheck/build → observation → stop behavior
- Confirm permissions and approval boundaries remain intact
- Freeze a known-good production baseline
- Prepare validated binary release artifacts

## Planned memory-core phase

### Project V // Mnemosyne — Phoenix Memory Core

After the v0.15.0a production baseline is frozen, Project V plans to evaluate a Phoenix-specific downstream fork of the Hindsight memory engine.

The goal is to keep Hindsight's proven retain / recall / reflect foundation and retrieval architecture while adding Phoenix-native semantics, project routing, Cortex integration, provenance, repair-learning, and portable-storage behavior.

The initial rule is compatibility first: Phoenix should be able to use Mnemosyne as a drop-in local memory sidecar without breaking the current `phoenix-core` bank or existing Hindsight lifecycle controls.

Planned stages include:

- **0.1 — Fork + API compatibility**
  - preserve existing retain / recall / reflect behavior
  - keep current Phoenix Hindsight health/lifecycle expectations working
  - run side-by-side with stock Hindsight for rollback

- **0.2 — Phoenix metadata schema**
  - add source, workspace, project, task, session, tool, memory-class, confidence, outcome, verification, and authority metadata
  - preserve the rule that remembered context never grants execution authority

- **0.3 — Workspace / project bank routing**
  - support project-scoped memory banks while preserving `phoenix-core`
  - allow cross-bank recall when a task spans multiple Project V projects

- **0.4 — Cortex-native memory records**
  - preserve structured beliefs, evidence, contradictions, knowledge gaps, predictions, and outcomes instead of flattening them into ordinary text

- **0.5 — Tool outcome and repair learning**
  - retain successful fixes, failed attempts, verification commands, and lessons learned
  - prioritize proven repair patterns during future ReAct tasks

- **0.6 — Provenance + contradiction handling**
  - attach source paths, tool outputs, timestamps, hashes, and evidence references
  - retain superseded facts with time/source context instead of silently overwriting them

- **0.7 — Retention and memory scoring**
  - classify memory as ephemeral, session, time-limited, project, or permanent
  - score durability, usefulness, confidence, novelty, redundancy, and sensitivity before retention

- **0.8 — Phoenix Memory Core UI**
  - add Phoenix-native views for memories, projects, lessons, contradictions, Cortex state, backups, and diagnostics

- **0.9 — Migration / backup / portable hardening**
  - migrate a copy of the current `phoenix-core` bank
  - validate recall/reflect parity before cutover
  - honor Phoenix-selected portable/local storage roots

- **1.0 — Stable Phoenix Memory Core**
  - promote only after side-by-side validation shows equal or better recall with no memory loss

Upstream Hindsight tracking should remain configured so Project V can selectively bring in relevant bug fixes, retrieval improvements, database migrations, performance work, and security fixes.

Project V // Mnemosyne would remain clearly attributed as a downstream Hindsight-derived project and would preserve applicable upstream license notices.

## Research phase

### Phoenix Unbound

Phoenix Unbound is planned as a separate research branch/environment for studying broader autonomous behavior inside a deliberately isolated sandbox.

It is not intended to replace or weaken the stable production Phoenix permission model.

Research goals include:

- sandboxed self-directed research
- controlled self-modification
- tool and workflow creation
- measurable iteration and rollback
- Model Council review
- strict separation from production data and systems

## Later considerations

After the stable and research phases are complete:

- evaluate source publication
- define final licensing
- publish developer/build documentation
- expand contribution guidance
- formalize plugin/tool interfaces
- continue Project V ecosystem integration
- evaluate optional security-toolkit integrations such as Ghidra, FFUF, and Eyeballer

The roadmap may change as validation results and safety requirements evolve.
