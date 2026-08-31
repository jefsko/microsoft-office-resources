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
  --------------------------------------------------------------------------

## Future Resources

Add Office application/category directories only when real content
exists; do not create speculative empty directories.
