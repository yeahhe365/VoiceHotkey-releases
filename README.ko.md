<p align="center">
  <img src="assets/app-icon.png" alt="VoiceHotkey 앱 아이콘" width="88" />
</p>

<h1 align="center">VoiceHotkey</h1>

<p align="center"><strong>단축키를 누르고 말하면 macOS에 입력됩니다</strong></p>

<p align="center">
  <a href="https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest"><strong>최신 버전 다운로드</strong></a> ·
  <a href="https://voicehotkey.pages.dev/docs/ko/getting-started/install/">설치 가이드</a>
</p>

[![Platform](https://img.shields.io/badge/platform-macOS%2014%2B-lightgrey.svg)](https://voicehotkey.pages.dev/)
[![Version](https://img.shields.io/badge/version-0.9.4-green.svg)](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest)
[![Download](https://img.shields.io/badge/download-Releases-blue.svg)](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest)
[![Docs](https://img.shields.io/badge/docs-handbook-informational.svg)](https://voicehotkey.pages.dev/docs/ko/)

**언어:** [简体中文](README.md) · [繁體中文](README.zh-Hant.md) · [English](README.en.md) · [日本語](README.ja.md) · 한국어 · [Deutsch](README.de.md) · [Español](README.es.md)

> **현재 공개 버전: 0.9.4**
> **Apple Silicon(arm64) Mac, macOS 14 이상**에서 사용할 수 있습니다. 현재 Intel 설치 파일은 제공하지 않습니다. [최신 버전 다운로드](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest).
> 이 설치 파일은 **Apple 공증을 받지 않았으며 Apple Developer ID로 서명되지 않았습니다**. macOS가 첫 실행을 차단할 수 있습니다. 0.9.3 설치 파일은 배포가 철회되었으므로 최신 버전을 사용하세요.

[VoiceHotkey](https://voicehotkey.pages.dev/) **공식 설치 파일 / 다운로드** 저장소입니다.

> **설치 파일은 [GitHub Releases](https://github.com/yeahhe365/VoiceHotkey-releases/releases) 로만 배포합니다.**
> `.dmg` / `.app` 바이너리는 git 에 커밋하지 않습니다.

## 제품 소개

macOS **음성 입력**: 단축키를 길게 누르거나 탭해 말하면 인식된 텍스트가 커서 위치에 삽입됩니다. 기기 내 모델, 클라우드 인식, 음성 명령, 번역 및 문장 다듬기, 파일 전사와 로컬 기록을 지원합니다.

<p align="center">
  <img src="assets/preview-en.png" alt="음성 인식 텍스트가 입력된 상태" width="840" />
</p>

- **제품 사이트:** [voicehotkey.pages.dev](https://voicehotkey.pages.dev/)
- **사용 설명서:** [voicehotkey.pages.dev/docs](https://voicehotkey.pages.dev/docs/ko/)
- **핵심 기능:**
  - **다중 음성인식 엔진**: Apple 시스템 음성인식, 기기 내 온디바이스 모델(Qwen3-ASR, SenseVoice, Whisper CoreML/ANE 가속, OpenMOSS 0.9B, FireRed, Fun-ASR, Parakeet), Doubao ASR 2.0, Bailian, Xiaomi MiMo, Azure, 클라우드 Whisper, Groq, ElevenLabs Scribe, Soniox, NVIDIA NIM, Gemini 등
  - **텍스트 처리**: 학습한 고빈도 구문으로 LLM 요청을 생략할 수 있으며, 정규식 및 맥락 기반 단어 치환, 선택적 LLM 윤문, Apple 네이티브 번역을 지원합니다(Apple 번역은 macOS 26+, 언어 리소스가 필요할 수 있음).
  - **음성 명령 및 제어**: 로컬 명령어 사전과 의도 해석 LLM을 통한 단축키 입력, 텍스트 확장, 단축어(Shortcuts) 앱 실행, 제어된 시스템 동작(임의 Shell 명령 미실행)
  - **파일 전사 및 내보내기**: 체험 / Pro에서 오디오·비디오를 전사하고 `.srt` / `.vtt` / `.ass` / `.lrc` 자막 또는 `.txt` 텍스트를 내보낼 수 있습니다.
  - **개인정보 설정**: API 키는 macOS 키체인에 저장됩니다. 로컬 전용 모드는 외부 ASR / LLM 엔드포인트를 제한하고 업데이트를 중지하지만, 라이선스 요청과 수동 모델 다운로드는 네트워크를 사용할 수 있습니다. [데이터 전송 안내](https://voicehotkey.pages.dev/docs/ko/privacy/local-only/).
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

1. Apple Silicon Mac과 macOS 14 이상인지 확인한 후 [최신 Release](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest)를 엽니다.
2. `VoiceHotkey-0.9.4.dmg`를 다운로드합니다. Source code 압축 파일은 설치 파일이 아닙니다.
3. **VoiceHotkey.app**을 **응용 프로그램**(`/Applications` 또는 `~/Applications`)으로 드래그한 후 해당 고정 경로에서 실행합니다.
4. macOS가 실행을 차단하면 공식 출처를 확인하고 [Apple 안내](https://support.apple.com/ko-kr/102445)를 따르세요. 파일 손상 경고라면 체크섬 확인 후 다시 다운로드하고, 문제가 계속되면 지원팀에 문의하세요.
5. 초기 설정에서 **손쉬운 사용**, **마이크**, 기본 Apple 엔진의 **음성 인식** 권한을 허용합니다.
6. 초기 설정의 연습 입력란을 클릭하고 기본 **Ctrl + Option + Space**로 한 문장을 말해 텍스트가 삽입되는지 확인합니다.

선택: 설치 전 Release 노트의 SHA-256 을 확인합니다. 자세한 안내: [설치 가이드](https://voicehotkey.pages.dev/docs/ko/getting-started/install/).

**첫 사용:** 기본 Apple 음성 인식은 API 키가 필요 없습니다. macOS 26+의 새 엔진은 언어 리소스를 다운로드해야 할 수 있습니다. 이전 시스템의 일반 Apple Speech 모드는 Apple 서비스를 이용할 수 있습니다. 독립적인 기기 내 모델은 먼저 설치해야 합니다. 클라우드 인식과 LLM 기능의 인증 정보 및 API 사용료는 선택한 서비스에 따릅니다.

**체험 및 라이선스:** 첫 실행 시 카드 등록 없이 14일 Pro 체험이 시작되며, 종료 후에도 Free를 사용할 수 있습니다. Pro 첫 활성화와 키 변경에는 온라인 확인이 필요합니다. 확인 후 최대 30일 동안 오프라인으로 사용할 수 있고, 개인 라이선스당 Mac 최대 3대를 등록할 수 있습니다. [라이선스 안내](https://voicehotkey.pages.dev/docs/ko/support/license/).

자세한 내용: [업데이트](https://voicehotkey.pages.dev/docs/ko/advanced/updates/).

## 라이선스 및 약관

VoiceHotkey는 독점 상용 소프트웨어이며, 이 저장소에서 앱 소스 코드를 공개하지 않습니다. 설치 파일을 다운로드하더라도 제품 라이선스 및 약관을 넘어서는 권리가 부여되지 않습니다.
본 저장소의 [LICENSE](LICENSE) · [NOTICE](NOTICE.md) 및 [플랜](https://voicehotkey.pages.dev/docs/ko/getting-started/plans/), [개인정보 처리방침](https://voicehotkey.pages.dev/docs/ko/privacy/policy/)을 확인해 주세요.

## 지원

- 사용 질문 및 버그 리포트 → [문의](https://voicehotkey.pages.dev/docs/ko/support/contact/)
- 다운로드 링크 깨짐 / 자산 누락 → 본 저장소 [Discussions](https://github.com/yeahhe365/VoiceHotkey-releases/discussions)
- 본 저장소는 **배포 전용**입니다. 제품 기능 제안 등은 공식 설명서의 문의 창구를 이용해 주세요
