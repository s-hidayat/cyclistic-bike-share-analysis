# Analisis Perilaku Pengguna Berbagi Sepeda Cyclistic

[![R](https://img.shields.io/badge/R-276DC3?style=for-the-badge&logo=r&logoColor=white)]()
[![DuckDB](https://img.shields.io/badge/DuckDB-FFF000?style=for-the-badge&logo=duckdb&logoColor=black)]()
[![Tableau](https://img.shields.io/badge/Tableau-E97627?style=for-the-badge&logo=Tableau&logoColor=white)]()

Selamat datang di repositori proyek analisis data saya! Proyek ini merupakan pemenuhan studi kasus dari **Google Data Analytics Capstone**. 

Sebagai analis yang berfokus pada *PropTech* (Property Technology) dan memiliki ketertarikan pada arsitektur serta perencanaan ruang kota, saya membedah lebih dari 5,5 juta baris data perjalanan sepeda historis. Tujuannya adalah untuk memahami bagaimana fasilitas infrastruktur mikro ini dimanfaatkan secara berbeda oleh berbagai demografi pengguna di Chicago.

👉 **[Klik di sini untuk membaca Laporan Analisis R Markdown (HTML) secara lengkap](https://s-hidayat.github.io/cyclistic-bike-share-analysis/)** 👉 **[Klik di sini untuk melihat Dasbor Tableau Interaktif]([MASUKKAN_LINK_TABLEAU_ANDA])**

---

## 🎯 1. Business Task (Tujuan Analisis)
Tujuan utama dari proyek ini adalah memberikan rekomendasi berbasis data kepada tim pemasaran Cyclistic guna **meningkatkan profitabilitas jangka panjang perusahaan**. 

Fokus strategi difokuskan pada pemahaman: *Bagaimana perilaku pengguna Casual (kasual/harian) berbeda dari Member (anggota tahunan)?* Hasil analisis ini akan digunakan untuk merancang strategi pemasaran yang efektif dalam mengubah pengendara *Casual* menjadi *Member* tahunan.

---

## 📂 2. Data Sources (Sumber Data)
Data yang digunakan dalam analisis ini merangkum 12 bulan perjalanan historis selama tahun 2025.
* **Sumber:** Data publik yang disediakan oleh Motivate International Inc.
* **Struktur:** 12 file `.csv` terpisah yang berisi rekaman data geografis (stasiun awal/akhir), waktu perjalanan, dan tipe keanggotaan.
* **Privasi:** Seluruh informasi pengenal pribadi (PII) pengguna telah dienkripsi atau dihapus untuk mematuhi etika data.

---

## 🛠️ 3. Methodology & Cleaning (Changelog)
Mengingat volume data yang masif, saya mengombinasikan **SQL (DuckDB)** untuk proses *Data Wrangling* dan **R** untuk verifikasi serta visualisasi statistik. 

Berikut adalah catatan pemrosesan (*Changelog*) untuk memastikan integritas data:
1. **Data Union:** Menggabungkan 12 file CSV bulanan menjadi satu tabel master (`all_trips_raw`) berjumlah **5.552.994 baris** menggunakan kueri `read_csv_auto`.
2. **Deduplikasi:** Menggunakan `SELECT DISTINCT` untuk menghapus anomali duplikat identik pada sistem.
3. **Filtering Logika Waktu:** * Mengekstrak durasi perjalanan menjadi menit (`ride_length_minutes`).
   * Menghapus anomali perjalanan di bawah 60 detik (kemungkinan uji coba mesin/sistem) dan di atas 24 jam (sepeda tidak dikembalikan).
4. **Hasil Akhir:** Dataset bersih yang siap dianalisis berjumlah **5.399.563 baris** (Tingkat retensi data yang sangat baik).

---

## 📊 4. Key Insights & Visualizations
Dari eksplorasi data menggunakan `ggplot2`, ditemukan tiga pola perilaku utama yang sangat membedakan kedua kelompok:

* **Lonjakan Akhir Pekan (The Weekend Spike):** Pengguna *Casual* menunjukkan lonjakan aktivitas yang sangat drastis pada hari Sabtu dan Minggu, mengindikasikan penggunaan fasilitas untuk rekreasi atau wisata kota. Sebaliknya, *Member* memiliki tren yang stabil di hari kerja (Senin-Jumat) yang menunjukkan pola komuter reguler.
* **Durasi Berkendara 2x Lipat:** Secara rata-rata, pengendara *Casual* menggunakan sepeda jauh lebih lama dibandingkan *Member* tahunan di setiap perjalanannya.
* **Dominasi Volume:** Meskipun *Casual* bersepeda lebih lama, komposisi total volume perjalanan tahunan masih didominasi oleh *Member* yang intensitas pemakaiannya lebih sering.

*(Grafik batang ganda dan donut chart tersedia selengkapnya di dalam [Laporan HTML]([MASUKKAN_LINK_GITHUB_PAGES_ANDA]))*

---

## 💡 5. Recommendations (Rekomendasi Bisnis)
Berdasarkan bukti data perilaku, strategi konversi harus menargetkan habitus rekreasi pengguna kasual:
1. **Promosi Terpusat di Akhir Pekan:** Mengalokasikan anggaran pemasaran secara maksimal pada hari Sabtu dan Minggu (khususnya di stasiun-stasiun dekat area wisata/taman kota) dengan menawarkan diskon khusus pendaftaran keanggotaan tahunan.
2. **Kampanye *Value-Driven*:** Memberikan notifikasi pop-up pada aplikasi kepada pengguna *Casual* setelah mereka bersepeda dengan durasi panjang, yang membandingkan total biaya yang mereka keluarkan hari itu dengan besarnya penghematan jika mereka menggunakan tarif *Member*.
3. **Produk Transisi:** Menguji coba tipe keanggotaan baru seperti "Paket Member Akhir Pekan" sebagai jembatan komitmen sebelum pengguna kasual memutuskan untuk mengambil langganan tahunan secara penuh.

---
*Silakan hubungi saya melalui [LinkedIn]([LINK_LINKEDIN_ANDA]) jika Anda ingin berdiskusi lebih lanjut mengenai metodologi atau temuan dalam studi kasus ini.*
