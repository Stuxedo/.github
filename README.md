<p align="center">
  <picture><source media="(prefers-color-scheme: dark)" srcset="https://global.media.stuxedo.com/logo-light.png"><source media="(prefers-color-scheme: light)" srcset="https://global.media.stuxedo.com/logo-dark.png"><img src="https://global.media.stuxedo.com/logo-dark.png" height="100" alt="Stuxedo Logo"></picture>
</p>

# Stuxedo GitHub Configuration

The organisation repository for [Stuxedo](https://github.com/Stuxedo) on GitHub: it holds the organisation's public profile.

## What's here

| Path | What it does |
| --- | --- |
| [`profile/README.md`](profile/README.md) | The profile shown on [github.com/Stuxedo](https://github.com/Stuxedo): who Stuxedo is, its projects and sites, and how to get in touch. |
| [`.github/workflows/generateMetrics.yml`](.github/workflows/generateMetrics.yml) | Rebuilds the profile's activity card (`stats.svg` on the `metrics` branch) daily and on every push to `main`. |
| [`CONTRIBUTING.md`](CONTRIBUTING.md) | How to contribute to Stuxedo's projects. |
| `commit.sh` / `commit.bat`, [`tests/version.sh`](tests/version.sh) | The release scripts and the version check (see Versioning). |

## Updating the profile

Edit `profile/README.md`. When a Stuxedo repository or site is added, renamed or retired, update the project table there too, so the profile lists what Stuxedo runs today. Stuxedo's status is linked as [status.stuxedo.com](https://status.stuxedo.com), the landing page for Stuxedo Web Status and Stuxedo Server Status.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).

## Versioning

This project uses [Date Versioning](https://datevers.ing): each release is numbered by its UTC release date as `YY.MM.DD` (for example `26.10.23`), with `-1`, `-2`… for later releases the same day. See [CHANGELOG.md](CHANGELOG.md) for what changed in each release.

## License

Copyright (c) 2026 Stux.Group. All rights reserved.

---

*Built & Maintained by <picture><source media="(prefers-color-scheme: dark)" srcset="https://global.media.stuxedo.com/icon-light.png"><source media="(prefers-color-scheme: light)" srcset="https://global.media.stuxedo.com/icon-dark.png"><img src="https://global.media.stuxedo.com/icon-dark.png" height="14" alt="Stuxedo" valign="middle"></picture> [Stuxedo](https://github.com/Stuxedo).  
Stuxedo is a part of the <picture><source media="(prefers-color-scheme: dark)" srcset="https://global.media.stux.group/icon-light.png"><source media="(prefers-color-scheme: light)" srcset="https://global.media.stux.group/icon-dark.png"><img src="https://global.media.stux.group/icon-dark.png" height="14" alt="Stux.Group" valign="middle"></picture> Stux.Group brand of businesses.*
