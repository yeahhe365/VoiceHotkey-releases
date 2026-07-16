# VoiceHotkey リリース（インストーラー）

[![Platform](https://img.shields.io/badge/platform-macOS%2014%2B-lightgrey.svg)](https://voicehotkey.pages.dev/)
[![Download](https://img.shields.io/badge/download-Releases-blue.svg)](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest)
[![Docs](https://img.shields.io/badge/docs-handbook-informational.svg)](https://voicehotkey.pages.dev/docs/ja/)

**言語：** [简体中文](README.md) · [繁體中文](README.zh-Hant.md) · [English](README.en.md) · 日本語 · [한국어](README.ko.md) · [Deutsch](README.de.md) · [Español](README.es.md)

[VoiceHotkey](https://voicehotkey.pages.dev/) の**公式インストーラー / ダウンロード**リポジトリです。

> **インストーラーは [GitHub Releases](https://github.com/yeahhe365/VoiceHotkey-releases/releases) のみで公開します。**  
> `.dmg` / `.app` などのバイナリを git にコミットしません。

## 製品について

macOS の**音声入力**：ホットキーを押しながら（またはタップして）話し、カーソル位置にテキストを挿入します。音声コマンド、後処理、ファイル文字起こし、端末内履歴にも対応。

- **公式サイト：** [voicehotkey.pages.dev](https://voicehotkey.pages.dev/)
- **ユーザーマニュアル：** [voicehotkey.pages.dev/docs](https://voicehotkey.pages.dev/docs/ja/)
- **UI 言語**（アプリと同じ）：简体中文、繁體中文、English、日本語、한국어、Deutsch、Español

## ダウンロード

| | |
|--|--|
| **最新版** | [Releases · Latest](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest) |
| **すべての版** | [Releases](https://github.com/yeahhe365/VoiceHotkey-releases/releases) |
| **公式サイト** | [voicehotkey.pages.dev](https://voicehotkey.pages.dev/) |
| **マニュアル** | [Docs](https://voicehotkey.pages.dev/docs/ja/) |
| **サポート** | [お問い合わせ](https://voicehotkey.pages.dev/docs/ja/support/contact/) |

### 推奨インストール手順

1. [最新 Release](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest) を開く。
2. `VoiceHotkey-X.Y.Z.dmg` をダウンロード（公証済み Developer ID ビルドの場合あり）。
3. DMG を開き、**VoiceHotkey** を **アプリケーション** にドラッグ。
4. `/Applications`（または `~/Applications`）から起動し、**アクセシビリティ** と **マイク** を許可。

任意：インストール前に Release 記載の SHA-256 を確認。[インストール手順](https://voicehotkey.pages.dev/docs/ja/getting-started/install/)。

## このリポジトリに置くもの

| 資産 | 用途 |
|------|------|
| `VoiceHotkey-X.Y.Z.dmg` | 公証済み macOS インストーラー（Release アセットのみ） |
| Release ノートのチェックサム | ダウンロード整合性確認 |
| （任意）Sparkle 公開ファイル | GitHub Pages 以外で配る場合 |

## 置かないもの

- アプリの**ソースコード**（本リポジトリでは管理しません）
- 署名秘密鍵、公証認証情報、Sparkle **秘密**鍵
- 大きな `.dmg` / `.app` の git コミット（**Release アセット**のみ）

## バージョン規則

- Tag：`vX.Y.Z`（例：`v0.9.0`）
- ファイル名：`VoiceHotkey-X.Y.Z.dmg`
- 製品の `CFBundleShortVersionString` と一致

直接ダウンロード URL：

```text
https://github.com/yeahhe365/VoiceHotkey-releases/releases/download/vX.Y.Z/VoiceHotkey-X.Y.Z.dmg
```

## メンテナー向け公開手順

ソースツリーでビルド・公証してから、ここに公開します：

```bash
export VH_SIGN_IDENTITY="Developer ID Application: …"
export VH_NOTARY_PROFILE=VH_NOTARY
make release-dmg

bash scripts/publish-release.sh
```

Sparkle appcast の enclosure は本リポジトリを指すこと：

```bash
VH_UPDATE_BASE_URL=https://github.com/yeahhe365/VoiceHotkey-releases/releases/download/v0.9.0 \
  make appcast
```

詳細：[アップデート](https://voicehotkey.pages.dev/docs/ja/advanced/updates/)。

## ライセンスと条項

VoiceHotkey はプロプライエタリ商用ソフトウェアです。インストーラーの入手は、製品ライセンス / 利用規約を超える権利を与えません。  
本リポジトリの [LICENSE](LICENSE) · [NOTICE](NOTICE.md)、および [プラン](https://voicehotkey.pages.dev/docs/ja/getting-started/plans/)、[プライバシー](https://voicehotkey.pages.dev/docs/ja/privacy/policy/)。

## サポート

- 不具合・使い方 → [お問い合わせ](https://voicehotkey.pages.dev/docs/ja/support/contact/)
- ダウンロード破損・アセット欠落 → [Discussions](https://github.com/yeahhe365/VoiceHotkey-releases/discussions)
- 本リポジトリは**配布専用**です。機能要望はマニュアルの連絡先をご利用ください
