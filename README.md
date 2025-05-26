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
- Melakukan 

## Modeling
Tahapan ini membahas mengenai model machine learning yang digunakan untuk menyelesaikan permasalahan. Anda perlu menjelaskan tahapan dan parameter yang digunakan pada proses pemodelan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan kelebihan dan kekurangan dari setiap algoritma yang digunakan.
- Jika menggunakan satu algoritma pada solution statement, lakukan proses improvement terhadap model dengan hyperparameter tuning. **Jelaskan proses improvement yang dilakukan**.
- Jika menggunakan dua atau lebih algoritma pada solution statement, maka pilih model terbaik sebagai solusi. **Jelaskan mengapa memilih model tersebut sebagai model terbaik**.

## Evaluation
Pada bagian ini anda perlu menyebutkan metrik evaluasi yang digunakan. Lalu anda perlu menjelaskan hasil proyek berdasarkan metrik evaluasi yang digunakan.

Sebagai contoh, Anda memiih kasus klasifikasi dan menggunakan metrik **akurasi, precision, recall, dan F1 score**. Jelaskan mengenai beberapa hal berikut:
- Penjelasan mengenai metrik yang digunakan
- Menjelaskan hasil proyek berdasarkan metrik evaluasi

Ingatlah, metrik evaluasi yang digunakan harus sesuai dengan konteks data, problem statement, dan solusi yang diinginkan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan formula metrik dan bagaimana metrik tersebut bekerja.

**---Ini adalah bagian akhir laporan---**

_Catatan:_
- _Anda dapat menambahkan gambar, kode, atau tabel ke dalam laporan jika diperlukan. Temukan caranya pada contoh dokumen markdown di situs editor [Dillinger](https://dillinger.io/), [Github Guides: Mastering markdown](https://guides.github.com/features/mastering-markdown/), atau sumber lain di internet. Semangat!_
- Jika terdapat penjelasan yang harus menyertakan code snippet, tuliskan dengan sewajarnya. Tidak perlu menuliskan keseluruhan kode project, cukup bagian yang ingin dijelaskan saja.
