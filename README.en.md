# VoiceHotkey Releases

[![Platform](https://img.shields.io/badge/platform-macOS%2014%2B-lightgrey.svg)](https://github.com/yeahhe365/VoiceHotkey-releases)
[![Docs](https://img.shields.io/badge/docs-voicehotkey.pages.dev-blue.svg)](https://voicehotkey.pages.dev/docs/)

**Language:** [中文](README.md) | English

Official **download / installer** repository for VoiceHotkey.

> **Installers are published only via [GitHub Releases](https://github.com/yeahhe365/VoiceHotkey-releases/releases).**  
> This repo does **not** commit `.dmg` / `.app` binaries into git history.

## Download

| | |
|--|--|
| **Latest release** | [Releases · Latest](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest) |
| **All versions** | [Releases](https://github.com/yeahhe365/VoiceHotkey-releases/releases) |
| **User manual** | [voicehotkey.pages.dev/docs](https://voicehotkey.pages.dev/docs/) |
| **Support** | [Contact](https://voicehotkey.pages.dev/docs/en/support/contact/) |

### Recommended install

1. Open [the latest Release](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest).
2. Download `VoiceHotkey-X.Y.Z.dmg` (notarized Developer ID build when available).
3. Open the DMG, drag **VoiceHotkey** into **Applications**.
4. Launch from `/Applications` (or `~/Applications`) and grant **Accessibility** + **Microphone** when prompted.

Optional: verify the published SHA-256 in the release notes before installing. See also [Install & permissions](https://voicehotkey.pages.dev/docs/en/getting-started/install/).

## What belongs here

| Asset | Purpose |
|-------|---------|
| `VoiceHotkey-X.Y.Z.dmg` | Notarized macOS installer disk image |
| Checksums in release notes | Integrity check for downloads |
| (optional) Sparkle-related public files | If not hosted solely via GitHub Pages |

## What does **not** belong here

- Application source code (this repo is distribution only)
- Signing secrets, notary credentials, Sparkle **private** EdDSA key
- Git commits that add large `.dmg` / `.app` blobs (use **Release assets** only)

## Versioning

- Tag format: `vX.Y.Z` (e.g. `v0.9.0`)
- Asset name: `VoiceHotkey-X.Y.Z.dmg`
- Aligns with `CFBundleShortVersionString` in the app’s `Info.plist`

Direct asset URL pattern:

```text
https://github.com/yeahhe365/VoiceHotkey-releases/releases/download/vX.Y.Z/VoiceHotkey-X.Y.Z.dmg
```

## Publisher workflow (maintainers)

Build and notarize in the **product source tree**, then publish here (e.g. via that tree’s `scripts/publish-release.sh`).

Sparkle appcast base URL should point at this repo:

```bash
VH_UPDATE_BASE_URL=https://github.com/yeahhe365/VoiceHotkey-releases/releases/download/v0.9.0 \
  make appcast
```

User-facing update notes: [Updates](https://voicehotkey.pages.dev/docs/en/advanced/updates/).

## License & terms

VoiceHotkey is proprietary commercial software. Installing a binary does not grant rights beyond the product license and the privacy/terms summaries in the user manual.  
See [Privacy policy](https://voicehotkey.pages.dev/docs/en/privacy/policy/).

## Support

- Bugs, features, and product questions → [Contact](https://voicehotkey.pages.dev/docs/en/support/contact/)
- This repo is for **distribution only**; please do not file product issues here unless they are about broken download links or missing assets.
