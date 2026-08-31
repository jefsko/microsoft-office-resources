# USPS Label 228

Microsoft Word resources for USPS Label 228 (December 2023), including
the canonical Word template, reference image, reusable logo assets,
calibration documents, and preserved template-development history.

## Canonical template

`USPS-Label-228-Template.dotx` is the canonical template filename. For
project version v1.0.0, it is based on Template Rev17.

## Repository layout

-   `assets/logos/` --- reusable USPS Label 228 logo/image assets.
-   `reference/` --- polished reference material for the physical label.
-   `development/template-revisions/` --- Template Rev1 through Rev17.
-   `development/calibration/` --- Calibration Rev1 and Rev2.
-   `docs/` --- handover, audits, and supporting project documentation.

Historical template files were originally developed under the
`USPS-Label-228-Production-Rev<N>.dotx` naming convention. Repository
copies were normalized to `USPS-Label-228-Template-Rev<N>.dotx`.

Template Rev18 was rejected/reverted and is permanently retired. It is
not included; future template development resumes at Rev19.

## Versioning terminology

Artifact revisions track individual artifact development. Component
versions use `vX.Y.Z` independently of the collection version. Formally
released component milestones use namespaced Git tags such as
`usps-label-228/v1.0.0`; GitHub Releases remain collection-level only.
Canonical means authoritative in context; the canonical filename remains
stable while component/collection tags provide version context.

## Checksums and releases

Routine per-file checksum sidecars are not stored in the source tree.
Published release payloads receive SHA-256 coverage at the distribution
boundary. Collection v1.0.1 used one `.sha256` sidecar per manually
uploaded payload, including the template, reference image, logo-assets
ZIP, and collection ZIP.
