# VoiceHotkey 安装包发布仓

[![Platform](https://img.shields.io/badge/platform-macOS%2014%2B-lightgrey.svg)](https://voicehotkey.pages.dev/)
[![Download](https://img.shields.io/badge/download-Releases-blue.svg)](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest)
[![Docs](https://img.shields.io/badge/docs-手册-informational.svg)](https://voicehotkey.pages.dev/docs/)

**语言：** 简体中文 · [繁體中文](README.zh-Hant.md) · [English](README.en.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Deutsch](README.de.md) · [Español](README.es.md)

[VoiceHotkey](https://voicehotkey.pages.dev/) 的**官方安装包 / 下载**仓库。

> **安装包只通过 [GitHub Releases](https://github.com/yeahhe365/VoiceHotkey-releases/releases) 发布。**  
> 本仓库不提交 `.dmg` / `.app` 等二进制文件，避免 git 历史膨胀。

## 产品简介

macOS **语音输入**：按住（或短按）热键说话，文字插入当前光标。可选语音命令、文本后处理、文件转写与本机历史。

- **产品官网**：[voicehotkey.pages.dev](https://voicehotkey.pages.dev/)
- **用户手册**：[voicehotkey.pages.dev/docs](https://voicehotkey.pages.dev/docs/)
- **界面语言**（与软件一致）：简体中文、繁體中文、English、日本語、한국어、Deutsch、Español

## 下载

| | |
|--|--|
| **最新版本** | [Releases · Latest](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest) |
| **全部版本** | [Releases](https://github.com/yeahhe365/VoiceHotkey-releases/releases) |
| **产品官网** | [voicehotkey.pages.dev](https://voicehotkey.pages.dev/) |
| **用户手册** | [手册](https://voicehotkey.pages.dev/docs/) |
| **问题反馈** | [联系与反馈](https://voicehotkey.pages.dev/docs/support/contact/) |

### 推荐安装步骤

1. 打开 [最新 Release](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest)。
2. 下载 `VoiceHotkey-X.Y.Z.dmg`（有公证时为 Developer ID 构建）。
3. 打开 DMG，将 **VoiceHotkey** 拖入 **应用程序**。
4. 从 `/Applications`（或 `~/Applications`）启动，按提示授权 **辅助功能** 与 **麦克风**。

可选：安装前核对 Release 说明中的 SHA-256。更完整的安装说明见 [安装手册](https://voicehotkey.pages.dev/docs/getting-started/install/)。

## 本仓应有内容

| 资产 | 用途 |
|------|------|
| `VoiceHotkey-X.Y.Z.dmg` | 公证后的 macOS 安装镜像（仅作 Release 附件） |
| Release 说明中的校验和 | 下载完整性核对 |
| （可选）Sparkle 相关公开文件 | 若不完全依赖 GitHub Pages |

## 本仓不应有的内容

- 应用**源码**（不在此仓维护）
- 签名私钥、公证凭据、Sparkle **私钥**
- 把大体积 `.dmg` / `.app` **commit 进 git**（请只用 **Release 附件**）

## 版本约定

- Tag：`vX.Y.Z`（例如 `v0.9.0`）
- 文件名：`VoiceHotkey-X.Y.Z.dmg`
- 与产品 `CFBundleShortVersionString` 对齐

直接下载 URL 形态：

```text
https://github.com/yeahhe365/VoiceHotkey-releases/releases/download/vX.Y.Z/VoiceHotkey-X.Y.Z.dmg
```

## 维护者发布流程

在源码树中构建并公证，再发布到这里：

```bash
export VH_SIGN_IDENTITY="Developer ID Application: …"
export VH_NOTARY_PROFILE=VH_NOTARY
make release-dmg

# 上传到本仓 Releases
bash scripts/publish-release.sh
```

Sparkle appcast 的 enclosure 基址应指向本仓：

```bash
VH_UPDATE_BASE_URL=https://github.com/yeahhe365/VoiceHotkey-releases/releases/download/v0.9.0 \
  make appcast
```

更新说明见用户手册：[更新](https://voicehotkey.pages.dev/docs/advanced/updates/)。

## 许可与条款

VoiceHotkey 为专有商业软件。下载安装包并不授予超出产品许可 / 使用条款的权利。  
见本仓 [LICENSE](LICENSE) · [NOTICE](NOTICE.md)，以及手册：[方案与商业](https://voicehotkey.pages.dev/docs/getting-started/plans/)、[隐私](https://voicehotkey.pages.dev/docs/privacy/policy/)。

## 支持

- 使用问题与缺陷 → [联系与反馈](https://voicehotkey.pages.dev/docs/support/contact/)
- 下载链接损坏、资源缺失 → 可在本仓 [Discussions](https://github.com/yeahhe365/VoiceHotkey-releases/discussions) 反馈
- 本仓仅用于**分发**；产品功能需求请走手册中的联系渠道，勿当作源码 Issues
