# Universal Downloader — Releases

This is the public release repository for **Universal Downloader**.

The Android source code is kept in the private [source repository](https://github.com/shambik/universal-downloader). This repository contains only APKs attached to GitHub Releases, so users can download the app without accessing the protected source code.

## Install

1. Open [the latest release](../../releases/latest).
2. Download the APK matching the device architecture.
3. Open it on Android and allow installation from the browser or file manager when prompted.

## APK variants

| File | Use |
| --- | --- |
| `app-family-arm64-v8a-release.apk` | Recommended for most modern Android phones. |
| `app-family-armeabi-v7a-release.apk` | Older 32-bit ARM phones. |
| `app-family-x86_64-release.apk` | x86_64 Android devices and emulators. |
| `app-family-universal-release.apk` | Larger fallback that supports every architecture included by the app. |

If you are unsure which APK the device needs, use the Universal APK. The in-app updater also uses it when it cannot find a compatible architecture-specific file.

## Release signing

Every production APK must be built by the signed-build workflow in the private source repository. Android only installs an APK as an update when its package name and signing certificate match the installed app.

The approved release certificate fingerprints are:

- SHA-1: `18:DB:D5:91:22:63:A5:0D:4E:19:8E:2B:98:F5:5D:FE:99:EB:CD:0D`
- SHA-256: `6F:5C:AD:EC:D0:B3:C5:3E:C2:99:89:FE:98:40:24:0C:5C:50:DE:68:3D:6C:E2:B0:90:32:C3:E9:E2:E6:C8:17`

Do not create a new signing key for later versions. Losing or replacing the permanent key prevents existing users from installing those versions as updates. The private key and its passwords must never be committed to this public repository.

Devices currently running a debug-signed APK must uninstall it once before installing the first release-signed APK. After that one-time migration, future APKs signed with the approved release key can update in place.
