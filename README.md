# Laporan Proyek Machine Learning -  Juli Arsi Sabrina
## 🧠 Domain Proyek
Domain yang dipilih untuk proyek machine learning ini adalah di bidang **Kesehatan**, dengan judul **Predictive Analytics: Prediksi Diabetes**.
### Latar Belakang
Diabetes merupakan penyakit kronis yang berdampak signifikan terhadap kesehatan global. Menurut Organisasi Kesehatan Dunia (WHO), jumlah penderita diabetes terus meningkat secara global, termasuk di kalangan masyarakat. Mendeteksi diabetes secara dini sangat penting untuk mencegah komplikasi yang serius, seperti kerusakan ginjal, penyakit kardiovaskular, dan kebutaan.
Prediksi diabetes dapat membantu tenaga medis dan pengambil kebijakan dalam memberikan intervensi dini serta meningkatkan kualitas hidup pasien. Dalam konteks ini, pendekatan Machine Learning (ML) digunakan untuk membangun model prediksi berbasis data medis guna mempermudah identifikasi risiko diabetes pada masyarakat Pima.
Berdasarkan penelitian yang dilakukan oleh Smith et al. (1988), dataset Pima Indians Diabetes dari UCI Machine Learning Repository merupakan kumpulan data yang sering digunakan dalam penelitian prediksi diabetes. Dataset ini memuat parameter kesehatan seperti tekanan darah, kadar glukosa, dan indeks massa tubuh (BMI), yang merupakan faktor risiko penting dalam diagnosis diabetes.

## 💼 Business Understanding
### Problem Statements
Jumlah penderita diabetes yang terus meningkat menimbulkan tantangan serius dalam hal pencegahan, diagnosis dini, dan pengelolaan penyakit. Data historis dari pasien sering kali belum dimanfaatkan secara maksimal untuk membuat prediksi berbasis data, padahal data tersebut dapat digunakan untuk deteksi dini risiko diabetes. Hal ini memunculkan beberapa pertanyaan penting, di antaranya:
- Bagaimana membangun model klasifikasi yang mampu memprediksi kemungkinan seseorang mengidap diabetes berdasarkan data klinis atau data personal?
- Sejauh mana model dapat diandalkan dalam konteks evaluasi risiko secara preventif?
### Goals
Proyek ini bertujuan untuk:
- Mengembangkan model klasifikasi yang mampu memprediksi apakah seseorang berisiko diabetes berdasarkan data input seperti usia, BMI, tekanan darah, dan faktor-faktor lainnya.
- Membandingkan kinerja dua algoritma klasifikasi yang berbeda untuk menentukan model mana yang paling efektif dan akurat.
- Memberikan wawasan terhadap faktor-faktor yang berkontribusi besar terhadap prediksi risiko diabetes.
### Solution Statemnts
- Melakukan analisis data secara mendalam dimulai dari eksplorasi satu variabel (univariate) hingga hubungan antar beberapa variabel (multivariate). Proses ini juga diperkuat dengan penggunaan visualisasi data untuk mendapatkan gambaran yang lebih jelas mengenai distribusi data dan pola yang muncul. Salah satu hal penting dalam tahap ini adalah mengidentifikasi hubungan antar fitur melalui matriks korelasi serta mengenali outlier yang dapat memengaruhi hasil analisis.
- Proyek ini bertujuan membangun model prediksi risiko diabetes yang akurat dan dapat diandalkan. Untuk mencapai tujuan ini, digunakan dua pendekatan algoritma machine learning, yaitu Support Vector Machine (SVM) dengan kernel linear dan Logistic Regression.
1. Support Vector Machine (SVM) dengan Kernel Linear
Support Vector Machine (SVM) adalah algoritma klasifikasi yang bekerja dengan mencari garis pemisah (hyperplane) terbaik yang memisahkan kelas-kelas data. Dalam proyek ini, digunakan kernel linear karena hubungan antar fitur dapat diasumsikan.
2. Logistic Regression
Logistic Regression adalah algoritma klasifikasi yang digunakan untuk memprediksi probabilitas suatu kejadian berdasarkan variabel input. Algoritma ini sangat cocok untuk klasifikasi biner, seperti kasus prediksi diabetes (positif/negatif). Logistic Regression menggunakan fungsi sigmoid untuk mengonversi output linear menjadi probabilitas.

## 🔍 Data Understanding
Dataset yang digunakan dalam proyek ini adalah [Pima Indians Diabetes Dataset](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database), yang diambil dari Kaggle. Dataset ini sering digunakan untuk melakukan klasifikasi dalam mendeteksi risiko diabetes berdasarkan data klinis.
Dataset ini berisi data dari 768 pasien dengan 9 fitur yang digunakan untuk memprediksi apakah seseorang menderita diabetes atau tidak. Setiap baris dalam dataset mewakili satu pasien dengan beberapa variabel yang menjelaskan kondisi klinisnya.
#### Tabel Data
| Pregnancies | Glucose | BloodPressure | SkinThickness | Insulin | BMI  | DiabetesPedigreeFunction | Age | Outcome |
|------------|--------:|--------------:|--------------:|--------:|-----:|--------------------------:|----:|-------:|
| 6          |     148 |            72 |            35 |       0 | 33.6 |                     0.627 |   50 |      1 |
| 1          |      85 |            66 |            29 |       0 | 26.6 |                     0.351 |   31 |      0 |
| 8          |     183 |            64 |             0 |       0 | 23.3 |                     0.672 |   32 |      1 |
| 1          |      89 |            66 |            23 |       94 | 28.1 |                     0.167 |   21 |      0 |
| 0          |     137 |            40 |            35 |     168 | 43.1 |                     2.288 |   33 |      1 |
### Deskripsi Variable
| Kolom                    | Deskripsi                                                                                             |
|-------------------------|----------------------------------------------------------------------------------------------------------|
| Pregnancies              | Jumlah kehamilan yang pernah dialami individu.                                                           |
| Glucose                  | Konsentrasi glukosa plasma (mg/dL) yang diukur selama tes toleransi glukosa oral.                        |
| BloodPressure            | Tekanan darah diastolik (mm Hg).                                                                         |
| SkinThickness            | Ketebalan lipatan kulit (mm) di bagian tricep.                                                           |
| Insulin                  | Kadar insulin serum 2 jam (mu U/ml).                                                                     |
| BMI                      | Indeks Massa Tubuh (BMI).                                                                                |
| DiabetesPedigreeFunction | Fungsi silsilah diabetes, mewakili kemungkinan terkena diabetes berdasarkan riwayat keluarga.            |
| Age                      | Usia individu (tahun).                                                                                  |
| Outcome                  | Label biner yang menunjukkan apakah individu menderita diabetes (1) atau tidak (0).                      |

### Visualization & Analysis
- Univariate Analysis
- Multivariate Analysis
- Outliners
## 🧹 Data Preparation
## 🤖 Modeling
## 📊 Evaluation
