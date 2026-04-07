# Heeph Launcher Updates

This repository hosts the **client update artifacts** via **GitHub Releases**.

## How to publish an update

1. Put the client files into `payload/`:
   - `payload/heeph-1.8.9.jar`
   - `payload/heeph-1.8.9.json`

2. Create and push a tag (the tag name becomes the manifest `version`):
   - Example tag: `2026.04.06-1`

3. GitHub Actions will build:
   - `heeph-1.8.9.zip`
   - `manifest.json` (with correct SHA256)

and upload both as Release assets.

## Launcher configuration

Point `updateManifestUrl` to the release asset:

`https://github.com/mcypreste/heeph-launcher-updates/releases/download/<TAG>/manifest.json`
