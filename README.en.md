# VoiceHotkey Releases

[![Platform](https://img.shields.io/badge/platform-macOS%2014%2B-lightgrey.svg)](https://voicehotkey.pages.dev/)
[![Version](https://img.shields.io/badge/version-0.9.4-green.svg)](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest)
[![Download](https://img.shields.io/badge/download-Releases-blue.svg)](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest)
[![Docs](https://img.shields.io/badge/docs-handbook-informational.svg)](https://voicehotkey.pages.dev/docs/en/)

**Language:** [简体中文](README.md) · [繁體中文](README.zh-Hant.md) · English · [日本語](README.ja.md) · [한국어](README.ko.md) · [Deutsch](README.de.md) · [Español](README.es.md)

> **Current public release: 0.9.4**
> For **Apple Silicon (arm64) Macs running macOS 14 or later**. No Intel installer is currently available. [Download the latest release](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest).
> This installer is **not notarized or signed with Apple Developer ID**. macOS may block its first launch. The 0.9.3 installer has been withdrawn; use the latest release.

Official **download / installer** repository for [VoiceHotkey](https://voicehotkey.pages.dev/).

> **Installers are published only via [GitHub Releases](https://github.com/yeahhe365/VoiceHotkey-releases/releases).**
> This repo does **not** commit `.dmg` / `.app` binaries into git history.

## About the product

macOS **voice typing**: hold or tap a hotkey, speak, and insert the recognized text at the caret. Supports on-device models, cloud recognition, voice commands, translation and polishing, file transcription, and local history.

- **Product site:** [voicehotkey.pages.dev](https://voicehotkey.pages.dev/)
- **User handbook:** [voicehotkey.pages.dev/docs](https://voicehotkey.pages.dev/docs/en/)
- **Key Features:**
  - **Multi-Engine ASR**: Apple system speech, on-device offline models (Qwen3-ASR, SenseVoice, Whisper CoreML/ANE accelerated, OpenMOSS 0.9B, FireRed, Fun-ASR, Parakeet), Doubao ASR 2.0, Alibaba Bailian, Xiaomi MiMo, Azure, cloud Whisper, Groq, ElevenLabs Scribe, Soniox, NVIDIA NIM, Gemini, and more.
  - **Text Processing**: Learned frequent phrases can skip LLM requests, word replacements support regex and contextual variants, and optional LLM polishing and native Apple translation are available (macOS 26+ for Apple translation; system language assets may be required).
  - **Voice Commands & Control**: Local command dictionary and intent LLMs for shortcut injection, text expansion, Shortcuts.app actions, and controlled system operations (no arbitrary shell execution).
  - **File Transcription & Export**: Trial / Pro can transcribe audio/video files and export `.srt`, `.vtt`, `.ass`, or `.lrc` subtitles, or `.txt` text.
  - **Privacy Settings**: API keys stay in macOS Keychain. Local Only Mode restricts public-network ASR / LLM endpoints and pauses updates; license requests and manual model downloads can still use the network. [Data flows](https://voicehotkey.pages.dev/docs/en/privacy/local-only/).
- **UI languages** (same as the app): 简体中文, 繁體中文, English, 日本語, 한국어, Deutsch, Español

## Download & Acquisition

| | |
|--|--|
| **Latest release** | [Releases · Latest](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest) |
| **All versions** | [Releases](https://github.com/yeahhe365/VoiceHotkey-releases/releases) |
| **Product site** | [voicehotkey.pages.dev](https://voicehotkey.pages.dev/) |
| **User handbook** | [Docs](https://voicehotkey.pages.dev/docs/en/) |
| **Support** | [Contact](https://voicehotkey.pages.dev/docs/en/support/contact/) |

### Recommended install

1. Confirm that your Mac uses Apple Silicon and runs macOS 14 or later, then open [the latest Release](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest).
2. Download `VoiceHotkey-0.9.4.dmg`; Source code archives are not installers.
3. Drag **VoiceHotkey.app** into **Applications** (`/Applications` or `~/Applications`), then launch from that fixed installed path.
4. If macOS blocks opening, verify the official source and follow [Apple’s guidance](https://support.apple.com/en-us/102445). If it reports a damaged file, check the checksum and download again; contact support if the issue persists.
5. In onboarding, grant **Accessibility**, **Microphone**, and **Speech Recognition** for the default Apple engine.
6. Click the onboarding practice field, use the default voice typing hotkey **Ctrl + Option + Space**, say a sentence, and confirm that the text appears.

Optional: verify the published SHA-256 in the release notes before installing. Full steps: [Install guide](https://voicehotkey.pages.dev/docs/en/getting-started/install/).

**First use:** Apple Speech is the default and needs no API key. Its new engine on macOS 26+ may need system language assets; regular legacy Apple Speech on older systems may use Apple services. Independent on-device models require installation. Cloud recognition and LLM features need the selected provider’s credentials where required; that provider bills API usage.

**Trial & licensing:** First launch starts a 14-day Pro trial without a payment card; Free remains available after it ends. First Pro activation and key changes require an online check. A successful check permits up to 30 days of offline use, with up to 3 Macs per personal license. [License details](https://voicehotkey.pages.dev/docs/en/support/license/).

See the handbook: [Updates](https://voicehotkey.pages.dev/docs/en/advanced/updates/).

## License & terms

VoiceHotkey is proprietary commercial software; application source code is not published in this repository. Installing a binary does not grant rights beyond the product license / terms.
See [LICENSE](LICENSE) · [NOTICE](NOTICE.md), plus [Plans & Commercial](https://voicehotkey.pages.dev/docs/en/getting-started/plans/) and [Privacy Policy](https://voicehotkey.pages.dev/docs/en/privacy/policy/).

## Support

- Bugs & usage questions → [Contact](https://voicehotkey.pages.dev/docs/en/support/contact/)
- Broken download links / missing assets → [Discussions](https://github.com/yeahhe365/VoiceHotkey-releases/discussions)
- This repo is for **distribution only**; please use handbook contact channels for product feature requests
