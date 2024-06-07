#Prediktif Pemeliharaan Analisis
Proyek ini bertujuan untuk melakukan analisis pemeliharaan prediktif menggunakan dataset yang berisi informasi tentang berbagai kondisi operasi dan kegagalan alat. Analisis ini melibatkan langkah-langkah preprocessing data, eksplorasi data, engineering fitur, pengembangan model, dan evaluasi model.

##Langkah-langkah
Pengaturan Awal

Mengimpor library yang diperlukan: numpy, pandas, seaborn, matplotlib, dan warnings.
Menonaktifkan peringatan yang tidak perlu untuk kenyamanan tampilan.
Konfigurasi Tampilan DataFrame

Mengatur tampilan pandas agar semua kolom dan baris dapat ditampilkan.
Memuat dan Membersihkan Data

Membaca dataset dari file CSV.
Menghapus kolom yang tidak diperlukan: UDI dan Product ID.
Mengonversi Suhu dari Kelvin ke Celsius

Mengonversi kolom suhu udara dan suhu proses dari Kelvin ke Celsius.
Mengganti nama kolom sesuai dengan satuan yang baru.
Menambahkan Fitur Baru

Menambahkan kolom baru yang menghitung perbedaan suhu antara suhu proses dan suhu udara.
Memeriksa Informasi Dataset

Memeriksa ukuran dataset.
Menampilkan informasi umum tentang dataset, termasuk tipe data dan jumlah nilai yang tidak kosong.
Eksplorasi Data

Memvisualisasikan nilai yang hilang dalam dataset menggunakan missingno.
Membuat distribusi histogram untuk kolom suhu udara, suhu proses, dan perbedaan suhu.
Memeriksa distribusi nilai kategorikal seperti Type, Target, dan Failure Type.
Visualisasi Data Kategorikal

Membuat count plot dan pie chart untuk kolom Type dan Target.
Visualisasi Hubungan Antar Fitur

Membuat scatter plot untuk menggambarkan hubungan antara torsi dan kecepatan rotasi berdasarkan Failure Type, Target, dan Type.
Engineering Fitur

Membuat histogram dan boxplot untuk memahami distribusi torsi dan kecepatan rotasi.
Encoding Variabel Kategorikal

Menggunakan OrdinalEncoder untuk meng-encode kolom Type dan Failure Type.
Menggunakan LabelEncoder untuk meng-encode kolom Failure Type.
Mempersiapkan Data untuk Pelatihan Model

Membagi dataset menjadi fitur (X) dan target (y).
Membagi data menjadi set pelatihan dan pengujian dengan rasio 80:20.
Pengembangan Model

Melatih model Regresi Logistik, Pohon Keputusan, dan Hutan Acak.
Mengevaluasi akurasi pelatihan dan akurasi model pada data uji.
Menampilkan laporan klasifikasi untuk setiap model.
Evaluasi Model

Membuat DataFrame untuk membandingkan akurasi pelatihan dan akurasi model dari ketiga model yang digunakan.
Prediksi

Menggunakan model Hutan Acak untuk melakukan prediksi pada data uji.
Menjalankan Kode
Pastikan semua library yang diperlukan sudah terinstal. Jika belum, instal menggunakan pip:
##pip install numpy pandas seaborn matplotlib missingno category_encoders scikit-learn

pip install numpy pandas seaborn matplotlib missingno category_encoders scikit-learn
Letakkan file predictive_maintenance.csv di direktori yang sesuai (/content/sample_data/).

Jalankan setiap sel kode secara berurutan, dimulai dari impor library hingga prediksi akhir.

Perhatikan hasil visualisasi dan metrik evaluasi yang ditampilkan untuk memahami performa masing-masing model.

Catatan
Pastikan dataset sudah bersih dan terstruktur dengan baik sebelum menjalankan analisis.
Visualisasi sangat penting untuk memahami distribusi data dan hubungan antar fitur.
Evaluasi model dilakukan untuk memilih model dengan performa terbaik berdasarkan akurasi dan laporan klasifikasi.
Dengan mengikuti langkah-langkah di atas, Anda akan dapat melakukan analisis pemeliharaan prediktif menggunakan dataset yang disediakan.
