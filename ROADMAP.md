# Roadmap GiziGym

Rencana update GiziGym ke depan. Urutan versi = urutan prioritas: yang paling sering dipakai sehari-hari dikerjakan duluan. Rencana bisa berubah setelah aplikasinya dipakai beneran.

Punya ide atau nemu bug? Buka [Issue baru](../../issues/new).

Status: `[x]` selesai · `[ ]` belum

---

## v1.0 — Rilis pertama (sekarang)

- [x] Catat makanan per waktu makan (sarapan, siang, malam, camilan) dengan kalori, protein, karbo, lemak, serat
- [x] Database ±110 makanan, kebanyakan makanan Indonesia, plus input manual dan "makananku"
- [x] Target harian dari profil (rumus Mifflin-St Jeor + faktor aktivitas)
- [x] Program diet: Cutting, Rekomposisi, Maintenance, Lean bulk, atau target manual
- [x] Pencatat air minum
- [x] 10 program gym siap pakai: 5 untuk pria (Full Body Pemula, Upper/Lower, Push/Pull/Legs, Home Workout, Fat Loss) dan 5 untuk wanita (Full Body Pemula, Glute & Legs Focus, Upper/Lower Toning, Home Workout, Fat Loss + Toning)
- [x] Daftar program otomatis menyesuaikan gender di profil, program gender lain tetap bisa dipilih
- [x] Sesi latihan: catat kg & reps per set, timer istirahat 90 detik, beban sesi lalu terisi otomatis
- [x] 115 gerakan dengan gambar posisi awal & akhir, otot yang dilatih, dan langkah
- [x] Foto makanan → estimasi gizi otomatis pakai Gemini (API key sendiri), dengan indikator progres dan batas waktu
- [x] Grafik kalori 7 hari, grafik berat badan, riwayat latihan
- [x] Backup & pulihkan lewat salin-tempel kode
- [x] APK native, jalan offline, build otomatis di GitHub Actions

## v1.1 — Rapihin yang dipakai tiap hari

- [ ] Langkah gerakan dalam bahasa Indonesia (sekarang masih bahasa Inggris)
- [ ] Edit item makanan yang sudah dicatat (ganti porsi tanpa hapus–tambah ulang)
- [ ] "Salin dari kemarin" untuk makan yang sama tiap hari
- [ ] Backup ke file (simpan `.json` ke HP / kirim ke WhatsApp atau Drive) dan pulihkan dari file
- [ ] Cek update otomatis: kasih tahu kalau ada APK baru di Releases
- [ ] Timer istirahat tetap bunyi/getar walau layar HP mati

## v1.2 — Catat makan lebih cepat

- [ ] Scan barcode kemasan (data gizi dari Open Food Facts)
- [ ] Menu favorit: simpan kombinasi makanan, mis. "sarapan biasa", tambah sekali tap
- [ ] Database makanan Indonesia diperluas ke 300+ item (warteg, padang, jajanan, minuman kekinian)
- [ ] Foto AI: pilihan penyedia lain (mis. OpenAI) dan simpan foto terakhir di riwayat
- [ ] Koreksi foto AI belajar dari kebiasaan: porsi yang sering diubah jadi default

## v1.3 — Gym lebih lengkap

- [ ] Bikin program sendiri: pilih gerakan, set, reps, urutan hari
- [ ] Grafik progres per gerakan dan rekor pribadi (PR, estimasi 1RM)
- [ ] Saran naik beban otomatis kalau semua set target tercapai (progressive overload)
- [ ] Tambah/ganti gerakan di tengah sesi
- [ ] Kalori terbakar dari latihan ikut dihitung di ringkasan harian

## v1.4 — Kebiasaan & integrasi HP

- [ ] Pengingat: minum air, catat makan, jadwal latihan
- [ ] Sinkron dengan Health Connect (langkah, berat badan, kalori aktif)
- [ ] Widget home screen: sisa kalori & protein hari ini
- [ ] Ringkasan mingguan: rata-rata kalori, protein, konsistensi latihan, perubahan berat

## v2.0 — Akun & distribusi

- [ ] Sinkron data antar HP (opsional, pakai akun)
- [ ] Rilis di Google Play Store
- [ ] Tampilan bahasa Inggris

---

## Ide yang belum dijadwalkan

- Video/animasi gerakan, bukan cuma 2 gambar
- Mode puasa (jendela makan, cocok untuk Ramadan)
- Kalkulator kebutuhan air dari berat badan & aktivitas
- Ekspor laporan bulanan (PDF/Excel)

## Catatan

- Nilai gizi di database dan hasil foto AI adalah **estimasi**. Selisih ±15–30% wajar, terutama untuk minyak dan santan.
- Setiap push ke `main` otomatis menghasilkan APK baru di [Releases](../../releases/latest) dengan nomor versi yang naik, jadi bisa langsung di-install di atas versi lama.
