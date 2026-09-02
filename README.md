# Allstar Remote Play — update channel

This repo is the auto-update source for **Allstar Remote Play**. It holds only
compiled release builds (`.exe`) and a `version.json` pointing at the latest one.

There is **no source code here** — the app is compiled to native machine code.

The app reads `version.json` on launch and offers the update if it's newer than
the running build.

## Publishing an update
1. Build the exe.
2. `gh release create vX.Y.Z "path/AllstarRemotePlay.exe#AllstarRemotePlay.exe" -t "vX.Y.Z" -n "notes"`
3. Bump `version` + `url` + `notes` in `version.json`, commit, push.
