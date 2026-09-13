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
| `app-family-arm64-v8a-debug.apk` | Recommended for most modern Android phones. |
| `app-family-armeabi-v7a-debug.apk` | Older 32-bit ARM phones. |
| `app-family-x86_64-debug.apk` | x86_64 Android devices and emulators. |
| `app-family-universal-debug.apk` | Universal fallback for unknown architectures. |

The current release is a family test build with the Downloader and local media editor. Future production builds should use the release signing key before being distributed as updates.
