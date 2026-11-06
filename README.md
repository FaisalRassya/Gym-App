# GiziGym

Aplikasi Android untuk tracking asupan harian (kalori, protein, karbo, lemak, serat, air), program diet, dan program gym dengan gambar gerakan yang benar.

**[Download APK terbaru](../../releases/latest)** · **[Roadmap](ROADMAP.md)** · **[Lapor bug / usul fitur](../../issues/new)**

## Fitur

- **Catat makanan** per waktu makan, dari database ±110 makanan (kebanyakan makanan Indonesia), input manual, atau **foto makanan** yang dihitung otomatis oleh Gemini.
- **Target harian** dihitung dari profil (Mifflin-St Jeor × faktor aktivitas), dengan program diet Cutting, Rekomposisi, Maintenance, Lean bulk, atau target manual.
- **Program gym** siap pakai, 5 untuk pria dan 5 untuk wanita (otomatis menyesuaikan gender di profil), dengan pencatat set, timer istirahat, dan beban sesi lalu terisi otomatis.
- **115 gerakan** dengan gambar posisi awal & akhir, otot yang dilatih, dan langkah.
- **Progres**: grafik kalori 7 hari, berat badan, riwayat latihan, backup & pulihkan.
- Jalan **offline**. Internet cuma dipakai untuk analisis foto.

## Install

1. Buka [Releases](../../releases/latest), download `GiziGym.apk` dari HP Android.
2. Buka file-nya dan izinkan "install dari sumber tidak dikenal".
3. Untuk fitur foto makanan: ambil API key gratis di [aistudio.google.com/apikey](https://aistudio.google.com/apikey), lalu tempel lewat tombol **Foto makanan** di aplikasi. Key cuma disimpan di HP.

Versi baru bisa langsung di-install di atas versi lama, data tetap aman.

## Struktur project

| Folder | Isi |
| --- | --- |
| `www/` | Aplikasi web (HTML/CSS/JS), data makanan (`foods.js`), data latihan & program (`data.js`), gambar gerakan (`img/`), font (`fonts/`) |
| `android/` | Project Android native ([Capacitor](https://capacitorjs.com) 7) yang membungkus `www/` |
| `.github/workflows/build-apk.yml` | Build APK otomatis dan publish ke Releases |

## Build

Setiap push ke `main` otomatis membangun APK bertanda tangan di GitHub Actions dan memasangnya di Releases. Nomor versi = nomor run Actions.

Kunci tanda tangan disimpan **terenkripsi** (AES-256) di `android/app/gizigym-release.jks.enc`. Workflow membukanya pakai satu repository secret:

| Secret | Isi |
| --- | --- |
| `KEYSTORE_PASSWORD` | Password kunci (alias `gizigym`) |

Tanpa password itu, file terenkripsi tidak bisa dipakai untuk menandatangani APK.

Pull request tetap di-build (debug, tanpa tanda tangan) untuk memastikan kodenya jalan.

Build lokal:

```bash
npm ci
npx cap sync android
cd android && ./gradlew assembleDebug
```

## Kredit

- Gambar & instruksi latihan: [free-exercise-db](https://github.com/yuhonas/free-exercise-db) (Unlicense / domain publik)
- Font: Archivo (SIL Open Font License) via [Fontsource](https://fontsource.org)
- Nilai gizi adalah estimasi dari rujukan umum (TKPI/USDA) dan bisa berbeda tergantung resep & merek.
