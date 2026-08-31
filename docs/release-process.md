# Release Process

## Scope

Collection tags and GitHub Releases publish complete Microsoft Office
Resources collection states. Components maintain independent
VERSION/CHANGELOG state inside that collection and formally released
component milestones use namespaced annotated Git tags.

## Pre-release gates

1.  Confirm the intended root `VERSION`.
2.  Confirm each changed component's `VERSION` and `CHANGELOG.md`.
3.  Confirm root `CHANGELOG.md` and `RELEASES.md`.
4.  Verify canonical artifacts against their documented source
    revisions.
5.  Review Office metadata when Office artifacts changed.
6.  Verify reference/assets and any component-specific audit
    requirements.
7.  Build curated release assets only when useful.
8.  Generate one `SHA256SUMS` covering manually uploaded payload assets.
9.  Stage the intended release state and require
    `git diff --cached --check` to produce no output.
10. Run the complete repository audit.
11. Require a clean Git working tree after the release commit and before
    tagging.

Stop on any failed verification.

## Commit and publication

1.  Commit the complete release state.
2.  Push `main`.
3.  Verify local `HEAD` equals `origin/main`.
4.  Create annotated collection tag `vX.Y.Z`.
5.  Create any component milestone tags due for this release using
    `<component>/vX.Y.Z`.
6.  Verify every tag object and target locally.
7.  Push the intended tags.
8.  Verify every remote tag resolves to the intended commit.
9.  Publish GitHub Release `Microsoft Office Resources vX.Y.Z` from the
    **collection** tag only.
10. Upload approved curated assets and `SHA256SUMS`.
11. Verify published assets/checksums.

Do not make an untagged post-release synchronization commit. Any
subsequent repository change belongs to a subsequent collection version.
