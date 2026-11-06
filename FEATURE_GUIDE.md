# WebMon Feature Guide

## 1. Selecting Website Components in the Browser
1. Open the **Browser & Picker** tab (`globe.desk.fill`).
2. Enter any website URL (or pick a preset such as `loweffort://dashboard-demo`, `https://www.githubstatus.com`, or `http://localhost:3000`).
3. If the website requires authentication, switch to **Browse / Sign-In Mode** to sign in interactively, or click **Auto-Fill Login** to inject credentials from your local macOS Keychain Vault.
4. Switch **Select Components: ON** and hover over any card, chart, table, or metric on the page. Click one or more DOM elements to add them to the **Selected Components** basket on the right.
5. Choose your **Intermittent Refresh Interval** (`5s` to `15m+`), initial window size preset, and click **Create & Pin Resizable Widget**.

## 2. Resizing & Refreshing Desktop Widgets
- Drag the header bar of any floating desktop widget to reposition it on screen.
- Drag the bottom-right corner grip (`WindowResizeGripView`) or use the size preset menu to resize the widget to any dimensions.
- Adjust page zoom (`−` / `+`) or toggle between **Live WebKit DOM View** and **8-Style Telemetry Card View** directly from the widget header.
- Widgets refresh intermittently according to their schedule, recording latency and DOM content diffs in the **Refresh & Diff Log** tab.

## 3. Local Sign-In & Keychain Credential Vault
- Open the **Sign-In & Auth Vault** tab (`key.fill`) to create or edit credential profiles stored locally in the macOS Keychain (`com.loweffort.webwidget.vault`).
- Supported authentication modes:
  - **Form Sign-In Auto-Fill**: Automatically populates username/password selectors and optionally submits login forms.
  - **HTTP Basic / Challenge Auth**: Automatically answers `WKNavigationDelegate` HTTP Basic/Digest challenges.
  - **Bearer Token / Custom Header**: Injects `Authorization: Bearer ...` or custom API headers into widget requests.
  - **Stored Session Cookies**: Captures live signed-in cookies from `WKHTTPCookieStore` and re-injects them before widget refreshes.

## 4. Cross-App Low Effort Suite Synchronization
- Open **Settings & Sync** (`slider.horizontal.3`) to sync your active Studio Theme, custom accent swatch, monogram role (`WM`/`WE`/`LE`), and HUD window settings with **PerfMon**, **EventMon**, and **VolMon**.
