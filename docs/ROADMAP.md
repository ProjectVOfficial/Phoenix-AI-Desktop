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
