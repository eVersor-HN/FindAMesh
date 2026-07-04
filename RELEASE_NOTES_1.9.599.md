## FAM — Find A Mesh 1.9.599

Offline-first, end-to-end-encrypted P2P / LAN + Bluetooth-mesh messenger for Android.
**Proprietary / closed source** — © 2026 Marco Aurelio Fattizzo. See the LICENSE and DISCLAIMER in this repository.

**Android 8.0 (API 26)+** • sideload the APK below • **verify before installing** (see below and [VERIFY.md](VERIFY.md)).

### What's new in 1.9.599
Security & stability hardening:
- Closed several network hardening gaps (redirect/SSRF guard on all local HTTP calls).
- Bounded resource use in the direct-message file transfer path (DoS hardening).
- Timer alarm holds a wake lock so it keeps ringing under power-save (Doze) and can show over the lock screen (on Android 14+, allow the app's full-screen-intent permission if the system asks); fixed a notification-id clash with SOS.
- Guard (microphone) service made robust against restarts and missing permission.
- Stronger release obfuscation; added an in-app **About & Authenticity** section (Settings → System) showing the signing fingerprint.

### Verify authenticity (do this before installing)
Only this file, signed by the author, is genuine.

| Field | Value |
|---|---|
| File | `FindAMesh-1.9.599-release.apk` |
| **SHA-256 (APK file)** | `83fe18d1e995ba833755b8d3789aa33b3c99f0d46379f0a22915d32d31ddac31` |
| **SHA-256 (signing certificate)** | `9A:A1:8D:62:93:C7:89:50:A3:D1:25:53:F5:0C:5F:CE:9A:68:69:60:EC:4C:4F:56:6E:9F:8C:1A:93:13:DF:8D` |
| Signing subject (reference only) | `CN=FindAMesh, OU=FindAMesh, O=eVersor-HN, L=, ST=, C=DE` |

- File checksum — PowerShell: `Get-FileHash .\FindAMesh-1.9.599-release.apk -Algorithm SHA256` · Linux: `sha256sum FindAMesh-1.9.599-release.apk`
- Certificate — `apksigner verify --print-certs FindAMesh-1.9.599-release.apk`, or read it in-app under **Settings → System → "ÜBER & ECHTHEIT"**.

If a value does not match, the app has been altered — **do not use it.** Full instructions: [VERIFY.md](VERIFY.md).
