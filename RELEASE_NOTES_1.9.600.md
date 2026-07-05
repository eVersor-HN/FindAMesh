## FAM — Find A Mesh 1.9.600

Offline-first, end-to-end-encrypted P2P / LAN + Bluetooth-mesh messenger for Android.
**Proprietary / closed source** — © 2026 Marco Aurelio Fattizzo. See the LICENSE and DISCLAIMER in this repository.

**Android 8.0 (API 26)+** • sideload the APK below • **verify before installing** (see below and [VERIFY.md](VERIFY.md)).

### What's new in 1.9.600
UI polish:
- The **"Allow autostart"** row (Settings → Background & Alarms, shown on Xiaomi/REDMAGIC/Oppo & co.) is now translated in all 16 app languages — it previously always appeared in German.
- **Bigger tab buttons** in the radial quick-navigation menu that opens from the float button (icons and labels scale up with them).

### Verify authenticity (do this before installing)
Only this file, signed by the author, is genuine.

| Field | Value |
|---|---|
| File | `FindAMesh-1.9.600-release.apk` |
| **SHA-256 (APK file)** | `707edeb8dcea1e14339712e503c394cd65f19b343af3c01f75490ba9ad0825a2` |
| **SHA-256 (signing certificate)** | `9A:A1:8D:62:93:C7:89:50:A3:D1:25:53:F5:0C:5F:CE:9A:68:69:60:EC:4C:4F:56:6E:9F:8C:1A:93:13:DF:8D` |
| Signing subject (reference only) | `CN=FindAMesh, OU=FindAMesh, O=eVersor-HN, L=, ST=, C=DE` |

- File checksum — PowerShell: `Get-FileHash .\FindAMesh-1.9.600-release.apk -Algorithm SHA256` · Linux: `sha256sum FindAMesh-1.9.600-release.apk`
- Certificate — `apksigner verify --print-certs FindAMesh-1.9.600-release.apk`, or read it in-app under **Settings → System → "ÜBER & ECHTHEIT"**.

If a value does not match, the app has been altered — **do not use it.** Full instructions: [VERIFY.md](VERIFY.md).
