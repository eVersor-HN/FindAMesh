# Verifying authenticity

Only builds published in this repository's **[Releases](https://github.com/eVersor-HN/FindAMesh/releases)**,
signed by the author **Marco Aurelio Fattizzo**, are genuine. Use the values below to confirm that the
file you downloaded — and the app you installed — is the untampered original.

Each release also repeats its own values in its release notes. If anything does not match, **do not
install or use the app.**

## Current release

| Field | Value |
|---|---|
| Version | `1.9.599` |
| File | `FindAMesh-1.9.599-release.apk` |
| **SHA-256 (APK file)** | `83fe18d1e995ba833755b8d3789aa33b3c99f0d46379f0a22915d32d31ddac31` |
| **SHA-256 (signing certificate)** | `9A:A1:8D:62:93:C7:89:50:A3:D1:25:53:F5:0C:5F:CE:9A:68:69:60:EC:4C:4F:56:6E:9F:8C:1A:93:13:DF:8D` |
| Signing subject | `CN=FindAMesh, O=eVersor-HN, C=DE` |

## 1. APK file checksum

Confirms the downloaded file is byte-for-byte identical to the published one.

**Windows (PowerShell)**
```powershell
Get-FileHash .\FindAMesh-1.9.599-release.apk -Algorithm SHA256
```

**Linux**
```bash
sha256sum FindAMesh-1.9.599-release.apk
```

**macOS**
```bash
shasum -a 256 FindAMesh-1.9.599-release.apk
```

Compare the output to **SHA-256 (APK file)** above.

## 2. Signing-certificate fingerprint

Confirms the app was signed with the author's private key. This survives file renaming and is the
strongest authenticity signal. It is **also shown inside the app**:
**Settings → System → "ÜBER & ECHTHEIT" (About & Authenticity)** → *Signatur-Fingerprint (SHA-256)*.

**With Android build-tools (`apksigner`)**
```bash
apksigner verify --print-certs FindAMesh-1.9.599-release.apk
```
Look for the `SHA-256` certificate digest and compare it to **SHA-256 (signing certificate)** above
(ignore the `:` separators / letter case when comparing).

**Or on the installed app:** open the About section and compare the displayed fingerprint.

---

If either value does not match, the APK has been modified or re-signed by someone other than the
author — **treat it as untrusted and delete it.**
