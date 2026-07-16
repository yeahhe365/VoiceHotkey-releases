# VoiceHotkey Releases

[![Platform](https://img.shields.io/badge/platform-macOS%2014%2B-lightgrey.svg)](https://voicehotkey.pages.dev/)
[![Download](https://img.shields.io/badge/download-Releases-blue.svg)](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest)
[![Docs](https://img.shields.io/badge/docs-handbook-informational.svg)](https://voicehotkey.pages.dev/docs/en/)

**Language:** [简体中文](README.md) · [繁體中文](README.zh-Hant.md) · English · [日本語](README.ja.md) · [한국어](README.ko.md) · [Deutsch](README.de.md) · [Español](README.es.md)

Official **download / installer** repository for [VoiceHotkey](https://voicehotkey.pages.dev/).

> **Installers are published only via [GitHub Releases](https://github.com/yeahhe365/VoiceHotkey-releases/releases).**  
> This repo does **not** commit `.dmg` / `.app` binaries into git history.

## About the product

macOS **voice typing**: hold (or tap) a hotkey, speak, and text is inserted at the caret. Optional voice commands, text post-process, file transcription, and on-device history.

- **Product site:** [voicehotkey.pages.dev](https://voicehotkey.pages.dev/)
- **User handbook:** [voicehotkey.pages.dev/docs](https://voicehotkey.pages.dev/docs/en/)
- **UI languages** (same as the app): 简体中文, 繁體中文, English, 日本語, 한국어, Deutsch, Español

## Download

| | |
|--|--|
| **Latest release** | [Releases · Latest](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest) |
| **All versions** | [Releases](https://github.com/yeahhe365/VoiceHotkey-releases/releases) |
| **Product site** | [voicehotkey.pages.dev](https://voicehotkey.pages.dev/) |
| **User handbook** | [Docs](https://voicehotkey.pages.dev/docs/en/) |
| **Support** | [Contact](https://voicehotkey.pages.dev/docs/en/support/contact/) |

### Recommended install

1. Open [the latest Release](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest).
2. Download `VoiceHotkey-X.Y.Z.dmg` (notarized Developer ID build when available).
3. Open the DMG, drag **VoiceHotkey** into **Applications**.
4. Launch from `/Applications` (or `~/Applications`) and grant **Accessibility** + **Microphone** when prompted.

Optional: verify the published SHA-256 in the release notes before installing. Full steps: [Install guide](https://voicehotkey.pages.dev/docs/en/getting-started/install/).

## What belongs here

| Asset | Purpose |
|-------|---------|
| `VoiceHotkey-X.Y.Z.dmg` | Notarized macOS installer (Release assets only) |
| Checksums in release notes | Integrity check for downloads |
| (optional) Sparkle-related public files | If not hosted solely via GitHub Pages |

## What does **not** belong here

- Application **source code** (not maintained in this repo)
- Signing secrets, notary credentials, Sparkle **private** EdDSA key
- Git commits that add large `.dmg` / `.app` blobs (use **Release assets** only)

## Versioning

- Tag format: `vX.Y.Z` (e.g. `v0.9.0`)
- Asset name: `VoiceHotkey-X.Y.Z.dmg`
- Aligns with the product `CFBundleShortVersionString`

Direct asset URL pattern:

```text
https://github.com/yeahhe365/VoiceHotkey-releases/releases/download/vX.Y.Z/VoiceHotkey-X.Y.Z.dmg
```

## Publisher workflow (maintainers)

Build and notarize in the source tree, then publish here:

```bash
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

See the handbook: [Updates](https://voicehotkey.pages.dev/docs/en/advanced/updates/).

## License & terms

VoiceHotkey is proprietary commercial software. Installing a binary does not grant rights beyond the product license / terms.  
See [LICENSE](LICENSE) · [NOTICE](NOTICE.md), plus [Plans](https://voicehotkey.pages.dev/docs/en/getting-started/plans/) and [Privacy](https://voicehotkey.pages.dev/docs/en/privacy/policy/).

## Support

- Bugs & usage questions → [Contact](https://voicehotkey.pages.dev/docs/en/support/contact/)
- Broken download links / missing assets → [Discussions](https://github.com/yeahhe365/VoiceHotkey-releases/discussions)
- This repo is for **distribution only**; please use handbook contact channels for product feature requests
