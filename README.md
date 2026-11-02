# Stage Rotation — releases

This repository only holds the downloadable program for Stage Rotation (Sugar Shack).
The app checks here for new versions. A manager installs them from
**Settings → Updates** (or the yellow "Update ready" banner) on the DJ screen.

Files:

- `StageRotation.exe` — the newest program
- `latest.json` — its version, what changed, and its SHA-256 checksum (the app refuses a download that doesn't match)

To install by hand: [download StageRotation.exe](https://github.com/fivealarmtech/rotation-releases/raw/main/StageRotation.exe)
and replace the old one in its folder (for example `C:\StageRotation`) while the app is shut down.
