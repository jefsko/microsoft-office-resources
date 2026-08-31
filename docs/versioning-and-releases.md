# Versioning and Releases

## Version scopes

This repository uses three distinct version/revision scopes.

### Collection version

The root `VERSION` identifies the version of the complete
`microsoft-office-resources` collection. Collection versions use
`X.Y.Z`. Collection Git tags use `vX.Y.Z`.

GitHub Releases apply to collection versions only.

### Component version

An independently maintained component may have its own `VERSION` file in
the component root. Component versions also use `X.Y.Z`, but are
independent of the collection version and of other components.

A formally released component-version milestone receives a namespaced
annotated Git tag in this form:

`<component>/vX.Y.Z`

For USPS Label 228, for example:

`usps-label-228/v1.0.0`

A component tag is an immutable Git milestone. It does **not** create or
require a separate GitHub Release.

### Artifact revision

A revision tracks the development lineage of an individual artifact,
such as Template Rev17. Revisions increase monotonically, do not reset
at collection or component release boundaries, and are never reused
after assignment.

## VERSION file format

A `VERSION` file contains only the numeric three-part version, such as
`1.0.1`. The `v` prefix is used in prose and Git tags.

## Tags and GitHub Releases

A collection tag identifies an immutable snapshot of the complete
repository. A collection GitHub Release is created from the appropriate
collection tag when that collection version is selected for publication.
Not every historical collection tag must have a GitHub Release.

A component tag identifies the repository commit at which that component
version is formally marked as a released milestone. Multiple collection
and component tags may legitimately point to the same commit.

Every collection release records the component versions it contains.

## Initial publication history

-   Collection v1.0.0 is the initial committed repository state and is
    preserved by collection tag `v1.0.0`. It has no GitHub Release.
-   Collection v1.0.1 establishes the finalized component-tag/release
    governance and is the first planned GitHub Release.
-   USPS Label 228 remains component v1.0.0 and is formally marked by
    component tag `usps-label-228/v1.0.0` at the v1.0.1 publication
    commit.
-   No separate GitHub Release is created for the component tag.

## Version increments

Collection and component version bumps are evaluated independently.

-   **MAJOR (`X`)** --- incompatible or fundamental change at that
    scope.
-   **MINOR (`Y`)** --- meaningful backward-compatible addition or
    enhancement.
-   **PATCH (`Z`)** --- backward-compatible correction or maintenance.

A collection-only documentation/governance correction may bump the
collection PATCH without changing component versions. Adding a new
component may bump the collection MINOR while existing component versions
remain unchanged.
