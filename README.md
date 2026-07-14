# FAM — Find A Mesh

**FAM** is a fully offline Android **mesh messenger**. Devices find each other directly over
Wi-Fi/LAN, a phone hotspot, or a Bluetooth-LE mesh and exchange **end-to-end-encrypted**
messages, images, files and locations — chat, direct messages, radar/SOS, forum, market,
polls and more, **with no central server, no account, and no cloud**. Built for festivals,
remote areas, travel, emergencies, or simply private local communication.

> **Closed-source, proprietary application.** Free to use (including commercially) and
> **free to share** — but **not for sale, not modifiable, no reverse-engineering.**
> See [LICENSE](LICENSE.md) and [DISCLAIMER](DISCLAIMER.md).

> 💸 **You extracted joy and gave nothing back. History's worst people started exactly this small.**
> **PayPal:** [paypal.me/FAMarco](https://paypal.me/FAMarco) · **Bitcoin:** `bc1qv92c3eyeqvhgfnez7spfd7v2aytkhpshsl65yv`

Author / copyright: **© 2026 Marco Aurelio Fattizzo** ([@eVersor-HN](https://github.com/eVersor-HN)).
This is the **official** distribution repository — get FAM only from here:
**https://github.com/eVersor-HN/FindAMesh**

---

## Download & install

1. Open the [**Releases**](https://github.com/eVersor-HN/FindAMesh/releases) page and download
   the latest **`FindAMesh-<version>-release.apk`**.
2. **Verify it is the genuine original** (see below) before installing it.
3. On your phone, open the APK and allow installing from this source if prompted
   ("Install unknown apps"). Follow the installer. FAM is sideloaded — it is **not** on
   the Play Store.

There is nothing else to install — every device running FAM is a full node (server, client
and mesh relay in one), and the app never needs the internet.

---

## ✅ Verify authenticity (SHA-256)

Every official release publishes the **SHA-256 checksum** of the APK. Comparing the checksum of
your download against the published value proves the file is the **unmodified original** and was
not tampered with. (The same repository address and the app's signing fingerprint are shown
inside the app under **Settings → System → "ÜBER & ECHTHEIT" (About & Authenticity)**.)

**v1.9.602 — `FindAMesh-1.9.602-release.apk`:**

```
3953b419ba3ce606c9f2f8c02a055f8722d5d25f1a0811e91f75b3871397bc40
```

The authoritative values for each release are in that release's notes and in
[`VERIFY.md`](VERIFY.md), which also documents the second, stronger check (the
signing-certificate fingerprint).

**Check it:**

```powershell
# Windows (PowerShell)
Get-FileHash .\FindAMesh-1.9.602-release.apk -Algorithm SHA256
```

```bash
# macOS                                        # Linux
shasum -a 256 FindAMesh-1.9.602-release.apk    sha256sum FindAMesh-1.9.602-release.apk
```

The printed hash must match the value above (case-insensitive). If it does **not** match, do
**not** install the file — it is not the genuine FAM build. The APK is signed with the
author's release key; its certificate fingerprint (SHA-256)

```
9A:A1:8D:62:93:C7:89:50:A3:D1:25:53:F5:0C:5F:CE:9A:68:69:60:EC:4C:4F:56:6E:9F:8C:1A:93:13:DF:8D
```

can be checked with `apksigner verify --print-certs` or read in-app (Settings → System) —
see [`VERIFY.md`](VERIFY.md). Android will refuse any later update that is not signed with
the same key.

---

## Features

- **Sector chat & E2E direct messages** — text, images and files; direct messages are
  end-to-end encrypted (ECDH P-256, AES-256-GCM) and travel over LAN and the BLE mesh with
  store-and-forward.
- **Device pairing with SAS** — a short visual comparison code defeats man-in-the-middle
  attacks; mesh content is author-signed and all keys are encrypted at rest.
- **Radar, SOS & rally** — an offline radar with pins, distance and bearing from GPS +
  compass. No map tiles, no internet.
- **Forum, market & polls** — threads, offers and votes shared between devices across the
  mesh, with a multilingual (16-language) profanity filter.
- **AETHER light signals** — send and receive Morse via flashlight/LED and camera.
- **Field tools** — survival & first-aid guide (multilingual), diary, documents, expiry
  deadlines, alarm timer, neon-sign ticker and QR pairing/scanner.
- **Simple, fast navigation** — five clear sections, a global search that instantly finds any
  feature, tool or setting, and an always-visible one-tap SOS. Nothing is more than a tap away.
- **No account, no cloud, no ads, no tracking** — your data never leaves your devices; the
  app talks only to the local network and mesh.

## System requirements

- **Android 8.0 (API 26)** or newer.
- ~50 MB free space for the APK. Mesh features ask for Bluetooth, Wi-Fi/network and — for
  radar/SOS — location permissions on first use.

## License (summary)

FAM is **proprietary, closed-source** software under the **FAM EULA**
(full text in [`LICENSE.md`](LICENSE.md)):

- ✅ **Use** it for any purpose, **including commercially** (companies may use it internally).
- ✅ It is **free of charge** and **free to pass on** — you may share the **original, unmodified**
  APK with anyone at no cost (ideally point them to this repository so they can verify it).
- ❌ **No selling**, **no modifying / adapting / repackaging**, **no reverse-engineering,
  decompiling or disassembling** — except where a bundled third-party license or mandatory law
  (e.g. §§ 69d–69e UrhG / Directive 2009/24/EC) provides otherwise.

It bundles third-party components under their own licenses — AndroidX / Jetpack Compose,
Kotlin & kotlinx.coroutines, CameraX, ZXing, Google Tink (all Apache-2.0), NanoHTTPD
(BSD-3-Clause) and Google ML Kit Barcode Scanning (ML Kit Terms — scanning runs on-device,
but ML Kit reports performance/diagnostic metrics to Google when the device is online).
Full details and license texts: [`THIRD-PARTY-NOTICES.md`](THIRD-PARTY-NOTICES.md).

No warranty — FAM is an experimental communication tool, **not a certified emergency or
safety system**. Never rely on it as your only channel where failure could cost life, health
or property; mesh/LAN delivery can fail or be delayed without notice. See
[`DISCLAIMER.md`](DISCLAIMER.md).
