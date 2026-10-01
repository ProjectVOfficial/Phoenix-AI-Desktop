# Roadmap

This roadmap is intentionally high level. It describes direction rather than promising specific release dates.

## Current production baseline

### Phoenix Desktop v0.15.0a6 — known-good repair baseline

The integrated Intelligence Core baseline is in place, including terminal tooling, ReAct, Memory/Hindsight, Cortex, Model Council, Curiosity, local model routing, Vision, Voice, Stop Thinking, Toolsmith / Skill Forge / Evolution surfaces, and operational telemetry.

The autonomous TypeScript repair regression has passed on the 0.15.0a6 baseline:

- Phoenix diagnosed the deliberately broken readiness project
- repaired the target source
- typecheck passed
- build passed
- tests passed: 3 passed / 0 failed
- the task completed normally in 8 of 12 available actions
- the earlier planner-guard / limit-reached regression is considered repaired for this validation case

The autonomous repair exam is therefore retired as a blocking test for the 0.15.0a6 baseline.

## Current development tail

### Phoenix Desktop v0.15.0a7 — Execution Console validation

The next patch builds on the known-good 0.15.0a6 baseline and extends operator-facing execution telemetry.

Current validation sequence:

1. install/apply the 0.15.0a7 Execution Console patch
2. run Phoenix TypeScript typecheck
3. start Phoenix and confirm normal startup
4. run a harmless bounded ReAct task
5. confirm Execution Console / Phoenix Activity Ledger telemetry is visible and accurate
6. verify no regression to permissions, approval boundaries, Memory/Hindsight, Cortex, Stop Thinking, or local-model routing
7. freeze the resulting known-good Phoenix 0.15 production baseline
8. prepare validated binary/release artifacts

No additional Phoenix feature phase should be inserted ahead of this validation tail unless required by a regression discovered during testing.

## Next development phase

### Project V // Mnemosyne 0.1 — Fork + API Compatibility

**Start only after the Phoenix 0.15 production baseline is frozen.**

Mnemosyne 0.1 is the next planned development phase after the current Phoenix update/build/validation process.

The objective is to prove that the Project V Hindsight fork can operate as a drop-in local memory sidecar for Phoenix without changing Phoenix's production permission model or risking the current `phoenix-core` bank.

#### 0.1 compatibility targets

- preserve Hindsight `retain`
- preserve Hindsight `recall`
- preserve Hindsight `reflect`
- preserve memory-bank handling
- preserve the current `phoenix-core` bank
- preserve Phoenix Hindsight health/readiness checks
- preserve Phoenix-managed local sidecar lifecycle behavior
- preserve local Ollama-based Hindsight operation where configured
- preserve backup/export expectations
- keep stock Hindsight available as a rollback path
- validate Mnemosyne side-by-side with stock Hindsight before cutover

#### 0.1 Phoenix validation set

Mnemosyne 0.1 should be tested against known Phoenix memory behaviors, including:

- ordinary retain → recall
- cross-session recall
- Hindsight reflection
- Phoenix startup with memory online
- Phoenix startup with memory unavailable / fail-open behavior
- current `phoenix-core` bank access
- Cortex/Hindsight interaction
- ReAct retrieval of prior experience
- clean shutdown/restart
- backup and restore sanity
- no change to tool authorization or approval behavior

#### 0.1 exit gate

Mnemosyne 0.1 passes only when:

- Phoenix can switch from stock Hindsight to Mnemosyne without an Intelligence Core rewrite
- known recall/reflect tests are equivalent or better
- the copied `phoenix-core` data remains intact
- Phoenix permissions and execution boundaries are unchanged
- stock Hindsight remains a working rollback option

Only after this gate should Phoenix-specific Mnemosyne behavior begin.

## Mnemosyne follow-on roadmap

After 0.1 compatibility is proven:

- **0.2 — Phoenix metadata schema**
- **0.3 — Workspace / project bank routing**
- **0.4 — Cortex-native memory records**
- **0.5 — Tool outcome and repair learning**
- **0.6 — Provenance + contradiction handling**
- **0.7 — Retention and memory scoring**
- **0.8 — Phoenix Memory Core UI**
- **0.9 — Migration / backup / portable hardening**
- **1.0 — Stable Phoenix Memory Core**

Project V should continue tracking upstream Hindsight so relevant bug fixes, retrieval improvements, database migrations, performance work, and security fixes can be selectively evaluated and merged.

## Research phase

### Phoenix Unbound

Phoenix Unbound remains a separate research branch/environment for studying broader autonomous behavior inside a deliberately isolated sandbox.

It is not intended to replace or weaken the stable production Phoenix permission model.

Research goals include:

- sandboxed self-directed research
- controlled self-modification
- tool and workflow creation
- measurable iteration and rollback
- Model Council review
- strict separation from production data and systems

Mnemosyne development should not require weakening Phoenix Unbound or production isolation boundaries.

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
