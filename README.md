# buku-kia-md

<div align="center">

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Format: Markdown](https://img.shields.io/badge/Format-Markdown-blue.svg)]()
[![Focus: HealthTech](https://img.shields.io/badge/Focus-HealthTech%20%7C%20AI%20Ready-emerald.svg)]()
[![Language: ID | EN](https://img.shields.io/badge/Language-ID%20%7C%20EN-red.svg)]()

**[🇮🇩 Bahasa Indonesia](#-bahasa-indonesia)** · **[🇬🇧 English](#-english)**

</div>

---

## 🇮🇩 Bahasa Indonesia

Digitalisasi dan penataan ulang dokumen resmi **Buku Kesehatan Ibu dan Anak (KIA)** dari Kementerian Kesehatan (Kemenkes) Republik Indonesia ke dalam format **Markdown (`.md`)**.

Proyek ini bertujuan untuk mengubah dokumen panduan kesehatan maternal yang bersifat tak terstruktur (PDF/Cetak) menjadi aset data terstruktur yang bersifat *Machine-Readable*. Format ini dioptimalkan khusus untuk digunakan sebagai *Knowledge Base* (RAG System) pada kecerdasan buatan (LLM) atau diintegrasikan ke dalam platform e-health/RME.

### Latar Belakang

Buku KIA Kemenkes RI adalah standar emas pemantauan kesehatan ibu hamil dan anak di Indonesia. Namun, format distribusinya yang dominan berupa buku fisik atau dokumen PDF hancur sering kali menyulitkan sistem komputer atau AI untuk mengekstraksi informasi secara presisi tanpa distorsi teks.

Dengan mengonversi seluruh isi buku ini ke dalam format **Markdown**, dokumen ini sekarang memiliki hierarki data yang jelas (`#`, `##`, `-`), tabel yang rapi, dan skema yang mudah dipahami oleh *Large Language Models* (seperti DeepSeek, Claude, atau GPT) untuk meminimalkan risiko halusinasi informasi medis.

### Metodologi & Pipeline Kerja

Proyek ini tidak sekadar melakukan *copy-paste*, melainkan melalui proses rekayasa data (*data engineering*) yang terukur:

1. **Raw Extraction:** Ekstraksi teks dan tabel dari PDF resmi Buku KIA menggunakan bantuan Advanced OCR dan LLM (DeepSeek).
2. **Manual Fine-Tuning & Verification:** Pemeriksaan manual baris demi baris untuk memastikan tidak ada salah ketik (*typo*), angka klinis yang bergeser, atau tabel medis yang rusak.
3. **Markdown Structuring:** Penyusunan ulang hierarki teks agar sesuai dengan standar dokumentasi teknis yang ramah terhadap algoritma NLP (*Natural Language Processing*).

### Struktur Dokumen

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
[Klik di sini untuk mengakses buku sumber](https://kesprimkom.kemkes.go.id/assets/uploads/contents/others/Buku_KIA_2024.pdf)  

<div align="right"><a href="#buku-kia-md">⬆ Kembali ke atas</a></div>

---

## 🇬🇧 English

A digitization and restructuring of the official **Maternal and Child Health Handbook (Buku Kesehatan Ibu dan Anak / Buku KIA)**, published by the Ministry of Health of the Republic of Indonesia (Kemenkes RI), into **Markdown (`.md`)** format.

This project converts an unstructured maternal health guide (PDF/print) into a structured, *machine-readable* data asset. The format is optimized for use as a *Knowledge Base* in RAG systems for large language models (LLMs), or for integration into e-health and electronic medical record (EMR/RME) platforms.

> **Note:** The content of the handbook itself remains in Indonesian, as in the original publication. File and folder names are also kept in Indonesian; English equivalents are given in the structure below.

### Background

The Kemenkes RI Buku KIA is the gold standard for monitoring the health of pregnant women and children in Indonesia. However, it is distributed mainly as a printed book or as flattened PDF documents, which makes it difficult for computer systems and AI to extract information precisely without distorting the text.

By converting the entire handbook into **Markdown**, the document now has a clear data hierarchy (`#`, `##`, `-`), clean tables, and a schema that *Large Language Models* (such as DeepSeek, Claude, or GPT) can parse easily, which reduces the risk of hallucinated medical information.

### Methodology & Pipeline

This project is not a simple *copy-paste*. Each file goes through a deliberate *data engineering* process:

1. **Raw Extraction:** Text and tables are extracted from the official Buku KIA PDF using Advanced OCR and an LLM (DeepSeek).
2. **Manual Fine-Tuning & Verification:** Every line is reviewed manually to catch typos, shifted clinical figures, and broken medical tables.
3. **Markdown Structuring:** The text hierarchy is reorganized to follow technical documentation standards that work well with NLP (*Natural Language Processing*) algorithms.

### Repository Structure

The repository follows the main sections of the Buku KIA:

```text
buku-kia-md/
│
├── 📁 perjalanan-ibu/                            # The Mother's Journey
│   ├── perjalanan-menjadi-seorang-ibu.md         # The journey to motherhood
│   ├── kehamilan.md                              # Pregnancy
│   ├── melahirkan.md                             # Childbirth
│   ├── setelah-melahirkan.md                     # Postpartum
│   └── menyusui.md                               # Breastfeeding
│
├── 📁 perjalanan-anak/                           # The Child's Journey
│   ├── 0-6-bulan.md                              # 0–6 months
│   ├── 6-12-bulan.md                             # 6–12 months
│   ├── 12-24-bulan.md                            # 12–24 months
│   └── 2-6-tahun.md                              # 2–6 years
│
├── 📁 informasi-umum/                            # General Information
│   └── informasi-umum.md
│
├── 📁 pengukuran-pencatatan-tenaga-kesehatan/    # Health Worker Measurements & Records
│   ├── pencatatan-ibu.md                         # Maternal records
│   └── pencatatan-anak.md                        # Child records
│
├── buku-kia-2024.md                              # Full handbook in a single file
├── CONTRIBUTING.md
├── LICENSE
└── README.md
```
[Click here to access source book](https://kesprimkom.kemkes.go.id/assets/uploads/contents/others/Buku_KIA_2024.pdf)  

<div align="right"><a href="#buku-kia-md">⬆ Back to top</a></div>  


