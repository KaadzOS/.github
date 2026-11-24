# Contributing

KaadzOS is built and verified in GitHub Actions. Changes should keep the base image small and the release path reproducible.

## Before you open a pull request

- Keep the base image minimal. Optional software belongs in a pack under `packs/`.
- Verify new package names against Debian trixie before adding them.
- Keep the AMOLED palette as the single source of truth in `theme/palette`; generated files are not the source.
- Run the relevant checks under `ci/` for the area you changed, and say what you ran.
- Keep commits focused and descriptions factual.

Every push that touches build inputs runs the ISO matrix, including BIOS and UEFI boot tests. A change is not ready until the relevant job is green.

The main repository's [AGENTS.md](https://github.com/KaadzOS/KaadzOS/blob/main/AGENTS.md) records the build loop, constraints and current phase status in more detail.

Security reports do not belong in a pull request; use the [security policy](SECURITY.md).
