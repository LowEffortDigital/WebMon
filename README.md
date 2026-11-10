# WebMon for macOS, iOS & Windows 11 (`WM`) — v2.2.0

**Interactive Website DOM Component Picker, Visual + Code JSON/XML Data Mapper, Resizable Desktop & iOS Home/Lock Screen Widgets, Intermittent Auto-Refresh & Local Keychain Credential Vault — by Low Effort Digital.**

`WebMon` (`com.loweffort.webmon`, formerly `WebWidget`) is a native Swift + SwiftUI + WebKit macOS, iOS (Home Screen, Lock Screen & StandBy), and Windows 11 WPF + WebView2 utility in the **Low Effort Digital** v2.2 suite alongside **PerfMon** (`PM`), **EventMon** (`EM`), and **VolMon** (`VM`).

---

## Key Capabilities

1. **Interactive Web Browser, Visual DOM Picker & JSON/XML Structured Data Mapper (`BrowserPickerTabView` / `StructuredDataMapperSheetView`)**
   - Browse any public or authenticated internal website, REST JSON endpoint (e.g., `https://api.github.com/rate_limit`), or XML/RSS feed in a full-featured WebKit browser.
   - Toggle **Select Components: ON** to hover and visually highlight HTML DOM elements (`<div>`, `<section>`, `<table>`, metric cards, charts) or automatically formatted JSON/XML `[data-wm-path]` field cards, and click/tap to add one or more components to your widget basket.
   - Open the **`{ } JSON / XML Mapper`** on macOS or iOS to browse flattened JSON/XML leaf nodes visually, click to assign any node as the **Target Value Path** (`$.resources.core.remaining`, `/rss/channel/item[0]/status`) or **Dynamic Label Path** (`$.resources.core.resource`, `/rss/channel/item[0]/title`), or edit raw JSON/XML code and custom value templates (`{{value}} / {{$.resources.core.limit}} req`) with live evaluation preview.
   - Includes a built-in interactive sandbox (`loweffort://dashboard-demo`) with live-updating telemetry and an interactive login portal for instant offline or online testing.

2. **Resizable Desktop Widgets with Intermittent Auto-Refresh (`ResizableWebComponentWidgetView`)**
   - Pin selected website components to your macOS desktop as borderless Liquid Glass HUD windows.
   - **Freely Resizable**: Drag the bottom-right resize grip (`WindowResizeGripView`), resize window edges, or pick quick size presets (`Compact`, `Standard`, `Wide`, `Tall`, `Large`), with per-widget zoom (`50%–200%`) and persistent size/position storage.
   - **Intermittent Refresh Scheduler**: Configure per-widget refresh intervals (`5s`, `15s`, `30s`, `1m`, `5m`, `15m`, up to `60m`) with **Soft DOM Poll (No Reload Flash)**, **In-Page Fetch Re-Run**, or **Full Page Reload**, plus DOM change detection and manual one-click sync.

3. **Sign-In & Locally Stored Credentials (`CredentialVaultManager`)**
   - Persistent `WKWebsiteDataStore.default()` session cookies shared between the interactive browser and all pinned desktop widgets.
   - Local **macOS Keychain Credential Vault** (`com.loweffort.webwidget.vault`) supporting:
     - **Form Login Auto-Fill** (React/Vue/DOM input event dispatch + optional auto-submit)
     - **HTTP Basic / Challenge Auth** (`URLSessionAuthChallengeDisposition`)
     - **Bearer Token & Custom HTTP Headers** (`Authorization`, `X-API-Key`)
     - **Captured Session Cookie Vault**

4. **Low Effort Suite Style Sync, 9 Themes & Menu Bar Designer**
   - **9 Studio Color Themes** (`Follow System`, `Dark Mode`, `Light Mode`, `Brand Purple`, `Hot Pink`, `Amber Gold`, `Cyber Cyan`, `Emerald Green`, `Monochrome`), custom accent swatches, and monogram switcher (`WM`, `WE`, `LE`).
   - **Cross-App Style Synchronization (`LowEffortThemeSyncManager`)**: One-click Pull/Push of themes, accents, monograms, HUD opacity, and window behaviours across `PerfMon`, `EventMon`, `VolMon`, and `WebMon`.
   - **8-Style Telemetry Card Gallery**: Switch any web widget between Live WebKit DOM rendering and 8 Low Effort Telemetry Card visualizations (`History Bars`, `Area Line`, `Horizontal Bar`, `Tachometer`, `Utilization Ring`, `Stat Tiles`, `Half Gauge`, `Signal Strip`).

---

## Building & Packaging

```bash
# Run unit tests
swift test

# Generate all 8 themed .icns bundles, build Release WebMon.app, and package WebMon.dmg
chmod +x Scripts/generate_icns.sh Scripts/build_app.sh Scripts/package_dmg.sh
./Scripts/generate_icns.sh
./Scripts/build_app.sh
./Scripts/package_dmg.sh
```
