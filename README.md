# Tavall Java Utils

`TavallStudios/tavall-java-utils` is the Tavall Studios aggregate view of standalone low-level Java utility repositories.

## Authority

The individual Tavall Studios utility repositories are the authoritative source trees. Currently tracked:

- `TavallStudios/tavall-custom-enum-java`

This repository is an automatically synchronized aggregate. Do not implement utility changes here first and do not copy source or commits into this repository. Make changes in the owning standalone repository; this aggregate advances its Git submodule pointer to the resulting canonical `main` revision.

## Synchronization

Each utility is tracked as a Git submodule pointing at its canonical Tavall Studios repository. `.github/workflows/sync-java-utils.yml` periodically advances configured utility pointers to their latest canonical `main` revisions and commits the aggregate pointer update when anything changed. The workflow may also be run manually.

This repository is itself consumed as a submodule by `TavallStudios/tavall-java-tools`, allowing the Java tools aggregate to include the utility aggregate without copying or taking ownership of its source.
