# Submission : Analisis Data Cuaca Stasiun Moratalaz di Madrid

Username dicoding: mzfuadi97

| | Deskripsi |
| ----------- | ----------- |
| Dataset | [Weather Prediction](https://www.kaggle.com/datasets/rober2598/madrid-weather-dataset-by-hours-20192022) |
| Masalah | Proyek ini bertujuan untuk menganalisis data cuaca yang dikumpulkan dari stasiun cuaca Moratalaz di Madrid, mulai dari Januari 2019 hingga Januari 2022. Dataset ini mencakup berbagai variabel meteorologi, termasuk suhu, kecepatan angin, arah angin, kelembaban, tekanan udara, radiasi matahari, dan presipitasi. Tujuan dari analisis ini adalah untuk mendapatkan wawasan tentang kondisi iklim di daerah tersebut selama periode ini. Dengan memeriksa tren dan pola dalam parameter cuaca ini, kita dapat lebih memahami dinamika iklim lokal, mengidentifikasi variasi musiman, dan potensialnya meramalkan pola cuaca di masa depan. Informasi ini dapat memiliki aplikasi dalam perencanaan perkotaan, pertanian, pengelolaan energi, dan kesiapsiagaan bencana, yang berkontribusi pada pengambilan keputusan berdasarkan data cuaca historis. |
| Arsitektur model | Arsitektur model yang digunakan adalah sebuah jaringan saraf rekuren (Recurrent Neural Network/RNN) dengan lapisan LSTM dan Bidirectional LSTM, diikuti oleh beberapa lapisan Dense (fully connected) pada akhirnya |
| Metrik evaluasi | Model ini menggunakan metrik Mean Absolute Error (MAE) untuk mengevaluasi akurasi prediksi suhu dengan mengukur rata-rata kesalahan absolut antara nilai prediksi dan nilai sebenarnya. Callback bernama myCallback digunakan untuk menghentikan pelatihan jika MAE model turun di bawah 10% dari skala data (threshold_mae), memastikan pelatihan berakhir saat performa sudah cukup baik. Arsitektur model melibatkan lapisan LSTM dan Bidirectional LSTM untuk ekstraksi pola dari data deret waktu suhu, serta lapisan Dense untuk pengolahan informasi guna meramalkan suhu. |
| Performa model | Pada Epoch 1, model memiliki loss sebesar 0.5596 dan Mean Absolute Error (MAE) sebesar 0.9191. Selama pelatihan berlanjut, baik loss maupun MAE menunjukkan penurunan yang signifikan. Pada Epoch 2, loss turun menjadi 0.2576 dan MAE menjadi 0.5764. Kemudian pada Epoch 3, loss lebih lanjut menurun menjadi 0.2330 dan MAE menjadi 0.5446. Pada Epoch 4, sebelum selesainya epoch, ada pengecekan apakah MAE model sudah lebih kecil dari 10% dari skala data. Karena kondisi ini terpenuhi (MAE = 0.5286 < 10% dari skala data), pelatihan dihentikan lebih awal.

Hasil ini menunjukkan bahwa model mengalami peningkatan dalam meramalkan suhu dari epoch ke epoch. Pelatihan dihentikan lebih awal karena model sudah cukup baik dalam meramalkan suhu dengan tingkat error yang rendah (MAE < 10% dari skala data), dan lebih lanjut tidak diperlukan untuk mencapai performa yang lebih baik |

### Dataset
![Dataset](https://github.com/mzfuadi97/ML-TimeSeries/assets/70827786/40371e95-e2db-480b-8821-87197308345c)

### Timeseries_viz
![Timeseries](https://github.com/mzfuadi97/ML-TimeSeries/assets/70827786/6e9cdf6b-4312-42ee-991a-ecb07ef9a440)

### Validation-epoch
![Metrik_Evaluasi](https://github.com/mzfuadi97/ML-TimeSeries/assets/70827786/d908c916-e02f-4777-8f3f-751d9093da54)


