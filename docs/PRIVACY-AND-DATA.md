# Privacy and Local Data

Phoenix is built around local-first operation, but local-first does not mean that every optional integration is offline.

## Local data

Depending on configuration and build, Phoenix may maintain local:

- preferences
- model settings
- conversation/project context
- long-term memory
- workspaces
- tool state
- logs
- indexes or embeddings
- integration configuration

These files can contain sensitive information.

## External services

If the user enables a cloud model, web research service, connector, email integration, repository integration, or another external provider, information sent through that integration is subject to the provider and the user's configuration.

Phoenix should not be described as fully offline when an enabled feature requires network access.

## Repository safety

Never upload personal Phoenix data to this repository. In particular, do not publish:

- memory databases
- chat exports containing private information
- connector credentials
- API keys
- authentication cookies/tokens
- private workspace contents
- local configuration containing secrets

## Backups

Users should back up important Phoenix data before major upgrades. Backup procedures may vary by version and storage configuration.

## Portable installations

Portable installations can move sensitive data between systems. Protect removable media appropriately and avoid leaving credentials or private memory on untrusted computers.
