# VoiceHotkey Releases

[![Platform](https://img.shields.io/badge/platform-macOS%2014%2B-lightgrey.svg)](https://github.com/yeahhe365/VoiceHotkey)
[![Source](https://img.shields.io/badge/source-VoiceHotkey-blue.svg)](https://github.com/yeahhe365/VoiceHotkey)

**Language:** [中文](README.md) | English

Official **download / installer** repository for [VoiceHotkey](https://github.com/yeahhe365/VoiceHotkey).

> **Installers are published only via [GitHub Releases](https://github.com/yeahhe365/VoiceHotkey-releases/releases).**  
> This repo does **not** commit `.dmg` / `.app` binaries into git history.

## Download

| | |
|--|--|
| **Latest release** | [Releases · Latest](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest) |
| **All versions** | [Releases](https://github.com/yeahhe365/VoiceHotkey-releases/releases) |
| **Source code** | [yeahhe365/VoiceHotkey](https://github.com/yeahhe365/VoiceHotkey) |
| **Issues / feedback** | Please open issues on the [source repository](https://github.com/yeahhe365/VoiceHotkey/issues) |

### Recommended install

1. Open [the latest Release](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest).
2. Download `VoiceHotkey-X.Y.Z.dmg` (notarized Developer ID build when available).
3. Open the DMG, drag **VoiceHotkey** into **Applications**.
4. Launch from `/Applications` (or `~/Applications`) and grant **Accessibility** + **Microphone** when prompted.

Optional: verify the published SHA-256 in the release notes before installing.

## What belongs here

| Asset | Purpose |
|-------|---------|
| `VoiceHotkey-X.Y.Z.dmg` | Notarized macOS installer disk image |
| Checksums in release notes | Integrity check for downloads |
| (optional) Sparkle-related public files | If not hosted solely via GitHub Pages |

## What does **not** belong here

- Application **source code** → [VoiceHotkey](https://github.com/yeahhe365/VoiceHotkey)
- Signing secrets, notary credentials, Sparkle **private** EdDSA key
- Git commits that add large `.dmg` / `.app` blobs (use **Release assets** only)

## Versioning

- Tag format: `vX.Y.Z` (e.g. `v0.9.0`)
- Asset name: `VoiceHotkey-X.Y.Z.dmg`
- Aligns with `CFBundleShortVersionString` in the source repo’s `Info.plist`

Direct asset URL pattern:

```text
https://github.com/yeahhe365/VoiceHotkey-releases/releases/download/vX.Y.Z/VoiceHotkey-X.Y.Z.dmg
```

## Publisher workflow (maintainers)

Build and notarize in the **source** repository, then publish here:

```bash
# In yeahhe365/VoiceHotkey
export VH_SIGN_IDENTITY="Developer ID Application: …"
export VH_NOTARY_PROFILE=VH_NOTARY
make release-dmg

# Upload to this repo’s Releases
bash scripts/publish-release.sh
```

Sparkle appcast base URL should point at this repo:

```bash
VH_UPDATE_BASE_URL=https://github.com/yeahhe365/VoiceHotkey-releases/releases/download/v0.9.0 \
  make appcast
```

See [docs/UPDATES.md](https://github.com/yeahhe365/VoiceHotkey/blob/main/docs/UPDATES.md) in the source repo.

## License & terms

VoiceHotkey is proprietary commercial software. Installing a binary does not grant rights beyond those in the product license / [TERMS](https://github.com/yeahhe365/VoiceHotkey/blob/main/docs/TERMS.md).  
Source, license text, and commercial notes live in the [main repository](https://github.com/yeahhe365/VoiceHotkey).

## Support

- Bugs & features → [VoiceHotkey Issues](https://github.com/yeahhe365/VoiceHotkey/issues)
- This repo is for **distribution only**; please do not file product issues here unless they are about broken download links or missing assets.
