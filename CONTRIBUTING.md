# Contributing to Tavall Java Utils

This repository is an aggregate view and integration checkout, not an implementation origin.

## Source Authority and Development Workflow

1. **Policy Authority**
   - Organization-wide policy is governed by [TavallStudios/tavall-docs](https://github.com/TavallStudios/tavall-docs).

2. **Implementation Belongs in Standalone Repositories**
   - Implementation changes belong in the owning canonical utility repository, currently TavallStudios/tavall-custom-enum-java.
   - Do not implement library source changes directly inside this aggregate or copy utility source and commits into it.
   - Do not use this repository as the branch, PR, issue, release, or publication authority for an individual utility.

3. **Update Aggregate Pointers Explicitly**
   - Advance each submodule pointer to the exact commit on its owning repository's canonical main branch.
   - Submit the pointer change through this repository's pull request workflow and preserve the exact owning source SHA.
   - This repository has no scheduled or manual GitHub Actions synchronization job. Do not add one or push an automated pointer update directly to main.
   - TavallStudios/tavall-java-tools consumes this aggregate as a nested submodule.

4. **Validate the Aggregate**
   - Parse the source-owned .tavallci/ci.yaml definition and verify that each gitlink matches the owning repository's current canonical main SHA.
   - The aggregate has no root build or implementation checks. Run code checks in the owning utility repository when its source changes.
   - Do not create GitHub Actions workflows for this validation path; use repository-local checks and available Tavall Bot checks.
