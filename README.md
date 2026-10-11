# Analisis Data Penjualan E-Commerce menggunakan EDA

## Deskripsi Proyek

Proyek ini merupakan praktikum analisis data yang bertujuan untuk memahami karakteristik, pola penjualan, dan informasi bisnis dari dataset *E-Commerce Sales Data Analysis and EDA*. Analisis dilakukan menggunakan Python untuk mengolah data, mengeksplorasi informasi, serta menyajikan hasil analisis dalam bentuk ringkasan bisnis (*Business Summary*) dan visualisasi data.

Tahapan yang dilakukan dalam praktikum meliputi:

- Memuat dataset dan memahami struktur data menggunakan Pandas.
- Melakukan pemeriksaan informasi dataset, tipe data, statistik deskriptif, missing values, dan data duplikat.
- Melakukan pembersihan data untuk memastikan kualitas dataset sebelum dianalisis lebih lanjut.
- Melakukan Exploratory Data Analysis (EDA) untuk memahami karakteristik dan pola dalam data penjualan.
- Menganalisis metrik bisnis, seperti jumlah pesanan, jumlah pelanggan, total penjualan, dan rata-rata usia pelanggan.
- Mengidentifikasi kategori produk dengan performa terbaik, produk terbaik, kota dengan penjualan tertinggi, metode pembayaran terpopuler, dan segmen pelanggan.
- Membuat visualisasi data untuk membantu memahami hasil analisis secara lebih mudah.
- Menyusun ringkasan bisnis berdasarkan hasil pengolahan dan analisis dataset.

Berdasarkan hasil analisis yang telah dibahas, diperoleh ringkasan bisnis sebagai berikut:

| **Metrik Bisnis** | **Hasil Analisis** |
|---|---:|
| Total pesanan | 49.222 |
| Jumlah pelanggan | 9.820 |
| Total penjualan | 3.444.830 |
| Rata-rata usia pelanggan | 41,28 tahun |
| Kategori produk terbaik | Electronics |
| Produk terbaik | Headphones |
| Kota dengan penjualan tertinggi | Tehran |
| Metode pembayaran terpopuler | Gateway |
| Segmen pelanggan mayoritas | Regular |

Hasil tersebut memberikan gambaran mengenai kondisi penjualan dan karakteristik pelanggan berdasarkan dataset yang dianalisis.

**Catatan interpretasi:** Hasil analisis di atas mengikuti ringkasan bisnis yang diperoleh dalam praktikum. Satuan total penjualan, definisi pelanggan, dan kriteria penentuan produk terbaik perlu disesuaikan dengan kolom serta perhitungan yang digunakan dalam notebook.

## Struktur Folder

Pastikan susunan file proyek disesuaikan dengan file yang digunakan dalam praktikum.

```text
ecommerce-sales-analysis/
├── README.md
├── requirements.txt
├── ECommerce_Sales_Analysis.ipynb
└── E-Commerce Sales Data.csv
```

Nama notebook dan file dataset dapat berbeda sesuai dengan file yang digunakan. Pastikan lokasi file CSV sesuai dengan kode pembacaan dataset di dalam notebook.

## Dataset

Dataset yang digunakan adalah *E-Commerce Sales Data Analysis and EDA* yang diperoleh dari Kaggle.

Dataset ini digunakan untuk mempelajari data penjualan e-commerce dan mengeksplorasi informasi bisnis, seperti transaksi, pelanggan, kategori produk, metode pembayaran, serta lokasi penjualan, sesuai dengan variabel yang tersedia.

Sumber dataset: [E-Commerce Sales Data Analysis and EDA – Kaggle](https://www.kaggle.com/datasets/erfan4524/e-commerce-sales-data-analysis-and-eda)

Dataset digunakan untuk keperluan pembelajaran dan analisis data. Penggunaan atau pendistribusian ulang dataset perlu mengikuti lisensi dan ketentuan dari sumber aslinya.

## Persiapan dan Menjalankan Notebook

1. Instal Python pada komputer.
2. Unduh dataset dari Kaggle.
3. Simpan file dataset pada folder proyek yang sama dengan notebook atau sesuaikan lokasi file pada kode.
4. Buka terminal pada folder proyek.
5. Instal library yang dibutuhkan:

   ```bash
   pip install -r requirements.txt
   ```

6. Buka notebook menggunakan Jupyter Notebook, JupyterLab, atau VS Code.
7. Pastikan file CSV dapat diakses oleh notebook.
8. Jalankan setiap sel notebook secara berurutan dari awal hingga akhir.
9. Periksa hasil analisis dan visualisasi untuk memahami pola penjualan.
10. Amati ringkasan bisnis yang dihasilkan setelah seluruh proses analisis selesai.

## Library yang Digunakan

Library berikut dapat digunakan dalam praktikum analisis data e-commerce, sesuai dengan kode yang diterapkan di notebook.

- **Pandas:** membaca, mengolah, dan membersihkan dataset.
- **NumPy:** mendukung operasi numerik.
- **Matplotlib:** membuat grafik dan visualisasi data.
- **Seaborn:** membuat visualisasi statistik.
- **Jupyter Notebook:** menjalankan kode Python dan mendokumentasikan hasil praktikum.

Instalasi library dapat dilakukan menggunakan perintah berikut:

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

## Hasil Analisis

Hasil praktikum menunjukkan bahwa proses analisis data dapat menghasilkan ringkasan bisnis yang mencakup jumlah pesanan, jumlah pelanggan, total penjualan, dan rata-rata usia pelanggan.

Analisis juga mengidentifikasi Electronics sebagai kategori produk terbaik, Headphones sebagai produk terbaik, Tehran sebagai kota dengan penjualan tertinggi, Gateway sebagai metode pembayaran terpopuler, serta Regular sebagai segmen pelanggan mayoritas.

Proses visualisasi ditandai dengan pesan:

`VISUALIZATION COMPLETED SUCCESSFULLY`

Pesan tersebut menunjukkan bahwa proses visualisasi pada notebook telah selesai dijalankan. Interpretasi hasil tetap perlu didasarkan pada perhitungan dan grafik yang dihasilkan.

## Kesimpulan

Berdasarkan praktikum yang dilakukan, Exploratory Data Analysis (EDA) membantu memahami karakteristik dan pola data penjualan e-commerce melalui proses pemuatan data, pemeriksaan kualitas data, analisis statistik, dan visualisasi.

Hasil analisis memberikan informasi mengenai performa produk, karakteristik pelanggan, metode pembayaran, dan kota dengan penjualan tertinggi. Informasi tersebut dapat digunakan sebagai bahan pertimbangan dalam mengevaluasi penjualan dan menyusun strategi bisnis berdasarkan data yang tersedia.

## Teknologi

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook
- Kaggle Dataset
