# Laporan Proyek Machine Learning -  Juli Arsi Sabrina
## 🧠 Domain Proyek
Domain yang dipilih untuk proyek machine learning ini adalah di bidang **Kesehatan**, dengan judul **Predictive Analytics: Prediksi Diabetes** (Klasifikasi).
### Latar Belakang
![diabetes](https://github.com/user-attachments/assets/edd760e8-6e88-4bc2-91b2-66e9a9929add)

Diabetes merupakan penyakit kronis yang berdampak signifikan terhadap kesehatan global. Menurut Organisasi Kesehatan Dunia (WHO), jumlah penderita diabetes terus meningkat secara global, termasuk di kalangan masyarakat. Mendeteksi diabetes secara dini sangat penting untuk mencegah komplikasi yang serius, seperti kerusakan ginjal, penyakit kardiovaskular, dan kebutaan.

Prediksi diabetes dapat membantu tenaga medis dan pengambil kebijakan dalam memberikan intervensi dini serta meningkatkan kualitas hidup pasien. Dalam konteks ini, pendekatan Machine Learning (ML) digunakan untuk membangun model prediksi berbasis data medis guna mempermudah identifikasi risiko diabetes pada masyarakat Pima.

Berdasarkan penelitian yang dilakukan oleh Smith et al. (1988), dataset Pima Indians Diabetes dari Kaggle merupakan kumpulan data yang sering digunakan dalam penelitian prediksi diabetes. Dataset ini memuat parameter kesehatan seperti tekanan darah, kadar glukosa, dan indeks massa tubuh (BMI), yang merupakan faktor risiko penting dalam diagnosis diabetes.

## 💼 Business Understanding
### Problem Statements
Jumlah penderita diabetes yang terus meningkat menimbulkan tantangan serius dalam hal pencegahan, diagnosis dini, dan pengelolaan penyakit. Data historis dari pasien sering kali belum dimanfaatkan secara maksimal untuk membuat prediksi berbasis data, padahal data tersebut dapat digunakan untuk deteksi dini risiko diabetes. Hal ini memunculkan beberapa pertanyaan penting, di antaranya:
- Bagaimana membangun model klasifikasi yang mampu memprediksi kemungkinan seseorang mengidap diabetes berdasarkan data klinis atau data personal?
- Sejauh mana model dapat diandalkan dalam konteks evaluasi risiko secara preventif?
### Goals
Proyek ini bertujuan untuk:
- Mengembangkan model klasifikasi yang mampu memprediksi apakah seseorang berisiko diabetes berdasarkan data input seperti usia, BMI, tekanan darah, dan faktor-faktor lainnya.
- Membandingkan kinerja dua algoritma klasifikasi yang berbeda untuk menentukan model mana yang paling efektif dan akurat serta dapat memberikan wawasan terhadap faktor-faktor yang berkontribusi besar terhadap prediksi risiko diabetes.
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
<p align="center">
  <img src="https://github.com/user-attachments/assets/44781fdf-38ee-46f9-8cbe-7f01b718212b" alt="piechart" width="400"/>
  <br>
  <em>Gambar 1. PieChart Distribusi Outcome</em>
</p>
Berdasarkan Visualisasi piechart menunjukan jumlah penderita diabetes yaitu mencapai 149 orang (26.8%) dan yang tidak memiliki penyakit diabetes yaitu 407 orang (73.2) dari total 556 sample dari dataset.

<p align="center">
  <img src="https://github.com/user-attachments/assets/71c02794-56ee-4244-bdfd-5ba2bdc41fb8" alt="piechart" width="400"/>
  <br>
  <em>Gambar 2. Histogram Feature Numerik</em>
</p>

Berdasarkan Visualisasi Gambar 2, distribusi data numerik menunjukkan bahwa Pregnancies sebagian besar berada di 0–3, sementara Glucose terdistribusi antara 80-120. BloodPressure sebagian besar berada di kisaran 70-80 mmHg, sedangkan SkinThickness banyak memiliki nilai 0, yang menandakan data hilang atau rendah. Insulin sebagian besar memiliki nilai rendah, dengan beberapa nilai ekstrem. BMI terdistribusi di kisaran 20-40 dengan puncak di sekitar 30. Diabetes Pedigree Function sebagian besar berada di sekitar 0.2, dan Age mayoritas berada di kisaran 20-30 tahun.
- Multivariate Analysis
<p align="center">
  <img src="https://github.com/user-attachments/assets/4ba43d48-ecd8-4e38-bc83-24947c4c8e9a" alt="piechart" width="400"/>
  <br>
  <em>Gambar 3. Visualisasi Multivariat Analysis</em>
</p>
Berdasarkan analisis multivariat yang ditunjukkan oleh pairplot dan matriks korelasi, dapat dilihat adanya hubungan yang cukup signifikan antara berbagai variabel dalam dataset Pima Indians Diabetes. Pada Pregnancies dan Age, terlihat adanya korelasi positif yang cukup kuat, yang menunjukkan bahwa semakin tua usia seseorang, semakin banyak jumlah kehamilan yang dimiliki. Hubungan antara Glucose dan BMI juga moderat, yang menunjukkan bahwa kadar glukosa cenderung lebih tinggi pada individu dengan BMI yang lebih tinggi. Selain itu, Insulin dan SkinThickness memiliki korelasi positif yang lebih tinggi, yang mengindikasikan bahwa pasien dengan kadar insulin tinggi cenderung memiliki ketebalan kulit lebih 

<p align="center">
  <img src="https://github.com/user-attachments/assets/9163ccdd-be15-4200-8111-be81ed4007c4" alt="piechart" width="400"/>
  <br>
  <em>Gambar 4. Matriks Korelasi</em>
</p>
Pada Gambar 4, Pregnancies dan Age menunjukkan korelasi yang kuat (0.64), mempertegas temuan bahwa semakin tua usia pasien, semakin banyak kehamilan yang dimiliki. Selain itu, BMI dan Insulin memiliki korelasi tinggi (0.49), menunjukkan bahwa pasien dengan BMI yang lebih tinggi cenderung memiliki kadar insulin yang lebih tinggi.

Secara keseluruhan, analisis ini mengungkapkan bahwa ada hubungan yang kuat dan moderat antara beberapa variabel, terutama antara Age, Pregnancies, Glucose, BMI, yang memberikan wawasan penting dalam memahami faktor-faktor yang berkontribusi terhadap risiko diabetes pada pasien dalam dataset ini.

## 🧹 Data Preparation
Data Preparation adalah proses dalam mempersiapkan data mentah agar dapat digunakan untuk analisis atau pemodelan lebih lanjut. Berikut beberapa teknik yang digunakan dalam persiapan data pada proyek ini:
- Penanganan Outliers
<p align="center">
  <img src="https://github.com/user-attachments/assets/767f0dd4-d5ab-4cf6-a6ef-15c2929f11f7" width="45%" />
  <img src="https://github.com/user-attachments/assets/23f4fc8d-38c3-4469-8f10-692c81ee7bde" width="45%" />
  <br>
  <em>Gambar 1. Visualisasi Missing Value</em>
</p>
Outliers adalah data yang memiliki nilai jauh lebih tinggi atau lebih rendah dibandingkan dengan sebagian besar data lainnya dalam sebuah dataset. Pada proyek ini, meskipun tidak ditemukan missing value maupun duplikat data, namun terdapat beberapa outliers yang perlu ditangani agar model yang dibangun tetap akurat. Outliers bisa muncul karena berbagai alasan, seperti kesalahan pengukuran, data yang tidak sesuai, atau kejadian yang jarang terjadi.
Untuk menangani outliers, salah satu metode yang digunakan adalah IQR (Interquartile Range). IQR adalah selisih antara kuartil ketiga (Q3) dan kuartil pertama (Q1).
(gambar)
Dengan menggunakan metode IQR, dataset ini dapat dibersihkan dari outliers yang berpotensi merusak kualitas model, sehingga analisis dan pemodelan yang dilakukan lebih dapat diandalkan. Setelah penanganan outliers, dataset menjadi lebih konsisten dan siap digunakan dalam proses analisis lebih lanjut atau pembuatan model prediksi yang lebih baik.

- Data Splitting

Data Splitting adalah proses membagi dataset menjadi dua bagian: satu untuk pelatihan model dan satu lagi untuk pengujian model. Pada proyek ini, pembagian dilakukan menggunakan metode Train-Test Split dengan proporsi 80:20 untuk data pelatihan dan data pengujian. Hal ini bertujuan untuk memastikan bahwa model yang dibangun dapat dievaluasi dengan data yang terpisah dari data pelatihan, sehingga memberikan gambaran yang lebih objektif tentang kinerjanya.
###### Distribusi Kelas
| Dataset       | Kelas | Jumlah |
|---------------|-------|--------|
| Data Pelatihan (`y_train`) | 0     | 324    |
|               | 1     | 120    |
| Data Pengujian (`y_test`)  | 0     | 83     |
|               | 1     | 29     |
- Standardisasi

Proses **standardisasi** dimulai dengan menginisialisasi objek `StandardScaler`, yang bertujuan untuk menormalkan data agar memiliki skala yang seragam. Langkah pertama adalah melakukan **fitting dan transformasi** pada data latih (X\_train) menggunakan `fit_transform()`, yang menghitung rata-rata dan standar deviasi pada data latih, kemudian mentransformasi data tersebut menjadi data dengan rata-rata 0 dan standar deviasi 1. Setelah itu, data uji (X\_test) ditransformasi menggunakan `transform()` agar distandarisasi dengan parameter yang sama seperti data latih.
##### Dataframe hasil Standarisasi
| Pregnancies | Glucose  | BloodPressure | SkinThickness | Insulin  | BMI     | DiabetesPedigreeFunction | Age     | Outcome |
|--------------|----------|---------------|---------------|----------|---------|--------------------------|---------|---------|
| -1.139048    | -0.296986 | -0.922834     | 0.580369      | 0.135153 | 0.772158| 1.515812                 | -0.672165 | 1       |
| -1.139048    | -0.048581 | -0.407485     | -1.371289     | -0.857601| 0.251391| -0.587158                | -0.877139 | 1       |
| -0.832726    | 0.199825  | 1.547758      | 1.295977      | 1.423050 | 2.145089| 0.418229                 | -0.569679 | 0       |
| 1.311526     | 1.524654  | 0.597531      | 0.710480      | 1.959674 | 1.766349| 0.457742                 | 0.455189  | 1       |
| -1.139048    | 0.945041  | -0.352697     | -0.460515     | 1.127907 | -1.089978| -1.179853                | -1.082112 | 0       |

Standarisasi ini penting untuk memastikan bahwa semua fitur memiliki rentang nilai yang seragam, yang memungkinkan model machine learning untuk bekerja lebih efektif, terutama untuk algoritma yang sensitif terhadap perbedaan skala fitur.

## 🤖 Modeling
Pada tahap ini, dilakukan pembangunan model machine learning untuk menyelesaikan permasalahan klasifikasi pada dataset yang telah melalui proses pra-pemrosesan sebelumnya. Dua algoritma yang digunakan dalam proses modeling adalah Support Vector Machine (SVM) dengan kernel linear dan Logistic Regression.
#### 1. Tahapan dan Parameter Pemodelan
- Support Vector Machine (SVM)

Proses pelatihan dilakukan dengan membagi data menjadi data latih dan data uji (dengan: 80:20). Model SVM dilatih untuk menemukan hyperplane terbaik yang memisahkan dua kelas secara maksimal.
- Logistic Regression

Model Logistic Regression dilatih untuk mempelajari hubungan linier antara fitur input dan probabilitas terklasifikasinya data ke masing-masing kelas target.

#### 2. Evaluasi Awal dan Perbandingan Akurasi

| Model                | Akurasi (%) |
|----------------------|-------------|
| SVM (Linear Kernel)  | 82.14       |
| Logistic Regression  | 83.04       |

Hasil evaluasi awal menunjukkan bahwa Logistic Regression sedikit lebih unggul dalam akurasi, walaupun perbedaannya relatif kecil.

---

#### 3. Kelebihan dan Kekurangan Setiap Algoritma

| Algoritma            | Kelebihan                                                                 | Kekurangan                                                                 |
|----------------------|---------------------------------------------------------------------------|----------------------------------------------------------------------------|
| **SVM**              | • Akurat pada data berdimensi tinggi<br>• Margin optimal                  | • Kurang interpretatif<br>• Kurang efisien pada dataset besar             |
| **Logistic Regression** | • Cepat dan sederhana<br>• Mudah diinterpretasikan                     | • Tidak optimal untuk data yang tidak linier<br>• Rentan terhadap outlier |

## 📊 Evaluation
### Metrik Evaluasi yang Digunakan
Dalam evaluasi model klasifikasi, digunakan beberapa metrik utama yang diperoleh dari classification report, yaitu:
- Precision: Proporsi prediksi positif yang benar-benar positif.
- Recall: Proporsi data positif yang berhasil ditemukan oleh model.
- F1-Score: Harmonik rata-rata antara precision dan recall, memberikan keseimbangan antara keduanya.
- Accuracy: Proporsi prediksi yang benar secara keseluruhan.
#### Hasil Evaluasi Model
##### Support Vector Machine (SVM) dengan Kernel Linear
| Kelas    | Precision | Recall | F1-Score | Support |
|----------|-----------|--------|----------|---------|
| 0        | 0.85      | 0.93   | 0.89     | 83      |
| 1        | 0.71      | 0.52   | 0.60     | 29      |
| **Accuracy** |           |        | **0.82** | 112     |

Model SVM menunjukkan performa baik pada kelas 0 dengan precision dan recall tinggi, namun performa menurun pada kelas 1, khususnya recall yang rendah (0.52). Hal ini menunjukkan model masih kesulitan mendeteksi beberapa sampel kelas 1 (false negatives cukup tinggi).

##### Logistic Regression
| Kelas    | Precision | Recall | F1-Score | Support |
|----------|-----------|--------|----------|---------|
| 0        | 0.85      | 0.94   | 0.89     | 83      |
| 1        | 0.75      | 0.52   | 0.61     | 29      |
| **Accuracy** |           |        | **0.83** | 112     |

Model Logistic Regression memiliki performa serupa dengan SVM, dengan sedikit peningkatan pada precision kelas 1 (0.75) dan akurasi keseluruhan (83%). Namun, recall untuk kelas 1 tetap rendah, mengindikasikan tantangan yang sama dalam mendeteksi kelas minoritas.

#### Perbandingan Akurasi
<p align="center">
  <img src="https://github.com/user-attachments/assets/f2923529-664d-4824-939f-11e0a62a94be" alt="piechart" width="400"/>
  <br>
  <em>Gambar 1. Visualisasi Perbandingan Akurasi</em>
</p>
Kedua model memiliki performa yang cukup baik dengan akurasi di atas 80%. Meskipun perbedaan akurasi antara keduanya tidak signifikan (sekitar 0.9%), Logistic Regression menunjukkan hasil yang sedikit lebih baik dibandingkan SVM dalam konteks Pima Indias Dataset.

