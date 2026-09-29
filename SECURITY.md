# Security Policy

## Reporting a security issue

Because Phoenix AI Desktop is currently distributed from a private repository, security findings should be reported privately to the Project V maintainers rather than posted in public discussion.

Do not include real credentials, private user data, tokens, memory databases, or other sensitive material in an issue.

## Sensitive data

The following must never be committed:

- passwords
- API keys
- access tokens
- connector/session credentials
- signing keys
- certificate private keys
- memory databases
- personal workspaces
- private logs
- local environment files containing secrets

## Executable releases

Only validated builds should be uploaded as official releases.

Where practical, releases should include a SHA-256 checksum so downloaded binaries can be verified.

## Local execution

Phoenix may have access to files, tools, models, scripts, and system functionality depending on user configuration. Users should understand the permissions granted to Phoenix and keep approval controls enabled for higher-impact actions unless they are operating in a deliberately isolated test environment.

## Experimental autonomy

Experimental autonomy research should be separated from normal production use and should not be conducted with valuable host data or credentials available to the test environment.
