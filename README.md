# Latihan Wawancara Mandarin

Aplikasi web statis untuk latihan wawancara Mandarin dan terjemahan Mandarin–Indonesia.

## Fitur

- Dua mode: **Jawab dalam Mandarin** dan **Latihan Terjemahan**.
- Empat kategori latihan, sesi 10 soal, dan urutan acak yang memprioritaskan soal belum dibuka.
- Pinyin, arti bahasa Indonesia, jawaban singkat dan lengkap dibuka secara terpisah.
- Audio text-to-speech Mandarin manual dengan pilihan kecepatan 0,75×, 1×, dan 1,25× (bergantung pada dukungan browser/perangkat).
- Pencarian Hanzi/kata Indonesia, tema terang/gelap, pemulihan sesi, ekspor/impor progres, dan reset progres.
- Progres disimpan di `localStorage`; tidak membutuhkan akun atau backend.

## File utama

- `index.html` — antarmuka dan logika aplikasi.
- `questions.json` — bank soal hasil ekstraksi materi wawancara yang diberikan.

Sebagian materi sumber belum lengkap atau belum dapat dipastikan. Soal tersebut disimpan dalam bank data dengan penanda peninjauan, tetapi tidak dimasukkan ke sesi latihan sampai pasangan pertanyaan/jawaban, pinyin, dan arti tersedia dengan memadai. Jawaban tambahan yang disesuaikan dengan pekerjaan admin standardisasi diberi label di aplikasi.

## Menjalankan secara lokal

Karena aplikasi memuat `questions.json` menggunakan `fetch`, jalankan melalui server statis lokal (bukan dengan membuka `index.html` langsung dari `file://`). Contoh jika Python tersedia:

```bash
python -m http.server 8000
```

Kemudian buka `http://localhost:8000`.

## Publikasi GitHub Pages

Workflow `.github/workflows/deploy-pages.yml` mencoba mengaktifkan GitHub Pages dan menerbitkan situs secara otomatis setiap kali ada perubahan ke branch `main`. Buka tab **Actions** untuk memeriksa hasil deployment. Jika GitHub menolak pengaktifan otomatis, buka **Settings → Pages** dan pilih **GitHub Actions** sebagai sumber deployment.

## Catatan privasi

Riwayat latihan hanya disimpan di browser perangkat yang sedang digunakan. Menghapus data situs/browser dapat menghapus progres. Ekspor cadangan secara berkala jika progres penting.
