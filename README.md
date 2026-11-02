# Stage Rotation — releases

This repository only holds the downloadable program for Stage Rotation (Sugar Shack).
The app checks here for new versions. A manager installs them from
**Settings → Updates** (or the yellow "Update ready" banner) on the DJ screen.

Each release has two files:

- `StageRotation.exe` — the program
- `StageRotation.exe.sha256` — its checksum; the app refuses a download that doesn't match

To install by hand: download `StageRotation.exe` from the latest release and replace the
old one in its folder (for example `C:\StageRotation`) while the app is shut down.
