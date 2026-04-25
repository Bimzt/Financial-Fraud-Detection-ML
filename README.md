# Financial-Fraud-Detection-ML

# End-to-End Machine Learning: Deteksi Anomali & Fraud Transaksi Keuangan

[![Python](https://img.shields.io/badge/Python-3.x-blue.svg)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-orange.svg)](https://scikit-learn.org/)
[![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-F37626.svg)](https://jupyter.org/)

Repositori ini berisi proyek akhir *Machine Learning* yang berfokus pada **Deteksi Anomali (Fraud Detection)** pada data transaksi keuangan. Proyek ini dikembangkan secara *End-to-End*, mulai dari eksplorasi data, *Clustering* untuk menemukan pola anomali, hingga pembuatan model *Klasifikasi* prediktif.

## Deskripsi Proyek
Seiring dengan meningkatnya volume transaksi digital, risiko penipuan (*fraud*) juga semakin tinggi. Proyek ini bertujuan untuk mengidentifikasi aktivitas transaksi yang mencurigakan menggunakan pendekatan Machine Learning. 

Proyek ini dibagi menjadi dua tahapan utama:
1. **Clustering (Unsupervised Learning):** Menggunakan algoritma **K-Means** dan **PCA** (Principal Component Analysis) untuk mengelompokkan transaksi ke dalam beberapa profil dan mengidentifikasi cluster yang merepresentasikan anomali/fraud.
2. **Klasifikasi (Supervised Learning):** Menggunakan target hasil dari tahapan clustering untuk melatih model prediktif (seperti **Decision Tree** dan **Random Forest**) guna mendeteksi transaksi penipuan secara otomatis di masa depan.

## Tujuan
- Menggali *insight* dari data profil nasabah dan perilaku transaksi.
- Membangun model *Clustering* untuk pelabelan otomatis data transaksi (Normal vs. Fraud).
- Membangun dan menguji model *Klasifikasi* dengan akurasi tinggi.
- Mengevaluasi model dan melakukan *Hyperparameter Tuning* untuk performa yang lebih optimal.

## Informasi Dataset
Dataset yang digunakan mencakup gambaran perilaku transaksi keuangan nasabah dengan total **2.512 sampel**. Fitur-fitur yang terdapat di dalam dataset antara lain:
- `TransactionAmount`: Nilai transaksi.
- `TransactionType`: Tipe transaksi (`Credit` / `Debit`).
- `Location`: Lokasi transaksi berlangsung.
- `Channel`: Kanal yang digunakan (`Online`, `ATM`, dll).
- `CustomerAge` & `CustomerOccupation`: Profil demografi nasabah.
- `TransactionDuration` & `LoginAttempts`: Indikator teknis saat transaksi.
- `AccountBalance`: Saldo akun pasca-transaksi.

## Teknologi & Library yang Digunakan
- **Bahasa Pemrograman:** Python 3
- **Manipulasi & Analisis Data:** Pandas, NumPy
- **Visualisasi Data:** Matplotlib, Seaborn, Yellowbrick
- **Machine Learning:** Scikit-Learn (K-Means, PCA, Decision Tree, Random Forest)
- **Deployment/Model Saving:** Joblib

## Struktur Repositori
```text
 📂 BMLP_Bima Setia Sugiharto/
  ┣ 📜 [Clustering]_Submission_Akhir_BMLP_Bima_Setia_Sugiharto.ipynb  # Notebook tahap Clustering
  ┣ 📜 [Klasifikasi]_Submission_Akhir_BMLP_Bima_Setia_Sugiharto.ipynb # Notebook tahap Klasifikasi
  ┣ 📊 data_clustering.csv                                            # Data hasil clustering
  ┣ 📊 data_clustering_inverse.csv                                    # Data inverse transform hasil clustering
  ┣ 💾 model_clustering.h5                                            # Model K-Means tersimpan
  ┣ 💾 PCA_model_clustering.h5                                        # Model PCA tersimpan
  ┣ 💾 decision_tree_model.h5                                         # Model Decision Tree tersimpan
  ┣ 💾 explore__Random-Forest__classification.h5                      # Model Random Forest tersimpan
  ┣ 💾 tuning_classification.h5                                       # Model terbaik hasil hyperparameter tuning
  ┗ 📜 README.md
```
## Cara Menjalankan Proyek
**1. Clone repositori ini ke lokal machine kamu:**
```bash
git clone [https://github.com/Bimzt/Financial-Fraud-Detection-ML.git](https://github.com/Bimzt/Financial-Fraud-Detection-ML.git)
```

**2. Pastikan kamu sudah menginstal semua pustaka yang dibutuhkan:**
```bash
pip install pandas numpy scikit-learn matplotlib seaborn yellowbrick joblib
```

**3. Buka Jupyter Notebook atau Google Colab.**
**4. Jalankan notebook secara berurutan:**
- Mulai dari ```Clustering_Bima_Setia_Sugiharto.ipynb``` untuk memahami proses rekayasa fitur dan pengelompokan data.
- Dilanjutkan dengan ```Klasifikasi_Bima_Setia_Sugiharto.ipynb``` untuk melihat evaluasi dari algoritma klasifikasi.
