# Laporan Proyek Machine Learning - Ikhzan Wicaksono

## Domain Proyek

- Menurut **[Junita et al.(2020)](https://ejournal.unsrat.ac.id/v3/index.php/msj/article/view/31108/29838)** Kanker paru dalam arti luas adalah semua penyakit keganasan di paru, men-cakup keganasan yang berasal dari paru itu sendiri (primer) maupun keganasan dari luar paru (metastasis). Dalam pengertian klinis yang dimaksud dengan kanker paru primeradalah tumor ganas yang berasal dari epitel bronkus (karsinoma bronkus).
- Dalam penelitian yang dilakukan oleh **[Dony et al.(2024)](https://jointer.id/index.php/jointer/article/view/331/47)** Gangguan pada paru-paru dapat mengurangi efisiensi dan fungsi paru-paru dalam menyerap oksigen dari udara[7]. Strategi deteksi  dini dan intervensi yang cepat sangatlah pentingdalam meminimalisirangka kematian akibatdarikanker  paru-paru. Salah  satu pendekatan  yang dapat digunakan adalah penerapan algoritma dalam bidang machine learning untuk mengidentifikasi kemungkinan adanya kanker paru-paru sejak dini.
- Berdasarkan peneitian tersebut, penerapan teknologi machine learning diharapkan dapat membantu dunia medis dalam mendeteksi penyakit kanker paru sejak dini. Hal ini akan memudahkan keputusan serta tindakan medis yang akan diambil selanjutntya. Tenaga medis dapat juga memberikan saran kesehatan kepada pasien di masa depan terkait gaya hidup yang berpengaruh terhadap penyakit ini. Oleh karena itu, implementasi ini diharapkan memberikan maanfaat besar baik untuk individu maupun dunia medis.

## Business Understanding

### Problem Statements

- Bagaimana memprediksi kemungkinan seseorang menderita kanker paru berdasarkan faktor kesehatan yang dialami?
- Seberapa akurat model machine learning ini dapat memprediksi kanker paru?

### Goals

- Membangun model mechine learning yang dapat memprediksi seseorang mengidap kanker paru berdasarkan faktor kesehatan yang diderita?
- Mengevaluasi kinerja model machine learning dengan berbagai metrik evaluasi seperti akurasi, precision, recall, F1-score, dan confusion matrix untuk memastikan model memiliki performa yang optimal dalam deteksi.


### Solution statements
- Menggunakan algoritma machine learning Random Forest dan XGBoost untuk membandingkan performa model yang lebih optimal dalam mendeteksi kanker paru.
- Membandingkan hasil dengan mengevaluasi metrik untuk memilih model yang paling akurat.

## Data Understanding
Kumpulan data ini merupakan aset yang sangat berharga dalam bidang Perawatan Kesehatan, yang menyediakan landasan terstruktur untuk pengembangan model deteksi kanker. Kumpulan data ini menggambarkan berbagai gejala Kanker Paru-paru. Dataset ini berisikan 16 kolom yang mewakili faktor ataupun gejala dari kanker paru dengan masing-masing kolom berisikan 3000 data, data pun sudah bersih tidak ada missing values. Data ini bersumber dari [Kaggle](https://www.kaggle.com/datasets/akashnath29/lung-cancer-dataset/data) 

### Variabel-variabel pada Lung Cancer dataset adalah sebagai berikut:
- Age : Faktor penting karena usia salah satu faktor yang mempengaruhi meningkatnya kanker paru.
- Gender : Jenis kelamin mengacu pada kerentanan suatu penyakit terhadap jenis kelamin tertentu.
- Smoking Status : Merokok merupakan salah satu faktor pemicu dari meningkatnya resiko kanker.
- Yellow Finger : Menandakan kebiasaan merokok berat dalam jangka panjang. Nikotin meninggalkan noda kuning di jari.
- Anxiety : Meskipun bukan penyebab langsung, kecemasan kronis bisa memperburuk gaya hidup tidak sehat seperti merokok dan alkohol.
- Peer Pressure : Sering menjadi faktor awal seseorang mulai merokok, terutama di usia muda.
- Chronic Disease : Penyakit kronis seperti PPOK (penyakit paru obstruktif kronis) atau TBC bisa merusak paru-paru dan membuat jaringan paru lebih rentan terhadap pertumbuhan sel kanker.
- Fatigue : Kelelahan kronis bisa menjadi gejala awal kanker paru-paru karena tubuh menggunakan energi untuk melawan pertumbuhan sel kanker.
- Allergy : Alergi pernapasan tidak langsung menyebabkan kanker paru, tetapi peradangan kronis berulang di saluran napas bisa memicu kerusakan jaringan dan meningkatkan kerentanan terhadap penyakit serius termasuk kanker.
- Wheezing : Suara napas seperti siulan bisa menandakan penyempitan saluran napas, yang bisa disebabkan oleh tumor paru yang menekan atau menyumbat saluran pernapasan.
- Alcohol Consuming : Konsumsi alkohol berat sering berkorelasi dengan gaya hidup tidak sehat, termasuk merokok—kombinasi ini sangat meningkatkan risiko kanker paru.
- Coughing : Batuk kronis adalah gejala umum kanker paru-paru, terutama jika berlangsung lebih dari beberapa minggu, berdarah, atau memburuk dari waktu ke waktu.
- Shortness of Breath : Bisa terjadi karena tumor mengganggu pertukaran udara di paru-paru, atau akibat efusi pleura (cairan di sekitar paru) yang sering terjadi pada penderita kanker paru.
- Swallowing Difficulty : Bisa terjadi jika kanker menyebar ke tenggorokan atau menekan esofagus. Biasanya gejala lanjut, tapi tetap penting sebagai indikasi medis serius.
- Chest Pain : Tumor paru bisa menekan jaringan atau saraf di rongga dada, menyebabkan nyeri. Nyeri yang bertahan lama atau terasa saat menarik napas dalam harus diwaspadai.

## Data Preparation
- Melakukan label encoding data kategorikal, beberapa fitur kategori dilakukan encoding agar menjadi fitur numerik.
- Melakukan normalisasi data dengan standard scaler agar data tidak memiliki penyimpangan nilai yang terlalu jauh.

## Modeling
Pada studi kasus ini, model yang digunakan adalah Random Forest dan XGBoost untuk memprediksi kemungkinan seseorang mengidap kanker paru berdasarkan fitur-fitur yang ada. Alasan pemilihan model tersebut adalah:
- Random Forest adalah model ensemble yang terdiri dari kumpulan decision tree. Keunggulannya terletak pada kemampuannya menangani data non-linear serta ketahanannya terhadap overfitting. Meski begitu, proses pelatihannya umumnya lebih lambat dibandingkan dengan metode boosting.
- XGBoost adalah algoritma boosting yang dilengkapi dengan teknik regularisasi, sehingga lebih efektif dalam mencegah overfitting dan menghasilkan model yang lebih akurat serta stabil. XGBoost umumya lebih lambat ketimbang Random Forest karena bersifat sekuensial.

Tahapan yang dilakukan saat modeling, yaitu:
1. Load model :
   - **Random Forest** diload dengan parameter `n_estimators=100` dan `random_state=42`:
     ```python
     train_rf = RandomForestClassifier(n_estimators=100, random_state=42)
     ```
   - **XGBoost** diload dengan parameter `random_state=42`:
     ```python
     train_xgb = XGBClassifier(random_state=42)
     ```
2. Train Model :
   - **Random Forest** dilatih dengan data latih yaitu `X_train dan y_train`:
     ```python
     train_rf.fit(X_train, y_train)
     ```
   - **XGBoost** dilatih dengan data latih yaitu `X_train dan y_train`:
     ```python
     train_xgb.fit(X_train, y_train)
     ```
Setelah dilakukan evaluasi, model XGBoost dipilih sebagai model yang paling optimal, karena memiliki akurasi yang lebih baik dibandingkan dengan Random Forest.

## Evaluation
Evaluasi terhadap model dilakukan dengan menggunakan sejumlah metrik utama yang relevan untuk klasifikasi biner, seperti **Accuracy**, **Precision**, **Recall**, **F1-Score**, serta **Confusion Matrix**. Pemilihan metrik-metrik ini didasarkan pada karakteristik dataset yang menuntut keseimbangan dalam mendeteksi kedua kelas, baik positif maupun negatif, secara akurat.
Berikut adalah metrik evaluasi yang digunakan:
1. **Accuracy Score** : Mengukur proporsi prediksi yang benar terhadap seluruh jumlah data.
2. **Classification Report** :
   - **Precision** : Mengukur proporsi prediksi positif yang benar.
   - **Recall (Sensitivity)** : Mengukur proporsi kasus positif yang berhasil dideteksi.
   - **F1-Score** : Menilai rata-rata harmonik antara Precision dan Recall, yang memberikan gambaran keseimbangan antara keduanya.
3. **Confusion Matrix** : Memberikan gambaran menyeluruh tentang jenis kesalahan yang dilakukan model.

Berikut hasil evaluasi dari hasil analisa prediksi data:
1. Accuracy dan Classification Report
    Model       | Precision | Recall | F1-Score | Accuracy
    ------------|-----------|--------|----------|---------
    RandomForest| 0.97      | 0.96   | 0.97     | 0.9667
    XGBoost     | 0.97      | 0.97   | 0.97     | 0.9733

   Analisa Hasil
   - Akurasi (Accuracy) : XGBoost unggul sedikit dengan akurasi 97.33%, dibandingkan Random Forest dengan 96.67%. Perbedaan ini kecil, tetapi tetap menunjukkan bahwa XGBoost sedikit lebih tepat dalam prediksi keseluruhan.
   - Precision : Keduanya memiliki precision yang sama di angka 0.97. Artinya, ketika model memprediksi positif, 97% dari prediksi tersebut benar.
   - Recall : Recall XGBoost lebih tinggi (0.97) dibanding Random Forest (0.96). Ini berarti XGBoost sedikit lebih baik dalam menangkap seluruh kasus positif (lebih sensitif terhadap kasus sebenarnya).
   - F1-Score : Keduanya sama di angka 0.97, menunjukkan keseimbangan antara precision dan recall yang sangat baik.

2. Confusion Matrix
    | Model         | Actual Class      | Predicted Negative (0) | Predicted Positive (1) |
    |---------------|-------------------|--------------------|--------------------|
    | Random Forest | Actual Negative (0) | 73                 | 2                  |
    | Random Forest | Actual Positive (1) | 3                  | 72                 |
    | XGBoost       | Actual Negative (0) | 73                 | 2                  |
    | XGBoost       | Actual Positive (1) | 2                  | 73                 |

   Berdasarkan hasil evaluasi Confusion Matrix menunjukan XGBoost lebih baik dibanding Random Forest, karena memiliki False Negative yang lebih rendah (2 vs 3). Dalam kasus deteksi penyakit seperti kanker paru, mengurangi False Negative sangat krusial untuk memastikan pasien yang sakit tidak luput dari diagnosis. Oleh karena itu, meskipun perbedaan kecil, XGBoost lebih unggul dalam konteks ini.


