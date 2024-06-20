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
Home Credit Indonesia merupakan perusahaan yang memberikan layanan kredit  yang mudah, cepat, dan terjangkau kepada masyarakat. Salah satu permasalahan yang terjadi pada perusahaan ini adalah adanya nasabah yang gagal dalam pembayaran kredit. Apabila banyak pelanggan yang mengalami masalah ini, maka akan berdampak secara signifikan bagi perusahaan.

Menurut artikel yang diterbitkan di Harvard Business Review, dinyatakan bahwa "*Non-payment by consumers can set off a chain reaction of bad debts, lower profits, layoffs, and even bankruptcies, ultimately affecting entire industries and even economies.*" 

Oleh karena itu, mengidentifikasi nasabah yang memiliki kemungkinan besar mengalami kegagalan dalam membayar kredit penting untuk dilakukan. Hal ini dapat menjadi tindakan preventif bagi perusahaan dan memastikan pelanggan yang mampu melakukan pelunasan tidak ditolak ketika melakukan pengajuan pinjaman.

### Goals
- Loss Reduction, mengurangi dampak kerugian yang ditimbulkan oleh "Default Customer" yang memiliki potensi gagal bayar.
- Memutuskan bahwa pengajuan pinjaman dapat diterima atau ditolak
  
### Objectives
- Membuat prediktif model untuk memprediksi dan mengklasifikasikan nasabah berpotensi gagal bayar atau tidak
- Mengidentifikasi karakteristik nasabah yang berpotensi gagal bayar
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
