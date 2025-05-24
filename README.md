# Laporan Proyek Machine Learning - Nathanael Dennis Gunawan

## Domain Proyek

Obesitas merupakan salah satu masalah kesehatan paling mendesak di dunia modern. Kondisi ini tidak hanya berdampak pada penampilan fisik, tetapi juga berisiko menimbulkan berbagai penyakit serius seperti diabetes tipe 2, tekanan darah tinggi, dan gangguan jantung. Di era modern, perubahan gaya hidup seperti konsumsi makanan tinggi kalori, kurangnya aktivitas fisik, serta kebiasaan duduk dalam waktu lama turut memperparah masalah obesitas

Permasalahan obesitas diperlukan pemanfaatan teknologi untuk membantu proses deteksi dini. Salah satu pendekatan yang dapat digunakan adalah machine learning, yang mampu mempelajari pola dari data gaya hidup untuk memprediksi status obesitas dengan lebih akurat. Dengan adanya model klasifikasi dari Machine Learning  kita dapat menganalisis berbagai faktor seperti jenis kelamin, usia, kebiasaan makan, dan aktivitas fisik, lalu mengkategorikan individu ke dalam tingkat obesitas tertentu. Solusi ini tidak hanya berguna untuk tenaga medis, tetapi juga dapat digunakan oleh masyarakat umum untuk meningkatkan kesadaran dan pencegahan terhadap obesitas sejak dini

**Rubrik/Kriteria Tambahan (Opsional)**:
Obesitas merupakan tantangan kesehatan global yang mendesak, dengan dampak serius terhadap kualitas hidup masyarakat. Jika terkena obesitas, kita terkena risiko  berbagai penyakit kronis seperti diabetes tipe 2, hipertensi, penyakit jantung, dan gangguan metabolik lainnya. Maka dari itu pentingnya menyelesaikan masalah obesitas ini  
Penyelesaian masalah obesitas penting karena:
- Dampak Kesehatan: Obesitas berhubungan erat dengan peningkatan risiko penyakit kronis yang dapat menurunkan harapan hidup dan kualitas hidup seseorang
- Beban Ekonomi: Biaya perawatan medis untuk penyakit terkait obesitas menambah beban pada sistem kesehatan dan ekonomi negara
- Kesejahteraan Sosial: Obesitas dapat mempengaruhi kesejahteraan psikologis dan sosial seseorang termasuk stigma sosial dan diskriminasi

Penyelesaian masalah dengan teknologi dengan memanfaatkan Machine Learning:
- Prediksi Dini: Model ML dapat menganalisis data gaya hidup, seperti pola makan dan aktivitas fisik, untuk memprediksi risiko obesitas secara dini
- Personalisasi Intervensi: Dengan memahami faktor risiko individu, intervensi dapat disesuaikan untuk meningkatkan efektivitas pencegahan dan pengobatan
- Skalabilitas: Teknologi memungkinkan penerapan solusi secara luas, menjangkau berbagai lapisan masyarakat

[1] Menurut Ji-Hoon Jeong dan rekan-rekannya, mereka menyatakan bahwa model DeepHealthNet yang dikembangkan mampu memprediksi tingkat obesitas pada remaja dengan akurasi tinggi, yaitu 88,42%. Model ini menggunakan data kesehatan harian seperti tinggi badan, berat badan, lingkar pinggang, asupan kalori, dan tingkat aktivitas fisik  
[2] Menurut Yichen Zhao dan rekan-rekannya, mereka menyatakan bahwa dengan mengintegrasikan pemrosesan bahasa alami (NLP) dan pemantauan aktivitas fisik, mereka berhasil mengembangkan model deep learning yang mampu mendiagnosis sindrom metabolik secara dini dengan area under the curve (AUROC) sebesar 0,806 dan recall sebesar 76,3%

[1] Jeong, J. H., Lee, I. G., Kim, S. K., Kam, T. E., Lee, S. W., & Lee, E. (2024). DeepHealthNet: Adolescent obesity prediction system based on a deep learning framework. IEEE Journal of Biomedical and Health Informatics, 28(4), 2282-2293.  
[2] Zhao, Y., Wang, Y., Cheng, X., Fang, J., & Yang, Y. (2025). Integrating Natural Language Processing and Exercise Monitoring for Early Diagnosis of Metabolic Syndrome: A Deep Learning Approach. arXiv preprint arXiv:2505.08628.

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

    ### Solution statements
- Perbandingan kinerja dari beberapa algoritma klasifikasi untuk mengidentifikasi model terbaik dalam klasifikasi tingkat obesitas
	- Membangun dan membandingkan performa beberapa algoritma Machine Learning yaitu K-Nearest Neighbors (KNN), Random Forest (RF), Logistic Regression
	- Metode evaluasi dengan melihat Akurasi, Precision, Recall, F1-Score per kelas, Confusion Matrix, dan skor akurasi data training dan testing
Dengan tujuan untuk menentukan model baseline terbaik berdasarkan kinerja klasifikasi 
- Tuning Hyperparameter pada Model Terbaik, setelah menemukan model baseline terbaik, solusi kedua adalah:
	- Melakukan hyperparameter tuning menggunakan teknik seperti Grid Search CV atau Randomized Search CV, Cross-validation untuk memastikan model tidak overfitting
	- Contoh parameter yang dituning: K pada KNN, n_estimators, max_depth, dan min_samples_split pada Random Forest, C dan penalty pada Logistic Regression
	- Metrik evaluasi: Peningkatan akurasi pada data testing, Keseimbangan F1-Score antar kelas, Performa stabil saat cross-validation
Tujuan: Mengoptimalkan model agar menghasilkan prediksi yang lebih akurat terhadap data yang belum pernah dilihat sebelumnya

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
- Import dan pemanggilan data  
Dataset dimuat menggunakan pandas
- Pemeriksaan awal dataset  
Menampilkan 5 baris pertama dengan head(), statistik deskriptif dengan describe()
- Visualisasi data  
Visualisasi outlier menggunakan boxplot menggunakan seaborn
- Pembersihan outlier  
Outlier dideteksi dan dihapus menggunakan metode IQR
- Identifikasi fitur  
Pemisahan fitur numerik dan kategorikal

## Data Preparation
- Memuat dataset
- Pemeriksaan data kosong dan tipe data
- Visualisasi dan deteksi outlier
- Pemisahan fitur kategorikal dan numerikal
- Pemisahan data latih dan uji
- Scaling pada fitur numerikal

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Memuat dataset
Dataset diimpor menggunakan pandas untuk kemudian dilakukan eksplorasi awal. Alasan: Membaca data merupakan langkah awal sebelum analisis lebih lanjut
- Pemeriksaan data kosong dan tipe data
Menggunakan df.info() dan df.isnull().sum() untuk mengecek nilai kosong dan tipe data. Alasan: Menghindari error dalam proses transformasi atau pelatihan model akibat missing value atau tipe data yang tidak sesuai
- Visualisasi dan deteksi outlier
Fitur numerik seperti Age, Height, dan Weight divisualisasikan menggunakan boxplot. Outlier diidentifikasi dan ditangani menggunakan metode IQR (Interquartile Range). Alasan: Outlier dapat merusak performa model, terutama pada algoritma berbasis jarak seperti KNN
- Pemisahan fitur kategorikal dan numerikal
Fitur diklasifikasikan agar bisa diproses sesuai jenisnya. Alasan: Transformasi untuk data kategorikal dan numerikal berbeda. Misalnya, numerik perlu distandarisasi, sementara kategorikal perlu encoding
- Pemisahan data latih dan uji
Data dibagi menjadi X_train, X_test, y_train, y_test menggunakan train_test_split. Alasan: Untuk menghindari overfitting dan mengukur generalisasi model
- Scaling pada Fitur Numerikal
Fitur numerik ['FCVC', 'NCP', 'CH2O', 'FAF', 'TUE'] dinormalisasi menggunakan StandardScaler dari scikit-learn. Alasan: Scaling diperlukan agar semua fitur numerik berada pada skala yang sama, yang penting untuk algoritma seperti KNN dan regresi logistik

## Modeling
Dalam proyek ini, saya menggunakan tiga algoritma klasifikasi untuk memprediksi tingkat obesitas seseorang berdasarkan data gaya hidup yaitu: K-Nearest Neighbors (KNN), Random Forest (RF), dan Logistic Regression (LR). Setiap model dievaluasi menggunakan metrik akurasi, precision, recall, dan f1-score pada data uji

**Rubrik/Kriteria Tambahan (Opsional)**: 
- K-Nearest Neighbors (KNN)
	- Akurasi Training: 0.92
	- Akurasi Testing: 0.73
	- Parameter: n_neighbors=5 (default)  
Kelebihan: Mudah dipahami dan diimplementasikan, Tidak membutuhkan proses pelatihan  
Kekurangan: Sensitif terhadap skala data dan outlier, Performa menurun pada data yang besar atau banyak fitur
- Random Forest (RF)
	- Akurasi Training: 1.00
	- Akurasi Testing: 0.79
	- Parameter: default (n_estimators=100)  
Kelebihan: Mampu menangani data yang kompleks dan fitur yang banyak, Tahan terhadap overfitting dibandingkan decision tree tunggal, Memberikan informasi fitur paling penting  
Kekurangan: Interpretasi hasil lebih kompleks, Waktu pelatihan bisa lebih lama dibanding model sederhana
- Logistic Regression (LR)
	- Akurasi Training: 0.85
	- Akurasi Testing: 0.57  
Kelebihan: Cepat dilatih dan memberikan output yang dapat diinterpretasi secara probabilistik, Cocok untuk baseline model  
Kekurangan: Performa buruk untuk data non-linear, Rentan terhadap multikolinearitas antar fitur

- Model Terbaik
Berdasarkan hasil evaluasi pada data uji:
	- Random Forest memiliki akurasi tertinggi (0.79) dan stabilitas metrik precision, recall, dan f1-score yang baik untuk hampir semua kelas, termasuk kelas dengan jumlah data kecil.
	- KNN memiliki akurasi lumayan (0.73) namun lebih sensitif terhadap perubahan data, serta beberapa kelas seperti Normal_Weight menunjukkan hasil f1-score yang rendah.
	- Logistic Regression menunjukkan performa yang paling rendah (0.57) dan tidak mampu memprediksi beberapa kelas dengan baik.
- Model Terpilih: Random Forest  
Random Forest dipilih sebagai model terbaik karena memberikan performa paling konsisten dan akurat pada berbagai kelas obesitas, serta memiliki keunggulan dalam menangani data dengan banyak fitur dan ketidakseimbangan antar kelas.

## Evaluation
- Metrik Evaluasi yang Digunakan
	- Akurasi (Accuracy): Mengukur proporsi prediksi yang benar dari total keseluruhan data. Akurasi memberikan gambaran umum tentang seberapa baik model dapat mengklasifikasikan data secara benar
	- Precision: Mengukur ketepatan prediksi positif, yaitu berapa banyak prediksi kelas tertentu yang benar-benar sesuai kelas tersebut
	- Recall (Sensitivity): Mengukur kemampuan model dalam menemukan seluruh data positif sebenarnya dari suatu kelas. Recall menilai seberapa baik model menangkap seluruh kasus dari kelas tertentu, penting terutama jika false negative harus diminimalkan
	- F1 Score: Merupakan harmonisasi rata-rata antara precision dan recall. F1 Score berguna sebagai metrik tunggal yang menyeimbangkan kedua aspek tersebut, khususnya ketika dataset tidak seimbang antar kelas
- Hasil Proyek Berdasarkan Metrik Evaluasi
	- Random Forest menunjukkan performa terbaik dengan akurasi pengujian mencapai sekitar 78,7%, didukung precision, recall, dan F1 score yang tinggi pada sebagian besar kelas obesitas. Model ini juga memperlihatkan kemampuan generalisasi yang baik antara data training dan testing
	- K-Nearest Neighbors memiliki akurasi pengujian sekitar 73%, dengan beberapa kelas tertentu seperti Insufficient Weight dan Obesity Type III mendapatkan skor recall yang tinggi, namun ada kelas lain yang performanya kurang optimal
	- Logistic Regression memiliki akurasi paling rendah (sekitar 57%), dengan ketidakseimbangan recall pada beberapa kelas yang menyebabkan performa kurang memadai untuk tugas klasifikasi multi-kelas ini  
Dari hasil tersebut, dapat disimpulkan bahwa Random Forest merupakan pilihan model yang paling sesuai untuk klasifikasi tingkat obesitas pada dataset ini, karena mampu memberikan keseimbangan yang baik antara akurasi dan kemampuan mengenali kelas minoritas.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Metrik evaluasi dan formula
Metrik evaluasi yang digunakan dalam proyek ini meliputi akurasi, precision, recall, dan F1 score. Akurasi mengukur proporsi prediksi yang benar dari keseluruhan data yang diuji, sehingga memberikan gambaran umum seberapa baik model dalam melakukan klasifikasi. Namun, akurasi bisa kurang tepat jika data tidak seimbang, sehingga perlu dilengkapi dengan metrik lain. Precision mengukur ketepatan model dalam memprediksi kelas positif, yakni seberapa banyak prediksi positif yang benar-benar relevan. Sementara itu, recall mengukur kemampuan model dalam menemukan semua data positif yang sebenarnya ada, dengan fokus pada minimnya data positif yang terlewatkan. F1 score merupakan rata-rata harmonis antara precision dan recall, memberikan penilaian seimbang antara keduanya terutama dalam kondisi data yang tidak seimbang. Dengan menggunakan keempat metrik ini, evaluasi performa model menjadi lebih komprehensif dan sesuai dengan konteks masalah klasifikasi yang dihadapi
- Cara kerja matrik
	- Akurasi menghitung keseluruhan benar/salah prediksi tanpa membedakan jenis kelas, cocok jika distribusi kelas merata
	- Precision fokus pada kualitas prediksi positif, menghindari terlalu banyak false alarm (false positive)
	- Recall fokus pada kemampuan menemukan semua kasus positif, menghindari kasus terlewat (false negative)
	- F1 Score menggabungkan precision dan recall, memberikan gambaran lengkap performa model terutama pada situasi dengan kelas tidak seimbang

**---Ini adalah bagian akhir laporan---**
