<p align="center">
  <img src="assets/app-icon.png" alt="VoiceHotkey-Appsymbol" width="88" />
</p>

<h1 align="center">VoiceHotkey</h1>

<p align="center"><strong>Mit einem Tastenkürzel sprechen und auf macOS tippen</strong></p>

<p align="center">
  <a href="https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest"><strong>Neueste Version herunterladen</strong></a> ·
  <a href="https://voicehotkey.pages.dev/docs/de/getting-started/install/">Installationsanleitung</a>
</p>

[![Platform](https://img.shields.io/badge/platform-macOS%2014%2B-lightgrey.svg)](https://voicehotkey.pages.dev/)
[![Version](https://img.shields.io/badge/version-0.9.4-green.svg)](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest)
[![Download](https://img.shields.io/badge/download-Releases-blue.svg)](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest)
[![Docs](https://img.shields.io/badge/docs-handbook-informational.svg)](https://voicehotkey.pages.dev/docs/de/)

**Sprache:** [简体中文](README.md) · [繁體中文](README.zh-Hant.md) · [English](README.en.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · Deutsch · [Español](README.es.md)

> **Aktuelle öffentliche Version: 0.9.4**
> Für **Apple-Silicon-Macs (arm64) mit macOS 14 oder neuer**. Derzeit gibt es keinen Intel-Installer. [Neueste Version herunterladen](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest).
> Dieser Installer ist **nicht von Apple notarisiert und nicht mit Apple Developer ID signiert**. macOS kann den ersten Start blockieren. Der Installer für 0.9.3 wurde zurückgezogen; bitte die neueste Version verwenden.

Offizielles **Download-/Installer-Repository** für [VoiceHotkey](https://voicehotkey.pages.dev/).

> **Installer werden nur über [GitHub Releases](https://github.com/yeahhe365/VoiceHotkey-releases/releases) veröffentlicht.**
> `.dmg` / `.app` werden **nicht** in die Git-Historie committed.

## Über das Produkt

macOS-**Spracheingabe**: Hotkey halten oder antippen, sprechen und den erkannten Text an der Cursorposition einfügen. Unterstützt lokale Modelle, Cloud-Erkennung, Sprachbefehle, Übersetzung und Textoptimierung, Dateitranskription und lokale Historie.

<p align="center">
  <img src="assets/preview-en.png" alt="Die erkannte Spracheingabe wurde eingefügt" width="840" />
</p>

- **Produktseite:** [voicehotkey.pages.dev](https://voicehotkey.pages.dev/)
- **Handbuch:** [voicehotkey.pages.dev/docs](https://voicehotkey.pages.dev/docs/de/)
- **Hauptmerkmale:**
  - **Multi-Engine ASR**: Apple System-Spracherkennung, lokale On-Device-Modelle (Qwen3-ASR, SenseVoice, Whisper CoreML/ANE beschleunigt, OpenMOSS 0.9B, FireRed, Fun-ASR, Parakeet), Doubao ASR 2.0, Bailian, Xiaomi MiMo, Azure, Cloud-Whisper, Groq, ElevenLabs Scribe, Soniox, NVIDIA NIM, Gemini u. v. m.
  - **Textverarbeitung**: Gelernte häufige Phrasen können LLM-Anfragen überspringen. Wortersetzungen unterstützen Regex und Kontextvarianten; optionale LLM-Textoptimierung und native Apple-Übersetzung sind verfügbar (Apple-Übersetzung ab macOS 26; Sprachressourcen können erforderlich sein).
  - **Sprachbefehle & Steuerung**: Lokales Befehlswörterbuch und Intent-LLMs für Tastenkombinationen, Texterweiterungen, Kurzbefehle (Shortcuts.app) und sichere Systemsteuerung (keine Ausführung beliebiger Shell-Befehle).
  - **Dateitranskription & Export**: Testversion / Pro transkribiert Audio-/Videodateien und exportiert `.srt`, `.vtt`, `.ass` oder `.lrc` als Untertitel oder `.txt` als Text.
  - **Datenschutzeinstellungen**: API-Schlüssel bleiben im macOS-Schlüsselbund. Der Nur-Lokal-Modus beschränkt öffentliche ASR-/LLM-Endpunkte und pausiert Updates; Lizenzanfragen und manuelle Modelldownloads können weiterhin das Netzwerk nutzen. [Datenflüsse](https://voicehotkey.pages.dev/docs/de/privacy/local-only/).
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

1. Apple Silicon und macOS 14 oder neuer prüfen, dann die [neueste Release](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest) öffnen.
2. `VoiceHotkey-0.9.4.dmg` herunterladen. Source-code-Archive sind keine Installer.
3. **VoiceHotkey.app** in **Programme** (`/Applications` oder `~/Applications`) ziehen und von diesem festen Installationspfad starten.
4. Bei einer macOS-Sperre die offizielle Quelle prüfen und [Apples Anleitung](https://support.apple.com/de-de/102445) folgen. Bei einer Beschädigungsmeldung Prüfsumme prüfen und erneut herunterladen; bei anhaltenden Problemen den Support kontaktieren.
5. Im Einrichtungsassistenten **Bedienungshilfen**, **Mikrofon** und **Spracherkennung** für die voreingestellte Apple-Engine erlauben.
6. Das Übungsfeld anklicken, mit dem Standard-Hotkey **Ctrl + Option + Space** einen Satz sprechen und prüfen, ob der Text eingefügt wird.

Optional: SHA-256 in den Release-Notes prüfen. Ausführlich: [Installationsanleitung](https://voicehotkey.pages.dev/docs/de/getting-started/install/).

**Erste Nutzung:** Apple-Spracherkennung ist voreingestellt und benötigt keinen API-Schlüssel. Die neue Engine ab macOS 26 kann Sprachressourcen herunterladen müssen; der reguläre ältere Apple-Speech-Modus kann Apple-Dienste verwenden. Eigenständige lokale Modelle müssen zuerst installiert werden. Für Cloud-Erkennung und LLM-Funktionen gelten die Zugangsdaten und API-Gebühren des gewählten Anbieters.

**Testversion & Lizenz:** Beim ersten Start beginnt eine 14-tägige Pro-Testversion ohne Zahlungskarte; danach bleibt Free verfügbar. Erste Pro-Aktivierung und Schlüsselwechsel benötigen eine Online-Prüfung. Danach ist die Offline-Nutzung bis zu 30 Tage möglich; eine persönliche Lizenz unterstützt bis zu 3 Macs. [Lizenzdetails](https://voicehotkey.pages.dev/docs/de/support/license/).

Details im Handbuch: [Aktualisierungen](https://voicehotkey.pages.dev/docs/de/advanced/updates/).

## Lizenz und Bedingungen

VoiceHotkey ist proprietäre kommerzielle Software; der Anwendungsquellcode wird in diesem Repository nicht veröffentlicht. Das Herunterladen eines Installers gewährt keine Rechte über die Lizenz- und Nutzungsbedingungen hinaus.
Siehe [LICENSE](LICENSE) · [NOTICE](NOTICE.md) sowie [Pläne](https://voicehotkey.pages.dev/docs/de/getting-started/plans/) und [Datenschutzrichtlinie](https://voicehotkey.pages.dev/docs/de/privacy/policy/).

## Support

- Fragen & Fehlerberichte → [Kontakt](https://voicehotkey.pages.dev/docs/de/support/contact/)
- Defekte Download-Links / fehlende Assets → [Discussions](https://github.com/yeahhe365/VoiceHotkey-releases/discussions)
- Dieses Repo dient **ausschließlich der Distribution**; Funktionswünsche bitte über die Support-Kanäle im Handbuch einreichen
