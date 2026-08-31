# Versioning and Releases

## Version scopes

This repository uses three distinct version/revision scopes.

### Collection version

The root `VERSION` identifies the version of the complete
`microsoft-office-resources` collection. Collection versions use
`X.Y.Z`. Git tags and GitHub Releases apply to collection versions.

### Component version

An independently maintained component may have its own `VERSION` file in
the component root. Component versions also use `X.Y.Z`, but are
independent of the collection version and of other components.

For the initial publication:

-   Microsoft Office Resources collection: v1.0.0
-   USPS Label 228 component: v1.0.0

These are two distinct v1.0.0 version sequences.

### Artifact revision

A revision tracks the development lineage of an individual artifact,
such as Template Rev17. Revisions increase monotonically, do not reset
at collection or component release boundaries, and are never reused
after assignment.

## VERSION file format

A `VERSION` file contains only the numeric three-part version, such as
`1.0.0`. The `v` prefix is used in prose, Git tags, and GitHub Release
titles.

## Collection releases and tags

A Git tag such as `v1.0.0` identifies an immutable snapshot of the
entire collection. A GitHub Release is collection-wide and is created
from that tag.

Every collection release records the component versions it contains.
Components normally do not require separate Git tags or GitHub Releases.

## Version increments

Collection and component version bumps are evaluated independently.

-   **MAJOR (`X`)** --- incompatible or fundamental change at that
    scope.
-   **MINOR (`Y`)** --- meaningful backward-compatible addition or
    enhancement.
-   **PATCH (`Z`)** --- backward-compatible correction or maintenance.

A collection-only documentation correction may bump the collection PATCH
without changing component versions. Adding a new component may bump the
collection MINOR while existing component versions remain unchanged.
