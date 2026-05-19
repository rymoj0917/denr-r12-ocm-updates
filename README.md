# DENR R12 One Control Map — OTA Updates

This repository hosts the over-the-air (OTA) update manifest for the **DENR R12 One Control Map (OCM)** Android app.

## How It Works

The app checks `version.json` on every startup. If a newer version is detected, users are prompted to download and install the update automatically — no Play Store needed.

## Files

| File | Description |
|------|-------------|
| `version.json` | Update manifest — edit this to trigger an update |
| `README.md` | This file |

## Releasing a New Version

1. Build the Release APK in Visual Studio:
   - `Build → Archive → Distribute → Ad Hoc → Save`
2. Upload the APK to the server:
   ```
   https://pscis.penrosocot.com/PSC_OCM/updates/OCM_MAUI.apk
   ```
3. Edit `version.json` in this repo — bump the version number:
 
4. Users open the app → update prompt appears automatically ✅

## Version Fields

| Field | Description |
|-------|-------------|
| `Version` | New version number (must be higher than current) |
| `DownloadUrl` | Direct link to the APK file |
| `ReleaseNotes` | What changed — shown to users in the prompt |
| `IsForced` | `true` = users cannot skip the update |
| `ReleasedAt` | Release date (informational only) |

## Current Version

See `version.json` for the latest released version.

---

**DENR Region XII — PENRO South Cotabato**  
Department of Environment and Natural Resources  
Developer: Jomyr H. Flores — ISA II / GIS Developer
