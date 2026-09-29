# Installation

Phoenix AI Desktop is currently distributed as a Windows executable/installer rather than as source code.

## Recommended installation

1. Open the repository's **Releases** page.
2. Download the newest validated Phoenix installer or portable executable.
3. If a checksum is published for the release, verify it before running the file.
4. Run the installer or launch the portable build.
5. Complete Phoenix's first-run configuration for local models, storage, memory, and optional integrations.

## Windows security prompts

Windows may display reputation or SmartScreen warnings for newly published builds, particularly while a release has limited download history. Verify that the file came from the official **ProjectVOfficial/Phoenix-AI-Desktop** repository before proceeding.

## Local AI dependencies

Some Phoenix capabilities depend on local inference software or separately installed models. Those components are not necessarily bundled with every Phoenix release.

Supported local inference integrations may evolve over time. Follow the notes included with each release for the exact requirements of that build.

## Updating

Before installing a new build:

- Exit Phoenix completely.
- Preserve any important user data or configuration.
- Read the release notes for migration or compatibility information.
- Do not overwrite or delete memory/configuration directories unless the release notes explicitly require it.

## Portable use

Phoenix is designed to support local and portable workflows. Where a build exposes a selectable data path, removable storage may be used for appropriate Phoenix data.

Portable storage should still be treated as sensitive if it contains memory, workspaces, credentials, or configuration.

## Source builds

Source build instructions are intentionally not published at this stage because this repository currently distributes binaries and documentation only.
