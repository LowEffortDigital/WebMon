# WebMon for macOS, iOS/iPadOS & Windows 11 (`WM`) — v2.2.1

**Interactive Website DOM Component Picker, Visual + Code JSON/XML Data Mapper, 12 Adaptive Telemetry Card Styles, Resizable Desktop & iPhone/iPad Home/Lock Screen Widgets, Intermittent Auto-Refresh & Local Keychain Credential Vault — by Low Effort Digital.**

`WebMon` (`com.loweffort.webmon`, formerly `WebWidget`) is a native Swift + SwiftUI + WebKit macOS, iOS/iPadOS (Home Screen, Lock Screen, StandBy & ExtraLarge iPad widgets), and Windows 11 WPF + WebView2 utility in the **Low Effort Digital** v2.2.1 suite alongside **PerfMon** (`PM`), **EventMon** (`EM`), and **VolMon** (`VM`).

---

## Key Capabilities

1. **Interactive Web Browser, Visual DOM Picker & JSON/XML Structured Data Mapper (`BrowserPickerTabView` / `StructuredDataMapperSheetView`)**
   - Browse any public or authenticated internal website, REST JSON endpoint (e.g., `https://api.github.com/rate_limit`), or XML/RSS feed in a full-featured WebKit browser.
   - Toggle **Select Components: ON** to hover and visually highlight HTML DOM elements (`<div>`, `<section>`, `<table>`, metric cards, charts) or automatically formatted JSON/XML `[data-wm-path]` field cards, and click/tap to add one or more components to your widget basket.
   - Open the **`{ } JSON / XML Mapper`** on macOS or iOS/iPadOS to browse flattened JSON/XML leaf nodes visually, click to assign any node as the **Target Value Path** (`$.resources.core.remaining`, `/rss/channel/item[0]/status`) or **Dynamic Label Path** (`$.resources.core.resource`, `/rss/channel/item[0]/title`), or edit raw JSON/XML code and custom value templates (`{{value}} / {{$.resources.core.limit}} req`) with live evaluation preview.
   - Compose custom widget items with **Static Text**, **Environment Variables** (`$USER`, `$HOST`, `$SHELL`, `$PWD`), and **Live Date/Time Presets**, complete with per-item typography formatting (Font Size, Weight, Italic/Monospace Style, Design, and Custom Color).
   - Includes a built-in interactive sandbox (`loweffort://dashboard-demo`) with live-updating telemetry and an interactive login portal for instant offline or online testing.

2. **12 Adaptive Telemetry Card Styles, Smart Data Dissolve & Resizable Desktop Widgets (`ResizableWebComponentWidgetView`)**
   - Pin selected website components to your macOS desktop as borderless Liquid Glass HUD windows or to your iPhone/iPad Home & Lock Screen (including ExtraLarge iPad widgets on iOS 16.0+).
   - **12 Adaptive Telemetry Card Styles**: Switch seamlessly between Live WebKit DOM rendering and 12 native SwiftUI Telemetry Card styles (`History Bars`, `Area Line`, `Horizontal Bar`, `Tachometer`, `Utilization Ring`, `Stat Tiles`, `Half Gauge`, `Signal Strip`, `Delta Comparison`, `Hero Center Metric`, `Key-Value Table`, and `Monospace Terminal`).
   - **Smart Data Dissolve Engine**: Automatically strips raw HTML tag noise, dissolves `Label : Value` pairs, parses duration-aware numeric metrics and units, and auto-heals multi-component structured selectors.
   - **Freely Resizable & Drag-Anchored**: Drag via the widget header bar or dedicated cross-arrow move icon (`NativeWindowDragHandle`), drag the bottom-right resize grip (`WindowResizeGripView`), or pick quick size presets (`Compact`, `Standard`, `Wide`, `Tall`, `Large`), with per-widget zoom (`50%–200%`) and active-screen multi-display position memory.
   - **Intermittent Refresh Scheduler**: Configure per-widget refresh intervals (`5s`, `15s`, `30s`, `1m`, `5m`, `15m`, up to `60m`) with **Soft DOM Poll (No Reload Flash)**, **In-Page Fetch Re-Run**, or **Full Page Reload**, SPA route awareness, 10–15s DOM settle protection, and manual one-click sync.

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
