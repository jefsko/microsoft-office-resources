# Release Process

## Scope

Git tags and GitHub Releases publish the complete Microsoft Office
Resources collection. Components maintain independent VERSION/CHANGELOG
state inside that collection.

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
9.  Run the complete repository audit.
10. Require a clean Git working tree before tagging.

Stop on any failed verification.

## Commit and publication

1.  Commit the complete release state.
2.  Push `main`.
3.  Verify local `HEAD` equals `origin/main`.
4.  Create annotated tag `vX.Y.Z`.
5.  Push the tag.
6.  Verify the remote tag resolves to the intended release commit.
7.  Publish GitHub Release `Microsoft Office Resources vX.Y.Z` from that
    tag.
8.  Upload approved curated assets and `SHA256SUMS`.
9.  Verify published assets/checksums.

Do not make an untagged post-release synchronization commit. Any
subsequent repository change belongs to a subsequent collection version.
