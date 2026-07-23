# scoop-ironflow

Scoop bucket for **Ironflow Desktop** — the GUI client for [Ironflow](https://ironflow.run).

[![Latest version](https://img.shields.io/github/v/release/sahina/ironflow-desktop-releases?label=ironflow-desktop&color=blue)](https://github.com/sahina/ironflow-desktop-releases/releases/latest)

Windows users install via [Scoop](https://scoop.sh) instead of the direct `setup.exe`. Scoop strips
Windows' **Mark-of-the-Web**, so the SmartScreen "unknown publisher" wall never fires — even though the
build is currently unsigned.

## Install

```powershell
scoop bucket add ironflow https://github.com/sahina/scoop-ironflow
scoop install ironflow/ironflow-desktop
scoop update  ironflow-desktop   # future upgrades
```

## What's here

| Path | Purpose |
|------|---------|
| `bucket/ironflow-desktop.json` | The Scoop manifest — points at the `.zip` in the releases repo below. |
| `.github/workflows/excavator.yml` | Cron that auto-bumps the manifest when a new release ships. |

## Releases

This bucket has **no GitHub Releases of its own** — that's normal. The actual builds (`.zip`, `.dmg`,
`.exe`, `.AppImage`) are published to **[sahina/ironflow-desktop-releases](https://github.com/sahina/ironflow-desktop-releases/releases)**.
The badge above tracks the latest version there.

## Auto-updates

An [excavator](https://github.com/ScoopInstaller/GithubActions) workflow polls the releases repo every
30 min, recomputes the hash, and commits the version bump here on its own — no manual step per release.
Keep this repo's default branch **unprotected** so it can push.
