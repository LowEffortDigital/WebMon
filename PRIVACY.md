# Privacy Policy — WebMon for macOS & Windows 11

**WebMon** (`com.loweffort.webmon`) is designed with a strict local-first privacy architecture:

1. **Zero External Telemetry or Analytics**: WebMon does not collect, transmit, or sell any analytics, browsing history, DOM snapshots, or usage telemetry.
2. **Local macOS Keychain Credential Storage**: All website credentials, passwords, API bearer tokens, and captured session cookies saved in the Auth Vault are stored locally on your Mac inside the macOS Keychain (`com.loweffort.webwidget.vault`) and are only sent to the matching website domains you explicitly configure.
3. **Direct WebKit Connections Only**: Network requests occur exclusively between your Mac's native `WKWebView` / `URLSession` and the website URLs you open or pin as widgets, plus optional GitHub Release update checks (`LowEffortDigital/WebMon`).
