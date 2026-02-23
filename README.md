#  Analisis Perilaku Pengguna Berbagi Sepeda (Cyclistic)

[![R](https://img.shields.io/badge/R-276DC3?style=for-the-badge&logo=r&logoColor=white)]()
[![DuckDB](https://img.shields.io/badge/DuckDB-FFF000?style=for-the-badge&logo=duckdb&logoColor=black)]()
[![Tableau](https://img.shields.io/badge/Tableau-E97627?style=for-the-badge&logo=Tableau&logoColor=white)]()

Proyek Capstone **Google Data Analytics** ini menganalisis >5,5 juta data historis perjalanan berbagi sepeda di Chicago. Proyek ini bertujuan untuk memecahkan masalah pemasaran utama Cyclistic: Bagaimana cara mengonversi Pengendara Kasual (Casual Riders) menjadi Anggota Tahunan (Annual Members)?.

Menganalisis lebih dari 5,7 juta data perjalanan sepanjang tahun 2025, studi ini mengungkap perbedaan perilaku fundamental antara kedua tipe pengguna—mulai dari kapan mereka berkendara, berapa lama durasinya, hingga di mana lokasi favorit mereka.

👉 **[Lihat Laporan R Markdown (HTML) Lengkap](https://s-hidayat.github.io/cyclistic-bike-share-analysis/)** 
---

### 🎯 Tujuan Bisnis
Menemukan perbedaan perilaku antara pengguna *Casual* (harian) dan *Member* (tahunan) untuk merancang strategi konversi keanggotaan yang berfokus pada peningkatan profitabilitas jangka panjang.

### 🛠️ Data & Metodologi
* **Data:** 12 bulan log perjalanan historis Cyclistic (2025).
* **Processing (SQL via DuckDB):** Menggabungkan 12 file CSV, menghapus duplikasi, dan memfilter anomali waktu. Berhasil mengekstrak **5.399.563 baris data bersih** dari 5.5M+ data mentah.
* **Analysis & Visualisasi:** R (`tidyverse`, `ggplot2`) dan Tableau.

### 💡 TL;DR Insights
1. 🚴 **Durasi:** Pengguna *Casual* bersepeda rata-rata **2x lebih lama** per perjalanan dibandingkan *Member*.
2. 📈 **Pola Waktu:** Pengguna *Casual* melonjak drastis di **akhir pekan** (indikasi rekreasi), sementara *Member* mendominasi **hari kerja** secara konsisten (indikasi komuter).
3. 📊 **Volume:** *Member* menghasilkan total volume perjalanan tahunan tertinggi karena frekuensi pemakaian yang intens.

### 🚀 TL;DR Rekomendasi
* **Kampanye Akhir Pekan:** Alokasikan promosi diskon *membership* secara agresif pada hari Sabtu-Minggu di stasiun-stasiun area rekreasi.
* **Fitur *Value-Driven*:** Tampilkan pop-up penghematan tarif (*"Berapa yang Anda hemat jika menjadi Member"*) di aplikasi khusus untuk pengguna *Casual* berdurasi panjang.
* **Opsi Transisi:** Perkenalkan "Paket Member Akhir Pekan" sebagai jembatan sebelum komitmen keanggotaan tahunan.

---
*Ingin berdiskusi lebih lanjut? Mari terhubung di [LinkedIn](https://www.linkedin.com/in/s-hidayat-69b1b5372).*
