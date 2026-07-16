# VoiceHotkey 安装包发布仓

[![Platform](https://img.shields.io/badge/platform-macOS%2014%2B-lightgrey.svg)](https://github.com/yeahhe365/VoiceHotkey-releases)
[![Docs](https://img.shields.io/badge/docs-voicehotkey.pages.dev-blue.svg)](https://voicehotkey.pages.dev/docs/)

**语言：** 中文 | [English](README.en.md)

VoiceHotkey 的**官方安装包 / 下载**仓库。

> **安装包只通过 [GitHub Releases](https://github.com/yeahhe365/VoiceHotkey-releases/releases) 发布。**  
> 本仓库不提交 `.dmg` / `.app` 等二进制文件，避免 git 历史膨胀。

## 下载

| | |
|--|--|
| **最新版本** | [Releases · Latest](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest) |
| **全部版本** | [Releases](https://github.com/yeahhe365/VoiceHotkey-releases/releases) |
| **用户手册** | [voicehotkey.pages.dev/docs](https://voicehotkey.pages.dev/docs/) |
| **问题反馈** | [联系与反馈](https://voicehotkey.pages.dev/docs/support/contact/) |

### 推荐安装步骤

1. 打开 [最新 Release](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest)。
2. 下载 `VoiceHotkey-X.Y.Z.dmg`（有公证时为 Developer ID 构建）。
3. 打开 DMG，将 **VoiceHotkey** 拖入 **应用程序**。
4. 从 `/Applications`（或 `~/Applications`）启动，按提示授权 **辅助功能** 与 **麦克风**。

可选：安装前核对 Release 说明中的 SHA-256。更多说明见 [安装与权限](https://voicehotkey.pages.dev/docs/getting-started/install/)。

## 本仓应有内容

| 资产 | 用途 |
|------|------|
| `VoiceHotkey-X.Y.Z.dmg` | 公证后的 macOS 安装镜像 |
| Release 说明中的校验和 | 下载完整性核对 |
| （可选）Sparkle 相关公开文件 | 若不完全依赖 GitHub Pages |

## 本仓不应有的内容

- 应用源码（本仓仅分发安装包）
- 签名私钥、公证凭据、Sparkle **私钥**
- 把大体积 `.dmg` / `.app` **commit 进 git**（请只用 **Release 附件**）

## 版本约定

- Tag：`vX.Y.Z`（例如 `v0.9.0`）
- 文件名：`VoiceHotkey-X.Y.Z.dmg`
- 与应用 `Info.plist` 中 `CFBundleShortVersionString` 对齐

直接下载 URL 形态：

```text
https://github.com/yeahhe365/VoiceHotkey-releases/releases/download/vX.Y.Z/VoiceHotkey-X.Y.Z.dmg
```

## 维护者发布流程

在**产品源码树**中构建并公证，再发布到本仓 Releases（使用源码树内的 `scripts/publish-release.sh` 等工具）。

Sparkle appcast 的 enclosure 基址应指向本仓：

```bash
VH_UPDATE_BASE_URL=https://github.com/yeahhe365/VoiceHotkey-releases/releases/download/v0.9.0 \
  make appcast
```

用户向的更新说明见 [自动更新](https://voicehotkey.pages.dev/docs/advanced/updates/)。

## 许可与条款

VoiceHotkey 为专有商业软件。下载安装包并不授予超出产品许可与用户手册中隐私/条款说明的权利。  
摘要见 [隐私政策](https://voicehotkey.pages.dev/docs/privacy/policy/)。

## 支持

- 缺陷、功能与使用问题 → [联系与反馈](https://voicehotkey.pages.dev/docs/support/contact/)
- 本仓仅用于**分发**；除非是下载链接损坏或资源缺失，请勿在此提产品 Issue。
