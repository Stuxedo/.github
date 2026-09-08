# Changelog

All notable changes to Stuxedo's `.github` organization repository are documented here.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/) (MAJOR.MINOR.PATCH).

## v1.0.2

### Changed
- `README.md` and `profile/README.md`'s footer brand-attribution block updated to the new format (Built & Maintained by Stuxedo / Stuxedo is a part of the Stux.Group brand of businesses), replacing the older disclaimer. No "Hosted by" clause here since Stuxedo is the hosting brand itself; `README.md`'s redundant separate "Made by Stuxedo" line was also removed since the new footer already covers that

## v1.0.1

### Fixed
- `generateMetrics.yml`'s `setup` job created the `metrics` branch by branching off `main`'s current commit, so
  it wasn't actually an orphan branch — it carried the whole repo history and file tree instead of starting
  empty. Now creates a true root commit (via the git empty-tree hash, no parents) and points `metrics` at that,
  so the branch only ever holds what the `gh-metrics/metrics` action commits to it. No `metrics` branch had been
  created yet here, so this lands before the bug ever manifests

## v1.0.0

### Added
- `VERSION.md` and this `CHANGELOG.md`, versioning the repo for the first time
- `commit.sh` / `commit.bat` — commit + tag scripts that read the release version from `VERSION.md`
