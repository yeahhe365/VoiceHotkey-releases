<p align="center">
  <img src="assets/app-icon.png" alt="VoiceHotkey 應用程式圖示" width="88" />
</p>

<h1 align="center">VoiceHotkey</h1>

<p align="center"><strong>按下快捷鍵，說話即可輸入</strong></p>

<p align="center">
  <a href="https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest"><strong>下載最新版</strong></a> ·
  <a href="https://voicehotkey.pages.dev/docs/zh-tw/getting-started/install/">安裝指南</a>
</p>

[![Platform](https://img.shields.io/badge/platform-macOS%2014%2B-lightgrey.svg)](https://voicehotkey.pages.dev/)
[![Version](https://img.shields.io/badge/version-0.9.4-green.svg)](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest)
[![Download](https://img.shields.io/badge/download-Releases-blue.svg)](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest)
[![Docs](https://img.shields.io/badge/docs-handbook-informational.svg)](https://voicehotkey.pages.dev/docs/zh-tw/)

**語言：** [简体中文](README.md) · 繁體中文 · [English](README.en.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Deutsch](README.de.md) · [Español](README.es.md)

> **目前公開版本：0.9.4**
> 適用於 **Apple Silicon（arm64）Mac，macOS 14 或更新版本**；目前未提供 Intel 安裝包。[下載最新版本](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest)。
> 此安裝包**尚未經過 Apple 公證，也未使用 Apple Developer ID 簽名**。首次開啟可能遭 macOS 阻擋。0.9.3 安裝包已撤下，請使用最新版本。

[VoiceHotkey](https://voicehotkey.pages.dev/) 的**官方安裝包 / 下載**倉庫。

> **安裝包只透過 [GitHub Releases](https://github.com/yeahhe365/VoiceHotkey-releases/releases) 發佈。**
> 本倉庫不提交 `.dmg` / `.app` 等二進位檔，避免 git 歷史膨脹。

## 產品簡介

macOS **語音輸入**：按住（或短按）熱鍵說話，識別完成後將文字插入目前游標。支援本機模型、雲端識別、語音指令、翻譯潤色、檔案轉寫與本機歷史。

<p align="center">
  <img src="assets/preview-zh.png" alt="語音辨識完成後，文字已插入游標位置" width="840" />
</p>

- **產品官網**：[voicehotkey.pages.dev](https://voicehotkey.pages.dev/)
- **使用手冊**：[voicehotkey.pages.dev/docs](https://voicehotkey.pages.dev/docs/zh-tw/)
- **核心功能**：
  - **多識別引擎**：Apple 系統語音、本機端側大模型（阿里 Qwen3-ASR、SenseVoice、Whisper CoreML/ANE 加速、復旦 MOSS-0.9B、小紅書 FireRed、Fun-ASR、Parakeet）、火山豆包 ASR 2.0、阿里百煉、小米 MiMo、Azure、雲端 Whisper、Groq、ElevenLabs Scribe、Soniox、NVIDIA NIM、Gemini 等
  - **文字處理**：自學習高頻短語可跳過大模型請求、詞替換（正則與上下文變體）、可選大模型潤色與 Apple 原生翻譯（macOS 26+，可能需要系統語言資源）。
  - **語音指令與控制**：本機詞典與意圖大模型，支援快捷鍵注入、文字展開、捷徑指令與受控系統操作（無任意 Shell 執行）
  - **檔案轉寫與匯出**：試用 / Pro 可轉寫音訊與視訊檔案，匯出 `.srt` / `.vtt` / `.ass` / `.lrc` 字幕或 `.txt` 文字。
  - **隱私設定**：API 金鑰保存在 macOS 鑰匙圈。「僅本機模式」限制公網 ASR / LLM 並暫停更新；商業授權請求與主動模型下載仍可連網。[查看資料去向](https://voicehotkey.pages.dev/docs/zh-tw/privacy/local-only/)。
- **介面語言**（與軟體一致）：简体中文、繁體中文、English、日本語、한국어、Deutsch、Español

## 下載與取得

| | |
|--|--|
| **最新版本** | [Releases · Latest](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest) |
| **全部版本** | [Releases](https://github.com/yeahhe365/VoiceHotkey-releases/releases) |
| **產品官網** | [voicehotkey.pages.dev](https://voicehotkey.pages.dev/) |
| **使用手冊** | [使用手冊](https://voicehotkey.pages.dev/docs/zh-tw/) |
| **問題回饋** | [聯絡與回饋](https://voicehotkey.pages.dev/docs/zh-tw/support/contact/) |

### 建議安裝步驟

1. 確認你的 Mac 使用 Apple Silicon，且執行 macOS 14 或更新版本，再開啟 [最新 Release](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest)。
2. 下載 `VoiceHotkey-0.9.4.dmg`；Source code 壓縮檔不是安裝包。
3. 將 **VoiceHotkey.app** 拖入 **應用程式**（`/Applications` 或 `~/Applications`），從安裝後的固定路徑啟動。
4. 若 macOS 阻擋開啟，核對官方來源後依 [Apple 官方說明](https://support.apple.com/zh-tw/102445)處理；若提示檔案損壞，先核對校驗和、重新下載，仍有問題請聯絡支援。
5. 在引導中授予 **輔助使用**、**麥克風**，以及預設 Apple 引擎需要的 **語音辨識** 權限。
6. 點選引導中的試用輸入框，用預設語音輸入熱鍵 **Ctrl + Option + Space** 說一句話，確認文字成功插入。

可選：安裝前核對 Release 說明中的 SHA-256。完整步驟見 [安裝手冊](https://voicehotkey.pages.dev/docs/zh-tw/getting-started/install/)。

**首次使用：** 預設 Apple 系統語音無需 API Key。macOS 26+ 使用新引擎時，可能需要下載系統語言資源；較早系統的 Apple Speech 一般模式可能使用 Apple 服務。本機獨立模型需要先安裝，雲端識別與大模型功能依服務要求填入憑證，API 費用由對應服務商收取。

**試用與授權：** 首次啟動自動開始 14 天 Pro 試用，無需綁卡；到期後繼續使用 Free。Pro 首次啟用與更換啟用碼需連網；驗證成功後可離線使用最長 30 天，每個個人授權最多綁定 3 台 Mac。[授權說明](https://voicehotkey.pages.dev/docs/zh-tw/support/license/)。

更新說明見手冊：[更新](https://voicehotkey.pages.dev/docs/zh-tw/advanced/updates/)。

## 授權與條款

VoiceHotkey 為閉源商業軟體，本倉庫不公開應用程式原始碼。下載安裝包並不授予超出產品授權 / 使用條款的權利。
見本倉 [LICENSE](LICENSE) · [NOTICE](NOTICE.md)，以及手冊：[方案與商業](https://voicehotkey.pages.dev/docs/zh-tw/getting-started/plans/)、[隱私](https://voicehotkey.pages.dev/docs/zh-tw/privacy/policy/)。

## 支援

- 使用問題與缺陷 → [聯絡與回饋](https://voicehotkey.pages.dev/docs/zh-tw/support/contact/)
- 下載連結損壞、資源缺失 → 可在本倉 [Discussions](https://github.com/yeahhe365/VoiceHotkey-releases/discussions) 回饋
- 本倉僅用於**分發**；產品功能需求請走手冊中的聯絡管道，勿當作源碼 Issues
