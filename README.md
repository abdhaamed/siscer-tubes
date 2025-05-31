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
