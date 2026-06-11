# Data-Analyst-Portofolio
Deskripsi Tugas

Saya melakukan Exploratory Data Analysis (EDA) dan data cleaning terhadap dataset penjualan restoran cepat saji Balaji Fast Food. Dataset terdiri dari 1.000 baris dan 10 kolom, meliputi informasi transaksi seperti tanggal, jenis item, harga, kuantitas, total transaksi, metode pembayaran, penerima pesanan, dan waktu penjualan dsb.


**Apa yang Saya Lakukan**
1. Data Exploration

-Memeriksa struktur dataset
-Menggunakan head(), tail(), info(), shape, dan columns.
-Tujuannya untuk memahami jumlah data, tipe data, dan atribut yang tersedia.
-Analisis statistik deskriptif
-Menggunakan describe() untuk melihat rata-rata, median, standar deviasi, nilai minimum, dan maksimum pada kolom numerik.
-Visualisasi distribusi data
-Histogram untuk transaction_amount, quantity, dan item_price.
-Pie chart dan bar chart untuk kolom kategorikal seperti item_type, transaction_type, dan time_of_sale.
-Pengecekan kualitas data
-Mengecek missing value dengan isnull().sum().
-Mengecek duplikasi data dengan duplicated().sum().
-Mengecek outlier menggunakan boxplot dan metode Interquartile Range (IQR).

2. Data Cleaning

-Menangani missing value
-Missing value ditemukan pada kolom transaction_type.
-Nilai kosong diisi menggunakan random choice berbasis probabilitas sesuai proporsi data asli (Cash vs Online), sehingga distribusi transaksi tetap realistis.
-Validasi hasil cleaning
-Membandingkan distribusi transaksi sebelum dan sesudah pengisian missing value melalui visualisasi pie chart.
-Memastikan tidak ada perubahan distribusi yang ekstrem.
-Standarisasi format tanggal
-Mengubah format tanggal yang bercampur (menggunakan / dan -) menjadi format yang konsisten.
-Mengonversi kolom date menjadi tipe data datetime.
-Optimasi tipe data
-Mengubah beberapa kolom objek menjadi tipe category (transaction_type, item_name, item_type, received_by, time_of_sale) untuk efisiensi memori dan analisis lanjutan.
-Evaluasi outlier
-Outlier pada transaction_amount dianalisis menggunakan metode IQR.
-Persentase outlier dihitung dan dinilai masih dalam batas aman (<5%), sehingga data tidak dihapus agar informasi transaksi tetap terjaga.

3.Analisis Lanjutan (Advanced EDA)

-Pairplot dan korelasi
-Menganalisis hubungan antara item_price, quantity, dan transaction_amount berdasarkan kategori produk.
-Grouping dan agregasi
-Mengelompokkan data berdasarkan item_type, time_of_sale, dan transaction_type.
-Menghitung total revenue, rata-rata transaksi, total quantity, dan jumlah transaksi.
-Deteksi outlier per kelompok yang bertujuan untuk membuat fungsi khusus untuk mendeteksi outlier berdasarkan kelompok (misalnya per waktu penjualan).

4.Hasil yang Diperoleh

-Dataset berhasil dibersihkan dan divalidasi
-Missing value pada transaction_type berhasil ditangani.
-Tidak ditemukan data duplikat.
-Format tanggal sudah konsisten dan siap dianalisis.
-Tipe data telah dioptimalkan.
-Diperoleh insight bisnis awal
-Distribusi metode pembayaran dapat dipetakan dengan lebih akurat.
-Pola penjualan berdasarkan waktu transaksi dapat dianalisis.
-Hubungan antara harga, kuantitas, dan total transaksi dapat terlihat melalui visualisasi.
-Performa kategori produk dapat dibandingkan melalui agregasi revenue dan jumlah transaksi.

5.Output akhir

-Dataset bersih (dataclean_final) siap digunakan untuk analisis lanjutan, dashboard, atau model analitik.
-Notebook EDA berisi dokumentasi proses eksplorasi, cleaning, visualisasi, dan interpretasi hasil.
