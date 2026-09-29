# Tiuvald

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-purple.svg)](LICENSE)
[![Platform: Windows](https://img.shields.io/badge/Platform-Windows%2010%20%2F%2011-purple.svg)](https://microsoft.com/windows)
[![Go](https://img.shields.io/badge/Backend-Go-purple.svg)](https://golang.org)
[![Svelte](https://img.shields.io/badge/Frontend-Svelte-purple.svg)](https://svelte.dev)
[![Crowdin Translate](https://img.shields.io/badge/Crowdin-Tiuvald-purple.svg)](https://crowdin.com/project/tiuvald)

> **Tiuvald** (*Old Norse: Tíu (Ten) + Valdr (Ruler)*) is a lightweight, performant 10-foot TV launcher shell for Windows. Built with Go and Svelte, it serves as a modern shell replacement designed to transform Windows into a lightning-fast, console-like living-room experience without the overhead and bloat of traditional web browsers or heavy runtimes.

---

## Key Features

- **Zero Bloat & High Performance:** Powered by a lean Go backend and a responsive Svelte (TypeScript) frontend. Starts up in milliseconds with minimal RAM usage.
- **Genuine 10-Foot Shell Experience:** Automatically replaces `explorer.exe` as the Windows shell, hiding the taskbar and desktop elements while allowing manual access to File Explorer and Windows Settings when needed.
- **Deep Controller Integration & Navigation:**
  - Designed from the ground up for D-pad and gamepad navigation with smooth focus-driven animations and visible focus rings.
  - Native controller shortcuts to seamlessly switch apps or return to the dashboard.
- **Universal ‘Watch Next’ Hub:**
  - Local integration with **Jellyfin** via direct REST APIs.
  - Optional **Trakt.tv** synchronisation for a unified watch-state-aware 'Continue Watching' row.
- **Modular Add-on System:** Expandable architecture allowing custom add-ons and apps (such as Jellyfin, VLC, or a tailored 10-foot browser) that automatically inherit the system's active theme and glass styling.
- **Streaming & Kiosk Apps:** Quick launching for streaming services (YouTube TV, Netflix, etc.) via kiosk modes with tailored controller-to-cursor handling.
- **Integrated System Settings:** Built-in Google TV-style settings panel for display, sound, network (Wi-Fi/Ethernet), Bluetooth, and controller configurations.
- **Fully Customisable Themes & i18n:** Dynamic ambient gradients derived from content artwork, variable font typography, and structured localization support.

---

## Architecture

|               |           TIUVALD CORE            |               |
|-----------------|:-----------------------------:|-----------------|
|   Input Daemon  |         Shell & Wails         |   Media Hub     |
|  • Gamepad D-Pad|     • Shell Replacement       |  • Jellyfin     |
|  • Focus Store  |     • Add-on Manager          |  • Trakt.tv     |
|                 |     • System Settings API     |  • Deep Links   |
|        ↪        |               ⬇               |        ↩        |
|               |      Svelte / TypeScript      |                 |
|               |  HTML5 / CSS (Backdrop Blur)  |                 |

---

## Building from Source

### Requirements
- Windows 10 / 11
- [Go](https://golang.org/) (latest stable version)
- [Node.js](https://nodejs.org/) & npm
- [Wails CLI](https://wails.io/) (`go install github.com/wailsapp/wails/v2/cmd/wails@latest`)

# Clone the repository
```
git clone [https://github.com/solivagantstudios/Tiuvald.git](https://github.com/solivagantstudios/Tiuvald.git)
cd Tiuvald
```
### Run in live development mode
```
wails dev
```

### Build production executable
```
wails build
```

## Themes & Design Assets
Tiuvald will be released with it's own theme. The theme will be heavily inspired by the current google tv launcher.
However there will be no links to Google itself, the fonts and symbols are included in the package and due to that no contact with Google's servers will be made.
Users can make there own themes, so everything can be tailored to their own heart's content.

## Contributions & Community
Contributions are very welcome! Whether it’s Go backend optimizations, Svelte UI components, new controller profiles, community themes or translations: feel free to open an issue or a pull request.

## AI Co-Creation Disclaimer
This project has been realised through a hybrid collaboration between human vision/architecture (Solivagant Studios) and advanced AI coding assistance. The functional specifications, hardware integration goals and architectural choices are human-led; AI models are used as powerful accelerators for implementing backend logic, UI components, protocol interoperability and documentation. All generated code is actively tested, reviewed and optimised for maximum efficiency and security.

## Design & Assets

Tiuvald's user interface is crafted with a clean, zero-bloat design philosophy tailored for 10-foot TV viewing. The following official Google assets are used in the default theme:

*   **Typography:** [Google Sans Flex](https://fonts.google.com) (specifically optimized via variable font weights for optimal readability from a couch distance). Licensed under the [SIL Open Font License (OFL)](https://scripts.sil.org/OFL).
*   **Icons:** [Material Symbols](https://fonts.google.com/icons) (Light and Light Filled weights). Licensed under the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0).

Full copyright and license notices for these assets will be included in the repository when the first version will be committed.
