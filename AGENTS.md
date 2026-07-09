# renovate-config

Shared Renovate presets: `default.json` (all repos, extended as
`github>riffingonsoftware/renovate-config`) and `go.json` for Go repos.

## Git Workflow

- Work directly on `trunk`; commit and push in logical chunks.

## Rules

- Changes take effect in every consuming repo on Renovate's next run; treat
  automerge, release-age, and lock-file policy changes as production changes
  and ask before loosening them.
- Validate config changes with
  `npx --yes --package renovate -- renovate-config-validator <file>` before
  finishing.
- No dependencies, build, or tests exist; keep it that way unless asked.
