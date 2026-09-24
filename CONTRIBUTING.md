# Contributing to Tavall Java Utils

This repository is an aggregate view and integration checkout, not an implementation origin.

## Source Authority & Development Workflow

1. **Policy Authority**:
   - Organization-wide policy is governed by [`TavallStudios/tavall-docs`](https://github.com/TavallStudios/tavall-docs).

2. **Implementation Belongs in Standalone Repositories**:
   - Implementation changes belong in the owning canonical utility repository (`TavallStudios/tavall-custom-enum-java`).
   - Do not implement library source changes directly inside this aggregate.
   - Do not copy utility source or commits into this repository.
   - Do not use this repository as the branch, PR, issue, release, or publication authority for an individual utility.

3. **Submodule Synchronization**:
   - Submodule pointers to canonical `main` revisions are advanced automatically via `.github/workflows/sync-java-utils.yml`.
   - This aggregate is tracked as a submodule by `TavallStudios/tavall-java-tools`.
