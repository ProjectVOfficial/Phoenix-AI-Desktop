# Binary Distribution Policy

This repository currently serves as a **binary and documentation repository** for Phoenix AI Desktop.

## What belongs here now

- Validated Windows installers
- Validated portable executables
- Release notes
- Checksums
- User-facing documentation
- Security and privacy documentation

## What does not belong here now

- Phoenix application source code
- Development branches or experimental source trees
- Local AI model files
- Python virtual environments
- Node.js dependency directories
- Build caches
- User memory databases
- Workspaces
- Logs
- API keys, tokens, or credentials
- Connector vaults
- Signing keys or certificates

## Releases vs repository files

Executable builds should normally be attached to **GitHub Releases** instead of committed directly to the Git history.

This keeps the repository readable, avoids bloating Git history, and makes each binary clearly associated with a version and release note.

## Future source publication

Source code may be introduced after the current Phoenix development cycle and the Phoenix Unbound research phase are complete.

When that happens, the repository structure, contribution policy, build instructions, dependency documentation, and licensing terms can be expanded accordingly.
