<p align="center">
  <h1 align="center">Project Pocket Mortys</h1>
  <p align="center">
    Community-maintained backend server for Pocket Mortys
  </p>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/status-work%20in%20progress-yellow?style=for-the-badge&logo=server&logoColor=white" />
</p>

This guide explains how to restore online functionality by replacing:
```
global-metadata.dat
```

If you cannot get it to work you can install the APK.

- ConspiracyRick.com Domain Name
- Achievement Support
- 32 Bit Support

[Version: 2.41.0](https://github.com/Project-Pocket-Mortys/Welcome/releases/download/V2.41.0/Pocket.Mortys.apk)
- Missing UI features like the Shop icon and displaying currency.

[Version: 2.40.2](https://github.com/Project-Pocket-Mortys/.github/releases/download/V2.40.2/Pocket.Mortys.apk)
- Has UI features.

Works on:
- 📱 Android phones (Pixel, Samsung, Nothing, Xiaomi, etc.)
- 📟 Tablets
- 🖥️ BlueStacks Android emulator for Windows and macOS

---

# ⚠️ Important Warnings

- Android 11+ restricts access to `Android/data`
- ADB cannot always write directly to game folders
- Some devices require manual file movement
- Root is NOT required but may improve compatibility
- BlueStacks may block direct filesystem writes depending on version

---

## 📱 Install Pocket Mortys

### 👉 **[Official App (Google Play)](https://play.google.com/store/apps/details?id=com.turner.pocketmorties&hl=en)**

## 📥 Required File

### 👉 **[Download global-metadata.dat](https://github.com/Project-Pocket-Mortys/.github/releases/download/metadata/global-metadata.dat)**

# 📦 Method 1 — File Manager (Easiest)

<details>
<summary>Click to expand</summary>

Download:
```
global-metadata.dat
```

Move it to:
```
Internal Storage / Android / data / com.turner.pocketmorties / files / il2cpp / Metadata /
```

If folders don’t exist, create them manually.

Restart the game.

</details>

---

# 🔌 Method 2 — ADB (Universal Method)

<details>
<summary>Click to expand</summary>

## 📥 Install ADB Platform Tools

👉 **[Download Official Platform Tools](https://developer.android.com/tools/releases/platform-tools)**

Verify:
```bash
adb version
```

Enable USB Debugging on phone.

Connect device:
```bash
adb devices
```

Push file:
```bash
adb push "C:\Users\yourpcusername\Downloads\global-metadata.dat" /sdcard/Android/data/com.turner.pocketmorties/files/il2cpp/Metadata/
```

</details>

---

# 🖥️ Method 3 — BlueStacks Emulator

<details>
<summary>Click to expand</summary>

Enable ADB in BlueStacks settings.

Connect:
```bash
adb connect 127.0.0.1:5555
adb devices
```

Push file:
```bash
adb push global-metadata.dat /sdcard/Download/
```

Move via shell:
```bash
adb shell
cp /sdcard/Download/global-metadata.dat /sdcard/Android/data/com.turner.pocketmorties/files/il2cpp/Metadata/
```

</details>

---

# 🧠 Storage Mapping

| Name | Path |
|------|------|
| Internal Storage | /sdcard/ |
| Download | /sdcard/Download/ |
| Android Data | /sdcard/Android/data/ |

---

# 🚀 Recommended Workflow

PC → ADB push → /sdcard/Download → Manual move

---

# ❗ Troubleshooting

- Operation not permitted → Android blocks Android/data
- File not found → wrong directory
- ADB not detected → USB debugging not enabled

---

# 💡 Notes

- /sdcard/ = Internal Storage
- Android/data is restricted on modern Android versions

