# NOTICE

## What this repository is

**VoiceHotkey-releases** publishes **official macOS installers** (DMG) as
[GitHub Release assets](https://github.com/yeahhe365/VoiceHotkey-releases/releases).
It is a **distribution** repository, not an application source tree.

- Product site: https://voicehotkey.pages.dev/
- User handbook: https://voicehotkey.pages.dev/docs/
- Support: https://voicehotkey.pages.dev/docs/support/contact/

## License history

- **Current product** (VoiceHotkey 0.9+): Proprietary commercial software — see [LICENSE](LICENSE).
- **Historical snapshots** published under MIT remain available under MIT for those specific commits only. New contributions, official installers, and commercial builds are not MIT.

## License

VoiceHotkey is **proprietary commercial software**. See [LICENSE](LICENSE).

Downloading or installing a binary does **not** grant rights beyond the product
license, trial/Free/Pro entitlements, and the privacy / terms summaries in the
user handbook.

## Third-party components

VoiceHotkey embeds or dynamically links the following open-source components:

| Component | License | Source | Usage |
|-----------|---------|--------|-------|
| [Sparkle 2](https://github.com/sparkle-project/Sparkle) | MIT | Copyright (c) Sparkle Project contributors | In-app automatic updates (`Sparkle.framework` is embedded in the shipped `.app`) |
| [sherpa-onnx](https://github.com/k2-fsa/sherpa-onnx) | Apache-2.0 | Copyright (c) sherpa-onnx authors | On-device speech recognition, loaded at runtime via `dlopen`; the C API header is vendored at `Sources/SherpaBridge/c-api.h` |
| [whisper.cpp](https://github.com/ggerganov/whisper.cpp) / GGML | MIT | Copyright (c) Georgi Gerganov and contributors | On-device speech recognition engine compiled into the app; sources vendored at `Sources/WhisperBridge/` |
| [Silero VAD](https://github.com/snakers4/silero-vad) | MIT | Copyright (c) Silero Team | Voice activity detection ONNX model embedded at `Sources/VoiceHotkey/Resources/silero_vad.onnx` |
| [OpenMOSS](https://github.com/OpenMOSS) | Apache-2.0 | Copyright (c) OpenMOSS authors | On-device speech recognition C++ bridge vendored at `Sources/MossBridge/` |
| [llama.cpp / GGML](https://github.com/ggml-org/llama.cpp) | MIT | Copyright (c) 2023–2026 The ggml authors | Local LLM inference via the bundled `Contents/MacOS/llama-server`; license in `Contents/Resources/Licenses/llama.cpp-LICENSE.txt` |
| [transcribe.cpp](https://github.com/handy-computer/transcribe.cpp) | MIT | Copyright (c) 2026 The transcribe.cpp authors | MOSS runtime bundled as `Contents/Frameworks/libtranscribe.dylib`; license in `Contents/Resources/Licenses/transcribe.cpp-LICENSE.txt` |

Preserve the applicable third-party copyright and license notices when redistributing the app. See the upstream repositories for the full license texts.

## Third-party services (BYOK)

Users may configure their own API keys for speech recognition and optional LLM features. Cloud recognition sends audio to the selected recognition service. Enabled cloud polishing, translation, and intent features may send text and configured context to the selected LLM service:

| Category | Examples |
|----------|----------|
| Speech (ASR) | 豆包 / Volcengine, 小米 MiMo, 阿里云百炼, Gemini, OpenAI Speech, OpenAI-compatible endpoints, Groq, ElevenLabs Scribe, Soniox, NVIDIA Speech NIM, Azure AI Speech |
| Intent LLM | NVIDIA NIM, OpenAI, Anthropic, DeepSeek, Qwen, Kimi, GLM, MiniMax, Xiaomi MiMo, Grok, Gemini, Volcengine Ark (火山方舟), OpenRouter, custom OpenAI-compatible |

Keys stay in the macOS Keychain under the app’s bundle service identity. Those services have their own terms, API usage costs, and privacy policies.

Fresh installations use real recording; the current settings have no Demo switch. Legacy or test Demo configurations may skip microphone capture and ASR, but enabled cloud LLM features can still receive demo text and configured context. Demo is not a network privacy control.

Local Only Mode restricts public-network ASR / LLM endpoints and pauses automatic updates. It does not block license requests or manually initiated model downloads. Apple Speech behavior and resource downloads depend on the system, language, and engine; it must not be described as guaranteeing zero network access.

## License service

First Pro activation and key changes require an online check. Successful verification returns a server-signed, device-bound receipt allowing up to 30 days of offline Pro access. License requests send the license key, device identifier and, for activation, Mac name, platform, and app version to the VoiceHotkey license service. They do not send ASR / LLM keys, audio, or transcripts. See the [privacy policy](https://voicehotkey.pages.dev/docs/privacy/policy/) and [license guide](https://voicehotkey.pages.dev/docs/support/license/).

## Brand & trademarks

VoiceHotkey and related marks are used to identify the official product and
installers. Do not imply endorsement or “official” status when redistributing
without permission. Provider logos are used for identification in settings;
trademarks belong to their respective owners.

## macOS system permissions

The app may require:

- **Microphone** — capture speech for ASR
- **Accessibility** — global hotkeys and `CGEvent` shortcut injection
- **Speech Recognition** (optional) — when using macOS Apple system speech recognition
- **Automation / Apple Events** (optional) — limited control of other apps

See [Privacy Policy](https://voicehotkey.pages.dev/docs/privacy/policy/) and [Local-only Mode](https://voicehotkey.pages.dev/docs/privacy/local-only/).
