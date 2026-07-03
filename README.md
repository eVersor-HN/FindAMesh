<div align="center">

# FAM — Find A Mesh

**Offline-first, end-to-end-encrypted P2P / LAN + Bluetooth-mesh messenger for Android.**
No central server. No account. No cloud. Your data stays on your devices.

Copyright © 2026 **Marco Aurelio Fattizzo** — All rights reserved.
**Proprietary / closed source.** See [LICENSE](LICENSE.md) and [DISCLAIMER](DISCLAIMER.md).

**Official releases:** https://github.com/eVersor-HN/FindAMesh/releases

</div>

---

> [!IMPORTANT]
> This repository distributes the **official, ready-to-install app only** (this README, the
> license, the disclaimer and the signed APK attached to each GitHub Release).
> The source code is **not** public. Only builds published here, by the author, are genuine.
> Always [verify what you downloaded](#verify-that-your-download-is-the-original) before installing.

## What it is

FAM (Find A Mesh) is a resilient communication app for situations where the normal internet is
unavailable, unreliable, or undesirable — festivals, remote areas, travel, emergencies, or simply
private local communication. Devices find each other directly over Wi-Fi/LAN, a phone hotspot, or a
Bluetooth-LE mesh, and exchange **end-to-end-encrypted** messages, images, files and locations
**without any central server**.

Highlights:

- **No server, no account, no tracking.** Everything runs peer-to-peer on the local network / mesh.
- **End-to-end encryption** for direct messages, images and files.
- **Device pairing** with a visual comparison code (SAS) to defeat man-in-the-middle attacks.
- **Offline by design** — the app blocks non-local network destinations.
- **Extras:** local radar/pins, SOS & rally, group circles, diary, documents, deadlines, timers, a
  built-in mini-game, and more.

## Requirements

- **Android 8.0 (API 26)** or newer.
- Installation from outside Google Play must be allowed on the device
  ("Install unknown apps" for your browser / file manager).

## Install

1. Open **[Releases](https://github.com/eVersor-HN/FindAMesh/releases)** and download the latest
   `FindAMesh-<version>-release.apk`.
2. **Verify it is the original** — see the next section. Do **not** skip this.
3. Open the downloaded APK and confirm the installation.

## Verify that your download is the original

Only builds published in this repository's Releases, signed by the author, are genuine. Two
independent checks are provided; ideally do both. The authoritative values are published in the
release notes of **each** release (and summarised in [VERIFY.md](VERIFY.md)).

**1. APK file checksum (SHA-256).** Compute the hash of the file you downloaded and compare it to the
value in the release notes.

- Windows (PowerShell): `Get-FileHash .\FindAMesh-<version>-release.apk -Algorithm SHA256`
- Linux/macOS: `sha256sum FindAMesh-<version>-release.apk`

**2. Signing-certificate fingerprint (SHA-256).** This proves the APK was signed with the author's
key even if the file was renamed or repackaged. It is also shown **inside the app** under
**Settings → System → "ÜBER & ECHTHEIT" (About & Authenticity)**, so you can compare the installed
app against the published fingerprint at any time.

- With Android build-tools: `apksigner verify --print-certs FindAMesh-<version>-release.apk`
- Or read it in-app (Settings → System) and compare.

If either value does **not** match the one published here, the app has been altered — **do not use it.**

## Author & contact

Created and maintained by **Marco Aurelio Fattizzo**.
Official distribution: https://github.com/eVersor-HN/FindAMesh

## License

**Proprietary. All rights reserved.** You may use the app privately and commercially, but you may
**not** modify, reverse-engineer, sell, sublicense or redistribute it. Full terms:
[LICENSE.md](LICENSE.md). Warranty and liability: [DISCLAIMER.md](DISCLAIMER.md).
