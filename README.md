# Prediksi Penyakit Jantung Menggunakan Algoritma K-Nearest Neighbor (KNN)

## Domain Proyek

Penyakit jantung adalah penyebab kematian tertinggi di dunia dan Indonesia. Deteksi dini sangat penting untuk menurunkan angka kematian dan komplikasi serius. Machine learning, khususnya KNN, kini digunakan untuk membantu skrining dan diagnosis otomatis penyakit jantung, sehingga masyarakat dan tenaga medis bisa mendapatkan hasil lebih cepat dan objektif.

## Referensi

* Agustiyar, A. (2023). Prediksi Penyakit Jantung Menggunakan Attribute Weighting k-Nearest Neighbor. InComTech, 13(2), 145-154.
* Sunarko, V. I., dkk. (2025). Implementasi K-Fold Dalam Prediksi Hasil Produksi Agrikultur Pada Algoritma KNN. INTEGER: Journal of Information Technology, 10(1), 10-16.
* Helilintar, R., dkk. (2017). Perancangan Sistem Diagnosa Penyakit Hepatitis Menggunakan Metode KNN. Jurnal Ilmiah ILKOM, 9(2), 145-152.
* Wardhani, A. S., dkk. (2024). Penerapan Model Hibrida CNN-KNN untuk Klasifikasi Penyakit Mata. JATI, 8(3), 3662-3667.
* Hakim, M. A., dkk. (2024). Implementasi Algoritma K-Nearest Neighbors untuk Menganalisis Pendapat Pakar AI. J. Comp & Info Sys Ampera, 5(2), 96-107.

## Business Understanding

### Problem Statement

1. Bagaimana memanfaatkan data rekam medis untuk memprediksi risiko penyakit jantung secara akurat?
2. Apakah pembobotan atribut pada KNN dapat meningkatkan akurasi prediksi penyakit jantung?
3. Bagaimana perbandingan performa model KNN yang dikembangkan dengan penelitian sebelumnya?

### Goals

* Mengembangkan model prediksi risiko penyakit jantung berbasis data rekam medis dengan algoritma KNN.
* Mengevaluasi dampak pembobotan atribut dalam meningkatkan akurasi prediksi.
* Membandingkan hasil model dengan literatur terkini.

### Solution Statement

1. Eksplorasi dataset penyakit jantung: statistik deskriptif, visualisasi, dan analisis awal.
2. Preprocessing data: penanganan missing value, encoding, normalisasi, splitting.
3. Modeling: implementasi KNN klasik dan KNN dengan attribute weighting.
4. Evaluasi: confusion matrix, akurasi, precision, recall, f1-score, serta perbandingan hasil.
5. Interpretasi: insight fitur penting, kelebihan, dan keterbatasan model.

## Data Understanding

### Sumber Dataset

* **heart\_cleveland\_upload.csv** dari [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/heart+Disease)
* Jumlah: 303 data, 14 atribut
* Target: 0 (sehat), 1 (sakit jantung)

| Fitur     | Deskripsi                                         | Tipe Data |
| --------- | ------------------------------------------------- | --------- |
| Age       | Usia pasien (tahun)                               | Numerik   |
| Sex       | Jenis kelamin (1 = laki-laki, 0 = perempuan)      | Kategorik |
| Cp        | Tipe nyeri dada                                   | Kategorik |
| Trestbps  | Tekanan darah istirahat (mm Hg)                   | Numerik   |
| Chol      | Kolesterol serum (mg/dl)                          | Numerik   |
| Fbs       | Gula darah puasa (1 = >120 mg/dl, 0 = ≤120 mg/dl) | Kategorik |
| ...       | ...                                               | ...       |
| Condition | 0 = sehat, 1 = sakit jantung                      | Kategorik |

### Eksplorasi Data (EDA)

* Visualisasi distribusi usia, tekanan darah, kolesterol, jenis kelamin.
* Analisis missing value dan duplikasi: dataset sudah cukup bersih.
* Korelasi fitur dan target divisualisasikan via heatmap.
* Keseimbangan kelas: diperhatikan agar model tidak bias.

## Data Preparation

* Penanganan missing value dan outlier.
* Encoding fitur kategorik (LabelEncoder, OneHotEncoder).
* Normalisasi fitur numerik (Min-Max Scaler / StandardScaler).
* Split data: train/test 80:20 (dengan cross-validation untuk evaluasi lebih robust).
* Penjelasan kode disediakan pada notebook .ipynb.

## Modeling

* Implementasi KNN klasik (tanpa bobot) dan KNN dengan Attribute Weighting (AWKNN).
* Penggunaan *weighted Euclidean distance* untuk KNN berbobot.
* Penentuan hyperparameter k: uji dengan nilai 3, 5, 7, 9.
* Pipeline kode tersedia di notebook .ipynb.
* Evaluasi: confusion matrix, accuracy, precision, recall, f1-score.

## Evaluation

* **KNN klasik**: Akurasi sekitar 65-70% (literatur dan eksperimen awal).
* **KNN + pembobotan atribut**: Akurasi meningkat hingga 79-85% (dari eksperimen kamu & referensi utama).
* Evaluasi hasil dengan metrik lain: precision, recall, f1-score, analisis confusion matrix, serta perbandingan dengan jurnal lain.
* Insight fitur penting: usia dan tekanan darah sangat mempengaruhi prediksi.

## Kesimpulan & Saran

* Model KNN dengan pembobotan atribut terbukti lebih efektif untuk prediksi penyakit jantung berbasis data rekam medis.
* Disarankan eksplorasi dataset lebih besar dan pembanding dengan model lain (Random Forest, SVM, dst).
* Potensi implementasi ke aplikasi skrining mandiri (mobile/website).

## Cara Menjalankan Kode

1. Clone repositori dan install library di `requirements.txt` (jika tersedia).
2. Jalankan notebook **AI\_TB.ipynb** secara urut.
3. Pastikan file **heart\_cleveland\_upload.csv** tersedia dalam direktori yang sama dengan notebook.
4. Ikuti penjelasan pada setiap cell untuk eksperimen, evaluasi, dan visualisasi hasil.

## Struktur Repositori

```
.
├── referensi_jurnal/
│   ├── 129-295-2-PB.pdf
│   ├── 456-Article Text-1324-3-10-20240208.pdf
│   └── dst.
├── AI_TB.ipynb         # Notebook kodingan utama
├── heart_cleveland_upload.csv
├── UAS_AI.pdf          # Laporan lengkap
└── README.md           # File ini
```

## Daftar Pustaka

1. Agustiyar, A. (2023). Prediksi Penyakit Jantung Menggunakan Attribute Weighting k-Nearest Neighbor. *InComTech*, 13(2), 145-154.
2. Sunarko, V. I., dkk. (2025). Implementasi K-Fold Dalam Prediksi Hasil Produksi Agrikultur Pada Algoritma KNN. *INTEGER: Journal of Information Technology*, 10(1), 10-16.
3. Helilintar, R., dkk. (2017). Perancangan Sistem Diagnosa Penyakit Hepatitis Menggunakan Metode KNN. *Jurnal Ilmiah ILKOM*, 9(2), 145-152.
4. Wardhani, A. S., dkk. (2024). Penerapan Model Hibrida CNN-KNN untuk Klasifikasi Penyakit Mata. *JATI*, 8(3), 3662-3667.
5. Hakim, M. A., dkk. (2024). Implementasi Algoritma K-Nearest Neighbors untuk Menganalisis Pendapat Pakar AI. *Journal of Computer and Information Systems Ampera*, 5(2), 96-107.
