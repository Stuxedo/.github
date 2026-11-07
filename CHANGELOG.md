# Changelog

All notable changes to Stuxedo's `.github` organization repository are documented here.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Date Versioning](https://datevers.ing) since v26.10.23 (`YY.MM.DD`, the UTC release date, with `-1`, `-2`… for later releases the same day); earlier releases used [Semantic Versioning](https://semver.org/).

## v26.11.07

### Changed

- **All rights reserved.** The License section now reads "Copyright (c) 2026 Stux.Group. All rights reserved. This repository is not licensed for reuse or redistribution", and a `LICENSE` file says the same.

## v26.11.06-2

### Changed

- **Work happens on `test`.** Changes reach `main` only through a pull request from `test`, and releases are made and tagged on `test`. CONTRIBUTING has a Branches section, and the README's Versioning section says so.

## v26.11.06-1

### Added

- The profile's project table links each project's live site and mentions the `-v1` design snapshots.

### Changed

- This repository's README describes what's actually in it (the profile, the metrics workflow, CONTRIBUTING and the release scripts) instead of issue templates, workflow templates and community files it never had.
- The logos in the profile and README switch between light and dark versions to match GitHub's theme.
- The README's licence line is now a Stux.Group copyright notice.

## v26.11.06

### Added

- The organisation profile lists **Stuxedo Status** (status.stuxedo.com, the landing page for Stuxedo Web Status and Stuxedo Server Status), **Stuxedo Server Status** (status.stuxedo.net) and the **Region Page**, and has a Service Status section linking status.stuxedo.com.

## v26.10.23

### Added

- `tests/version.sh`, which checks that `VERSION.md` is a valid Date Version, a real calendar date not in the future, and the same as the newest entry in this changelog

### Changed

- Switched from Semantic Versioning to [Date Versioning](https://datevers.ing): releases are numbered by their UTC release date as `YY.MM.DD`, with `-1`, `-2`… for later releases the same day. This release follows v1.0.7
- `commit.sh` and `commit.bat` refuse a `VERSION.md` that isn't a valid Date Version or is dated in the future (UTC), and warn when it's dated before today
- `README.md` and `CONTRIBUTING.md` describe Date Versioning and the release steps

## v1.0.7

### Changed

- README, organisation profile and CONTRIBUTING footers now match the other Stux.Group brands' `.github` repos: "Built & Maintained by Stuxedo" with the Stuxedo icon from `global.media.stuxedo.com`, "Stuxedo is a part of the Stux.Group brand of businesses", and "Stuxedo is part of the Stux.Group Brand of Companies" in CONTRIBUTING (they previously read "operated by Stux.Cloud, which is operated by Stux Group Ltd…")

## v1.0.6

### Added
- `profile/README.md` gained the "Our Projects" table (Instance Page, Maintenance Page, Soon Page) and a `legal@stuxedo.com` contact line, matching the fuller template already used by Stux.Group's own profile.

## v1.0.5

### Fixed
- `README.md`, `CONTRIBUTING.md`, and `profile/README.md` said Stuxedo is "a part of the Stux.Group brand" directly — the actual chain is Stuxedo → Stux.Cloud → Stux Group Ltd. Corrected all three to name Stux.Cloud as the direct operator, with Stux Group Ltd's full registration details.

## v1.0.4

### Fixed
- `README.md` and `profile/README.md`'s Stux.Group brand icon URL had a leftover duplicated `/global/` path segment (`global.media.stux.group/global/icon.png`) — corrected to `https://global.media.stux.group/icon.png`

## v1.0.3

### Changed
- `CONTRIBUTING.md` and `profile/README.md`'s general contact address changed from `contact@stuxedo.com` to `hello@stuxedo.com`, matching the convention used across other Stux.Group brand repos

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
