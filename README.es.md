# VoiceHotkey Releases (instaladores)

[![Platform](https://img.shields.io/badge/platform-macOS%2014%2B-lightgrey.svg)](https://voicehotkey.pages.dev/)
[![Download](https://img.shields.io/badge/download-Releases-blue.svg)](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest)
[![Docs](https://img.shields.io/badge/docs-handbook-informational.svg)](https://voicehotkey.pages.dev/docs/es/)

**Idioma:** [简体中文](README.md) · [繁體中文](README.zh-Hant.md) · [English](README.en.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Deutsch](README.de.md) · Español

Repositorio **oficial de descarga / instaladores** de [VoiceHotkey](https://voicehotkey.pages.dev/).

> **Los instaladores se publican solo en [GitHub Releases](https://github.com/yeahhe365/VoiceHotkey-releases/releases).**  
> Este repo **no** sube `.dmg` / `.app` al historial de git.

## Sobre el producto

**Escritura por voz** en macOS: mantén (o pulsa) un atajo, habla y el texto se inserta en el cursor. Opcional: comandos de voz, posprocesado de texto, transcripción de archivos e historial en el dispositivo.

- **Sitio del producto:** [voicehotkey.pages.dev](https://voicehotkey.pages.dev/)
- **Manual de usuario:** [voicehotkey.pages.dev/docs](https://voicehotkey.pages.dev/docs/es/)
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

1. Abre [la última Release](https://github.com/yeahhe365/VoiceHotkey-releases/releases/latest).
2. Descarga `VoiceHotkey-X.Y.Z.dmg` (compilación Developer ID notariada cuando esté disponible).
3. Abre el DMG y arrastra **VoiceHotkey** a **Aplicaciones**.
4. Inicia desde `/Applications` (o `~/Applications`) y concede **Accesibilidad** y **Micrófono**.

Opcional: verifica el SHA-256 en las notas de la release. Guía completa: [Instalación](https://voicehotkey.pages.dev/docs/es/getting-started/install/).

## Qué debe estar aquí

| Activo | Propósito |
|--------|-----------|
| `VoiceHotkey-X.Y.Z.dmg` | Instalador macOS notariado (solo adjuntos de Release) |
| Sumas de verificación en las notas | Integridad de la descarga |
| (opcional) archivos públicos de Sparkle | Si no se alojan solo en GitHub Pages |

## Qué **no** debe estar aquí

- **Código fuente** de la app (no se mantiene en este repo)
- Secretos de firma, credenciales de notarización, clave **privada** de Sparkle
- Commits de git con `.dmg` / `.app` grandes (solo **activos de Release**)

## Versionado

- Etiqueta: `vX.Y.Z` (p. ej. `v0.9.0`)
- Nombre del archivo: `VoiceHotkey-X.Y.Z.dmg`
- Alineado con `CFBundleShortVersionString` del producto

URL directa de descarga:

```text
https://github.com/yeahhe365/VoiceHotkey-releases/releases/download/vX.Y.Z/VoiceHotkey-X.Y.Z.dmg
```

## Flujo para mantenedores

Compila y notaría en el árbol fuente, luego publica aquí:

```bash
export VH_SIGN_IDENTITY="Developer ID Application: …"
export VH_NOTARY_PROFILE=VH_NOTARY
make release-dmg

bash scripts/publish-release.sh
```

La base del appcast de Sparkle debe apuntar a este repo:

```bash
VH_UPDATE_BASE_URL=https://github.com/yeahhe365/VoiceHotkey-releases/releases/download/v0.9.0 \
  make appcast
```

Ver manual: [Actualizaciones](https://voicehotkey.pages.dev/docs/es/advanced/updates/).

## Licencia y términos

VoiceHotkey es software comercial propietario. Descargar el instalador no otorga derechos más allá de la licencia / términos del producto.  
Ver [LICENSE](LICENSE) · [NOTICE](NOTICE.md), [Planes](https://voicehotkey.pages.dev/docs/es/getting-started/plans/), [Privacidad](https://voicehotkey.pages.dev/docs/es/privacy/policy/).

## Soporte

- Errores y uso → [Contacto](https://voicehotkey.pages.dev/docs/es/support/contact/)
- Enlaces rotos / assets faltantes → [Discussions](https://github.com/yeahhe365/VoiceHotkey-releases/discussions)
- Este repo es solo de **distribución**; para funciones nuevas usa los canales del manual
