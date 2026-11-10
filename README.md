# DreamWeaver desktop (offline)

Windows app (Tauri + WebView2) with DreamWeaver bundled inside the exe.
It makes no network requests and works with no internet connection.

1. Push this folder to a GitHub repo (new repo, files at the root).
2. Actions tab -> "Build Windows exe" -> Run workflow -> wait ~5-8 min.
3. Download the artifact `DreamWeaver-exe`, unzip, run `dream-weaver.exe`.

Notes
- The page is baked into the exe. To change DreamWeaver, replace `dist/index.html`
  and rebuild (it does NOT update itself like a live-site wrapper would).
- Needs the Microsoft WebView2 runtime, which comes with Windows 11 and up-to-date Windows 10.
- Saved data (settings, completed tasks, etc.) is stored on this PC in
  %LOCALAPPDATA%\com.dreamweaver.desktop. Deleting that folder resets the app.
