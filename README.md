# Laporan Proyek Machine Learning - Nathanael Dennis Gunawan

## Domain Proyek

Obesitas merupakan salah satu masalah kesehatan paling mendesak di dunia modern. Kondisi ini tidak hanya berdampak pada penampilan fisik, tetapi juga berisiko menimbulkan berbagai penyakit serius seperti diabetes tipe 2, tekanan darah tinggi, dan gangguan jantung. Di era modern, perubahan gaya hidup seperti konsumsi makanan tinggi kalori, kurangnya aktivitas fisik, serta kebiasaan duduk dalam waktu lama turut memperparah masalah obesitas

Permasalahan obesitas diperlukan pemanfaatan teknologi untuk membantu proses deteksi dini. Salah satu pendekatan yang dapat digunakan adalah machine learning, yang mampu mempelajari pola dari data gaya hidup untuk memprediksi status obesitas dengan lebih akurat. Dengan adanya model klasifikasi dari Machine Learning  orang-orang dapat menganalisis berbagai faktor seperti jenis kelamin, usia, kebiasaan makan, dan aktivitas fisik, lalu mengkategorikan individu ke dalam tingkat obesitas tertentu. Solusi ini tidak hanya berguna untuk tenaga medis, tetapi juga dapat digunakan oleh masyarakat umum untuk meningkatkan kesadaran dan pencegahan terhadap obesitas sejak dini

**Rumusan Masalah dan Penyelesaian Masalah**  
Obesitas merupakan tantangan kesehatan global yang mendesak, dengan dampak serius terhadap kualitas hidup masyarakat. Jika terkena obesitas, masyarakat terkena risiko  berbagai penyakit kronis seperti diabetes tipe 2, hipertensi, penyakit jantung, dan gangguan metabolik lainnya. Maka dari itu pentingnya menyelesaikan masalah obesitas ini  
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
Dataset yang digunakan dalam proyek ini berasal dari Kaggle. Dataset ini berisi data survei mengenai gaya hidup, pola makan, dan kebiasaan individu yang digunakan untuk mengklasifikasikan tingkat obesitas berdasarkan Body Mass Index (BMI) dan karakteristik lainnya  
- **URL/Tautan Sumber Data** 
Dataset yang digunakan dalam proyek ini dapat diunduh melalui link ini: https://www.kaggle.com/datasets/fatemehmehrparvar/obesity-levels?resource=download
- **Jumlah Baris dan Kolom**
Dataset yang digunakan ini terdiri dari 2111 baris data dan 17 kolom yang mencerminkan kondisi fisik individu. Tujuan utamanya adalah untuk mengklasifikasikan individu ke salah satu dari ketujuh kelas  
- **Kondisi Data**
	- Missing Value: Tidak ditemukan nilai yang hilang dalam dataset
	- Duplikat: Tidak terdapat duplikasi baris data
	- Outlier: Outlier terdeteksi pada beberapa fitur numerik seperti Age, Height, dan Weight, dan telah dibersihkan menggunakan metode IQR (Interquartile Range).

**Variabel-variabel dalam dataset adalah sebagai berikut:**
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

**Tahapan**  
- Pertama-tama dilakukan proses identifikasi struktur dan isi dataset. Dataset dimuat guna memperoleh gambaran umum tentang jumlah fitur, tipe data, serta nilai pada tiap kolom. Informasi tersebutlah yang digunakan untuk dasar dalam menentukan langkah selanjutnya  
- Lima baris pertama ditampilkan untuk mengecek bentuk dan isi data mentah, sedangkan statistik deskriptif berguna untuk memberikan ringkasan seperti nilai rata-rata, standar deviasi, serta nilai minimum dan maksimum dari tiap fitur numerik. Hal tersebut membantu dalam memahami sebaran nilai serta mendeteksi nilai
- Visualisasi digunakan untuk alat bantu eksplorasi data, Salah satunya adalah boxplot yang mampu menunjukkan distribusi data serta mendeteksi keberadaan outlier pada fitur numerik. Identifikasi dan juga penghapusan outlier pun juga dilakukan menggunakan metode  Interquartile Range (IQR) agar data lebih bersih
- Klasifikasi fitur dibagi menjadi dua jenis utama yaitu fitur numerik dan kategorikal. Fitur ini dipisah karena untuk memastikan perlakuan yang sesuai terhadap setiap fitur dalam tahap praproses dan analisis selanjutnya. Dengan memahami tipe data dari masing-masing fitur, proses analisis dapat dilakukan secara tepat dan efisien

## Data Preparation

Dalam tahap Data Preparation ini, dilakukan beberapa proses penting untuk memastikan data siap digunakan dalam pemodelan Machine Learning - Dataset yang telah dimuat kemudian diperiksa untuk memastikan tidak terdapat nilai kosong (missing value) dan semua tipe data sudah sesuai dengan karakteristik fitur masing-masing. Pada dataset ini, tidak ditemukan missing value sehingga tidak diperlukan penanganan khusus untuk missing value
- Dilakukan visualisasi dan deteksi outlier terutama pada fitur numerikal menggunakan metode boxplot. Outlier yang terdeteksi kemudian diatasi dengan menggunakan metode Interquartile Range (IQR) untuk menghapus nilai-nilai ekstrem yang dapat memengaruhi kinerja model
- Fitur pada dataset kemudian dipisahkan menjadi dua kelompok utama yaitu fitur kategorikal dan fitur numerikal agar dapat dilakukan proses pemrosesan yang sesuai untuk masing-masing tipe data
- Fitur kategorikal seperti Gender, family_history_with_overweight, FAVC, CAEC, SMOKE, SCC, CALC, MTRANS diubah menjadi representasi numerik menggunakan One-Hot Encoding, dengan alasan model Machine Learning tidak dapat bekerja dengan data kategorikal langsung, sehingga dilakukan tahap encoding untuk representasi numerik tanpa memberikan urutan pada kategori
- Setelah encoding dan scaling, dilakukan reduksi dimensi menggunakan PCA terhadap 'Age', 'Height', 'Weight' untuk menyederhanakan kompleksitas fitur dan mempercepat proses pelatihan. Hal ini dilakukan untuk mengurangi fitur sambil mempertahankan informasi penting dari data dan mengurangi beban komputasi
- Dataset dibagi menjadi training set dan test set dengan rasio pembagian yang sesuai, untuk memastikan model dapat diuji performanya secara objektif 
- Pada fitur numerikal seperti FCVC, NCP, CH2O, FAF, dan TUE, dilakukan proses scaling menggunakan teknik standardisasi (StandardScaler) agar setiap fitur memiliki rentang nilai dan distribusi yang seragam. Hal ini penting untuk membantu algoritma machine learning yang sensitif terhadap skala data agar dapat belajar secara optimal
- Seluruh tahapan pemrosesan ini dilakukan secara runtut dan menyeluruh agar data yang digunakan dalam pemodelan sudah bersih, terstruktur, dan sesuai kebutuhan algoritma yang digunakan

**Proses Data Preparation**
- Memuat dataset
Dataset diimpor menggunakan pandas untuk kemudian dilakukan eksplorasi awal. Alasan: Membaca data merupakan langkah awal sebelum analisis lebih lanjut
- Pemeriksaan data kosong dan tipe data
Menggunakan df.info() dan df.isnull().sum() untuk mengecek nilai kosong dan tipe data. Alasan: Menghindari error dalam proses transformasi atau pelatihan model akibat missing value atau tipe data yang tidak sesuai
- Visualisasi dan deteksi outlier
Fitur numerik seperti Age, Height, dan Weight divisualisasikan menggunakan boxplot. Outlier diidentifikasi dan ditangani menggunakan metode IQR (Interquartile Range). Alasan: Outlier dapat merusak performa model, terutama pada algoritma berbasis jarak seperti KNN
- Pemisahan fitur kategorikal dan numerikal
Fitur diklasifikasikan agar bisa diproses sesuai jenisnya. Alasan: Transformasi untuk data kategorikal dan numerikal berbeda. Misalnya, numerik perlu distandarisasi, sementara kategorikal perlu encoding
- One-Hot Encoding pada Fitur Kategorikal  
Fitur kategorikal seperti Gender, family_history_with_overweight, FAVC, CAEC, SMOKE, SCC, CALC, MTRANS dan lainnya diubah menjadi representasi numerik menggunakan One-Hot Encoding. Alasan: Model machine learning tidak dapat bekerja dengan data kategorikal langsung, sehingga encoding diperlukan untuk representasi numerik tanpa memberikan urutan pada kategori
- Reduksi Dimensi dengan Principal Component Analysis (PCA)  
Setelah encoding dan scaling, dilakukan reduksi dimensi menggunakan PCA untuk menyederhanakan kompleksitas fitur dan mempercepat proses pelatihan. Alasan: Mengurangi jumlah fitur sambil mempertahankan informasi penting dari data, membantu mencegah overfitting dan mengurangi beban komputasi
- Pemisahan data latih dan uji
Data dibagi menjadi X_train, X_test, y_train, y_test menggunakan train_test_split. Alasan: Untuk menghindari overfitting dan mengukur generalisasi model
- Scaling pada Fitur Numerikal
Fitur numerik ['FCVC', 'NCP', 'CH2O', 'FAF', 'TUE'] dinormalisasi menggunakan StandardScaler dari scikit-learn. Alasan: Scaling diperlukan agar semua fitur numerik berada pada skala yang sama, yang penting untuk algoritma seperti KNN dan regresi logistik

## Modeling
Dalam proyek ini, digunakan tiga algoritma klasifikasi untuk memprediksi tingkat obesitas seseorang berdasarkan data gaya hidup, yaitu K-Nearest Neighbors (KNN), Random Forest (RF), dan Logistic Regression (LR). Setiap model dievaluasi menggunakan metrik akurasi, precision, recall, dan F1-score pada data uji.

#### K-Nearest Neighbors (KNN)

KNN bekerja dengan mengklasifikasikan sebuah data berdasarkan mayoritas kelas dari tetangga terdekatnya. Pada proyek ini, parameter yang digunakan adalah `n_neighbors=5` yang merupakan nilai default.

- **Akurasi Training:** 0.92  
- **Akurasi Testing:** 0.73  
- **Kelebihan:** Mudah dipahami dan diimplementasikan, tidak membutuhkan proses pelatihan yang kompleks.  
- **Kekurangan:** Sensitif terhadap skala data dan outlier, serta performa menurun jika dataset besar atau memiliki banyak fitur.

#### Random Forest (RF)

Random Forest merupakan ensemble learning yang membangun banyak decision tree secara acak dan mengambil hasil voting terbanyak sebagai prediksi akhir  
Parameter yang digunakan pada model ini adalah:  
- n_estimators=100: Jumlah pohon dalam hutan. Sebagai nilai default
- max_depth=16: Kedalaman maksimum tiap pohon keputusan untuk menghindari overfitting. Pengaturan max_depth bertujuan untuk membatasi kompleksitas model dan mencegah overfitting
- random_state=55: Untuk memastikan reprodusibilitas hasil. random_state digunakan untuk menjaga hasil
- n_jobs=-1: Menggunakan seluruh core CPU yang tersedia untuk mempercepat proses pelatihan. n_jobs digunakan untuk proses pelatihan bisa berjalan secara paralel dan lebih efisien

Nilai akurasi yang didapat dengan menggunakan model Random Forest:  
- **Akurasi Training:** 1.00  
- **Akurasi Testing:** 0.78  
- **Kelebihan:** Mampu menangani data yang kompleks dengan banyak fitur, lebih tahan terhadap overfitting dibanding decision tree tunggal, serta memberikan informasi mengenai fitur penting.  
- **Kekurangan:** Interpretasi model lebih kompleks dan waktu pelatihan bisa lebih lama dibanding model sederhana.

#### Logistic Regression (LR)

Logistic Regression memodelkan probabilitas keluaran sebagai fungsi logistik dari kombinasi linier fitur input  
Parameter yang digunakan pada model ini adalah: 
- max_iter=500: untuk memastikan model mencapai konvergensi karena jumlah iterasi default (100) tidak mencukupi
- random_state=55: untuk menjaga konsistensi hasil 

Nilai akurasi yang didapat dengan menggunakan model Random Forest:  
- **Akurasi Training:** 0.85  
- **Akurasi Testing:** 0.57  
- **Kelebihan:** Cepat dilatih, mudah diinterpretasi secara probabilistik, cocok sebagai baseline model.  
- **Kekurangan:** Kurang cocok untuk data dengan pola non-linear, dan rentan terhadap multikolinearitas antar fitur.

#### Model Terbaik

Berdasarkan hasil evaluasi pada data uji:

- Random Forest memiliki akurasi tertinggi (0.78) dan metrik precision, recall, serta F1-score yang stabil untuk hampir semua kelas, termasuk kelas dengan jumlah data kecil.  
- KNN memiliki akurasi yang cukup baik (0.73) namun lebih sensitif terhadap perubahan data dan beberapa kelas seperti *Normal_Weight* menunjukkan F1-score yang rendah.  
- Logistic Regression menunjukkan performa paling rendah (0.57) dan kesulitan memprediksi beberapa kelas dengan baik.

**Model Terpilih:** Random Forest  
Random Forest dipilih sebagai model terbaik karena memberikan performa paling konsisten dan akurat pada berbagai kelas obesitas, serta memiliki keunggulan dalam menangani data dengan banyak fitur dan ketidakseimbangan kelas.

## Evaluation

#### Metrik Evaluasi yang Digunakan

- **Akurasi (Accuracy)**  
Mengukur proporsi prediksi yang benar dari total keseluruhan data. Akurasi memberikan gambaran umum tentang seberapa baik model dapat mengklasifikasikan data secara tepat.
- **Precision**  
Mengukur ketepatan prediksi positif, yaitu berapa banyak prediksi kelas tertentu yang benar-benar sesuai dengan kelas tersebut. Precision penting untuk menghindari false positive yang berlebihan.
- **Recall (Sensitivity)**  
Mengukur kemampuan model dalam menemukan seluruh data positif sebenarnya dari suatu kelas. Recall menilai seberapa baik model menangkap semua kasus dari kelas tertentu, sangat penting apabila false negative harus diminimalkan.
- **F1 Score**  
Merupakan rata-rata harmonis antara precision dan recall, memberikan metrik tunggal yang menyeimbangkan keduanya. F1 score sangat berguna saat dataset tidak seimbang antar kelas.

#### Hasil Evaluasi Model

- K-Nearest Neighbors
	- Akurasi Training: 92.2%
	- Akurasi Testing: 73.0%
 	- Akurasi mse (train): 92.19%
  	- Akurasi mse (test): 91.49%     
   	- Precision (macro avg): 0.74
   	- Precision (weighted avg): 0.76
   	- Recall (macro avg): 0.71
   	- Recall (weighted avg): 0.73
  	- F1 Score (macro avg): 0.69
   	- F1 Score (weighted avg): 0.71
- Random Forest  
  	- Akurasi Training: 100.0%  
  	- Akurasi Testing: 78.7%
	- Akurasi  mse (train): 100.0%
 	- Akurasi  mse (test): 90.78%  
  	- Precision (macro avg): 0.79  
  	- Precision (weighted avg): 0.83  
  	- Recall (macro avg): 0.76  
  	- Recall (weighted avg): 0.79  
  	- F1 Score (macro avg): 0.76
  	- F1 Score (weighted avg): 0.79  
- Logistic Regression
	- Akurasi Training: 85.5%  
	- Akurasi Testing: 57.4%
	- Akurasi mse (train): 85.49%
 	- Akurasi mse (test): 82.98%  
	- Precision (macro avg): 0.57  
	- Precision (weighted avg): 0.55  
	- Recall (macro avg): 0.55  
	- Recall (weighted avg): 0.57  
	- F1 Score (macro avg): 0.47  
	- F1 Score (weighted avg): 0.49 

#### Kesimpulan dan Model Terbaik

Berdasarkan hasil evaluasi metrik, **Random Forest** menunjukkan performa terbaik dengan keseimbangan antara akurasi dan kemampuan mengenali kelas minoritas secara stabil. Model ini mampu menangani kompleksitas data dan ketidakseimbangan kelas lebih baik dibandingkan KNN dan Logistic Regression

#### Hubungan dengan Business Understanding

Model klasifikasi tingkat obesitas ini memberikan kontribusi penting bagi pengambilan keputusan dalam bidang kesehatan, khususnya:
- **Menjawab Problem Statement**  
Model telah mampu memprediksi tingkat obesitas berdasarkan data gaya hidup dengan akurasi yang cukup tinggi, yang artinya sudah menjawab permasalahan utama proyek
- **Mencapai Goals yang Diharapkan**  
Model Random Forest yang dipilih memenuhi target untuk klasifikasi multi-kelas yang seimbang dan dapat diandalkan dalam konteks prediksi obesitas
- **Dampak Solusi terhadap Business**  
Solusi ini membantu dalam deteksi dini risiko obesitas sehingga memungkinkan intervensi lebih cepat dan tepat sasaran. Ini berpotensi meningkatkan efektivitas program kesehatan masyarakat dan mengurangi biaya perawatan jangka panjang akibat obesitas


**---Ini adalah bagian akhir laporan---**
