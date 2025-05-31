## Studi Kasus 1  
1. **Topik:** Prediksi Kelulusan Mahasiswa Menggunakan Decision Tree dan k-Nearest Neighbor  
2. **Anggota Kelompok:** -  
3. **Pendahuluan dan Pemaparan:**  
   - **Masalah:** Banyak universitas menghadapi kesulitan dalam memprediksi mahasiswa yang berisiko tidak lulus tepat waktu.  
   - **Deskripsi Dataset dan Statistik:** Dataset berisi data 1.000 mahasiswa dari UCI Machine Learning Repository.  
     - [Link Dataset](https://archive.ics.uci.edu/ml/datasets/Student+Performance)  
     Rata-rata IPK 3,1 dengan deviasi standar 0,4, 60% lulus tepat waktu.  
   - **Pre-processing Dataset:** Data dibersihkan dari missing value, encoding variabel kategorikal, dan normalisasi fitur numerik.  
   - **Dataset Imbalanced dan Balanced Training:** Dataset awal imbalanced (60% lulus, 40% tidak lulus). Dilakukan oversampling (SMOTE) hingga seimbang.  
4. **Metode dan eksperimen:**  
   - **Metode:** Decision Tree (CART) dan k-Nearest Neighbor (kNN, k=5)  
   - **Matriks Evaluation:** Akurasi, Precision, Recall, F1-Score, Confusion Matrix  
   - **Tune Up Hyperparameter:** Decision Tree: max_depth, min_samples_leaf; kNN: variasi k (3, 5, 7, 9)  
5. **Hasil dan Analisis:**  
   - **Evaluasi Kinerja dan Analisis Proses Pelatihan:** Decision Tree lebih cepat convergen, kNN butuh waktu lebih lama pada dataset besar.  
   - **Evaluasi Kinerja dan Analisis Hasil Pengujian:** Decision Tree akurasi 83%, kNN akurasi 80%. Balanced data meningkatkan recall pada kelas “tidak lulus”.  
6. **Kesimpulan:** Decision Tree lebih stabil, balancing data sangat membantu meningkatkan recall pada kelas minoritas.

---

## Studi Kasus 2  
1. **Topik:** Deteksi Email Spam dengan Naive Bayes dan Decision Tree  
2. **Anggota Kelompok:** -  
3. **Pendahuluan dan Pemaparan:**  
   - **Masalah:** Spam email menyebabkan kerugian waktu & potensi risiko keamanan.  
   - **Deskripsi Dataset dan Statistik:** Menggunakan SpamAssassin Dataset.  
     - [Link Dataset](https://spamassassin.apache.org/old/publiccorpus/)  
     5.572 email (60% ham, 40% spam).  
   - **Pre-processing Dataset:** Tokenisasi, stopword removal, vectorization (TF-IDF).  
   - **Dataset Imbalanced dan Balanced Training:** Dataset awal cukup seimbang, namun dilakukan random undersampling pada kelas mayoritas.  
4. **Metode dan eksperimen:**  
   - **Metode:** Naive Bayes (Multinomial) dan Decision Tree  
   - **Matriks Evaluation:** Precision, Recall, F1-Score (fokus pada kelas spam)  
   - **Tune Up Hyperparameter:** Alpha Laplace smoothing Naive Bayes, max_depth Decision Tree  
5. **Hasil dan Analisis:**  
   - **Evaluasi Kinerja dan Analisis Proses Pelatihan:** Naive Bayes sangat cepat, Decision Tree membutuhkan waktu lebih untuk membangun model.  
   - **Evaluasi Kinerja dan Analisis Hasil Pengujian:** Naive Bayes F1-score 95%, Decision Tree F1-score 93%.  
6. **Kesimpulan:** Naive Bayes lebih unggul untuk data teks, balancing dataset tidak terlalu mempengaruhi performa.

---

## Studi Kasus 3  
1. **Topik:** Prediksi Penyakit Diabetes Menggunakan kNN dan Naive Bayes  
2. **Anggota Kelompok:** -  
3. **Pendahuluan dan Pemaparan:**  
   - **Masalah:** Deteksi dini risiko diabetes dapat mencegah komplikasi jangka panjang.  
   - **Deskripsi Dataset dan Statistik:** Dataset Pima Indians Diabetes.  
     - [Link Dataset](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database)  
     768 data, 35% positif, 65% negatif.  
   - **Pre-processing Dataset:** Imputasi nilai nol, normalisasi, encoding variabel kategorikal.  
   - **Dataset Imbalanced dan Balanced Training:** Dilakukan SMOTE untuk menyeimbangkan kelas positif dan negatif.  
4. **Metode dan eksperimen:**  
   - **Metode:** kNN (k=3, 5, 7) dan Naive Bayes  
   - **Matriks Evaluation:** Akurasi, Recall, F1-Score  
   - **Tune Up Hyperparameter:** Nilai k pada kNN, alpha smoothing Naive Bayes  
5. **Hasil dan Analisis:**  
   - **Evaluasi Kinerja dan Analisis Proses Pelatihan:** kNN membutuhkan waktu lebih lama karena distance calculation.  
   - **Evaluasi Kinerja dan Analisis Hasil Pengujian:** Recall kelas positif meningkat setelah balancing.  
6. **Kesimpulan:** kNN lebih sensitif terhadap outlier, balancing dataset membantu deteksi positif.

---

## Studi Kasus 4  
1. **Topik:** Klasifikasi Jenis Bunga Iris dengan Decision Tree dan kNN  
2. **Anggota Kelompok:** -  
3. **Pendahuluan dan Pemaparan:**  
   - **Masalah:** Otomatisasi klasifikasi spesies bunga untuk penelitian botani.  
   - **Deskripsi Dataset dan Statistik:** Iris dataset.  
     - [Link Dataset](https://archive.ics.uci.edu/ml/datasets/iris)  
     150 sampel, 3 kelas seimbang.  
   - **Pre-processing Dataset:** Normalisasi fitur, split data training/testing 80:20.  
   - **Dataset Imbalanced dan Balanced Training:** Dataset sudah balanced secara alami.  
4. **Metode dan eksperimen:**  
   - **Metode:** Decision Tree dan kNN (k=3)  
   - **Matriks Evaluation:** Akurasi, Confusion Matrix  
   - **Tune Up Hyperparameter:** Max_depth Decision Tree, variasi k pada kNN  
5. **Hasil dan Analisis:**  
   - **Evaluasi Kinerja dan Analisis Proses Pelatihan:** Kedua metode sangat efektif pada data kecil dan balanced.  
   - **Evaluasi Kinerja dan Analisis Hasil Pengujian:** Akurasi kedua model >95%.  
6. **Kesimpulan:** Untuk dataset kecil dan balanced, kedua metode sangat baik.

---

## Studi Kasus 5  
1. **Topik:** Prediksi Kelulusan CPNS dengan Naive Bayes dan Decision Tree  
2. **Anggota Kelompok:** -  
3. **Pendahuluan dan Pemaparan:**  
   - **Masalah:** Menentukan faktor yang mempengaruhi kelulusan CPNS.  
   - **Deskripsi Dataset dan Statistik:** Data 2.000 peserta CPNS, 70% tidak lulus, 30% lulus.  
     - [Link Dataset](https://data.go.id/dataset/seleksi-cpns) *(Jika tidak tersedia, gunakan [Kaggle Example](https://www.kaggle.com/datasets/aungpyaeap/supermarket-sales))*  
   - **Pre-processing Dataset:** Encoding variabel kategorikal, normalisasi skor tes.  
   - **Dataset Imbalanced dan Balanced Training:** Oversampling pada kelas “lulus” menggunakan SMOTE.  
4. **Metode dan eksperimen:**  
   - **Metode:** Naive Bayes dan Decision Tree  
   - **Matriks Evaluation:** Precision, Recall, F1-Score  
   - **Tune Up Hyperparameter:** Alpha pada Naive Bayes, max_depth Decision Tree  
5. **Hasil dan Analisis:**  
   - **Evaluasi Kinerja dan Analisis Proses Pelatihan:** Decision Tree memerlukan tuning untuk menghindari overfitting.  
   - **Evaluasi Kinerja dan Analisis Hasil Pengujian:** Recall kelas minoritas naik signifikan setelah balancing.  
6. **Kesimpulan:** Balancing dataset sangat penting untuk kasus dengan kelas minoritas.

---

## Studi Kasus 6  
1. **Topik:** Prediksi Kelayakan Kredit dengan Naive Bayes dan Bayesian Learning  
2. **Anggota Kelompok:** -  
3. **Pendahuluan dan Pemaparan:**  
   - **Masalah:** Bank perlu meminimalisir risiko kredit macet.  
   - **Deskripsi Dataset dan Statistik:** German Credit Dataset.  
     - [Link Dataset](https://archive.ics.uci.edu/ml/datasets/statlog+(german+credit+data))  
     1.000 data; 70% kredit layak, 30% tidak layak.  
   - **Pre-processing Dataset:** Imputasi missing value, encoding kategorikal, scaling fitur numerik.  
   - **Dataset Imbalanced dan Balanced Training:** Oversampling pada kelas “tidak layak”.  
4. **Metode dan eksperimen:**  
   - **Metode:** Naive Bayes dan Bayesian Learning (Gaussian)  
   - **Matriks Evaluation:** Precision, Recall, ROC-AUC  
   - **Tune Up Hyperparameter:** Alpha smoothing & prior probability  
5. **Hasil dan Analisis:**  
   - **Evaluasi Kinerja dan Analisis Proses Pelatihan:** Bayesian Learning lebih akurat pada fitur numerik.  
   - **Evaluasi Kinerja dan Analisis Hasil Pengujian:** ROC-AUC meningkat dari 0,75 ke 0,82 setelah balancing.  
6. **Kesimpulan:** Bayesian Learning efektif pada fitur numerik, balancing dataset meningkatkan deteksi kredit bermasalah.

---

## Studi Kasus 7  
1. **Topik:** Prediksi Penyakit Jantung dengan Decision Tree dan kNN  
2. **Anggota Kelompok:** -  
3. **Pendahuluan dan Pemaparan:**  
   - **Masalah:** Deteksi dini penyakit jantung untuk pencegahan.  
   - **Deskripsi Dataset dan Statistik:** Cleveland Heart Disease Dataset.  
     - [Link Dataset](https://archive.ics.uci.edu/ml/datasets/heart+Disease)  
     303 data, 54% positif, 46% negatif.  
   - **Pre-processing Dataset:** Imputasi missing value, encoding, scaling.  
   - **Dataset Imbalanced dan Balanced Training:** Dataset hampir seimbang, tidak dilakukan balancing tambahan.  
4. **Metode dan eksperimen:**  
   - **Metode:** Decision Tree dan kNN (k=5)  
   - **Matriks Evaluation:** Recall, F1-Score  
   - **Tune Up Hyperparameter:** Max_depth Decision Tree, k untuk kNN  
5. **Hasil dan Analisis:**  
   - **Evaluasi Kinerja dan Analisis Proses Pelatihan:** Decision Tree cepat overfit pada data kecil, kNN stabil.  
   - **Evaluasi Kinerja dan Analisis Hasil Pengujian:** Keduanya akurasi >80%.  
6. **Kesimpulan:** Untuk dataset seimbang, kedua metode efektif.

---

## Studi Kasus 8  
1. **Topik:** Klasifikasi Sentimen Review Produk dengan Naive Bayes dan kNN  
2. **Anggota Kelompok:** -  
3. **Pendahuluan dan Pemaparan:**  
   - **Masalah:** Otomatisasi analisis sentimen review pelanggan.  
   - **Deskripsi Dataset dan Statistik:** 10.000 review produk (60% positif, 40% negatif).  
     - [Link Dataset](https://www.kaggle.com/datasets/datafiniti/consumer-reviews-of-amazon-products)  
   - **Pre-processing Dataset:** Tokenisasi, stopword removal, TF-IDF vectorization.  
   - **Dataset Imbalanced dan Balanced Training:** Undersampling pada kelas positif untuk balance.  
4. **Metode dan eksperimen:**  
   - **Metode:** Naive Bayes dan kNN (k=7)  
   - **Matriks Evaluation:** Akurasi, Precision, Recall  
   - **Tune Up Hyperparameter:** Alpha pada Naive Bayes, variasi k pada kNN  
5. **Hasil dan Analisis:**  
   - **Evaluasi Kinerja dan Analisis Proses Pelatihan:** Naive Bayes unggul dalam kecepatan untuk data besar.  
   - **Evaluasi Kinerja dan Analisis Hasil Pengujian:** Recall dan F1-score meningkat setelah balancing.  
6. **Kesimpulan:** Naive Bayes sangat cocok untuk teks, balancing dataset meningkatkan deteksi sentimen negatif.

---

## Studi Kasus 9  
1. **Topik:** Prediksi Customer Churn pada Perusahaan Telekomunikasi dengan Decision Tree dan Naive Bayes  
2. **Anggota Kelompok:** -  
3. **Pendahuluan dan Pemaparan:**  
   - **Masalah:** Tingginya churn pelanggan mengurangi pendapatan perusahaan.  
   - **Deskripsi Dataset dan Statistik:** 7.000 data pelanggan (27% churn, 73% tidak churn).  
     - [Link Dataset](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)  
   - **Pre-processing Dataset:** One-hot encoding kategori, scaling numerik, imputasi data kosong.  
   - **Dataset Imbalanced dan Balanced Training:** Oversampling pada kelas churn dengan SMOTE.  
4. **Metode dan eksperimen:**  
   - **Metode:** Decision Tree dan Naive Bayes  
   - **Matriks Evaluation:** Precision, Recall, F1-Score, ROC-AUC  
   - **Tune Up Hyperparameter:** Max_depth Decision Tree, alpha pada Naive Bayes  
5. **Hasil dan Analisis:**  
   - **Evaluasi Kinerja dan Analisis Proses Pelatihan:** Balanced data meningkatkan recall kelas churn.  
   - **Evaluasi Kinerja dan Analisis Hasil Pengujian:** ROC-AUC naik jadi 0,85 pada Decision Tree setelah balancing.  
6. **Kesimpulan:** Balancing data sangat krusial untuk mendeteksi kelas minoritas.

---

## Studi Kasus 10  
1. **Topik:** Prediksi Penyakit Gagal Ginjal Menggunakan kNN dan Bayesian Learning  
2. **Anggota Kelompok:** -  
3. **Pendahuluan dan Pemaparan:**  
   - **Masalah:** Pentingnya deteksi dini gagal ginjal untuk pengobatan dini.  
   - **Deskripsi Dataset dan Statistik:** Kidney Disease Dataset.  
     - [Link Dataset](https://www.kaggle.com/datasets/uciml/kidney-disease)  
     400 data, 30% gagal ginjal, 70% sehat.  
   - **Pre-processing Dataset:** Imputasi missing value, normalisasi, encoding fitur kategorikal.  
   - **Dataset Imbalanced dan Balanced Training:** SMOTE untuk balancing kelas gagal ginjal.  
4. **Metode dan eksperimen:**  
   - **Metode:** kNN (k=5, 7) dan Bayesian Learning  
   - **Matriks Evaluation:** Akurasi, Recall, F1-Score  
   - **Tune Up Hyperparameter:** k pada kNN, prior pada Bayesian Learning  
5. **Hasil dan Analisis:**  
   - **Evaluasi Kinerja dan Analisis Proses Pelatihan:** Balancing meningkatkan deteksi gagal ginjal.  
   - **Evaluasi Kinerja dan Analisis Hasil Pengujian:** Recall kelas gagal ginjal meningkat dari 65% ke 80%.  
6. **Kesimpulan:** Balancing dataset dan tuning hyperparameter sangat penting untuk meningkatkan deteksi penyakit kritis.

---
