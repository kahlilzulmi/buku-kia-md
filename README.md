# buku-kia-md

<p align="center">
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Format: Markdown](https://img.shields.io/badge/Format-Markdown-blue.svg)]()
[![Focus: HealthTech](https://img.shields.io/badge/Focus-HealthTech%20%7C%20AI%20Ready-emerald.svg)]()
</p>

Digitalisasi dan penataan ulang dokumen resmi **Buku Kesehatan Ibu dan Anak (KIA)** dari Kementerian Kesehatan (Kemenkes) Republik Indonesia ke dalam format **Markdown (`.md`)**. 

Proyek ini bertujuan untuk mengubah dokumen panduan kesehatan maternal yang bersifat tak terstruktur (PDF/Cetak) menjadi aset data terstruktur yang bersifat *Machine-Readable*. Format ini dioptimalkan khusus untuk digunakan sebagai *Knowledge Base* (RAG System) pada kecerdasan buatan (LLM) atau diintegrasikan ke dalam platform e-health/RME.

---

## Latar Belakang

Buku KIA Kemenkes RI adalah standar emas pemantauan kesehatan ibu hamil dan anak di Indonesia. Namun, format distribusinya yang dominan berupa buku fisik atau dokumen PDF hancur sering kali menyulitkan sistem komputer atau AI untuk mengekstraksi informasi secara presisi tanpa distorsi teks.

Dengan mengonversi seluruh isi buku ini ke dalam format **Markdown**, dokumen ini sekarang memiliki hierarki data yang jelas (`#`, `##`, `-`), tabel yang rapi, dan skema yang mudah dipahami oleh *Large Language Models* (seperti DeepSeek, Claude, atau GPT) untuk meminimalkan risiko halusinasi informasi medis.

## Metodologi & Pipeline Kerja

Proyek ini tidak sekadar melakukan *copy-paste*, melainkan melalui proses rekayasa data (*data engineering*) yang terukur:
1. **Raw Extraction:** Ekstraksi teks dan tabel dari PDF resmi Buku KIA menggunakan bantuan Advanced OCR dan LLM (DeepSeek).
2. **Manual Fine-Tuning & Verification:** Pemeriksaan manual baris demi baris untuk memastikan tidak ada salah ketik (*typo*), angka klinis yang bergeser, atau tabel medis yang rusak.
3. **Markdown Structuring:** Penyusunan ulang hierarki teks agar sesuai dengan standar dokumentasi teknis yang ramah terhadap algoritma NLP (*Natural Language Processing*).

---

## Struktur Dokumen

Repositori ini dibagi berdasarkan bagian utama pada Buku KIA:

```text
buku-kia-md/
│
├── 📁 perjalanan-ibu/
│   ├── perjalanan-menjadi-seorang-ibu.md
│   ├── kehamilan.md
│   ├── melahirkan.md
│   ├── setelah-melahirkan.md
│   └── menyusui.md
│
├── 📁 perjalanan-anak/
│   ├── 0-6-bulan.md
│   ├── 6-12-bulan.md
│   ├── 12-24-bulan.md
│   └── 2-6-tahun.md
│
├── 📁 informasi-umum/
│   └── informasi-umum.md
│
├── 📁 pengukuran-pencatatan-tenaga-kesehatan/
│   ├── pencatatan-ibu.md
│   └── pencatatan-anak.md
│
├── buku-kia-2024.md
├── CONTRIBUTING.md
├── LICENSE
└── README.md
```
