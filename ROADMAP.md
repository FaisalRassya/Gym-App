# Roadmap GiziGym

Rencana update GiziGym ke depan, diurutkan berdasarkan prioritas. Ukurannya sederhana: apa yang paling bikin orang tetap rajin mencatat tiap hari dikerjakan duluan, karena aplikasi tracking biasanya ditinggal bukan karena kurang fitur, tapi karena mencatat terasa ribet. Di dalam tiap versi, urutan poin juga urutan pengerjaan. Rencana bisa berubah setelah aplikasinya dipakai beneran.

Punya ide atau nemu bug? Buka [Issue baru](../../issues/new).

Status: `[x]` selesai, `[ ]` belum

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

## v1.1 — Data aman & mencatat lebih cepat

Prioritas tertinggi: yang menentukan aplikasinya tetap dipakai atau ditinggal.

- [x] Backup ke file + backup otomatis harian: tiap hari ke `Documents/GiziGym` (7 hari terakhir disimpan), tombol kirim ke WhatsApp/Drive, pulihkan dari file dengan konfirmasi.
- [ ] Menu favorit dan "salin dari kemarin": simpan kombinasi seperti "sarapan biasa", tambah sekali tap. Waktu mencatat turun dari ±1 menit jadi beberapa detik.
- [ ] Edit item yang sudah dicatat (ganti porsi/nama tanpa hapus–tambah ulang), terutama untuk membetulkan hasil foto AI.
- [ ] Isi profil di awal: saat pertama buka, tanya gender, umur, berat/tinggi, dan tujuan, supaya target dan program gym langsung sesuai (tidak lagi pakai profil contoh).
- [ ] Grafik progres beban per gerakan dan rekor pribadi (PR, estimasi 1RM). Datanya sudah tercatat tiap sesi, tinggal ditampilkan.

## v1.2 — Rapihin pengalaman harian

- [ ] Langkah gerakan dalam bahasa Indonesia (sekarang masih bahasa Inggris)
- [ ] Timer istirahat tetap bunyi/getar walau layar HP mati
- [ ] Database makanan Indonesia diperluas ke 300+ item (warteg, padang, jajanan, minuman kekinian), supaya pencarian jarang kosong
- [ ] Cek update otomatis: kasih tahu kalau ada APK baru di Releases
- [ ] Foto AI: simpan foto terakhir di riwayat, porsi yang sering diubah jadi default, dan pilihan penyedia lain (mis. OpenAI)

## v1.3 — Gym lebih lengkap

- [ ] Saran naik beban otomatis kalau semua set target tercapai (progressive overload)
- [ ] Tambah/ganti gerakan di tengah sesi
- [ ] Bikin program sendiri: pilih gerakan, set, reps, urutan hari
- [ ] Kalori terbakar dari latihan ikut dihitung di ringkasan harian

## v1.4 — Kebiasaan & integrasi HP

- [ ] Pengingat: minum air, catat makan, jadwal latihan
- [ ] Ringkasan mingguan: rata-rata kalori, protein, konsistensi latihan, perubahan berat
- [ ] Widget home screen: sisa kalori & protein hari ini
- [ ] Sinkron dengan Health Connect (langkah, berat badan, kalori aktif)

## v2.0 — Akun & distribusi

Baru masuk akal kalau aplikasinya sudah dipakai orang lain selain pemiliknya.

- [ ] Sinkron data antar HP (opsional, pakai akun; butuh server)
- [ ] Rilis di Google Play Store
- [ ] Tampilan bahasa Inggris

---

## Ide yang belum dijadwalkan

- Scan barcode kemasan (Open Food Facts). Ditunda karena data produk Indonesia di sana masih banyak yang kosong, jadi hasilnya bakal sering "produk tidak ditemukan".
- Video/animasi gerakan, bukan cuma 2 gambar
- Mode puasa (jendela makan, cocok untuk Ramadan)
- Kalkulator kebutuhan air dari berat badan & aktivitas
- Ekspor laporan bulanan (PDF/Excel)

## Catatan

- Nilai gizi di database dan hasil foto AI adalah **estimasi**. Selisih ±15–30% wajar, terutama untuk minyak dan santan.
- Setiap push ke `main` otomatis menghasilkan APK baru di [Releases](../../releases/latest) dengan nomor versi yang naik, jadi bisa langsung di-install di atas versi lama.
