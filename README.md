#Prediktif Pemeliharaan Analisis
Proyek ini bertujuan untuk melakukan analisis pemeliharaan prediktif menggunakan dataset yang berisi informasi tentang berbagai kondisi operasi dan kegagalan alat. Analisis ini melibatkan langkah-langkah preprocessing data, eksplorasi data, engineering fitur, pengembangan model, dan evaluasi model.
Langkah-langkah
1.	Pengaturan Awal
o	Mengimpor library yang diperlukan: numpy, pandas, seaborn, matplotlib, dan warnings.
o	Menonaktifkan peringatan yang tidak perlu untuk kenyamanan tampilan.
2.	Konfigurasi Tampilan DataFrame
o	Mengatur tampilan pandas agar semua kolom dan baris dapat ditampilkan.
3.	Memuat dan Membersihkan Data
o	Membaca dataset dari file CSV.
o	Menghapus kolom yang tidak diperlukan: UDI dan Product ID.
4.	Mengonversi Suhu dari Kelvin ke Celsius
o	Mengonversi kolom suhu udara dan suhu proses dari Kelvin ke Celsius.
o	Mengganti nama kolom sesuai dengan satuan yang baru.
5.	Menambahkan Fitur Baru
o	Menambahkan kolom baru yang menghitung perbedaan suhu antara suhu proses dan suhu udara.
6.	Memeriksa Informasi Dataset
o	Memeriksa ukuran dataset.
o	Menampilkan informasi umum tentang dataset, termasuk tipe data dan jumlah nilai yang tidak kosong.
7.	Eksplorasi Data
o	Memvisualisasikan nilai yang hilang dalam dataset menggunakan missingno.
o	Membuat distribusi histogram untuk kolom suhu udara, suhu proses, dan perbedaan suhu.
o	Memeriksa distribusi nilai kategorikal seperti Type, Target, dan Failure Type.
8.	Visualisasi Data Kategorikal
o	Membuat count plot dan pie chart untuk kolom Type dan Target.
9.	Visualisasi Hubungan Antar Fitur
o	Membuat scatter plot untuk menggambarkan hubungan antara torsi dan kecepatan rotasi berdasarkan Failure Type, Target, dan Type.
10.	Engineering Fitur
o	Membuat histogram dan boxplot untuk memahami distribusi torsi dan kecepatan rotasi.
11.	Encoding Variabel Kategorikal
o	Menggunakan OrdinalEncoder untuk meng-encode kolom Type dan Failure Type.
o	Menggunakan LabelEncoder untuk meng-encode kolom Failure Type.
12.	Mempersiapkan Data untuk Pelatihan Model
o	Membagi dataset menjadi fitur (X) dan target (y).
o	Membagi data menjadi set pelatihan dan pengujian dengan rasio 80:20.
13.	Pengembangan Model
o	Melatih model Regresi Logistik, Pohon Keputusan, dan Hutan Acak.
o	Mengevaluasi akurasi pelatihan dan akurasi model pada data uji.
o	Menampilkan laporan klasifikasi untuk setiap model.
14.	Evaluasi Model
o	Membuat DataFrame untuk membandingkan akurasi pelatihan dan akurasi model dari ketiga model yang digunakan.
15.	Prediksi
o	Menggunakan model Hutan Acak untuk melakukan prediksi pada data uji.
Menjalankan Kode
1.	Pastikan semua library yang diperlukan sudah terinstal. Jika belum, instal menggunakan pip:
bash
Salin kode
pip install numpy pandas seaborn matplotlib missingno category_encoders scikit-learn
2.	Letakkan file predictive_maintenance.csv di direktori yang sesuai (/content/sample_data/).
3.	Jalankan setiap sel kode secara berurutan, dimulai dari impor library hingga prediksi akhir.
4.	Perhatikan hasil visualisasi dan metrik evaluasi yang ditampilkan untuk memahami performa masing-masing model.
Catatan
•	Pastikan dataset sudah bersih dan terstruktur dengan baik sebelum menjalankan analisis.
•	Visualisasi sangat penting untuk memahami distribusi data dan hubungan antar fitur.
•	Evaluasi model dilakukan untuk memilih model dengan performa terbaik berdasarkan akurasi dan laporan klasifikasi.
________________________________________
Dengan mengikuti langkah-langkah di atas, Anda akan dapat melakukan analisis pemeliharaan prediktif menggunakan dataset yang disediakan.

