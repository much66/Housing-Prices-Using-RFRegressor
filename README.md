# Housing Price Regression

**Dataset** : [source](https://www.kaggle.com/competitions/home-data-for-ml-course/data) <br>
**Notebook** : [view](https://github.com/much66/Housing-Prices-Using-RFRegressor/blob/main/Housing%20Prices%20Regression.ipynb)<br>
**Dashboard** : [view](https://lookerstudio.google.com/reporting/8ca7f8ae-8867-4555-824b-7d8e8834dd4c)<br>

<br>

**Table of Contents**
- [Business Understanding](https://github.com/much66/Housing-Prices-Using-RFRegressor/blob/main/README.md#-business-understanding)
- [Workflow](https://github.com/much66/Housing-Prices-Using-RFRegressor/blob/main/README.md#-workflow)
- [Insight](https://github.com/much66/Housing-Prices-Using-RFRegressor/blob/main/README.md#-insight)
- [Modeling and Evaluation](https://github.com/much66/Housing-Prices-Using-RFRegressor/blob/main/README.md#-modeling-and-evaluation)
- [Recommendation](https://github.com/much66/Housing-Prices-Using-RFRegressor/blob/main/README.md#-recommendations)
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
  
b. Mengidentifikasi Faktor Kunci Penentu Harga:
- Melakukan eksplorasi dan analisis data secara menyeluruh untuk memahami hubungan antara berbagai fitur dan harga rumah.
- Mengidentifikasi dan merangking variabel-variabel yang paling signifikan yang mempengaruhi harga rumah melalui analisis kepentingan fitur.
<br>


## 📂 Workflow

<p align="center">
    <kbd> <img width="1000" alt="workflow" src="Workflow.png"> </kbd> <br>
    Gambar 1 — Workflow Model
</p>

<br>

## 📂 Insight
- Distribusi Harga Rumah: Rata - rata harga rumah di dataset ini adalah $176,000, dengan harga tertinggi mencapai $446,000 dan harga terendah $34,900.
- Faktor Utama yang Mempengaruhi Harga Rumah:
  - Kualitas Material dan Selesai: Rumah dengan kualitas material dan selesai yang lebih tinggi (misalnya, OverallQual dan OverallCond) memiliki harga yang signifikan lebih tinggi.
  - Ukuran Rumah: Luas lantai di atas tanah (GrLivArea) dan total luas area keseluruhan bangunan (TotalSF) secara signifikan berkontribusi terhadap harga rumah.
  - Lokasi: Zoning Classification, seperti di lingkungan Floating Village, menunjukkan harga yang lebih tinggi dibandingkan dengan lingkungan lainnya.
  - Fitur Ekstra: Keberadaan fitur tambahan seperti garasi (GarageCars), kolam renang (PoolArea), dan renovasi terbaru (YearRemodAdd) juga meningkatkan nilai rumah.
<br>

## 📂 Modeling and Evaluation
- Split dataset dengan rasio 75% Train : 25% Test
- Handling Missing Values: Mengisi nilai yang hilang dengan metode yang sesuai, seperti median untuk nilai numerik dan modus untuk nilai kategorikal.
- Feature Engineering: Membuat fitur baru yang mungkin relevan seperti umur rumah (YearBuilt).
- Scaling Data: Menggunakan Z-Score normalization untuk menormalkan data agar mengatasi outliers.
- Algoritma XGBoost Regressor dan Random Forest Regressor digunakan sebagaim 2 model komparasi untuk regressi pada penentuan harga rumah ini.
- Hyperparameter Tuning menggunakan grid search untuk meningkatkan performa model.
- Hasil akhir menunjukan performa dari Random Forest Regressor lebih baik dibanding XGBoost dengan R2 Score sebesar 91.6% dan good fit, dibanding XGBoost yang memiliki R2 Score 95% namun model terindikasi overfit.
<br>



<div align="center">
    <div style="margin-right: 10px;">
        <kbd> <img width="400" alt="feats" src="XGBoost.png"> </kbd> <br>
        Gambar 2 — Final XGBoost Evaluation
    </div>
  <br><br>
    <div style="margin-left: 10px;">
        <kbd> <img width="400" alt="feats" src="Random Forest.png"> </kbd> <br>
        Gambar 3 — Final Random Forest Evaluation
    </div>
</div>

<br>


## 📂 Recommendations
- Penentuan Harga Rumah dengan Random Forest Regressor:
    - Gunakan model Random Forest Regressor untuk mengevaluasi faktor-faktor yang paling berpengaruh terhadap penentuan harga rumah.
    - Identifikasi variabel-variabel yang memiliki kontribusi signifikan dalam menentukan harga rumah berdasarkan analisis model Random Forest.
- Fokus pada Kualitas dan Ukuran:
   - Pertimbangkan untuk meningkatkan kualitas material dan penyelesaian rumah, seperti memperbaiki atau mengganti elemen-elemen utama yang dapat meningkatkan `OverallQual` dan `OverallCond`.
   - Perluas ruang lantai di atas tanah (`GrLivArea`) dan pertimbangkan untuk memperbesar lahan (`LotArea`) jika memungkinkan, karena ini merupakan faktor signifikan dalam meningkatkan nilai rumah.
- Perawatan dan Pemeliharaan Rumah:
   - Pertimbangkan untuk melakukan renovasi atau pemeliharaan secara rutin, karena rumah yang lebih terurus dan diperbarui (`YearRemodAdd`) menunjukkan nilai yang lebih tinggi. Rumah yang terawat dengan baik cenderung memiliki harga jual yang lebih baik di pasar.
 
## 📂 Dashboard
 
<p align="center">
    <kbd><a href="https://lookerstudio.google.com/reporting/8ca7f8ae-8867-4555-824b-7d8e8834dd4c" target="_blank"><img width="1000" alt="Dashboard" src="Dashboard.jpg"></a></kbd> <br>
    Gambar 4 — Housing Price Dashboard
</p>

