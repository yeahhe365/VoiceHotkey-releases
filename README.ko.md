# VoiceHotkey 릴리스 (설치 파일)

[![Platform](https://img.shields.io/badge/platform-macOS%2014%2B-lightgrey.svg)](https://voicehotkey.pages.dev/)
[![Download](https://img.shields.io/badge/download-Releases-blue.svg)](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest)
[![Docs](https://img.shields.io/badge/docs-handbook-informational.svg)](https://voicehotkey.pages.dev/docs/ko/)

**언어:** [简体中文](README.md) · [繁體中文](README.zh-Hant.md) · [English](README.en.md) · [日本語](README.ja.md) · 한국어 · [Deutsch](README.de.md) · [Español](README.es.md)

[VoiceHotkey](https://voicehotkey.pages.dev/) **공식 설치 파일 / 다운로드** 저장소입니다.

> **설치 파일은 [GitHub Releases](https://github.com/yeahhe365/VoiceHotkey-releases/releases) 로만 배포합니다.**  
> `.dmg` / `.app` 바이너리는 git 에 커밋하지 않습니다.

## 제품 소개

macOS **음성 입력**: 단축키를 누른 채(또는 탭하여) 말하면 커서 위치에 텍스트가 삽입됩니다. 음성 명령, 후처리, 파일 전사, 기기 내 기록도 지원합니다.

- **제품 사이트:** [voicehotkey.pages.dev](https://voicehotkey.pages.dev/)
- **사용 설명서:** [voicehotkey.pages.dev/docs](https://voicehotkey.pages.dev/docs/ko/)
- **UI 언어** (앱과 동일): 简体中文, 繁體中文, English, 日本語, 한국어, Deutsch, Español

## 다운로드

| | |
|--|--|
| **최신 버전** | [Releases · Latest](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest) |
| **전체 버전** | [Releases](https://github.com/yeahhe365/VoiceHotkey-releases/releases) |
| **제품 사이트** | [voicehotkey.pages.dev](https://voicehotkey.pages.dev/) |
| **설명서** | [Docs](https://voicehotkey.pages.dev/docs/ko/) |
| **문의** | [연락처](https://voicehotkey.pages.dev/docs/ko/support/contact/) |

### 권장 설치 단계

1. [최신 Release](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest) 를 엽니다.
2. `VoiceHotkey-X.Y.Z.dmg` 를 다운로드합니다 (공증된 Developer ID 빌드일 수 있음).
3. DMG 를 열고 **VoiceHotkey** 를 **응용 프로그램** 으로 드래그합니다.
4. `/Applications` (또는 `~/Applications`) 에서 실행하고 **손쉬운 사용** 과 **마이크** 권한을 허용합니다.

선택: 설치 전 Release 노트의 SHA-256 을 확인합니다. [설치 가이드](https://voicehotkey.pages.dev/docs/ko/getting-started/install/).

## 이 저장소에 둘 것

| 자산 | 용도 |
|------|------|
| `VoiceHotkey-X.Y.Z.dmg` | 공증된 macOS 설치 이미지 (Release 자산만) |
| Release 노트의 체크섬 | 다운로드 무결성 확인 |
| (선택) Sparkle 공개 파일 | GitHub Pages 외 호스팅 시 |

## 두지 말 것

- 앱 **소스 코드** (이 저장소에서 관리하지 않음)
- 서명 비밀키, 공증 자격 증명, Sparkle **비밀** 키
- 대용량 `.dmg` / `.app` 의 git 커밋 (**Release 자산**만 사용)

## 버전 규칙

- Tag: `vX.Y.Z` (예: `v0.9.0`)
- 파일명: `VoiceHotkey-X.Y.Z.dmg`
- 제품 `CFBundleShortVersionString` 과 일치

직접 다운로드 URL:

```text
https://github.com/yeahhe365/VoiceHotkey-releases/releases/download/vX.Y.Z/VoiceHotkey-X.Y.Z.dmg
```

## 유지보수자 배포 절차

소스 트리에서 빌드·공증 후 여기에 게시:

```bash
export VH_SIGN_IDENTITY="Developer ID Application: …"
export VH_NOTARY_PROFILE=VH_NOTARY
make release-dmg

bash scripts/publish-release.sh
```

Sparkle appcast enclosure 는 이 저장소를 가리켜야 합니다:

```bash
VH_UPDATE_BASE_URL=https://github.com/yeahhe365/VoiceHotkey-releases/releases/download/v0.9.0 \
  make appcast
```

설명서: [업데이트](https://voicehotkey.pages.dev/docs/ko/advanced/updates/).

## 라이선스 및 약관

VoiceHotkey 는 독점 상용 소프트웨어입니다. 설치 파일을 받는 것만으로 제품 라이선스/약관을 넘는 권한이 부여되지 않습니다.  
[LICENSE](LICENSE) · [NOTICE](NOTICE.md), [요금제](https://voicehotkey.pages.dev/docs/ko/getting-started/plans/), [개인정보](https://voicehotkey.pages.dev/docs/ko/privacy/policy/).

## 지원

- 버그·사용 문의 → [연락처](https://voicehotkey.pages.dev/docs/ko/support/contact/)
- 다운로드 링크 파손·자산 누락 → [Discussions](https://github.com/yeahhe365/VoiceHotkey-releases/discussions)
- 이 저장소는 **배포 전용**입니다. 기능 요청은 설명서의 연락 채널을 이용해 주세요
