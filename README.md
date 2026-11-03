# Stage Rotation — releases

This repository holds the downloadable program for Stage Rotation (Sugar Shack).

## Install

[Download StageRotationSetup.exe](https://github.com/fivealarmtech/rotation-releases/raw/main/StageRotationSetup.exe)
and run it. It installs Stage Rotation for the current Windows user (no administrator
password), adds it to the Start menu and desktop, and lists it in
**Settings → Apps → Installed apps** so it can be uninstalled there.

Windows may show "Windows protected your PC" because the program is unsigned:
click **More info → Run anyway**.

## Updates

The installed app checks this repository for new versions. A manager installs them from
**Settings → Updates** (or the yellow "Update ready" banner) on the DJ screen. Nothing
installs by itself.

Files:

- `StageRotationSetup.exe` — the installer (includes the newest program)
- `StageRotation.exe` — the newest program, used by the in-app updater
- `latest.json` — its version, what changed, and its SHA-256 checksum (the app refuses a download that doesn't match)

## Windows in Parallels on a Mac (iPads)

Parallels' normal "Shared Network" hides Windows behind the Mac, so iPads can't reach
Stage Rotation. Run the relay on the Mac: open **Terminal** and paste this one line:

```
curl -fL -o ~/StageRotationRelay https://github.com/fivealarmtech/rotation-releases/raw/main/mac/StageRotationRelay && chmod +x ~/StageRotationRelay && ~/StageRotationRelay
```

It finds Stage Rotation in Windows by itself and prints the address for the iPads (the Mac's
address). The first time, it asks whether to start by itself whenever the Mac starts (in the
background, no window to keep open). Otherwise keep the window open, and next time double-click
**Stage Rotation Relay** on the Desktop. Stage Rotation's Settings > iPads shows the address too.

To update the relay, paste the same line again. Other commands:
`~/StageRotationRelay --status`, `~/StageRotationRelay --autostart on|off`.
