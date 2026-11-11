# Native Camera Pro (Android Camera2 project)

Kotlin app (`com.rawcam.nativepro`) using `android.hardware.camera2` + `MediaRecorder`.

## Features
- **RAW ISP switch**: `EDGE_MODE_OFF` + `NOISE_REDUCTION_MODE_MINIMAL` (or `OFF`), applied only if the device reports support (safe on Samsung A-series).
- **Bitrate / FPS**: H.264 MP4 at 20 / 50 / 80 / 120 Mbps, 24 / 30 / 60 FPS (falls back to the closest range the device supports and tells you).
- **Manual controls**: ISO, shutter (1/24 – 1/2000), boosted ISO (`CONTROL_POST_RAW_SENSITIVITY_BOOST`), manual focus, white balance lock.
- **Pro audio**: `UNPROCESSED` mic (falls back to `CAMCORDER`/`MIC`), 48 kHz, 320 kbps stereo AAC.
- **Storage**: saves to `DCIM/NativeCamera/` via MediaStore (Android 10+; no storage permission needed).

## Get the APK
**GitHub Actions (no install):** upload this folder to a GitHub repo (keep `.github/workflows/build-apk.yml`), open **Actions → Build Native Camera Pro APK → Run workflow**, then download the `NativeCameraPro-debug-apk` artifact.

**Android Studio:** open the folder, wait for Gradle sync, then *Build > Build APK(s)*.
Output: `app/build/outputs/apk/debug/app-debug.apk`
