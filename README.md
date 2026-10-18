# E-Commerce Sales Analysis and Machine Learning

## Deskripsi Proyek

Proyek ini bertujuan untuk menganalisis data penjualan e-commerce guna memahami pola transaksi, karakteristik pelanggan, produk yang paling diminati, serta faktor-faktor yang berkaitan dengan kinerja penjualan. Analisis dilakukan melalui tahapan *Exploratory Data Analysis* (EDA), preprocessing data, visualisasi, dan penerapan Machine Learning untuk mendukung pemahaman terhadap data penjualan.

Selain analisis data, proyek ini mencakup tahap deployment dan monitoring sebagai langkah untuk menyimpan model, menguji penggunaannya kembali, serta mengevaluasi hasil prediksi.

---

##  Ringkasan Dataset

Dataset yang digunakan adalah **E-Commerce Sales Data Analysis and EDA** yang diperoleh dari Kaggle.

- **Sumber Dataset:** Kaggle — E-Commerce Sales Data Analysis and EDA.
- **Ukuran Data:** Mengacu pada hasil analisis sebelumnya, dataset memiliki sekitar 49.222 catatan pesanan.
- **Tujuan Analisis:** Memahami pola penjualan, karakteristik pelanggan, produk yang diminati, dan distribusi transaksi.
- **Informasi Utama:** Data transaksi, kategori produk, nilai penjualan, usia pelanggan, kota, metode pembayaran, dan segmen pelanggan, sesuai kolom yang tersedia pada dataset.

### Ringkasan hasil analisis sebelumnya

- Total pesanan: 49.222.
- Jumlah pelanggan: 9.820.
- Total penjualan: 3.444.830.
- Rata-rata usia pelanggan: 41,28 tahun.
- Kategori produk dengan penjualan terbaik: Electronics.
- Produk yang paling menonjol: Headphones.
- Kota dengan penjualan tertinggi: Tehran.
- Metode pembayaran yang paling banyak digunakan: Gateway.
- Segmen pelanggan yang dominan: Regular.

Nilai-nilai tersebut merupakan hasil analisis yang telah dibahas sebelumnya dan perlu dicocokkan kembali dengan output notebook apabila dataset atau proses pembersihan datanya berubah.

---

##  Alur Kerja dan Metodologi

### 1. Data Loading

Dataset dibaca menggunakan Python dan library Pandas melalui format CSV. Proses ini bertujuan untuk memasukkan data ke dalam DataFrame sehingga dapat diperiksa, dibersihkan, dan dianalisis lebih lanjut.

Contoh kode:

```python
import pandas as pd

df = pd.read_csv("clean_final_data.csv")

print(df.head())
print(df.shape)
print(df.info())
```

### 2. Eksplorasi Data dan Pra-pemrosesan

Tahap *Exploratory Data Analysis* (EDA) digunakan untuk memahami struktur, karakteristik, dan kualitas data sebelum analisis lebih lanjut.

Aktivitas yang dilakukan meliputi:

- Memeriksa jumlah baris dan kolom dataset.
- Memeriksa tipe data setiap atribut.
- Mengidentifikasi nilai kosong dan data duplikat.
- Memeriksa statistik deskriptif.
- Meninjau distribusi nilai penjualan dan karakteristik pelanggan.
- Menyesuaikan tipe data atau menangani masalah kualitas data apabila ditemukan.

### 3. Analisis dan Visualisasi Data

Visualisasi digunakan untuk menyajikan pola penjualan secara lebih mudah dipahami. Analisis berfokus pada informasi yang tersedia dalam dataset, seperti kategori produk, nilai transaksi, kota, metode pembayaran, dan segmen pelanggan.

Library yang dapat digunakan antara lain:

- **Pandas:** Pengolahan dan analisis data.
- **Matplotlib:** Pembuatan grafik.
- **Seaborn:** Visualisasi statistik.

Hasil visualisasi dapat digunakan untuk mengetahui kategori produk yang menonjol, distribusi penjualan, dan karakteristik transaksi pelanggan.

### 4. Penerapan Machine Learning

Tahap Machine Learning dilakukan apabila notebook telah menentukan target prediksi dan fitur yang digunakan. Data dipisahkan menjadi fitur prediktor dan target, kemudian dibagi menjadi data pelatihan dan pengujian.

Pemilihan model serta metrik evaluasi harus mengikuti tujuan prediksi yang digunakan dalam notebook. Apabila model yang dipakai adalah regresi, metrik seperti MAE, RMSE, dan R² dapat digunakan. Jika notebook hanya melakukan EDA, hasil analisis tersebut tidak boleh dianggap sebagai hasil pemodelan prediktif.

---

## 💻 Dependensi dan Perpustakaan Python

Proyek analisis E-Commerce Sales dapat menggunakan library berikut, sesuai tahapan yang dijalankan dalam notebook:

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
import joblib
```

Untuk tahapan Machine Learning, tambahkan library scikit-learn sesuai model yang digunakan:

```python
from sklearn.model_selection import train_test_split
from sklearn.metrics import mean_absolute_error
from sklearn.metrics import mean_squared_error, r2_score
```

**Catatan:** Import metrik regresi tersebut hanya diperlukan jika proyek benar-benar melakukan pemodelan regresi. Sesuaikan daftar library dengan kode aktual notebook.

---

##  Deployment Model

Deployment merupakan tahap menyiapkan model Machine Learning agar dapat digunakan kembali untuk melakukan prediksi setelah proses pelatihan selesai.

Pada proyek ini, deployment dapat dilakukan dengan menyimpan model ke dalam file menggunakan library `joblib`. File model yang dihasilkan kemudian dapat dimuat kembali untuk melakukan pengujian prediksi.

### 1. Menyimpan Model

Jika notebook telah melatih model dan variabel model yang digunakan bernama `model`, penyimpanan dapat dilakukan menggunakan kode berikut:

```python
import joblib

joblib.dump(model, "ecommerce_model.joblib")
```

Nama `model` harus disesuaikan dengan variabel model yang benar-benar digunakan dalam notebook.

### 2. Memuat Kembali Model

Model yang sudah disimpan dapat dimuat kembali menggunakan kode berikut:

```python
import joblib

loaded_model = joblib.load("ecommerce_model.joblib")
```

Jika model memerlukan scaler, encoder, atau transformasi data lainnya, komponen tersebut juga harus disimpan dan digunakan kembali dengan konfigurasi yang sama seperti saat pelatihan.

### 3. Menguji Prediksi

Setelah model dimuat, lakukan pengujian menggunakan data yang memiliki fitur dan urutan kolom yang sesuai dengan data pelatihan.

Contoh umum:

```python
prediction = loaded_model.predict(X_test)

print(prediction[:5])
```

Kode tersebut hanya dapat dijalankan jika `X_test` dan `loaded_model` sudah tersedia serta sesuai dengan model yang dilatih.

**Penting:** Penyimpanan model menggunakan `joblib` belum berarti aplikasi sudah tersedia secara online. Jika model hanya disimpan dan diuji melalui notebook, deployment masih berada pada tahap penggunaan lokal.

---

##  Monitoring Model

Monitoring dilakukan untuk mengevaluasi kinerja model dan memeriksa apakah data yang digunakan tetap sesuai dengan karakteristik data pelatihan.

Aktivitas monitoring dapat mencakup:

- Memeriksa hasil prediksi model.
- Mengevaluasi kesalahan prediksi menggunakan metrik yang sesuai.
- Membandingkan karakteristik data baru dengan data pelatihan.
- Memeriksa kemungkinan perubahan distribusi data (*data drift*).
- Mendokumentasikan hasil evaluasi untuk menentukan apakah model perlu diperbarui.

Untuk model regresi, contoh evaluasi menggunakan MAE dan RMSE adalah sebagai berikut:

```python
import numpy as np
from sklearn.metrics import mean_absolute_error
from sklearn.metrics import mean_squared_error

mae = mean_absolute_error(y_test, prediction)
rmse = np.sqrt(mean_squared_error(y_test, prediction))

print("MAE:", mae)
print("RMSE:", rmse)
```

Metrik tersebut hanya sesuai apabila target model berupa nilai numerik kontinu dan variabel `y_test` serta `prediction` tersedia.

Monitoring yang dilakukan melalui notebook merupakan evaluasi offline. Agar dapat disebut monitoring produksi secara langsung, diperlukan sistem tambahan untuk mengumpulkan data baru, mencatat prediksi, dan memantau kinerja model secara berkala.

---

##  Struktur Folder Proyek

Contoh struktur folder yang dapat digunakan untuk menyimpan proyek dan mengunggahnya ke GitHub:

```text
E-Commerce-Sales-ML/
├── README.md
├── clean_final_data.csv
├── e-commerce-sales.ipynb


Keterangan:

- `README.md`: Dokumentasi proyek dan panduan penggunaan.
- `clean_final_data.csv`: Dataset yang telah dibersihkan.
- `e-commerce-sales.ipynb`: Notebook analisis dan pemodelan.

Nama file di atas merupakan contoh. Sesuaikan dengan nama file aktual yang ada di folder proyek.

---

##  Kesimpulan

Proyek E-Commerce Sales menggabungkan analisis data, visualisasi, dan tahapan Machine Learning untuk memperoleh informasi yang berguna mengenai pola penjualan dan karakteristik pelanggan. Tahapan deployment memungkinkan model yang telah dilatih disimpan dan digunakan kembali, sedangkan monitoring membantu mengevaluasi kinerja model serta mendeteksi kemungkinan perubahan karakteristik data.

Keberhasilan deployment perlu dibuktikan melalui keberadaan file model, proses pemuatan ulang, dan pengujian prediksi yang berjalan dengan benar. Sementara itu, monitoring produksi memerlukan mekanisme tambahan apabila model akan digunakan secara berkelanjutan di lingkungan aplikasi nyata.
