# OPERATIONAL_STATE

project_id: squirtle-lab
project_name: Squirtle Lab
revision: 1
status: seeded

## Current baseline

- Repository: `westkitty/Squirtle_Lab`
- Branch: `main`
- Implementation state: not yet built; repository is seeded for reconstruction.
- Reconstruction contract: `docs/EEVEE_LAB_CHARACTER_RECONSTRUCTION_HANDOFF.md`
- Squirtle source archive: `assets/source/squirtle/Archive.zip`
- Canonical reference project: `westkitty/eevee_lab`

## Active invariants

- Build Squirtle Lab as a separate project; do not mutate `westkitty/eevee_lab`.
- Preserve the reconstruction contract's system-depth, room-count, lifecycle, accessibility, responsive, persistence, validation, and deployment requirements.
- Treat Squirtle as the STAR_CHARACTER.
- Inspect the source archive before choosing runtime model format or animation mappings.
- Do not invent animation semantics or model capabilities not supported by the supplied assets.
- Do not claim implementation, tests, visual QA, Pages deployment, or runtime behavior until actually verified.

## Verified

- The reconstruction contract is committed on `main`.
- The Squirtle source archive is committed on `main` as the original ZIP payload.

## Pending

- Inspect and normalize Squirtle model assets.
- Build the Squirtle-specific adaptation matrices.
- Reconstruct the full lab.
- Run contract, lifecycle, browser, viewport, and rendered visual validation.
- Configure and verify GitHub Pages when implementation is ready.
