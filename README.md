# Vlou Motion

Photo, video & motion graphics editor untuk Android — terinspirasi Alight Motion, dibangun 100% native Kotlin.

**Developer:** xyrcodex
**Version:** 1.2.0 (versionCode 120)

## Fitur

- **Canvas & Layer system** — shape, image, video, text, audio layer, multi-track timeline
- **Move & Transform** — posisi, scale, rotasi, opacity dengan gesture pinch/drag di canvas
- **Keyframes + Kurva easing lengkap** — Linear, Ease In/Out, Strong, Overshoot, Anticipate, Custom Bezier (edit titik kontrol manual)
- **Effects** — Brightness, Contrast, Saturation, Hue, Blur, Glow, Vignette, RGB Shift/Glitch, Tint, Stroke, Shadow, Gradient
- **Motion Graphics & Typography** — 8 bentuk shape, 40+ font/style teks, letter spacing, align, gradient fill
- **Export video** — H.264 MP4, pilih 24/30/60/**120 fps**, resolusi 100/75/50%, bitrate 2–60 Mbps, audio AAC mix
- **Export photo** — PNG/JPEG frame saat ini
- Auto simpan ke **Pictures/vlou-motion** (foto) & **Movies/vlou-motion** (video) via MediaStore
- **Media picker dalam app** — browse foto/video/audio dari galeri langsung di Vlou Motion (izin diminta dulu), plus Android Photo Picker tanpa izin
- Media di-copy ke storage private app → project aman dibuka ulang tanpa izin ulang
- **UI hitam-hijau** gaya Alight Motion, berbasis View (ringan, smooth di HP low-spec)
- Undo (30 langkah), autosave project, multi project
- Logo app adaptive vector (V + play hijau di atas hitam)

## Build

Buka di Android Studio (AGP 8.5.2, Gradle 8.7, Kotlin 1.9.24, JDK 17) atau:

```bash
gradle :app:assembleRelease
```

## Auto Release

Setiap push ke `main`, GitHub Actions otomatis build APK release dan membuat **GitHub Release** dengan tag `v<versionName>` (saat ini `v1.2.0`) + lampiran APK siap install. Naikkan `versionName`/`versionCode` di `app/build.gradle.kts` lalu push → release baru muncul otomatis.

## Teknologi

Kotlin • Android View (non-Compose, hemat resource) • MediaCodec (encoder/decoder H.264) • MediaMuxer • Media3 / ExoPlayer (audio preview) • Photo Picker • MediaStore API • Gson (project file) • Custom easing bezier engine
