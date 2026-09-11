# 0merUfuk/rifja (Homebrew tap)

Dedicated Homebrew tap for [Rifja](https://github.com/0merUfuk/rifja) — offline,
evidence-aware continuity for local agent sessions and Git.

```sh
brew install 0merUfuk/rifja/rifja
rifja --version
```

Homebrew installs Python 3.14 and Git and owns the application's private
environment. Updates: `brew update && brew upgrade 0merUfuk/rifja/rifja`.
Removal: `brew uninstall --force 0merUfuk/rifja/rifja` (application state,
exports and backups are preserved). See the [product documentation](https://github.com/0merUfuk/rifja/blob/main/docs/usage.md).

## Migrating from the former shared tap

Rifja previously shipped from `0merUfuk/thematrix`. To move an existing
installation over:

```sh
brew uninstall --force 0merUfuk/thematrix/rifja
brew untap 0merUfuk/thematrix   # only if you do not use its other formulas
brew install 0merUfuk/rifja/rifja
```

Application state lives outside Homebrew and is untouched by any of these
steps.

## Verification

Every push runs the formula's install test on ubuntu-24.04, macos-15 and
macos-15-intel (`.github/workflows/rifja.yml`).
