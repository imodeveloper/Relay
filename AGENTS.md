# Agent Instructions

## Project Purpose
- Relay is a Swift package used as a fixture/support dependency for RSS-related tests and tooling in the workspace.
- Keep changes small and package-focused unless a consuming repo requires a coordinated release.

## Branching And Release Process
- Default working branch is `development`.
- `main` is release-only. Do not commit normal feature, fix, or exploratory work directly to `main`.
- Start new work by fetching and switching to `development`, then keep it current with `origin/development`.
- Release preparation means reviewing the full `development` diff against `main`, validating package tests and impacted consumers, then merging `development` into `main` only when ready.
- After the release merge, tag the release version on `main`, push `main`, `development`, and the tag.
- If Relay changes are part of a multi-repo release, coordinate the merge/tag version with the other affected workspace repos before shipping.

## Validation
- Run Swift package tests from the repo root when changing package code:
  - `swift test`
