# Release Process

Phoenix executable releases should be published through GitHub Releases.

## Versioning

Use a clear version identifier for every distributed build. Alpha or experimental builds should remain visibly identified as such.

Example:

`Phoenix Desktop 0.15.0-a`

## Each release should include

- version number
- release date
- stability designation
- concise summary of changes
- important fixes
- known limitations
- upgrade notes
- installer/portable filename
- checksum when available

## Recommended assets

Typical release assets may include:

- Windows installer
- Windows portable executable/package
- SHA-256 checksum file
- optional release-specific notes

## Validation before publishing

Before attaching a build:

1. Confirm the intended version number.
2. Run the project's required typecheck/build/test validation.
3. Launch the packaged application.
4. Confirm core startup and memory behavior.
5. Verify no credentials or personal data are embedded in the package.
6. Generate and record checksums.
7. Publish clear release notes.

## Source code

Until the repository policy changes, releases contain binaries and documentation rather than the application source tree.
