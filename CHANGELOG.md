# Changelog

This changelog records changes to the Microsoft Office Resources
collection. Component-specific changes are recorded in each component's
changelog.

## Unreleased

### Changed

-   Implemented `MOR-006` to reconcile current documentation with the
    verified, published v1.0.1 release state.
-   Replaced stale release-candidate/planning language, recorded the
    actual v1.0.1 Git/tag/release facts, and aligned checksum guidance
    with the payload-specific `.sha256` sidecars used for publication.
-   Corrected USPS Label 228 handover references to the locked Template
    Rev17 baseline and its post-normalization repository SHA-256.
-   No collection/component version, published tag/release, Office
    binary, reference image, or logo asset changed.

## v1.0.1

Governance and release-model correction. No USPS Label 228 artifact
content changed in this collection update.

### Changed

-   Established namespaced component milestone tags in
    `<component>/vX.Y.Z` form.
-   Confirmed that GitHub Releases remain collection-level only;
    component tags do not receive separate GitHub Releases.
-   Recorded collection v1.0.0 as the tagged initial repository state
    without a GitHub Release.
-   Added `git diff --cached --check` as an explicit mandatory staged-tree
    release gate.
-   Corrected release/governance documentation to distinguish the
    collection version, component version, and artifact revision.

### Components

-   USPS Label 228 remains v1.0.0, based on Template Rev17.

## v1.0.0

Initial committed collection state.

### Components

-   USPS Label 228 v1.0.0.

### Repository framework

-   Established collection/component/artifact versioning model.
-   Added repository governance, release-process, Git/GitHub workflow,
    and configuration documentation.
-   Added `.editorconfig`, `.gitattributes`, and `.gitignore`.
-   Added scoped repository licensing with explicit third-party
    exclusions.
