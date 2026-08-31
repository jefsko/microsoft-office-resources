# USPS Label 228 --- Handover and Summary

**Document revision:** Rev. 12\
**As of:** August 29, 2026\
**Subject:** Microsoft Word template for USPS Label 228 (December 2023
Priority Mail label)\
**Canonical Word template name:** `USPS-Label-228-Template.dotx`\
**Canonical reference image name:** `USPS-Label-228-Reference.png`\
**Canonical handover name:** `USPS-Label-228-Handover-and-Summary.md`

## Current Status

**Accepted / locked baseline.**

The Word-template interaction model has been validated in desktop
Microsoft Word:

-   Both sample addresses initially appear.
-   `From Address` and `To Address` are the approved long
    content-control field names.
-   Field labels appear only while the corresponding field has focus and
    do not print.
-   Tab navigation works between the two address fields.
-   The entire sample placeholder disappears when the user begins
    typing.
-   All four editing-region boundaries are visible as nonprinting Word
    gridlines.
-   The address text has comfortable buffer space from the
    editing-region boundaries.
-   The template remains macro-free.
-   Opening the `.dotx` creates a new Word document; editing and saving
    that document does not alter the defaults stored in the template.
-   The final alignment target for both FROM and TO values is
    approximately **1/4 inch down × 3/8 inch right** from the
    corresponding printed label legends. Production Rev. 15 incorporates
    the final TO vertical correction requested during physical alignment
    review.

The canonical template filename remains:

`USPS-Label-228-Template.dotx`

The project now also includes a locked clean reference image:

`USPS-Label-228-Reference.png`

## Purpose

Create a macro-free Microsoft Word `.dotx` template aligned to the
self-adhesive USPS Label 228, with convenient FROM and TO address-entry
regions, useful editing guidance, predictable keyboard navigation, and
clean printed output.

The template is intended for individually fed USPS Label 228 stock.
Ordinary 8.5 × 11 inch paper may be used for calibration/overlay
testing.

## Physical Label Measurements and Calibration Basis

Measurements established from the physical December 2023 USPS Label 228
and ruler-reference photographs:

-   Backing/media sheet: approximately **5 8/16 in × 4 5/16 in**
    -   Equivalent: **5 1/2 in × 4 5/16 in**
-   Adhesive label: approximately **5 5/16 in × 4 2/16 in**
    -   Equivalent: **5 5/16 in × 4 1/8 in**

The Word page is oriented so the media dimensions are represented as
approximately:

-   Width: **4 5/16 in**
-   Height: **5 1/2 in**

Reference measurements from the adhesive label included:

-   Bottom of physical `FROM:` legend: approximately **1 1/8 in** from
    the top.
-   Right edge of physical `FROM:` legend: approximately **9/16 in**
    from the left.
-   Bottom of physical `TO:` legend: approximately **3 in** from the
    top.
-   Right edge of physical `TO:` legend: approximately **1 1/16 in**
    from the left.

Physical print/overlay testing is authoritative over screen appearance
or theoretical geometry.

## Accepted Editing and Field Design

The template contains two multiline address-entry controls:

-   **From Address**
    -   Internal identifier/tag: `FromAddress`
-   **To Address**
    -   Internal identifier/tag: `ToAddress`

The longer field names are preferred over simply `FROM:` and `TO:`
because they more clearly identify the editing controls.

The field names are Word content-control UI metadata rather than
ordinary document text. They appear when the corresponding control has
focus and disappear when focus changes. They do **not** print.

### Address Formatting

Actual entered address values should use:

-   Arial
-   10 pt
-   Regular/nonitalic
-   Black
-   Left aligned
-   Multiline

The FROM region is intended for approximately four lines and the TO
region for approximately five lines. These are practical recommendations
rather than hard character/line limits.

## Placeholder / Sample Data

Approved sample data:

### From Address

    John Smith
    123 Example Street
    Bellevue, WA 98000

### To Address

    Jane Smith
    Example Company
    456 Example Avenue, Suite 100
    Seattle, WA 98101-1234

The sample data is displayed as gray italic placeholder content.

Verified behavior:

-   The sample appears when a fresh document is created from the
    template.
-   As soon as the user begins typing in a field---even a single
    character---the **entire sample for that field disappears**.
-   The sample data is known to appear in Print Preview and **will print
    if the user leaves the field untouched**.
-   This printing limitation is accepted after testing alternative
    macro-free approaches.

Do not convert the sample addresses into ordinary permanent document
text.

## Nonprinting Editing Boundaries

The FROM and TO regions use Word table gridlines as nonprinting editing
boundaries.

Accepted behavior in Production Rev. 13:

-   All four sides of both address regions are visible when Word's
    **View Gridlines** behavior is active.
-   Gridlines do not appear in Print Preview and do not print.
-   A slight internal buffer keeps address text from touching the
    editing boundaries on any side.

The successful padding implementation is based on the Rev. 10 table
structure with paragraph-level spacing/indenting. Do **not** reintroduce
the Rev. 11/12 cell-margin approach, which caused the top and bottom
gridlines to disappear in desktop Word.

## Keyboard Navigation

Verified:

-   Tab moves between the two address fields.
-   The field-specific content-control label appears when that field has
    focus.
-   The current field's placeholder disappears completely once entry
    begins.

The form should remain macro-free.

## Verified Acceptance Baseline

The following behaviors have been personally tested in desktop Microsoft
Word and should be treated as regression requirements:

1.  **Tab works between the two fields.**
2.  **Field labels appear only when the corresponding field has focus.**
3.  **Sample data appears initially, prints if untouched, and disappears
    completely after the user enters a single character.**
4.  **All four nonprinting editing borders/gridlines are visible.**
5.  **There is buffer space between field values and all border sides.**
6.  Compatibility Mode is no longer displayed.
7.  The long field labels themselves do not print.
8.  Gridlines do not print.
9.  Multiline address entry works.
10. Physical alignment is generally good. Production Rev. 16
    incorporates the final approved TO vertical correction documented
    below.

## Remaining Physical Calibration

A more careful physical measurement superseded the earlier proposed
FROM-only adjustment.

Measured pre-Rev. 14 spacing:

-   FROM: approximately **4/16 inch down** and **7/16 inch right** of
    the physical `FROM:` legend.
-   TO: approximately **3/16 inch down** and **6/16 inch right** of the
    physical `TO:` legend.

Approved common target:

-   **4/16 inch (1/4 inch) down**
-   **6/16 inch (3/8 inch) right**

Implemented in Production Rev. 14:

-   **FROM: move left 1/16 inch; no vertical change**
-   **TO: move down 1/16 inch; no horizontal change**

No other intentional geometry or behavior change was made.

After this adjustment, perform another actual Label 228 print. If
alignment is satisfactory and the accepted Rev. 13 behavior remains
intact, promote the result to the canonical final template.

## DOTX Workflow --- Verified

Normal intended use:

1.  Double-click/open `USPS-Label-228-Template.dotx`.
2.  Word creates a **new document based on the template** rather than
    modifying the template itself.
3.  Replace the sample FROM and TO addresses.
4.  Print and/or save the resulting document as a `.docx`.
5.  Opening the `.dotx` again creates another fresh document containing
    the original sample/default addresses.

This behavior has been tested successfully.

Changing and saving a document created from the DOTX does **not** modify
the canonical DOTX defaults.

Editing the DOTX itself as a template is a different operation and can
change its defaults.

## Canonical Filename

Use:

`USPS-Label-228-Template.dotx`

Development revisions such as `USPS-Label-228-Production-Rev13.dotx` are
useful during development and testing but should not be exposed as the
canonical production filename.

## Development / Revision History

### Calibration Rev. 1

Established the initial physical/media geometry and printable
calibration layout.

### Calibration Rev. 2

Added reference replicas for the physical USPS `FROM:` and `TO:` legends
to help compare printed registration.

### Production Rev. 1

Established the initial functional Word-template concept with multiline
address controls. Physical testing showed generally good alignment but
identified placement and editing-UI issues.

### Production Rev. 2

Experimented with hidden calibration artwork/information. Desktop Word
did not reliably display the intended hidden guidance. Rejected.

### Production Rev. 3

Moved toward borderless tables and Word gridlines. Corrected modern Word
compatibility behavior. Physical alignment improved.

### Production Rev. 4

Fine-tuned FROM/TO vertical positioning and introduced approved sample
placeholder addresses. Testing established that the placeholder samples
print when untouched.

### Production Rev. 5

Temporarily removed sample data and changed control titles to `FROM:` /
`TO:`. Blank printing behavior was proven, but the shorter control
titles were less desirable.

### Production Rev. 6

Restored longer sample placeholders and `From Address` / `To Address`
terminology. Continued work on gridline behavior.

### Production Rev. 7

Successfully improved the four-sided gridline structure and suppressed
intrusive content-control box behavior. This was an important structural
improvement.

### Production Rev. 8

Experimented with separate hidden-text field labels and altered form
structure. Desktop Word showed empty structural boxes instead of the
intended labels. Rejected.

### Production Rev. 9

Experimented with ordinary visible `From Address` / `To Address` text.
The labels printed, which was undesirable. Rejected.

### Production Rev. 10

Restored the preferred long, focus-dependent, nonprinting
content-control labels while retaining the successful four-sided
gridline structure. Became the stable structural baseline.

### Production Rev. 11

Attempted four-sided internal padding using table-cell margins. This
caused top/bottom gridlines to disappear. Rejected.

### Production Rev. 12

Attempted to repair the Rev. 11 horizontal-gridline regression. Desktop
Word still lacked top/bottom gridlines. Rejected.

### Production Rev. 13

Rebuilt from the known-good Rev. 10 structure and implemented the
desired buffer using paragraph-level spacing/indenting rather than cell
margins.

Desktop Word verification confirmed:

-   Tab works between fields.
-   Long field labels appear on focus only.
-   Placeholder behavior works.
-   All four gridline sides are visible.
-   Buffer exists on all sides.

**Rev. 13 is the current accepted functional baseline.**

## Approaches Tested and Rejected

### Hidden Text for General Screen-Only Guidance

Word supports hidden text, but the attempts to force template-provided
hidden labels/guidance to be visible while remaining nonprinting were
not reliable in the user's desktop Word environment.

Do not rely on this approach for the production template.

### Ordinary Visible Field Labels

Ordinary `From Address` / `To Address` text prints. Do not use it for
editing-only field identification.

### Short `FROM:` / `TO:` Content-Control Titles

Technically workable and nonprinting, but the longer `From Address` /
`To Address` titles are preferred for clarity.

### Cell-Margin Padding

Changing cell margins destabilized Word's nonprinting gridline display.
Rev. 11 and Rev. 12 demonstrated this. Preserve the successful Rev. 13
paragraph-level buffer approach instead.

### Macros

The template is intentionally macro-free. Do not introduce VBA merely to
manage placeholder printing, field labels, focus, or overflow unless
this requirement is explicitly reconsidered later.

## Locked Reference Image

The canonical clean reference image is:

`USPS-Label-228-Reference.png`

Accepted specifications:

-   Source basis: the photographed physical **December 2023 USPS Label
    228**.
-   Intended role: clean visual/reference asset, distinct from the
    functional Word template.
-   Processing method for the locked final geometry: **deterministic /
    non-generative raster processing**. Generative recreation is not
    appropriate for the canonical measurement/reference asset because it
    can silently alter typography, logo geometry, spacing, line weights,
    or other source details.
-   Adhesive-label physical dimensions: **4 1/8 in wide × 5 5/16 in
    high**.
-   Exact width:height aspect ratio: **66:85**.
-   Final raster dimensions: **1320 × 1700 px**.
-   Embedded resolution: **320 DPI**.
-   At 320 DPI, 1320 × 1700 px corresponds exactly to **4.125 × 5.3125
    in**.
-   Corners: **square** for the reference exercise.
-   Background/perimeter: **pure white**.
-   Outer black outline: **none**.
-   File format: **PNG**, selected as the lossless canonical reference
    format.
-   The wax-paper backing is not part of the reference-image geometry.

The physical backing/media measurements remain useful for Word
printer/page setup, but they must not be confused with the
adhesive-label dimensions used for the reference image.

### Reference-Image Methodology

For future revisions, prefer a non-generative workflow:

1.  Start from the highest-quality original photograph.
2.  Correct perspective/rotation.
3.  Isolate the adhesive label rather than the backing sheet.
4.  Correct illumination, white balance, contrast, shadows, and
    photographic noise while preserving printed artwork.
5.  Preserve the measured **66:85** label geometry.
6.  Use square corners and a pure-white intended background/perimeter
    for this reference asset.
7.  Do not add a black perimeter outline.
8.  Export losslessly as PNG.
9.  Verify the actual pixel dimensions and calculate the aspect ratio
    before accepting the file.

If a future restoration is rebuilt directly from an original photograph,
that higher-fidelity source workflow is preferable to repeatedly
resampling an intermediate cleaned image.

## Known Word Limitations / Accepted Tradeoffs

-   Content-control field labels are contextual Word UI; they are not
    permanent captions.
-   Placeholder sample addresses print if untouched.
-   Word does not provide a sufficiently reliable, simple macro-free
    mechanism discovered in this project for arbitrary rich
    informational text that is always visible on screen yet guaranteed
    never to print.
-   Gridlines are an editing aid and are controlled/displayed by Word
    rather than being printable borders.
-   Line/character capacity is not hard-enforced. Users can enter more
    text than the recommended region accommodates; visual region
    boundaries provide the practical cue.

These are accepted tradeoffs.

## Do-Not-Regress Guidance

The current design is the result of repeated desktop-Word and
physical-print testing. Avoid casual structural changes.

In particular:

-   Do not change the successful Rev. 13 table/gridline structure merely
    for cosmetic reasons.
-   Do not reintroduce Rev. 11/12 cell-margin padding.
-   Do not turn editing gridlines into printable borders.
-   Do not turn the focus-dependent field labels into ordinary document
    text.
-   Do not replace the long `From Address` / `To Address` labels with
    shorter names unless explicitly requested.
-   Do not introduce macros.
-   Do not change TO geometry without a new physical calibration reason.
-   Preserve the approved sample data unless explicitly changed.
-   Preserve the behavior in which the entire placeholder disappears on
    first input.
-   Treat an actual physical Label 228 print as the final authority for
    alignment.

## Final Acceptance / Lock-In

The current project artifacts are considered the accepted baseline.

Before replacing either canonical artifact in the future, re-verify:

1.  Word-template content-control behavior and Tab navigation.
2.  Placeholder replacement behavior.
3.  Nonprinting field labels and gridlines.
4.  Actual physical print alignment on USPS Label 228 stock.
5.  Reference-image dimensions of **1320 × 1700 px**.
6.  Exact reference-image aspect ratio of **66:85**.
7.  Embedded **320 DPI** metadata.
8.  Pure-white perimeter, square corners, and absence of a black outer
    outline.
9.  Non-generative preservation of the reference artwork unless
    reconstruction is explicitly approved.

## Canonical Artifact Set

-   `USPS-Label-228-Template.dotx` --- functional Microsoft Word
    template.
-   `USPS-Label-228-Reference.png` --- locked clean visual/reference
    image.
-   `USPS-Label-228-Handover-and-Summary.md` --- authoritative project
    handover and summary.
-   `USPS-Label-228-Logo-Asset-Set.zip` --- locked packaged USPS logo
    reference asset set.
-   `USPS-Logo-Asset-Preview-Sheet.png` --- compact visual/contact-sheet
    reference included with the logo asset set.

Working files such as `USPS-Label-228-Production-Rev17.dotx`,
calibration documents, and earlier revisions are development/history
artifacts and should not replace the canonical filenames above.

## Public-Repository Normalization Plan

The new public `microsoft-office-resources` repository will preserve the
USPS Label 228 development history while normalizing its organization
and terminology for long-term consistency.

### Historical Template Naming

Historical template-development files were originally named
`USPS-Label-228-Production-Rev<N>.dotx`. For import into the public
repository, repository copies will be renamed
`USPS-Label-228-Template-Rev<N>.dotx`.

This is repository naming normalization: legacy working filenames are
brought into the repository's chosen artifact-based naming convention
without changing their historical identity or revision sequence. The
original term `Production` remains part of the historical record.

Normalized locations:

-   `development/template-revisions/` --- Template Rev1 through Rev17.
-   `development/calibration/` --- Calibration Rev1 and Rev2.

Template Rev17 (originally Production Rev17) is the source revision for
the canonical `USPS-Label-228-Template.dotx`. Rev18 was created,
rejected, reverted, and permanently retired. Revision 18 will not be
reused; future template development resumes with Template Rev19.

### Revision, Version, Release, and Canonical Terminology

-   **Revision** tracks an individual artifact's development lineage.
    Revisions increase monotonically, do not reset at release
    boundaries, and are never reused.
-   **Component version** identifies an approved USPS Label 228 project
    state and uses `vX.Y.Z`. The current component version is v1.0.0.
-   **Collection version** identifies the complete
    `microsoft-office-resources` repository state independently of the
    component version.
-   **Release** is formal publication/distribution. GitHub Releases are
    collection-level; the component receives a namespaced Git milestone
    tag when formally released.
-   **Canonical** means authoritative in context. Use **canonical
    filename** for the official filename.

The canonical template filename is `USPS-Label-228-Template.dotx` and
remains stable across releases; component VERSION/changelog state and Git
tags supply version context.

### Metadata Normalization Policy

Before repository import, the 17 template revisions and two calibration
documents will undergo controlled metadata-accuracy normalization. No
Office file is to be modified until the before/after specification is
reviewed and approved.

-   Normalize Title, Subject, and Description to identify each artifact
    and revision accurately.
-   Descriptions must be factual and evidence-based and must not encode
    transient status such as accepted, current, latest, locked, or
    released.
-   Normalize Word's internal Revision property to the artifact
    revision: Template Rev1--Rev17 use 1--17; Calibration Rev1--Rev2 use
    1--2.
-   Preserve Creator.
-   Preserve the empty LastModifiedBy property.
-   Preserve Created and Modified. All inspected files contain
    `2013-12-23T23:15:00Z`; these appear inherited rather than reliable
    project-history timestamps, but they are intentionally not
    rewritten.
-   Preserve `TotalTime = 0`.
-   Preserve benign Application/AppVersion and other Office metadata.
-   Do not perform broad metadata stripping.
-   Preserve embedded thumbnails/resources unless a concrete reason
    requires otherwise.

The normalization audit will record original and normalized filenames,
before/after SHA-256 values, metadata corrections, and verification that
no unintended content, layout, formatting, or behavior changed.

### SHA-256 and Release Assets

Routine per-file `.sha256` sidecars will not be committed throughout the
source tree. SHA-256 is used at the release/distribution boundary and in
the normalization audit.

Planned curated assets for the first collection GitHub Release
(collection v1.0.1, containing USPS Label 228 component v1.0.0):

-   `USPS-Label-228-Template.dotx`
-   `USPS-Label-228-Reference.png`
-   `USPS-Label-228-Logo-Asset-Set.zip`
-   `SHA256SUMS`

`SHA256SUMS` will reference the other release assets. The old Complete
Project ZIP will not be a GitHub Release asset.

Planned audit: `docs/audits/v1.0.0-repository-normalization-audit.md`

## Repository Normalization Execution Update

The approved v1.0.0 repository-normalization pass has now been executed
on repository copies of the 17 historical template revisions and two
calibration documents. Original source artifacts were not overwritten.

Execution results:

-   Historical template repository filenames were normalized from
    `USPS-Label-228-Production-Rev<N>.dotx` to
    `USPS-Label-228-Template-Rev<N>.dotx`.
-   Calibration filenames were retained.
-   Title, Subject, Description, and the Word core Revision property
    were normalized according to the approved metadata policy.
-   Creator, empty LastModifiedBy, Created, Modified, TotalTime,
    Application/AppVersion, embedded thumbnails, and other package
    content were preserved.
-   For every normalized Office file, every OOXML package member except
    `docProps/core.xml` was verified byte-for-byte identical to the
    source counterpart.
-   All 19 normalized Office files rendered successfully to one-page
    PNGs and were visually reviewed; no normalization-related layout
    defects were observed.
-   The canonical `USPS-Label-228-Template.dotx` was created as a
    byte-for-byte copy of normalized Template Rev17.
-   A detailed normalization audit was created at
    `docs/audits/v1.0.0-repository-normalization-audit.md`.

Direct OOXML comparison also established the late template geometry
lineage:

-   Rev14 -\> Rev15: TO moved down 1/8 inch.
-   Rev15 -\> Rev16: TO moved up 1/4 inch.
-   Rev16 -\> Rev17: TO moved down 1/16 inch.

Rev18 remains rejected/reverted and permanently retired; future template
development resumes with Rev19.

## Final Word-Template Lock-In

**Template Rev. 17 is locked as the accepted current/final
Word-template baseline for now.**

-   Canonical template: `USPS-Label-228-Template.dotx`
-   Preserved normalized template revision:
    `development/template-revisions/USPS-Label-228-Template-Rev17.dotx`
-   The canonical template and normalized Template Rev. 17 are
    byte-for-byte identical.
-   SHA-256:
    `ed0f5eca21ddb88fb2179c935a534e2c13b03eba8e6057ad601cccd58c1a1f9d`
-   Template Rev. 18 was reverted and is explicitly **not accepted**.
-   No further alignment change is currently required.
-   Any future Word-template change must begin from the locked Rev. 17
    baseline and create a **new production revision** rather than
    silently altering Rev. 17 or the historical record.

## Canonical Distribution Package

The final complete distribution package uses **canonical final filenames
only**. The revision-specific development copy
`USPS-Label-228-Production-Rev17.dotx` is preserved as historical
working evidence outside the distribution package, but is intentionally
omitted from `USPS-Label-228-Complete-Project.zip` because it is
byte-for-byte identical to the canonical `USPS-Label-228-Template.dotx`.

The canonical complete ZIP therefore contains six files:

-   `USPS-Label-228-Template.dotx`
-   `USPS-Label-228-Reference.png`
-   `USPS-Label-228-Logo-Asset-Set.zip`
-   `USPS-Label-228-Handover-and-Summary.md`
-   `USPS-Label-228-Manifest.md`
-   `USPS-Label-228-Complete-Project.sha256`

## USPS Logo Asset Set

A derived USPS Label 228 logo/reference asset set was subsequently
created from the approved Label 228 reference material and is now
**locked as an accepted final baseline**.

### Canonical Logo Configurations

The set contains three artwork configurations, each supplied in both a
pure-white-background PNG and a transparent-background PNG:

1.  `USPS-Logo-Postal-Service-White.png`
2.  `USPS-Logo-Postal-Service-Transparent.png`
3.  `USPS-Logo-Postal-Service-Priority-Mail-White.png`
4.  `USPS-Logo-Postal-Service-Priority-Mail-Transparent.png`
5.  `USPS-Logo-Priority-Mail-White.png`
6.  `USPS-Logo-Priority-Mail-Transparent.png`

The package also contains:

-   `USPS-Logo-Asset-Preview-Sheet.png` --- compact visual/contact-sheet
    reference for the six logo assets.
-   `USPS-Label-228-Logo-Asset-Set.zip` --- packaged distribution set.

"Logo asset" is used as the practical project term for these
extracted/reference artwork files. They are intended to remain faithful
to the printed artwork visible on the USPS Label 228 reference rather
than to reinterpret or redesign it.

### Final Geometry and Centering

All six logo PNGs were rebuilt and verified from their **actual visible
artwork bounds**. The accepted versions use exact geometric centering
rather than subjective optical offsets.

  ---------------------------------------------------------------------
  Logo             Final dimensions      Left / right      Top / bottom
  configuration                               padding           padding
  --------------- ----------------- ----------------- -----------------
  Postal Service        213 × 48 px        13 / 13 px          8 / 8 px

  Postal                371 × 48 px        23 / 23 px          8 / 8 px
  Service +
  Priority Mail

  Priority Mail         128 × 49 px        10 / 10 px          8 / 8 px
  ---------------------------------------------------------------------

For every configuration:

-   The white and transparent variants use **identical canvas dimensions
    and artwork placement**.
-   Opposing padding is numerically equal.
-   White-background variants use pure **#FFFFFF**.
-   Transparent variants use transparency outside the artwork.
-   Different logo configurations intentionally have different
    dimensions; they are not forced into a common canvas size.
-   The combined Postal Service + Priority Mail configuration was
    already visually well proportioned, but it was nevertheless included
    in the final geometric revalidation.
-   The final Priority Mail assets specifically correct an earlier
    version that appeared to contain excess whitespace on the right and
    bottom.

### Asset Methodology

The preferred methodology is preservation/restoration rather than
creative regeneration:

1.  Use the approved USPS Label 228 reference artwork as the source.
2.  Preserve the appearance, proportions, colors, wording, and
    arrangement of the printed marks.
3.  Determine the visible artwork bounds.
4.  Crop to those bounds.
5.  Add deliberate equal opposing padding.
6.  Produce the white and transparent variants from the same geometry.
7.  Verify geometric centering programmatically.
8.  Rebuild the preview sheet from the accepted masters.

Minor technical reconstruction or cleanup is acceptable only when it is
visually indistinguishable and improves fidelity. Creative
reinterpretation or redesign is not the objective.

### Locked Package

The accepted packaged set is:

`USPS-Label-228-Logo-Asset-Set.zip`

SHA-256:

`3b87c23f6ad55ac6e933f9137a6852b30a6b0ab8b6c1d81a738eaf92981a4fde`

Treat this hash as identifying the currently locked logo-asset package.
Any future change to an included logo asset or preview sheet should
produce a new package revision and a new SHA-256 rather than silently
replacing this baseline.

## Continuation Point

No additional feature work is currently required. Production Rev. 17 is
locked as the accepted Word-template baseline for now.

If work resumes, begin from the locked canonical artifacts above,
including the accepted USPS logo asset set, rather than from earlier
experimental revisions. Preserve the accepted Word behavior and the
exact **66:85** reference-image geometry unless a new physical
calibration or explicitly approved design change provides a reason to
revise them.

## Collection v1.0.1 Tagging Integration

The finalized repository tagging model distinguishes collection and
component milestones:

-   Collection tags use `vX.Y.Z`.
-   USPS Label 228 component milestones use namespaced tags such as
    `usps-label-228/v1.0.0`.
-   GitHub Releases remain collection-level only.
-   USPS Label 228 remains component v1.0.0; no Label 228 Office, image,
    or logo artifact changed as part of collection v1.0.1.
-   The initial `usps-label-228/v1.0.0` component tag is intended to
    point to the collection v1.0.1 publication commit.
