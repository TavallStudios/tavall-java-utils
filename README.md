# Tavall Java Utils

`TavallStudios/tavall-java-utils` is the Tavall Studios aggregate view of standalone low-level Java utility repositories.

## Authority

The individual Tavall Studios utility repositories are the authoritative source trees. Currently tracked:

- `TavallStudios/tavall-custom-enum-java`

This repository is an automatically synchronized aggregate. Do not implement utility changes here first and do not copy source or commits into this repository. Make changes in the owning standalone repository; this aggregate advances its Git submodule pointer to the resulting canonical `main` revision.

## Synchronization

Each utility is tracked as a Git submodule pointing at its canonical Tavall Studios repository. `.github/workflows/sync-java-utils.yml` periodically advances configured utility pointers to their latest canonical `main` revisions and commits the aggregate pointer update when anything changed. The workflow may also be run manually.

This repository is itself consumed as a submodule by `TavallStudios/tavall-java-tools`, allowing the Java tools aggregate to include the utility aggregate without copying or taking ownership of its source.

## Module and runtime boundary

**Responsibility:** This repository owns the aggregate pointer and synchronization workflow for standalone low-level Java utilities.

**Does not own:** Utility source code, utility release policy, or runtime deployment.

- `tavall-java-utils/` — **← This Module**
  - `tavall-custom-enum-java/`

**Relationships:** [`tavall-custom-enum-java`](https://github.com/TavallStudios/tavall-custom-enum-java) owns the utility implementation and release. [`tavall-java-tools`](https://github.com/TavallStudios/tavall-java-tools) consumes this aggregate as a nested submodule.

**Governing documentation:** [Authority](#authority), [Synchronization](#synchronization), [CONTRIBUTING.md](CONTRIBUTING.md), [submodule declaration](.gitmodules), and [sync workflow](.github/workflows/sync-java-utils.yml).

**Runtime owner:** None. The aggregate is a recursive source checkout, not an executable.

## Development

| Field | Value |
| --- | --- |
| Module Type | Git-submodule aggregate |
| Runtime | None |
| Current PR Stack | No module-specific dependency order is recorded here. See the [open repository pull requests](https://github.com/TavallStudios/tavall-java-utils/pulls). |
| Development Guide | [CONTRIBUTING.md](CONTRIBUTING.md) and [Synchronization](#synchronization) |
| Check | Initialize the pinned submodule and use the owning utility repository's check task. |

---

Notion: NOT_APPLICABLE
Updated: 2026-09-27 02:32 PM PDT · PR: [#3](https://github.com/TavallStudios/tavall-java-utils/pull/3)
