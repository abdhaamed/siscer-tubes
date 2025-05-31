## Studi Kasus 1: Prediksi Kelulusan Mahasiswa Menggunakan Decision Tree dan k-Nearest Neighbor

1. **Topik:**  
   Prediksi Kelulusan Mahasiswa Menggunakan Decision Tree dan k-Nearest Neighbor

2. **Anggota Kelompok:**  
   -

3. **Pendahuluan dan Pemaparan:**  
   - **Masalah:**  
     Banyak universitas menghadapi kesulitan dalam memprediksi mahasiswa yang berisiko tidak lulus tepat waktu. Prediksi ini penting untuk memberikan intervensi lebih awal agar tingkat kelulusan meningkat.
   - **Deskripsi Dataset dan Statistik:**  
     Dataset berisi data 1.000 mahasiswa dari UCI Machine Learning Repository, termasuk variabel IPK, kehadiran, jumlah SKS, dan atribut lainnya.  
     - Rata-rata IPK: 3,1  
     - Deviasi standar IPK: 0,4  
     - Proporsi kelulusan tepat waktu: 60%  
     - [Link Dataset Student Performance UCI](https://archive.ics.uci.edu/ml/datasets/Student+Performance)
   - **Pre-processing Dataset:**  
     Data dibersihkan dari missing value, dilakukan encoding pada variabel kategorikal (misal: jenis kelamin, jurusan), dan normalisasi fitur numerik seperti IPK dan jumlah SKS.
   - **Dataset Imbalanced dan Balanced Training:**  
     Dataset awal imbalanced (60% lulus, 40% tidak lulus). Dilakukan oversampling pada kelas minoritas menggunakan metode SMOTE hingga kedua kelas seimbang sebelum proses pelatihan.

4. **Metode dan Eksperimen:**  
   - **Metode:**  
     - Decision Tree (CART)  
     - k-Nearest Neighbor (kNN, k=5)
   - **Matriks Evaluation:**  
     - Akurasi  
     - Precision  
     - Recall  
     - F1-Score  
     - Confusion Matrix
   - **Tune Up Hyperparameter:**  
     - Decision Tree: max_depth, min_samples_leaf  
     - kNN: variasi nilai k (3, 5, 7, 9)

5. **Hasil dan Analisis:**  
   - **Evaluasi Kinerja dan Analisis Proses Pelatihan:**  
     Decision Tree lebih cepat dalam proses pelatihan dan konvergen, sedangkan kNN membutuhkan waktu lebih lama terutama pada dataset yang lebih besar karena proses perhitungan jarak antar data.
   - **Evaluasi Kinerja dan Analisis Hasil Pengujian:**  
     - Decision Tree: akurasi 83%  
     - kNN: akurasi 80%  
     Balancing data menggunakan SMOTE meningkatkan recall pada kelas “tidak lulus”, sehingga model lebih sensitif dalam mendeteksi mahasiswa yang berisiko tidak lulus.

6. **Kesimpulan:**  
   Decision Tree lebih stabil pada dataset dengan fitur kategorikal. Balancing data sangat membantu meningkatkan recall pada kelas minoritas (mahasiswa yang tidak lulus tepat waktu). Model yang baik dapat menjadi alat bantu untuk intervensi lebih dini pada mahasiswa berisiko.
