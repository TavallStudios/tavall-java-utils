# Tavall Java Utils Aggregate Agent Guidance

This repository is an aggregate view, not an implementation origin.

## Source authority

Implementation changes belong in the owning canonical utility repository. Currently tracked:

- `TavallStudios/tavall-custom-enum-java`

Do not implement library source changes directly inside this aggregate. Do not copy utility source or commits into this repository. Do not use this repository as the branch, PR, issue, release, or publication authority for an individual utility.

## Aggregate synchronization

The aggregate tracks each direct canonical utility repository as a Git submodule. `.github/workflows/sync-java-utils.yml` advances direct pointers to canonical `main` revisions automatically.

Normal implementation flow is:

```text
owning TavallStudios utility repo
-> normal PR / review / main promotion
-> TavallStudios/tavall-java-utils pointer synchronization
-> TavallStudios/tavall-java-tools pointer synchronization
```

`tavall-java-utils` owns the pointers to utility repositories inside it. The outer `tavall-java-tools` aggregate must advance only the `tavall-java-utils` pointer and must not reach through this aggregate to commit nested utility pointer changes.

A utility implementation commit must not require a second copy of that implementation in either aggregate.
