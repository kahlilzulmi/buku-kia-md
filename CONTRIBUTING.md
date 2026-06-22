# Panduan Kontribusi

Terima kasih atas minat Anda untuk berkontribusi pada **buku-kia-md**. Proyek ini mendigitalisasi Buku Kesehatan Ibu dan Anak (KIA) Kemenkes RI ke format Markdown yang terstruktur dan siap dipakai sebagai knowledge base (RAG, e-health, RME).

## Prinsip Utama

1. **Akurasi medis di atas segalanya** — Jangan mengubah makna, angka klinis, dosis, jadwal imunisasi, atau isi tabel tanpa verifikasi terhadap sumber resmi.
2. **Jangan parafrase konten klinis** — Perbaikan yang diizinkan: typo, format markdown, hierarki heading, dan struktur tabel. Bukan penulisan ulang isi panduan.
3. **Pertahankan struktur folder** — Konten inti berada di file modular per bagian, bukan ditambah bebas di root.
4. **Jaga konsistensi dengan sumber** — `buku-kia-2024.md` adalah referensi lengkap; file di folder adalah pecahan modular dari dokumen tersebut.

## Struktur Repositori

```text
buku-kia-md/
├── perjalanan-ibu/
│   ├── perjalanan-menjadi-seorang-ibu.md
│   ├── kehamilan.md
│   ├── melahirkan.md
│   ├── setelah-melahirkan.md
│   └── menyusui.md
├── perjalanan-anak/
│   ├── 0-6-bulan.md
│   ├── 6-12-bulan.md
│   ├── 12-24-bulan.md
│   └── 2-6-tahun.md
├── informasi-umum/
│   └── informasi-umum.md
├── pengukuran-pencatatan-tenaga-kesehatan/
│   ├── pencatatan-ibu.md
│   └── pencatatan-anak.md
├── buku-kia-2024.md
└── README.md
```

### Pemetaan Konten

| File target | Bagian sumber (heading utama) |
| --- | --- |
| `perjalanan-ibu/perjalanan-menjadi-seorang-ibu.md` | `## Perjalanan Menjadi Seorang Ibu` sampai sebelum `# Kehamilan` |
| `perjalanan-ibu/kehamilan.md` | `# Kehamilan` sampai sebelum `# Melahirkan` |
| `perjalanan-ibu/melahirkan.md` | `# Melahirkan` sampai sebelum `# Setelah Melahirkan` |
| `perjalanan-ibu/setelah-melahirkan.md` | `# Setelah Melahirkan` sampai sebelum `# Menyusui` |
| `perjalanan-ibu/menyusui.md` | `# Menyusui` sampai sebelum `# 0 - 6 Bulan` |
| `perjalanan-anak/0-6-bulan.md` | `# 0 - 6 Bulan` sampai sebelum `# 6 - 12 Bulan` |
| `perjalanan-anak/6-12-bulan.md` | `# 6 - 12 Bulan` sampai sebelum `# 12 - 24 Bulan` |
| `perjalanan-anak/12-24-bulan.md` | `# 12 - 24 Bulan` sampai sebelum `# 2 - 6 Tahun` |
| `perjalanan-anak/2-6-tahun.md` | `# 2 - 6 Tahun` sampai sebelum `# Informasi Umum` |
| `informasi-umum/informasi-umum.md` | `# Informasi Umum` sampai sebelum `# Pengukuran & Pencatatan oleh Tenaga Kesehatan` |
| `pengukuran-pencatatan-tenaga-kesehatan/pencatatan-ibu.md` | `# Pengukuran & Pencatatan oleh Tenaga Kesehatan` sampai sebelum `## Catatan Pelayanan Kesehatan Anak` |
| `pengukuran-pencatatan-tenaga-kesehatan/pencatatan-anak.md` | `## Catatan Pelayanan Kesehatan Anak` sampai akhir dokumen |

Bagian pembuka dokumen (cover, katalog, pengantar, daftar isi) saat ini hanya ada di `buku-kia-2024.md` (baris awal dokumen).

## Jenis Kontribusi yang Diterima

- Koreksi typo atau kesalahan transkripsi OCR
- Perbaikan format markdown (heading, list, tabel, blockquote)
- Penyelarasan hierarki heading agar konsisten antar file
- Penambahan atau perbaikan metadata struktural (tanpa mengubah isi klinis)
- Perbaikan dokumentasi (`README.md`, `CONTRIBUTING.md`)
- Pelaporan bagian yang hilang, terduplikasi, atau terpotong antar file

## Jenis Kontribusi yang Tidak Diterima

- Mengubah rekomendasi medis tanpa rujukan sumber resmi Kemenkes
- Memecah atau menggabungkan file di luar pemetaan yang disepakati
- Menghapus `buku-kia-2024.md` tanpa kesepakatan maintainer
- Menambahkan opini klinis pribadi ke dalam konten Buku KIA

## Konvensi Markdown

- Gunakan `#` untuk judul utama bagian, `##` untuk subbagian, `###` untuk sub-subbagian.
- Pertahankan urutan konten seperti pada sumber PDF/Buku KIA.
- Tabel medis harus tetap berupa tabel markdown (`| ... |`), bukan teks bebas.
- Blockquote (`>`) dipakai untuk penekanan atau catatan penting, sesuai sumber.
- Hindari HTML inline kecuali benar-benar diperlukan untuk tabel kompleks.
- Nama file: huruf kecil, pemisah kata dengan tanda hubung (`kehamilan.md`, `0-6-bulan.md`).

## Alur Kerja Kontribusi

1. **Fork** repositori (jika berkontribusi dari luar).
2. **Buat branch** dengan nama deskriptif, misalnya `fix/kehamilan-typo-trimester-1` atau `docs/update-contributing`.
3. **Lakukan perubahan** hanya pada file yang relevan dengan scope PR.
4. **Verifikasi** perubahan Anda:
   - Bandingkan dengan `buku-kia-2024.md` untuk bagian yang sama.
   - Pastikan tidak ada konten hilang atau terduplikasi antar file modular.
   - Cek tabel dan angka klinis baris demi baris jika Anda menyentuh bagian medis.
5. **Commit** dengan pesan jelas dalam bahasa Indonesia atau Inggris, contoh:
   - `fix: koreksi typo tanda bahaya trimester 1`
   - `docs: perjelas pemetaan file di CONTRIBUTING`
6. **Buka Pull Request** dengan deskripsi:
   - Apa yang diubah
   - File mana saja yang terdampak
   - Sumber verifikasi (halaman PDF Buku KIA, jika ada)
   - Checklist verifikasi (lihat bawah)

## Checklist Pull Request

Centang di deskripsi PR:

- [ ] Perubahan tidak mengubah makna konten medis
- [ ] File diubah sesuai pemetaan folder yang berlaku
- [ ] Tidak ada duplikasi atau bagian terpotong antar file modular
- [ ] Format markdown tetap valid (heading, list, tabel)
- [ ] Perubahan terbatas pada scope yang dijelaskan di PR

## Menambah atau Memecah File Baru

Jika Anda ingin menambah file (misalnya untuk bagian pembuka dokumen), buka **issue** terlebih dahulu dan jelaskan:

- Nama file dan folder tujuan
- Rentang heading/barisan sumber di `buku-kia-2024.md`
- Alasan pemecahan diperlukan

Jangan memecah konten berdasarkan jumlah baris tetap; gunakan batas heading yang jelas.

## Pelaporan Masalah

Saat membuka issue, sertakan:

- Path file (contoh: `perjalanan-ibu/kehamilan.md`)
- Kutipan teks yang bermasalah
- Perbandingan dengan `buku-kia-2024.md` atau PDF resmi
- Usulan perbaikan (jika ada)

## Lisensi

Dengan berkontribusi, Anda setuju bahwa kontribusi Anda dilisensikan di bawah lisensi yang sama dengan proyek ini (MIT), sesuai `README.md`.

## Pertanyaan

Untuk pertanyaan tentang scope kontribusi atau struktur file, buka issue dengan label `question` atau diskusikan di PR terkait.
