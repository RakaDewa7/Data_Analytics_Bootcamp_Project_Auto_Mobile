# Dashboard Analisis Kinerja Penjualan Auto Mobile

## Ringkasan
Membangun dasbor analisis kinerja penjualan kendaraan otomotif (Automobile Sales) untuk mengidentifikasi tren musiman tahunan, lini produk terlaris, serta segmentasi pelanggan berdasarkan perilaku belanja menggunakan pendekatan RFM (*Recency, Frequency, Monetary*).

## Problem Statement
Industri penjualan kendaraan sering kali menghadapi fluktuasi permintaan yang dipengaruhi oleh musim tertentu serta ketergantungan pada kelompok produk unggulan. Tanpa analisis mendalam terhadap tren bulanan dan segmentasi pelanggan (terutama pelanggan yang mulai pasif atau berisiko *churn*), perusahaan berpotensi kehilangan momentum penjualan dan loyalitas konsumen.

## Data Exploration & Understanding
- **Sumber Data:** Dataset Penjualan Kendaraan Otomotif (*Automobile Sales Data.csv* dari Kaggle)[cite: 124].
- **Ukuran Dataset:** 2.747 baris × 20 kolom[cite: 124].
- **Tipe Data:** 13 kolom string, 5 integer, dan 2 float[cite: 123].
- **Kolom Utama:** `ORDERNUMBER`, `QUANTITYORDERED`, `PRICEEACH`, `SALES`, `ORDERDATE`, `STATUS`, `PRODUCTLINE`, `MSRP`, `CUSTOMERNAME`, `CITY`, `COUNTRY`, `DEALSIZE`[cite: 124].

## Data Preparation & Cleaning
- **Missing Value:** Pengecekan menggunakan Python menunjukkan **tidak ada missing value (0)**[cite: 125].
- **Duplikasi:** Tidak ditemukan adanya data terduplikasi (**0%**)[cite: 125].
- **Konsistensi & Tipe Data:** Kolom tanggal (`ORDERDATE`) disesuaikan ke format *DATE*[cite: 123]; tidak ditemukan kesalahan ketik (*typo*)[cite: 125].
- **Outlier:** Deteksi menggunakan metode Z-Score menunjukkan adanya *outlier* pada volume pesanan dan nilai penjualan, namun dibiarkan karena merepresentasikan data transaksi penjualan riil yang valid[cite: 126].

## Visualization & Output (Dashboard Highlights)
- **KPI Utama:** Total Transaksi 2.747 · Total Pembelian 96.428 · Total Pelanggan 89 · Rata-rata *Recency* 15,985 · *Frequency* 298 · Total *Monetary* / Pendapatan Keseluruhan = **$369,891,925.51**[cite: 127].
- **Lonjakan Musiman (November Spike):** Penjualan melonjak sangat drastis pada bulan November di setiap tahunnya (mencapai $37,93 juta dari 296 transaksi pada 2018[cite: 128] dan $40,18 juta dari 293 transaksi pada 2019[cite: 127]), yang didorong oleh momentum liburan/acara seperti *Thanksgiving*[cite: 128].
- **Lini Produk Terlaris:** **Classic Cars** memimpin dengan pendapatan kotor terbesar mencapai **$145.962.789,72**, disusul oleh **Vintage Cars** sebesar **$67.824.778,22**[cite: 129].
- **Segmentasi Pelanggan (RFM):** Segmen **At Risk** mendominasi porsi transaksi sebesar **37,25%** dengan total nilai penjualan mencapai **$37.364.968,84**, diikuti oleh *Loyal Customers* (27,45%), *Hibernating Customers* (19,61%), dan *Champions* (15,69%)[cite: 130, 131].

## Conclusion
- Perusahaan sangat bergantung pada lini produk unggulan (*Classic Cars*) dan sangat dipengaruhi oleh lonjakan musiman yang masif pada bulan November[cite: 132].
- Tingginya persentase transaksi dari segmen *At Risk* (pelanggan yang sebelumnya aktif namun sudah lama tidak bertransaksi) menunjukkan adanya risiko *churn* yang perlu segera ditangani[cite: 130, 131].

## Recommendation
- **Amankan Rantai Pasok & Stok:** Perusahaan wajib memastikan ketersediaan inventaris dan rantai pasok untuk produk terlaris (terutama lini *Classic Cars*) jauh-jauh hari sebelum bulan November tiba guna memaksimalkan momentum lonjakan musiman[cite: 129, 132].
- **Program Pemasaran Personalisasi untuk *At Risk*:** Segera rancang kampanye pemasaran yang dipersonalisasi khusus bagi segmen pelanggan *At Risk* (seperti penawaran diskon khusus, voucer eksklusif, atau rekomendasi produk *upgrade*) untuk merangsang mereka kembali aktif bertransaksi sebelum jatuh ke status *Hibernating*[cite: 130, 132].

## Tools yang Digunakan
Tableau (Dashboard Interaktif) · Python (Pandas, Z-Score, Data Preparation) · Analisis RFM (*Recency, Frequency, Monetary*) · Data Cleaning & Exploratory Data Analysis (EDA)

---
*Bagian dari Portofolio Graphic Design & Data Analytics Career Accelerator — Tempat Belajar (2026)*[cite: 115]  
*Disusun oleh: Raka Dewa Dipa Mahesa Arsandy*[cite: 114]
