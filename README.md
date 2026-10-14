# VoiceHotkey 安装包发布仓

[![Platform](https://img.shields.io/badge/platform-macOS%2014%2B-lightgrey.svg)](https://voicehotkey.pages.dev/)
[![Version](https://img.shields.io/badge/version-0.9.4-green.svg)](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest)
[![Download](https://img.shields.io/badge/download-Releases-blue.svg)](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest)
[![Docs](https://img.shields.io/badge/docs-手册-informational.svg)](https://voicehotkey.pages.dev/docs/)

**语言：** 简体中文 · [繁體中文](README.zh-Hant.md) · [English](README.en.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Deutsch](README.de.md) · [Español](README.es.md)

> **当前公开版本：0.9.4**
> 适用于 **Apple Silicon（arm64）Mac，macOS 14 或更高版本**；当前未提供 Intel 安装包。[下载最新版本](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest)。
> 此安装包**尚未经过 Apple 公证，也未使用 Apple Developer ID 签名**。首次打开可能被 macOS 拦截。0.9.3 安装包已撤下，请使用最新版本。

[VoiceHotkey](https://voicehotkey.pages.dev/) 的**官方安装包 / 下载**仓库。

> **安装包只通过 [GitHub Releases](https://github.com/yeahhe365/VoiceHotkey-releases/releases) 发布。**
> 本仓库不提交 `.dmg` / `.app` 等二进制文件，避免 git 历史膨胀。

## 产品简介

macOS **语音输入**：按住（或短按）热键说话，识别完成后将文字插入当前光标。支持本机模型、云端识别、语音命令、翻译润色、文件转写与本机历史。

- **产品官网**：[voicehotkey.pages.dev](https://voicehotkey.pages.dev/)
- **用户手册**：[voicehotkey.pages.dev/docs](https://voicehotkey.pages.dev/docs/)
- **核心功能**：
  - **多识别引擎**：Apple 系统语音、本机端侧大模型（阿里 Qwen3-ASR、SenseVoice、Whisper CoreML/ANE 加速、复旦 MOSS-0.9B、小红书 FireRed、Fun-ASR、Parakeet）、火山豆包 ASR 2.0、阿里百炼、小米 MiMo、Azure、云端 Whisper、Groq、ElevenLabs Scribe、Soniox、NVIDIA NIM、Gemini 等
  - **文本处理**：自学习高频短语可跳过大模型请求、词替换（正则与上下文变体）、可选大模型润色与 Apple 原生翻译（macOS 26+，可能需要系统语言资源）。
  - **语音命令与控制**：本地词典与意图大模型，支持快捷键注入、文本展开、快捷指令与受控系统操作（无任意 Shell 执行）
  - **文件转写与导出**：试用 / Pro 可转写音视频文件，导出 `.srt` / `.vtt` / `.ass` / `.lrc` 字幕或 `.txt` 文本。
  - **隐私设置**：API 密钥保存在 macOS 钥匙串。“仅本地模式”限制公网 ASR / LLM 并暂停更新；商业许可请求与主动模型下载仍可联网。[查看数据去向](https://voicehotkey.pages.dev/docs/privacy/local-only/)。
- **界面语言**（与软件一致）：简体中文、繁體中文、English、日本語、한국어、Deutsch、Español

## 下载与获取

| | |
|--|--|
| **最新版本** | [Releases · Latest](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest) |
| **全部版本** | [Releases](https://github.com/yeahhe365/VoiceHotkey-releases/releases) |
| **产品官网** | [voicehotkey.pages.dev](https://voicehotkey.pages.dev/) |
| **用户手册** | [在线手册](https://voicehotkey.pages.dev/docs/) |
| **问题反馈** | [联系与反馈](https://voicehotkey.pages.dev/docs/support/contact/) |

### 推荐安装步骤

1. 确认你的 Mac 使用 Apple Silicon，且运行 macOS 14 或更高版本，再打开 [最新 Release](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest)。
2. 下载 `VoiceHotkey-0.9.4.dmg`；Source code 压缩包不是安装包。
3. 将 **VoiceHotkey.app** 拖入 **应用程序**（`/Applications` 或 `~/Applications`），从安装后的固定路径启动。
4. 若 macOS 阻止打开，核对官方来源后按 [Apple 官方说明](https://support.apple.com/zh-cn/102445)处理；若提示文件损坏，先核对校验和、重新下载，仍有问题请联系支持。
5. 在引导中授予 **辅助功能**、**麦克风**，以及默认 Apple 引擎需要的 **语音识别** 权限。
6. 点击引导中的试用输入框，用默认语音输入热键 **Ctrl + Option + Space** 说一句话，确认文字成功插入。

可选：安装前核对 Release 说明中的 SHA-256。更完整的安装说明见 [安装手册](https://voicehotkey.pages.dev/docs/getting-started/install/)。

**首次使用：** 默认 Apple 系统语音无需 API Key。macOS 26+ 使用新引擎时，可能需要下载系统语言资源；较早系统的 Apple Speech 常规模式可能使用 Apple 服务。本机独立模型需要先安装，云端识别与大模型功能按服务要求填写凭证，API 费用由对应服务商收取。

**试用与许可：** 首次启动自动开始 14 天 Pro 试用，无需绑卡；到期后继续使用 Free。Pro 首次激活和更换激活码需联网；验证成功后可离线使用最长 30 天，每个个人许可证最多绑定 3 台 Mac。[许可证说明](https://voicehotkey.pages.dev/docs/support/license/)。

更新说明见用户手册：[更新](https://voicehotkey.pages.dev/docs/advanced/updates/)。

## 许可与条款

VoiceHotkey 为闭源商业软件，本仓库不公开应用源码。下载安装包并不授予超出产品许可 / 使用条款的权利。
见本仓 [LICENSE](LICENSE) · [NOTICE](NOTICE.md)，以及手册：[方案与商业](https://voicehotkey.pages.dev/docs/getting-started/plans/)、[隐私](https://voicehotkey.pages.dev/docs/privacy/policy/)。

## 支持

- 使用问题与缺陷 → [联系与反馈](https://voicehotkey.pages.dev/docs/support/contact/)
- 下载链接损坏、资源缺失 → 可在本仓 [Discussions](https://github.com/yeahhe365/VoiceHotkey-releases/discussions) 反馈
- 本仓仅用于**分发**；产品功能需求请走手册中的联系渠道，勿当作源码 Issues
