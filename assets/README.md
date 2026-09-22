# Authentic PixelPal media

Current capture set: [Windows v2.3.0 source run, 2026-09-22](windows-v2.3.0-20260922/capture-manifest.json).

The app was run from the unchanged source commit `a3f6606444a3a3a37a2360fbb5c3689e8eb003c8`, matching the public v2.3.0 release manifest, with Electron 43.6.0 on Windows 11 build 22631. A separate empty profile was used. The normal renderer prebuild was performed; the final capture used no smoke mode, mock provider or patched UI. This is a source-run presentation capture, not an installer or full product regression test.

| File | What it actually shows |
|---|---|
| `01-companion.png` | Real pet and AI / Workstation / radio quick actions |
| `02-ai-unconfigured.png` | AI panel with the provider and experience mode not configured/enabled |
| `03-workstation.png` | A real saved reminder and Memo, explicitly labelled as demo inputs |
| `04-radio-hub.png` | The actual FlowPal / Pal FM / PixelWave entry panel |
| `05-pal-fm.png` | Initial Pal FM interface; no account, track or DJ session active |
| `pixelpal-hero.png` | 1440×840 composition with the unchanged AI/companion capture, product name and short copy |
| `pixelpal-social-preview.png` | 1200×630 social preview using that same real capture |
| `pixelpal-walkthrough.mp4` | Approximately 13 seconds of continuous real navigation and Memo entry; silent H.264 |
| `pixelpal-walkthrough.gif` | Smaller-dimension looping alternative; MP4 preserves more detail |

## Capture and editing boundaries

The transparent Electron product window was captured without the surrounding desktop. Transparent outer margins were cropped and a neutral background was added. Hero/social graphics add title text outside the product capture. Video uses one constant crop enclosing all captured visible UI, proportionate scaling and original timing. No product control, status, message or response was redrawn, synthesized or hidden. Full provenance and hashes are in the manifest; raw capture evidence is retained locally by the maintainer.

No private source files, API keys, provider configuration, personal files, private prompts or music account data are included. The pre-existing installed `2.3.0-candidate.2` app was not used for stable-version media. All five images are Windows captures and do not imply macOS parity.

## Still worth capturing later

- A real, harmless supported Agent task with progress and final outcome, using a separately authorized provider configuration.
- Pal FM playback / DJ / mini bar with rights-cleared audio and a non-sensitive account view.
- A separate macOS v2.0.0 capture, labelled with its own version and validation limits.

These gaps are not filled with mockups or generated UI. They do not block the current truthful product/navigation walkthrough.
