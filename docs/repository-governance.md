# Repository Governance

## Purpose

`microsoft-office-resources` is a versioned collection of Microsoft
Office templates, reference materials, measurements, documentation,
examples, and tips.

## Organization

Resources are organized first by Office application, then by resource
type and component. Do not create empty application/category directories
merely to reserve future hierarchy. Add directories when content exists.

Component-specific development/reference history remains with the
component.

## Version scopes

The root `VERSION` identifies the collection version. Independently
maintained components may have their own component-root `VERSION`. These
are independent Semantic Versioning sequences. Individual artifacts may
additionally maintain monotonically increasing revision lineages.

Collection tags use annotated `vX.Y.Z` tags. Formally released component
version milestones use namespaced annotated tags such as
`usps-label-228/v1.0.0`. Each collection release records the component
versions it contains.

GitHub Releases are collection-level only. Component tags do not receive
separate GitHub Releases.

## Naming

Use descriptive, stable, filesystem-safe names. Canonical component
filenames normally remain stable across component and collection
versions; Git history provides historical snapshots.

Historical artifact revisions may use:

`<Project>-<Artifact>-Rev<N>.<ext>`

Revision numbers are monotonically increasing within an artifact
lineage, do not reset at release boundaries, and are never reused after
assignment, including rejected/reverted revisions.

Legacy filenames may be normalized when importing material.
Normalization brings historical names into the repository's chosen
convention while preserving provenance and documenting the mapping.

## Canonical artifacts

Canonical means authoritative in a particular context. Use **canonical
filename** when referring specifically to the official stable filename.

## Development history

Development artifacts with durable reference value may be retained in a
component-local `development/` hierarchy. Rejected revisions need not be
stored as binaries, but assigned revision numbers are not reused and
material omissions/gaps must be documented.

## Metadata

Public Office artifacts receive a deliberate metadata review before
release. Correct demonstrably inaccurate descriptive metadata, preserve
legitimate provenance unless there is a reason not to, avoid inventing
history, and document normalization that changes artifact bytes.

## Checksums

Do not create routine per-file `.sha256` sidecars throughout the tracked
source tree. Use SHA-256 at release/distribution boundaries and for
integrity-sensitive normalization/audit operations. A GitHub Release
should normally use one `SHA256SUMS` file listing the other manually
uploaded release assets.

## Archives

Do not commit ZIP files merely as duplicates of source-tree content.
Archives intended for convenient distribution belong primarily as GitHub
Release assets. Git tags and GitHub source archives preserve complete
versioned repository snapshots.

## Git files

Use `.editorconfig` for basic text-editor consistency, `.gitignore` for
local, editor, and Office temporary files, and `.gitattributes` to
normalize text and classify Office/image/archive artifacts as binary.
Add other Git dotfiles only when a concrete repository need develops.

## Licensing

The repository uses the standard MIT `LICENSE` for material for which
Jeff Skone has the right to grant that license.

Third-party material is not relicensed merely because it appears in the
repository. `THIRD-PARTY-NOTICES.md` records exclusions and
rights/provenance notes, including USPS names, marks, logos, Priority
Mail branding, and reference/derived imagery.

Review both licensing documents whenever materially different
third-party content is introduced.
