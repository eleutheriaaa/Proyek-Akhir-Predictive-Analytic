# Laporan Proyek Machine Learning - Nathanael Dennis Gunawan

## Domain Proyek

Obesitas merupakan salah satu masalah kesehatan paling mendesak di dunia modern. Kondisi ini tidak hanya berdampak pada penampilan fisik, tetapi juga berisiko menimbulkan berbagai penyakit serius seperti diabetes tipe 2, tekanan darah tinggi, dan gangguan jantung. Di era modern, perubahan gaya hidup seperti konsumsi makanan tinggi kalori, kurangnya aktivitas fisik, serta kebiasaan duduk dalam waktu lama turut memperparah masalah obesitas

Permasalahan obesitas diperlukan pemanfaatan teknologi untuk membantu proses deteksi dini. Salah satu pendekatan yang dapat digunakan adalah machine learning, yang mampu mempelajari pola dari data gaya hidup untuk memprediksi status obesitas dengan lebih akurat. Dengan adanya model klasifikasi dari Machine Learning  kita dapat menganalisis berbagai faktor seperti jenis kelamin, usia, kebiasaan makan, dan aktivitas fisik, lalu mengkategorikan individu ke dalam tingkat obesitas tertentu. Solusi ini tidak hanya berguna untuk tenaga medis, tetapi juga dapat digunakan oleh masyarakat umum untuk meningkatkan kesadaran dan pencegahan terhadap obesitas sejak dini

**Rubrik/Kriteria Tambahan (Opsional)**:
- Jelaskan mengapa dan bagaimana masalah tersebut harus diselesaikan
- Menyertakan hasil riset terkait atau referensi. Referensi yang diberikan harus berasal dari sumber yang kredibel dan author yang jelas.
- Format Referensi dapat mengacu pada penulisan sitasi [IEEE](https://journals.ieeeauthorcenter.ieee.org/wp-content/uploads/sites/7/IEEE_Reference_Guide.pdf), [APA](https://www.mendeley.com/guides/apa-citation-guide/) atau secara umum seperti [di sini](https://penerbitdeepublish.com/menulis-buku-membuat-sitasi-dengan-mudah/)
- Sumber yang bisa digunakan [Scholar](https://scholar.google.com/)

## Business Understanding

### Problem Statements

- Bagaimana mengidentifikasi faktor-faktor gaya hidup yang berkontribusi terhadap tingkat obesitas seseorang?  
Banyak individu yang tidak menyadari bahwa kebiasaan sehari-hari seperti pola makan, aktivitas fisik, dan waktu luang sangat mempengaruhi status berat badan mereka
- Bagaimana membangun model klasifikasi yang mampu mengelompokkan status obesitas seseorang secara otomatis berdasarkan data gaya hidup?  
Klasifikasi manual berdasarkan parameter gaya hidup seringkali tidak efisien dan rawan kesalahan subjektif. Diperlukan pendekatan otomatis yang dapat mengolah data dengan akurat
- Model machine learning mana yang memberikan performa terbaik dalam mengklasifikasikan tingkat obesitas?  
Terdapat berbagai algoritma klasifikasi yang dapat digunakan, namun masing-masing memiliki kelebihan dan kelemahan tergantung pada karakteristik data

### Goals

- Mengidentifikasi fitur penting dari data yang berkaitan dengan gaya hidup dan obesitas  
Proyek ini bertujuan untuk memahami bagaimana variabel seperti konsumsi makanan tinggi kalori, aktivitas fisik, dan lain-lain berkorelasi dengan status obesitas
- Mengembangkan dan melatih model klasifikasi berbasis machine learning untuk mengklasifikasikan individu ke dalam level obesitas yang sesuai  
Diharapkan model dapat melakukan prediksi secara otomatis dan akurat berdasarkan data masukan dari pengguna
- Membandingkan performa beberapa algoritma klasifikasi seperti K-Nearest Neighbors, Random Forest, dan Logistic Regression untuk menentukan model terbaik  
Evaluasi dilakukan menggunakan metrik akurasi, precision, recall, dan f1-score agar dapat dipilih model yang paling tepat untuk diterapkan di dunia nyata

**Rubrik/Kriteria Tambahan (Opsional)**:
- Menambahkan bagian “Solution Statement” yang menguraikan cara untuk meraih goals. Bagian ini dibuat dengan ketentuan sebagai berikut: 

    ### Solution statements
    - Mengajukan 2 atau lebih solution statement. Misalnya, menggunakan dua atau lebih algoritma untuk mencapai solusi yang diinginkan atau melakukan improvement pada baseline model dengan hyperparameter tuning.
    - Solusi yang diberikan harus dapat terukur dengan metrik evaluasi.

## Data Understanding
Dataset yang saya gunakan dalam proyek ini dapat diunduh melalui link atau tautan ini : https://www.kaggle.com/datasets/fatemehmehrparvar/obesity-levels?resource=download
Dataset ini dikumpulkan berdasarkan data survei kebiasaan gaya hidup dan pola makan dari berbagai individu, serta label klasifikasi tingkat obesitas berdasarkan kalkulasi Body Mass Index (BMI) dan karakteristik pribadi lainnya

Dataset yang digunakan ini terdiri dari 2111 baris data dan 17 kolom yang mencerminkan kondisi fisik individu. Tujuan utamanya adalah untuk mengklasifikasikan individu ke salah satu dari ketujuh kelas

Variabel-variabel dalam dataset adalah sebagai berikut:
- Gender : Jenis kelamin individu (Male / Female)
- Age : Usia individu (dalam tahun)
- Height : Tinggi badan (dalam meter)
- Weight : Berat badan (dalam kilogram)
- family_history_with_overweight : Riwayat keluarga dengan kelebihan berat badan (yes / no)
- FAVC : Apakah individu mengonsumsi makanan tinggi kalori secara rutin? (yes / no)
- FCVC : Frekuensi konsumsi sayuran
- NCP : Jumlah makanan utama yang dikonsumsi per hari
- CAEC : Konsumsi makanan di luar jam makan utama (frekuensi ngemil)
- SMOKE : Apakah individu merokok? (yes / no)
- CH2O : Konsumsi air putih harian
- SCC : Apakah individu memantau konsumsi kalori? (yes / no)
- FAF : Frekuensi aktivitas fisik mingguan
- TUE : Waktu yang dihabiskan menggunakan perangkat elektronik (TV, gadget) setiap hari
- CALC : Frekuensi konsumsi alkohol
- MTRANS : Jenis transportasi utama yang digunakan (Public_Transportation, Walking, Automobile, Motorcycle, Bike)
- NObeyesdad : Label klasifikasi tingkat obesitas:
	- Insufficient_Weight
	- Normal_Weight
	- Overweight_Level_I
	- Overweight_Level_II
	- Obesity_Type_I
	- Obesity_Type_II
	- Obesity_Type_III

**Rubrik/Kriteria Tambahan (Opsional)**:
- Melakukan beberapa tahapan yang diperlukan untuk memahami data, contohnya teknik visualisasi data atau exploratory data analysis.

## Data Preparation
Pada bagian ini Anda menerapkan dan menyebutkan teknik data preparation yang dilakukan. Teknik yang digunakan pada notebook dan laporan harus berurutan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan proses data preparation yang dilakukan
- Menjelaskan alasan mengapa diperlukan tahapan data preparation tersebut.

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
