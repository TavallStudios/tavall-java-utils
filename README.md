# Tavall Java Utils

TavallStudios/tavall-java-utils records the canonical source revisions of standalone low-level Java utility repositories.

## Authority

The individual Tavall Studios utility repositories own their implementation. This aggregate records those sources as Git submodule pointers. Update a pointer to the exact canonical main revision through an explicit change to this repository. Do not implement utility changes here first or copy source commits into this aggregate.

## Source updates

Each utility is tracked as a Git submodule at its canonical Tavall Studios repository. Pointer updates are made explicitly through this repository's pull request workflow; there is no scheduled or manual GitHub Actions synchronization job. The source-owned .tavallci/ci.yaml declares this aggregate as a no-build source checkout. Local validation checks the CI definition and verifies each pointer against its canonical repository main. Implementation checks remain owned by the utility source repository.

This repository is consumed as a submodule by TavallStudios/tavall-java-tools. The aggregate does not copy or take ownership of utility source.

## Module and runtime boundary

**Responsibility:** This repository owns aggregate source pointers and its source-owned Tavall CI definition.

**Does not own:** Utility source code, utility release policy, or runtime deployment.

- tavall-java-utils/ — this module
  - tavall-custom-enum-java/

**Relationships:** tavall-custom-enum-java owns the utility implementation and release. tavall-java-tools consumes this aggregate as a nested submodule.

**Governing documentation:** CONTRIBUTING.md, .gitmodules, and .tavallci/ci.yaml.

**Runtime owner:** None. The aggregate is a recursive source checkout, not an executable.

## Development

| Field | Value |
| --- | --- |
| Module Type | Git-submodule aggregate |
| Runtime | None |
| Current PR Stack | See the [open repository pull requests](https://github.com/TavallStudios/tavall-java-utils/pulls). |
| Development Guide | CONTRIBUTING.md and Source updates above |
| Check | Parse the source-owned CI definition, compare each gitlink with its canonical repository main SHA, and use the owning utility repository's checks for source changes. There is no aggregate build. |

---

Notion: NOT_APPLICABLE
Updated: 2026-10-20 UTC · PR: [#2](https://github.com/TavallStudios/tavall-java-utils/pull/2)
