# VoiceHotkey Releases (Installer)

[![Platform](https://img.shields.io/badge/platform-macOS%2014%2B-lightgrey.svg)](https://voicehotkey.pages.dev/)
[![Download](https://img.shields.io/badge/download-Releases-blue.svg)](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest)
[![Docs](https://img.shields.io/badge/docs-handbook-informational.svg)](https://voicehotkey.pages.dev/docs/de/)

**Sprache:** [简体中文](README.md) · [繁體中文](README.zh-Hant.md) · [English](README.en.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · Deutsch · [Español](README.es.md)

Offizielles **Download-/Installer-Repository** für [VoiceHotkey](https://voicehotkey.pages.dev/).

> **Installer werden nur über [GitHub Releases](https://github.com/yeahhe365/VoiceHotkey-releases/releases) veröffentlicht.**  
> `.dmg` / `.app` werden **nicht** in die Git-Historie committed.

## Über das Produkt

macOS-**Spracheingabe**: Hotkey halten (oder tippen), sprechen — Text erscheint am Cursor. Optional: Sprachbefehle, Text-Nachbearbeitung, Dateitranskription und lokale Historie.

- **Produktseite:** [voicehotkey.pages.dev](https://voicehotkey.pages.dev/)
- **Handbuch:** [voicehotkey.pages.dev/docs](https://voicehotkey.pages.dev/docs/de/)
- **UI-Sprachen** (wie in der App): 简体中文, 繁體中文, English, 日本語, 한국어, Deutsch, Español

## Download

| | |
|--|--|
| **Neueste Version** | [Releases · Latest](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest) |
| **Alle Versionen** | [Releases](https://github.com/yeahhe365/VoiceHotkey-releases/releases) |
| **Produktseite** | [voicehotkey.pages.dev](https://voicehotkey.pages.dev/) |
| **Handbuch** | [Docs](https://voicehotkey.pages.dev/docs/de/) |
| **Support** | [Kontakt](https://voicehotkey.pages.dev/docs/de/support/contact/) |

### Empfohlene Installation

1. [Neueste Release](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest) öffnen.
2. `VoiceHotkey-X.Y.Z.dmg` herunterladen (ggf. notarisierte Developer-ID-Build).
3. DMG öffnen, **VoiceHotkey** in **Programme** ziehen.
4. Aus `/Applications` (oder `~/Applications`) starten und **Bedienungshilfen** + **Mikrofon** erlauben.

Optional: SHA-256 in den Release-Notes prüfen. Ausführlich: [Installationsanleitung](https://voicehotkey.pages.dev/docs/de/getting-started/install/).

## Was hier hingehört

| Asset | Zweck |
|-------|--------|
| `VoiceHotkey-X.Y.Z.dmg` | Notarisierter macOS-Installer (nur Release-Assets) |
| Prüfsummen in Release-Notes | Integritätsprüfung |
| (optional) öffentliche Sparkle-Dateien | Falls nicht nur über GitHub Pages |

## Was hier **nicht** hingehört

- Anwendungs-**Quellcode** (nicht in diesem Repo)
- Signaturgeheimnisse, Notary-Credentials, Sparkle-**Privat**schlüssel
- Git-Commits mit großen `.dmg` / `.app` (nur **Release-Assets**)

## Versionierung

- Tag: `vX.Y.Z` (z. B. `v0.9.0`)
- Dateiname: `VoiceHotkey-X.Y.Z.dmg`
- Entspricht `CFBundleShortVersionString` des Produkts

Direkte Download-URL:

```text
https://github.com/yeahhe365/VoiceHotkey-releases/releases/download/vX.Y.Z/VoiceHotkey-X.Y.Z.dmg
```

## Workflow für Maintainer

Im Quellbaum bauen und notarisieren, dann hier veröffentlichen:

```bash
export VH_SIGN_IDENTITY="Developer ID Application: …"
export VH_NOTARY_PROFILE=VH_NOTARY
make release-dmg

bash scripts/publish-release.sh
```

Sparkle-Appcast-Enclosure sollte auf dieses Repo zeigen:

```bash
VH_UPDATE_BASE_URL=https://github.com/yeahhe365/VoiceHotkey-releases/releases/download/v0.9.0 \
  make appcast
```

Siehe Handbuch: [Updates](https://voicehotkey.pages.dev/docs/de/advanced/updates/).

## Lizenz & Bedingungen

VoiceHotkey ist proprietäre kommerzielle Software. Der Download gewährt keine Rechte über die Produktlizenz / AGB hinaus.  
[Pläne](https://voicehotkey.pages.dev/docs/de/getting-started/plans/), [Datenschutz](https://voicehotkey.pages.dev/docs/de/privacy/policy/).

## Support

- Fehler & Nutzung → [Kontakt](https://voicehotkey.pages.dev/docs/de/support/contact/)
- Dieses Repo dient nur der **Verteilung**; bitte keine Produkt-Issues hier, außer bei defekten Download-Links oder fehlenden Assets
