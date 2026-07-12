# VoiceHotkey 安装包发布仓

[![Platform](https://img.shields.io/badge/platform-macOS%2014%2B-lightgrey.svg)](https://github.com/yeahhe365/VoiceHotkey)
[![Source](https://img.shields.io/badge/source-VoiceHotkey-blue.svg)](https://github.com/yeahhe365/VoiceHotkey)

**语言：** 中文 | [English](README.en.md)

[VoiceHotkey](https://github.com/yeahhe365/VoiceHotkey) 的**官方安装包 / 下载**仓库。

> **安装包只通过 [GitHub Releases](https://github.com/yeahhe365/VoiceHotkey-releases/releases) 发布。**  
> 本仓库不提交 `.dmg` / `.app` 等二进制文件，避免 git 历史膨胀。

## 下载

| | |
|--|--|
| **最新版本** | [Releases · Latest](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest) |
| **全部版本** | [Releases](https://github.com/yeahhe365/VoiceHotkey-releases/releases) |
| **源码** | [yeahhe365/VoiceHotkey](https://github.com/yeahhe365/VoiceHotkey) |
| **问题反馈** | 请到[源码仓 Issues](https://github.com/yeahhe365/VoiceHotkey/issues) |

### 推荐安装步骤

1. 打开 [最新 Release](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest)。
2. 下载 `VoiceHotkey-X.Y.Z.dmg`（有公证时为 Developer ID 构建）。
3. 打开 DMG，将 **VoiceHotkey** 拖入 **应用程序**。
4. 从 `/Applications`（或 `~/Applications`）启动，按提示授权 **辅助功能** 与 **麦克风**。

可选：安装前核对 Release 说明中的 SHA-256。

## 本仓应有内容

| 资产 | 用途 |
|------|------|
| `VoiceHotkey-X.Y.Z.dmg` | 公证后的 macOS 安装镜像 |
| Release 说明中的校验和 | 下载完整性核对 |
| （可选）Sparkle 相关公开文件 | 若不完全依赖 GitHub Pages |

## 本仓不应有的内容

- 应用**源码** → [VoiceHotkey](https://github.com/yeahhe365/VoiceHotkey)
- 签名私钥、公证凭据、Sparkle **私钥**
- 把大体积 `.dmg` / `.app` **commit 进 git**（请只用 **Release 附件**）

## 版本约定

- Tag：`vX.Y.Z`（例如 `v0.9.0`）
- 文件名：`VoiceHotkey-X.Y.Z.dmg`
- 与源码仓 `Info.plist` 中 `CFBundleShortVersionString` 对齐

直接下载 URL 形态：

```text
https://github.com/yeahhe365/VoiceHotkey-releases/releases/download/vX.Y.Z/VoiceHotkey-X.Y.Z.dmg
```

## 维护者发布流程

在**源码仓**构建并公证，再发布到这里：

```bash
# 在 yeahhe365/VoiceHotkey
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

详见源码仓 [docs/UPDATES.md](https://github.com/yeahhe365/VoiceHotkey/blob/main/docs/UPDATES.md)。

## 许可与条款

VoiceHotkey 为专有商业软件。下载安装包并不授予超出产品许可 / [TERMS](https://github.com/yeahhe365/VoiceHotkey/blob/main/docs/TERMS.md) 的权利。  
源码、许可证全文与商业说明见[主仓库](https://github.com/yeahhe365/VoiceHotkey)。

## 支持

- 缺陷与功能 → [VoiceHotkey Issues](https://github.com/yeahhe365/VoiceHotkey/issues)
- 本仓仅用于**分发**；除非是下载链接损坏或资源缺失，请勿在此提产品 Issue。
