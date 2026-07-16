# VoiceHotkey 安裝包發佈倉

[![Platform](https://img.shields.io/badge/platform-macOS%2014%2B-lightgrey.svg)](https://voicehotkey.pages.dev/)
[![Download](https://img.shields.io/badge/download-Releases-blue.svg)](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest)
[![Docs](https://img.shields.io/badge/docs-handbook-informational.svg)](https://voicehotkey.pages.dev/docs/zh-tw/)

**語言：** [简体中文](README.md) · 繁體中文 · [English](README.en.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Deutsch](README.de.md) · [Español](README.es.md)

[VoiceHotkey](https://voicehotkey.pages.dev/) 的**官方安裝包 / 下載**倉庫。

> **安裝包只透過 [GitHub Releases](https://github.com/yeahhe365/VoiceHotkey-releases/releases) 發佈。**  
> 本倉庫不提交 `.dmg` / `.app` 等二進位檔，避免 git 歷史膨脹。

## 產品簡介

macOS **語音輸入**：按住（或短按）熱鍵說話，文字插入目前游標。可選語音指令、文本後處理、檔案轉寫與本機歷史。

- **產品官網**：[voicehotkey.pages.dev](https://voicehotkey.pages.dev/)
- **使用手冊**：[voicehotkey.pages.dev/docs](https://voicehotkey.pages.dev/docs/zh-tw/)
- **介面語言**（與軟體相同）：简体中文、繁體中文、English、日本語、한국어、Deutsch、Español

## 下載

| | |
|--|--|
| **最新版本** | [Releases · Latest](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest) |
| **全部版本** | [Releases](https://github.com/yeahhe365/VoiceHotkey-releases/releases) |
| **產品官網** | [voicehotkey.pages.dev](https://voicehotkey.pages.dev/) |
| **使用手冊** | [手冊](https://voicehotkey.pages.dev/docs/zh-tw/) |
| **問題回饋** | [聯絡與回饋](https://voicehotkey.pages.dev/docs/zh-tw/support/contact/) |

### 建議安裝步驟

1. 開啟 [最新 Release](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest)。
2. 下載 `VoiceHotkey-X.Y.Z.dmg`（有公證時為 Developer ID 建置）。
3. 開啟 DMG，將 **VoiceHotkey** 拖入 **應用程式**。
4. 從 `/Applications`（或 `~/Applications`）啟動，依提示授權 **輔助使用** 與 **麥克風**。

可選：安裝前核對 Release 說明中的 SHA-256。完整步驟見 [安裝手冊](https://voicehotkey.pages.dev/docs/zh-tw/getting-started/install/)。

## 本倉應有內容

| 資產 | 用途 |
|------|------|
| `VoiceHotkey-X.Y.Z.dmg` | 公證後的 macOS 安裝映像（僅作 Release 附件） |
| Release 說明中的校驗和 | 下載完整性核對 |
| （可選）Sparkle 相關公開檔 | 若不完全依賴 GitHub Pages |

## 本倉不應有的內容

- 應用**原始碼**（不在此倉維護）
- 簽名私鑰、公證憑據、Sparkle **私鑰**
- 將大體積 `.dmg` / `.app` **commit 進 git**（請只用 **Release 附件**）

## 版本約定

- Tag：`vX.Y.Z`（例如 `v0.9.0`）
- 檔名：`VoiceHotkey-X.Y.Z.dmg`
- 與產品 `CFBundleShortVersionString` 對齊

直接下載 URL 形態：

```text
https://github.com/yeahhe365/VoiceHotkey-releases/releases/download/vX.Y.Z/VoiceHotkey-X.Y.Z.dmg
```

## 維護者發佈流程

在原始碼樹中建置並公證，再發佈到此：

```bash
export VH_SIGN_IDENTITY="Developer ID Application: …"
export VH_NOTARY_PROFILE=VH_NOTARY
make release-dmg

bash scripts/publish-release.sh
```

Sparkle appcast 的 enclosure 基址應指向本倉：

```bash
VH_UPDATE_BASE_URL=https://github.com/yeahhe365/VoiceHotkey-releases/releases/download/v0.9.0 \
  make appcast
```

更新說明見手冊：[更新](https://voicehotkey.pages.dev/docs/zh-tw/advanced/updates/)。

## 授權與條款

VoiceHotkey 為專有商業軟體。下載安裝包並不授予超出產品授權 / 使用條款的權利。  
說明見手冊：[方案](https://voicehotkey.pages.dev/docs/zh-tw/getting-started/plans/)、[隱私](https://voicehotkey.pages.dev/docs/zh-tw/privacy/policy/)。

## 支援

- 使用問題與缺陷 → [聯絡與回饋](https://voicehotkey.pages.dev/docs/zh-tw/support/contact/)
- 本倉僅用於**分發**；除非是下載連結損壞或資源缺失，請勿在此提產品 Issue
