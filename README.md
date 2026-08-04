# scoop-ironflow

[![Latest version](https://img.shields.io/github/v/release/sahina/ironflow-desktop-releases?label=ironflow-desktop&color=blue)](https://github.com/sahina/ironflow-desktop-releases/releases/latest)

Scoop bucket for **Ironflow Desktop** — the desktop app for [Ironflow](https://ironflow.run).
One app; this bucket carries nothing else.

Windows users install via [Scoop](https://scoop.sh) instead of the direct `setup.exe`. Scoop strips
Windows' **Mark-of-the-Web**, so the SmartScreen "unknown publisher" wall never fires — even though
the build is currently unsigned.

> **Windows is an experimental platform.** Builds ship on every release and auto-update, but they are
> not regularly tested — Ironflow is built by one developer working on macOS. If you hit a problem, or
> want to help look after the Windows build,
> [open an issue](https://github.com/sahina/ironflow-desktop-releases/issues).

## Install

```powershell
scoop bucket add ironflow https://github.com/sahina/scoop-ironflow
scoop install ironflow/ironflow-desktop
```

## Upgrade

```powershell
scoop update ironflow-desktop
```

Scoop is the update channel on Windows — the app's in-app auto-updater serves macOS and Linux only.

## Uninstall

```powershell
scoop uninstall ironflow-desktop
scoop bucket rm ironflow          # optional
```

## Releases

This bucket has **no GitHub Releases of its own** — that's normal. The actual builds (`.zip`, `.dmg`,
`.exe`, `.AppImage`) are published to
**[sahina/ironflow-desktop-releases](https://github.com/sahina/ironflow-desktop-releases/releases)**.

The badge above tracks the latest version *there*. An
[excavator](https://github.com/ScoopInstaller/GithubActions) workflow bumps this bucket's manifest
within 30 minutes of a release.

## What's here

| Path                              | Purpose                                                         |
| --------------------------------- | --------------------------------------------------------------- |
| `bucket/ironflow-desktop.json`    | The Scoop manifest — points at the `.zip` in the releases repo. |
| `.github/workflows/excavator.yml` | Cron that auto-bumps the manifest when a new release ships.     |

## License

The manifest and workflow in this repository are MIT-licensed. **Ironflow Desktop itself is not** —
it ships under the Functional Source License v1.1 with an Apache-2.0 future grant. See
[LICENSE](https://github.com/sahina/ironflow-releases/blob/main/LICENSE) and
<https://docs.ironflow.run/explanation/licensing/>.
