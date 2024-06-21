# Housing Price Regression

**Dataset** : [source](https://www.kaggle.com/competitions/home-data-for-ml-course/data) <br>
**Notebook** : [view](https://github.com/much66/Housing-Prices-Using-RFRegressor/blob/main/Housing%20Prices%20Regression.ipynb)<br>

<br>

**Table of Contents**
- [Business Understanding]()
- [Workflow]()
- [Insight]()
- [Modeling and Evaluation]()
<br>


## 📂 Business Understanding
### Problem Statement
Dalam pasar real estate, berbagai faktor mempengaruhi harga akhir dari sebuah properti residensial selain dari fitur-fitur yang jelas seperti luas tanah dan bangunan atau jumlah kamar. Memahami faktor-faktor ini sangat penting untuk penilaian properti yang akurat dan negosiasi harga yang sukses. Dataset yang disediakan untuk kompetisi ini mencakup 79 variabel yang menangkap hampir setiap aspek dari rumah-rumah residensial di Ames, Iowa. Variabel-variabel ini mencakup atribut fisik, detail lokasi, dan faktor signifikan lainnya yang mempengaruhi harga rumah.

Tantangannya adalah membangun model prediktif yang dapat menentukan harga akhir sebuah rumah dengan akurat berdasarkan variabel-variabel ini. Ini akan membantu agen real estate, pembeli, dan penjual dalam membuat keputusan yang lebih baik, sehingga meningkatkan efisiensi pasar perumahan.

### Goals
a. Pengurangan Kerugian: Mengurangi dampak kerugian yang ditimbulkan oleh penetapan harga rumah yang tidak akurat melalui model prediktif yang dapat diandalkan.
b. Keputusan yang Lebih Baik: Membantu agen real estate, pembeli, dan penjual dalam membuat keputusan yang lebih baik dan berbasis data mengenai harga rumah.
  
### Objectives
a. Membangun Model Prediktif:
- Mengembangkan model regresi yang mampu memprediksi harga akhir rumah dengan akurasi tinggi.
- Menggunakan teknik pemodelan lanjutan seperti XGBoost, Random Forest, dan metode lain untuk meningkatkan performa prediksi.
- 
b. Mengidentifikasi Faktor Kunci Penentu Harga:
- Melakukan eksplorasi dan analisis data secara menyeluruh untuk memahami hubungan antara berbagai fitur dan harga rumah.
- Mengidentifikasi dan merangking variabel-variabel yang paling signifikan yang mempengaruhi harga rumah melalui analisis kepentingan fitur.
<br>


## 📂 Workflow
<p align="center">
    <kbd> <img width="1000" alt="workflow" src="#"> </kbd> <br>
    Gambar 1 — Workflow Pembuatan Model
</p>
<br>

## 📂 Insight
- Tingkat default kredit nasabah dari dataset mencapai 9%
- Karakteristik mayoritas nasabah yang cenderung mengalami masalah dalam pembayaran kredit yaitu:
  - Laki-laki
  - Kelompok pendidikan rendah, "lower secondary"
  - Rentang usia 25 - 40 tahun
  - Lama bekerja 1 - 5 tahun
  - Tipe kredit "Cash Loan"
<br>

## 📂 Modeling and Evaluation
- Split dataset dengan rasio 80% Train : 20% Test
- Mengatasi data Train yang tidak seimbang menggunakan RandomUnderSampler
- Scaling data dengan RobustScaler
- Eksperimen menggunakan beberapa algoritma Logistic Regression, Random Forest, dan XGBoost
- Best fit model didapatkan menggunakan Logistic Regression dengan hyperparameter tuning, menghasilkan akurasi 87% dan AUC 73%

<br>
<p align="center">
    <kbd> <img width="800" alt="feats" src="#"> </kbd> <br>
    Gambar 2 — Feature Importance
</p>
<br>


## 📂 Recommendations
- Mempertimbangkan untuk membuat Credit Scorecard, menggunakan Information Value dan Feature Engineering menggunakan Weight of Evidence
- Melakukan analisis kredit yang lebih mendalam 
- Meningkatkan seleksi calon peminjam dengan memperketat persyaratan dan mengumpulkan informasi yang lebih lengkap tentang calon peminjam
