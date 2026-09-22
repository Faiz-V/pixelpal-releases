# PixelPal

A desktop companion that brings a pet, AI assistance, a workstation and music into one personal workspace.

中文简介：PixelPal 是将桌宠、AI、工作站和音乐结合在一起的桌面产品；本仓库提供官方介绍、安装包和反馈入口。

**[Download](#download) · [Product & setup guide](https://play.levius.com.cn/pixelpal/) · [Try PixelPal Play](https://play.levius.com.cn/) · [Feedback](https://github.com/Faiz-V/pixelpal-releases/issues)**

## Product demo

Explore the [desktop product page](https://play.levius.com.cn/pixelpal/) for an overview and configuration instructions. The separate [PixelPal Play web experience](https://play.levius.com.cn/) can be opened in a browser without installing the desktop app.

Current-version desktop screenshots and a short recorded walkthrough are still to be added. The [media checklist](assets/README.md) describes the real captures needed; no generated product screenshots are used here.

## Core experiences

- **Desktop Companion** — an animated desktop pet and a personal desktop panel.
- **AI** — connect your own supported model provider. Windows v2.3.0 retains Memo and bounded document/OCR summaries; availability depends on your configuration and provider.
- **Workstation / Agent Experience** — on Windows v2.3.0, combine supported PixelPal actions into a goal. Agent Activity shows progress, cancellation and completed, partial or failed outcomes. Tidy requires confirmation. This is bounded in-app assistance, not arbitrary Windows or file control.
- **Pal FM / DJ** — music playback with your own supported sources, plus optional voice transitions through your Fish Audio configuration. Pal FM playback and FlowPal source management are distinct. Session Music Policy can be queried, paused or cancelled and yields to manual actions; long-term policies and named routines are not included.
- **PixelPal Play** — a separate browser multiplayer experience, linked from the product ecosystem. It uses an online room service; it is not an offline desktop feature or a source release in this repository.

## Windows and macOS support

Release inventory checked on **2026-09-22**. Versions differ by platform.

| Platform | Published download | Evidence and limits |
|---|---|---|
| Windows x64 | **v2.3.0** | Current stable Windows release. Published release evidence covers Agent Experience and the retained Windows security/runtime work. Unsigned installer. |
| macOS Apple Silicon (arm64) | **v2.0.0 — Previous Stable** | Existing DMG. Agent Foundation and Agent Experience are **NOT VALIDATED**; Security Modernization is **NOT YET VALIDATED** on macOS. Ad-hoc integrity seal, no Developer ID, not notarized. |
| Intel Mac / Linux / other architectures | No asset listed | No compatible build is distributed here. |

Do not assume Windows feature parity on macOS. The v2.3.0 release did not produce or replace a macOS binary.

## Download

| Platform | Installer | Release notes and integrity evidence |
|---|---|---|
| Windows x64 | [PixelPal-Windows-x64-Setup.exe · v2.3.0](https://github.com/Faiz-V/pixelpal-releases/releases/download/v2.3.0/PixelPal-Windows-x64-Setup.exe) | [Release](https://github.com/Faiz-V/pixelpal-releases/releases/tag/v2.3.0) · [SHA256SUMS](https://github.com/Faiz-V/pixelpal-releases/releases/download/v2.3.0/SHA256SUMS.txt) · [Manifest](https://github.com/Faiz-V/pixelpal-releases/releases/download/v2.3.0/release-manifest.json) |
| macOS arm64 | [PixelPal-macOS-arm64.dmg · v2.0.0](https://github.com/Faiz-V/pixelpal-releases/releases/download/v2.0.0/PixelPal-macOS-arm64.dmg) | [Release](https://github.com/Faiz-V/pixelpal-releases/releases/tag/v2.0.0) · [SHA256SUMS](https://github.com/Faiz-V/pixelpal-releases/releases/download/v2.0.0/SHA256SUMS.txt) · [Manifest](https://github.com/Faiz-V/pixelpal-releases/releases/download/v2.0.0/release-manifest.json) |

These links are version-pinned so the macOS button does not point at a Windows-only latest release. For older builds, use [all Releases](https://github.com/Faiz-V/pixelpal-releases/releases). GitHub's automatically generated “Source code” archives contain this repository's documentation, not the PixelPal application source.

## Live web experience and configuration

- [PixelPal Play](https://play.levius.com.cn/) is the live browser entry point. Room availability depends on its online service.
- [Desktop download and configuration guide](https://play.levius.com.cn/pixelpal/#setup-guides) explains AI provider settings, music login and DJ setup.
- Configure credentials inside the installed desktop app. This repository and the web product page do not provide an API-key upload form or a hosted API service.

AI uses your own provider account and API key. DJ is optional and uses your own Fish Audio key and authorized Voice Model ID. Music service access depends on your own account and content availability. Provider charges, quotas and outages are separate from the desktop download.

## Installation

1. Download the asset for your platform and its matching `SHA256SUMS.txt`.
2. Check the downloaded file before running it:

   Windows PowerShell:

   ```powershell
   Get-FileHash .\PixelPal-Windows-x64-Setup.exe -Algorithm SHA256
   ```

   macOS Terminal:

   ```sh
   shasum -a 256 PixelPal-macOS-arm64.dmg
   ```

3. Compare the full hash with the corresponding filename in the sums file. A checksum checks file integrity; it is not a publisher signature or a malware assessment.
4. On Windows, run the installer and follow its prompts. On macOS, open the DMG and install the app. The [installation guide](https://play.levius.com.cn/pixelpal/) explains the unsigned-build prompts. Any decision to allow an unsigned app stays with you; do not disable operating-system protections globally.
5. Open PixelPal, then configure optional AI, music and DJ services as needed. AI or DJ credentials are not required just to launch the desktop companion.

## Safety and privacy

Windows v2.3.0's release notes describe sandboxed renderers, narrowly validated capabilities, bounded requests/streams and DPAPI-protected credentials. These Windows guarantees must not be applied to the older macOS build.

AI prompts and selected document content may be sent to the provider you configure. Music login/playback and DJ synthesis involve their respective external services. PixelPal Play exchanges room/game data with its server. The product is therefore not wholly offline, and provider data policies still apply.

Never post API keys, cookies, session files, local configuration, personal documents or unredacted logs in Issues. Review screenshots before sharing. This repository distributes binaries and does not collect credentials through configuration forms.

## Current version differences and verification

[Windows v2.3.0 release notes](https://github.com/Faiz-V/pixelpal-releases/releases/tag/v2.3.0) describe Agent Experience on top of Agent Foundation, Memo, document/OCR summaries, music sources, FM/DJ, volume, background playback and mini-bar interaction. General Windows automation, long-term policy and named routines remain outside this release.

The release includes a [regression summary](https://github.com/Faiz-V/pixelpal-releases/releases/download/v2.3.0/release-regression-summary.json) and [installation gate evidence](https://github.com/Faiz-V/pixelpal-releases/releases/download/v2.3.0/windows-install-gate.json). These are published release records, not a claim that every platform or external provider was re-tested during this documentation update. A downloadable asset alone does not establish feature parity.

## Feedback / Issues

[Open an issue](https://github.com/Faiz-V/pixelpal-releases/issues) with your OS/architecture, PixelPal version, steps, expected result and actual result. Include a redacted screenshot when useful. Do not attach credentials, whole profiles or private source code.

This is the official public product and binary distribution repository. Source contributions and build-from-source instructions are not offered here; documentation corrections are welcome as pull requests.

## Source Code Status

**PixelPal source code is maintained separately and is currently not distributed through this repository.**

Public downloads do not make this an open-source repository. No new license or permission to redistribute third-party code, artwork, voices or music is granted by this README.
