# Backlog

Future work for the Microsoft Office Resources collection is tracked
here.

## Repository Governance

  --------------------------------------------------------------------------
  ID           Status       Target       Work Item       Rationale / Notes
  ------------ ------------ ------------ --------------- -------------------
  `MOR-001`    Deferred     Repository   Revisit         Keep the repository
                                         licensing scope license and
                                         as new          exclusions accurate
                                         third-party     as the collection
                                         material is     grows.
                                         added

  `MOR-002`    Deferred     Repository   Revisit Git LFS Avoid Git LFS
                                         if repository   complexity unless
                                         size becomes    binary growth
                                         materially      justifies it.
                                         large

  `MOR-003`    Deferred     Repository   Evaluate        Add
                                         contribution    `CONTRIBUTING.md`
                                         policy if       only when there is
                                         outside         a concrete need.
                                         contributions
                                         become relevant

  `MOR-004`    Deferred     Repository   Standardize     Reconcile
                                         `VERSION`       `.gitattributes`
                                         line endings    with `.editorconfig`
                                                         and eliminate
                                                         ambiguous LF/CRLF
                                                         handling.

  `MOR-005`    Deferred     Repository   Establish       Use a
                                         repository      non-modifying
                                         cleanup         assessment first;
                                         procedure       review proposed
                                                         cleanup before
                                                         changing files and
                                                         verify repository
                                                         state afterward.

  `MOR-006`    Completed    Repository   Reconcile       Replace stale
                                         release         pre-publication
                                         documentation   wording, align
                                                         release-asset and
                                                         checksum guidance
                                                         with published
                                                         v1.0.1, and correct
                                                         USPS Label 228
                                                         Rev17/release
                                                         references. No
                                                         binary assets were
                                                         changed.
  --------------------------------------------------------------------------

### MOR-004 implementation notes

When MOR-004 is selected for implementation, prefer LF as the explicit
line ending for root and component `VERSION` files so the Git blob,
GitHub representation, Windows working tree, and generated repository
snapshots use the same bytes. The implementation should:

- set an explicit `.gitattributes` rule for `VERSION` files, such as
  `VERSION text eol=lf`, with an equivalent rule for component `VERSION`
  files as needed;
- reconcile `.editorconfig` so it expresses the same LF policy;
- normalize the tracked `VERSION` files once after the policy is set;
- verify that the raw working-tree hash and Git-normalized hash no longer
  diverge solely because of CRLF/LF conversion; and
- confirm that the version text itself is unchanged and that no unrelated
  files are modified.

This should be implemented deliberately as MOR-004 rather than as an
incidental side effect of another work item.

## Future Resources

Add Office application/category directories only when real content
exists; do not create speculative empty directories.
