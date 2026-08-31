# Git and GitHub Workflow Guide

## Principles

-   Verify before changing.
-   Stop on errors.
-   Keep `main` synchronized with `origin/main`.
-   Preserve historical tags/releases.
-   Use annotated collection tags in `vX.Y.Z` form.
-   Use annotated component milestone tags in `<component>/vX.Y.Z` form.
-   Keep root/component VERSION and changelog state synchronized with
    their respective scopes.
-   Preserve published release states as immutable; later commits on
    `main` are normal future development and do not alter prior tags or
    releases.

## Normal update workflow

``` powershell
git status
git fetch --all --tags --prune
git status
git diff --check
```

Review changes before staging:

``` powershell
git diff
git diff --stat
```

Stage deliberately and verify:

``` powershell
git add <paths>
git diff --cached --check
git diff --cached
git status
```

Commit and push:

``` powershell
git commit -m "<message>"
if ($LASTEXITCODE -ne 0) { throw "git commit failed" }

git push origin main
if ($LASTEXITCODE -ne 0) { throw "git push failed" }

git status
```

For releases, follow `docs/release-process.md`. GitHub Releases are
collection-level only; component tags do not receive separate GitHub
Releases.
