# VoiceHotkey Releases (instaladores)

[![Platform](https://img.shields.io/badge/platform-macOS%2014%2B-lightgrey.svg)](https://voicehotkey.pages.dev/)
[![Version](https://img.shields.io/badge/version-0.9.4-green.svg)](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest)
[![Download](https://img.shields.io/badge/download-Releases-blue.svg)](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest)
[![Docs](https://img.shields.io/badge/docs-handbook-informational.svg)](https://voicehotkey.pages.dev/docs/es/)

**Idioma:** [简体中文](README.md) · [繁體中文](README.zh-Hant.md) · [English](README.en.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Deutsch](README.de.md) · Español

> **Versión pública actual: 0.9.4**
> Para **Mac con Apple Silicon (arm64) y macOS 14 o posterior**. Actualmente no hay instalador para Intel. [Descargar la última versión](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest).
> Este instalador **no está notarizado por Apple ni firmado con Apple Developer ID**. macOS puede bloquear su primer inicio. El instalador de 0.9.3 se ha retirado; utiliza la última versión.

Repositorio **oficial de descarga / instaladores** de [VoiceHotkey](https://voicehotkey.pages.dev/).

> **Los instaladores se publican solo en [GitHub Releases](https://github.com/yeahhe365/VoiceHotkey-releases/releases).**
> Este repo **no** sube `.dmg` / `.app` al historial de git.

## Sobre el producto

**Escritura por voz** en macOS: mantén o pulsa un atajo, habla e inserta el texto reconocido en el cursor. Admite modelos locales, reconocimiento en la nube, comandos de voz, traducción y pulido, transcripción de archivos e historial local.

- **Sitio del producto:** [voicehotkey.pages.dev](https://voicehotkey.pages.dev/)
- **Manual de usuario:** [voicehotkey.pages.dev/docs](https://voicehotkey.pages.dev/docs/es/)
- **Características principales:**
  - **Múltiples motores ASR**: Reconocimiento de voz del sistema Apple, modelos locales sin conexión (Qwen3-ASR, SenseVoice, Whisper acelerado por CoreML/ANE, OpenMOSS 0.9B, FireRed, Fun-ASR, Parakeet), Doubao ASR 2.0, Bailian, Xiaomi MiMo, Azure, Whisper en la nube, Groq, ElevenLabs Scribe, Soniox, NVIDIA NIM, Gemini y más.
  - **Procesamiento de texto**: Las frases frecuentes aprendidas pueden omitir solicitudes al LLM. Los reemplazos admiten regex y variantes de contexto; hay pulido opcional con LLM y traducción nativa de Apple (macOS 26+ para Apple; puede requerir recursos de idiomas).
  - **Comandos de voz y control**: Diccionario local de comandos y modelos de intención LLM para inyección de atajos, expansión de texto, acciones de Atajos (Shortcuts) y control seguro del sistema (sin ejecución de comandos shell arbitrarios).
  - **Transcripción y exportación**: La prueba / Pro transcribe audio y vídeo y exporta subtítulos `.srt`, `.vtt`, `.ass` o `.lrc`, o texto `.txt`.
  - **Ajustes de privacidad**: Las claves API se guardan en macOS Keychain. Solo local limita los servicios ASR / LLM en redes públicas y pausa las actualizaciones; las solicitudes de licencia y las descargas manuales de modelos pueden seguir usando la red. [Flujos de datos](https://voicehotkey.pages.dev/docs/es/privacy/local-only/).
- **Idiomas de la interfaz** (igual que la app): 简体中文, 繁體中文, English, 日本語, 한국어, Deutsch, Español

## Descarga

| | |
|--|--|
| **Última versión** | [Releases · Latest](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest) |
| **Todas las versiones** | [Releases](https://github.com/yeahhe365/VoiceHotkey-releases/releases) |
| **Sitio del producto** | [voicehotkey.pages.dev](https://voicehotkey.pages.dev/) |
| **Manual** | [Docs](https://voicehotkey.pages.dev/docs/es/) |
| **Soporte** | [Contacto](https://voicehotkey.pages.dev/docs/es/support/contact/) |

### Instalación recomendada

1. Confirma que tu Mac utiliza Apple Silicon y macOS 14 o posterior; abre [la última Release](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest).
2. Descarga `VoiceHotkey-0.9.4.dmg`. Los archivos Source code no son instaladores.
3. Arrastra **VoiceHotkey.app** a **Aplicaciones** (`/Applications` o `~/Applications`) e inicia desde esa ruta fija.
4. Si macOS bloquea el inicio, verifica el origen oficial y sigue [la guía de Apple](https://support.apple.com/es-es/102445). Si indica que el archivo está dañado, verifica la suma y vuelve a descargarlo; contacta con soporte si persiste.
5. En la configuración inicial, permite **Accesibilidad**, **Micrófono** y **Reconocimiento de voz** para el motor Apple predeterminado.
6. Haz clic en el campo de práctica, usa el atajo predeterminado **Ctrl + Option + Space**, di una frase y confirma que el texto aparece.

Opcional: verifica el SHA-256 en las notas de la release antes de instalar. Guía completa: [Instalación](https://voicehotkey.pages.dev/docs/es/getting-started/install/).

**Primer uso:** Apple es el motor predeterminado y no necesita clave API. El nuevo motor de macOS 26+ puede necesitar recursos de idiomas; el modo habitual del antiguo Apple Speech puede usar servicios de Apple. Los modelos locales independientes requieren instalación previa. Las credenciales y los costes API de reconocimiento en la nube y funciones LLM dependen del proveedor elegido.

**Prueba y licencia:** El primer inicio activa 14 días de prueba Pro sin tarjeta; Free sigue disponible después. La primera activación Pro y los cambios de clave requieren verificación en línea. Una verificación permite hasta 30 días sin conexión y hasta 3 Mac por licencia personal. [Detalles de licencia](https://voicehotkey.pages.dev/docs/es/support/license/).

Consulta el manual: [Actualizaciones](https://voicehotkey.pages.dev/docs/es/advanced/updates/).

## Licencia y términos

VoiceHotkey es software comercial propietario; este repositorio no publica el código fuente de la aplicación. Descargar o instalar un binario no otorga derechos más allá de la licencia y los términos de uso del producto.
Consulta [LICENSE](LICENSE) · [NOTICE](NOTICE.md), además de [Planes](https://voicehotkey.pages.dev/docs/es/getting-started/plans/) y [Política de privacidad](https://voicehotkey.pages.dev/docs/es/privacy/policy/).

## Soporte

- Dudas y reporte de fallos → [Contacto](https://voicehotkey.pages.dev/docs/es/support/contact/)
- Enlaces rotos o archivos ausentes → [Discussions](https://github.com/yeahhe365/VoiceHotkey-releases/discussions)
- Este repositorio es **solo para distribución**; para solicitudes de funciones, utiliza los canales del manual
