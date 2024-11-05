# Laporan Proyek Machine Learning - Nauval Dwi Primadya

<div align="justify">


   
## Domain Proyek
Domain yang dipilih untuk proyek *machine learning* ini adalah **Pertanian**, dengan judul **Predictive Analytics: Kualitas Buah Pisang**


![Foto Buah Pisang](https://github.com/Primadya/predictiveanalyticsdicoding/blob/main/image/buahpisang.jpg)



Indonesia merupakan salah satu produsen pisang utama di Asia Tenggara dengan produksi tahunan yang mencapai sekitar 8 juta ton, menjadikannya komoditas pertanian bernilai tinggi yang memberikan kontribusi penting terhadap perekonomian nasional. Pisang memiliki nilai ekonomis yang besar bagi petani lokal, namun industri ini menghadapi tantangan signifikan dalam menjaga mutu produk. Mutu pisang dapat mengalami penurunan akibat sejumlah faktor, seperti ukuran buah yang tidak sesuai standar, tingkat kematangan yang tidak optimal, dan tekstur yang tidak memenuhi kualitas ideal. Penurunan mutu ini dapat menimbulkan dampak ekonomi yang merugikan, baik bagi petani maupun distributoraatan [[1](https://journal.ipb.ac.id/index.php/jagbi/article/view/36753)].
Predictive analytics dalam sektor pisang menunjukkan potensi besar dalam meningkatkan nilai komoditas ini. Teknologi ini dapat mendukung petani dengan meningkatkan kualitas serta jumlah hasil panen, yang pada akhirnya dapat meningkatkan pendapatan mereka. Selain itu, distributor diuntungkan melalui pengurangan risiko kerugian dan peningkatan efisiensi dalam manajemen rantai pasokan. Dari sisi konsumen, teknologi ini memungkinkan akses terhadap pisang berkualitas tinggi dengan harga yang lebih stabil. 

## Business Understanding

Pengembangan model prediksi kualitas buah pisang memiliki potensi signifikan untuk memberikan manfaat bagi berbagai pemangku kepentingan, termasuk petani dan distributor. Model ini dapat berfungsi untuk meningkatkan mutu hasil panen pisang, memperkuat nilai ekonomi buah, serta meningkatkan tingkat kepercayaan konsumen. Sebagai contoh, akurasi prediksi kualitas pisang yang tinggi dapat mendukung petani dalam melakukan seleksi buah secara lebih efektif dan memungkinkan penentuan harga jual yang lebih presisi di masa mendatang.

### Problem Statements

Berdasarkan latar belakang yang telah dijelaskan, berikut ini adalah perincian masalah yang dapat diatasi dalam proyek ini:

1.  Bagaimana cara mengembangkan model machine learning untuk memprediksi kualitas pisang berdasarkan data visual dan sensorik?
2.  Model seperti apa yang mampu mencapai tingkat akurasi prediksi tertinggi?
3.  Bagaimana penerapan model ini dapat mendukung petani dan distributor dalam meningkatkan kualitas serta nilai ekonomi dari buah pisang?

### Goals

Berikut adalah tujuan atau hasil yang diharapkan dari masing-masing pertanyaan dalam proyek ini:

1. **Pengembangan model machine learning untuk memprediksi kualitas pisang**  
   - Menghasilkan model machine learning yang dapat menganalisis data untuk memprediksi kualitas pisang secara akurat. Model ini diharapkan mampu mengidentifikasi faktor-faktor yang memengaruhi kualitas pisang sehingga dapat membantu dalam proses seleksi dan pemantauan kualitas.

2. **Menentukan model dengan akurasi prediksi terbaik**  
   - Menemukan model yang memiliki tingkat akurasi paling tinggi melalui evaluasi berbagai algoritma machine learning. Model terbaik akan diidentifikasi berdasarkan hasil uji akurasi dan konsistensinya dalam memprediksi kualitas pisang di berbagai kondisi.

3. **Mengoptimalkan kualitas dan nilai jual pisang bagi petani dan distributor**  
   - Memberikan solusi bagi petani dan distributor untuk meningkatkan kualitas pisang melalui panduan pemilahan dan pengelolaan buah berdasarkan prediksi model. Dengan demikian, model ini diharapkan membantu meningkatkan nilai jual pisang, mengurangi buah yang rusak atau tidak layak jual, dan memperbaiki efisiensi rantai pasokan.


### Solution statements
Melakukan analisis data secara mendalam melalui univariate dan multivariate analysis merupakan langkah penting dalam memahami karakteristik data. Visualisasi data juga digunakan untuk memperoleh pemahaman yang lebih komprehensif, termasuk dalam mengidentifikasi matriks korelasi antar fitur dan mendeteksi keberadaan outlier. 
- Melakukan pembersihan data (_data cleaning_) dan normalisasi data untuk memastikan prediksi yang optimal.
- Mengembangkan beberapa variasi model machine learning untuk membandingkan performa dan menentukan model terbaik dalam memprediksi kualitas pisang. diantaranya adalah :
    * Random Forest
      Random forest adalah salah satu metode machine learning yang digunakan untuk tugas klasifikasi dan regresi [[2](https://repository.uinjkt.ac.id/dspace/handle/123456789/55034)]. Metode ini bekerja dengan menggabungkan beberapa pohon keputusan untuk meningkatkan akurasi dan mengurangi masalah overfitting. Random forest cukup populer karena kemudahan implementasinya, kemampuannya mengatasi ketidakseimbangan data, serta penerapannya pada klasifikasi dengan banyak kelas (multiclass).
    * Gradient Boosting
      Gradient boosting adalah teknik pembelajaran mesin yang sangat efektif dalam meningkatkan kinerja model klasifikasi dan regresi. Teknik ini bekerja dengan menggabungkan beberapa pohon keputusan kecil yang diperbaiki secara iteratif untuk memperoleh model akhir yang lebih akurat. Gradient boosting telah digunakan dalam berbagai aplikasi, termasuk prediksi keberhasilan telemarketing, deteksi penyakit, dan klasifikasi aktivitas fisik [[3](https://ejournal3.undip.ac.id/index.php/gaussian/article/view/31335)].
    * Support Vector Machine
      Support Vector Machine (SVM) adalah algoritma pembelajaran terarah yang digunakan untuk tugas klasifikasi dan regresi. SVM bekerja dengan mencari garis atau hiperseperti yang memaksimalkan jarak antara data dari setiap kelas dalam ruang N-dimensi2. SVM dikenal karena kemampuannya dalam mengatasi masalah klasifikasi linear dan non-linear dengan menggunakan fungsi kernel, seperti kernel linear, polynomial, radial basis function (RBF), atau sigmoid [[4](https://jurnal.umk.ac.id/index.php/ijtis/article/download/7530/pdf)].
    * K-Nearest Neighbors
      K-Nearest Neighbor (KNN) adalah salah satu algoritma machine learning yang digunakan dalam tugas klasifikasi dan regresi. Pendekatan ini dilakukan dengan mencari sejumlah k titik data terdekat dengan data yang ingin diklasifikasikan atau diregresikan. Selanjutnya, KNN memilih kelas atau nilai regresi yang paling sering muncul di antara k titik data tersebut. KNN dikenal karena kesederhanaannya dalam implementasi dan mampu memberikan hasil yang memuaskan, terutama pada dataset yang berukuran relatif kecil [[5](https://journal.ugm.ac.id/ijccs/article/view/65176)].
    * Logistic Regression 
      merupakan salah satu metode statistika yang digunakan untuk memprediksi hasil biner dari suatu variabel dependen berdasarkan satu atau lebih variabel independen. Pendekatan ini telah  menjadi  sangat  populer  dalam  analisis  data  yang  melibatkan  variabel  kategorial  dan  memiliki penerapan yang luas di berbagai bidang disiplin ilmu, termasuk ekonomi, kedokteran, dan ilmu sosial [[6](https://core.ac.uk/download/pdf/327105237.pdf)]

## Data Understanding
### EDA - Deskripsi Variabel
**Informasi Datasets**


| Jenis | Keterangan |
| ------ | ------ |
| Title | Banana Quality |
| Source | [Kaggle](https://www.kaggle.com/datasets/l3llff/banana) |
| Maintainer | [l3LlFF ](https://www.kaggle.com/l3llff) |
| License | [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0) |
| Visibility | Publik |
| Tags | _Earth and Nature, Education, Food, Data Visualization, Exploratory Data Analysis, Binary Classification_ |
| Usability | 10.00 |

Berikut informasi pada dataset: 


 | Size | Weight | Sweetness | Softness | HarvestTime | Ripeness | Acidity | Quality |
 | ------ |------ | ------ | ------ | ------ |------ | ------ |------ |
 | -1.924968 |0.468078 | 3.077832 |-1.472177 | 0.294799 |2.435570	| 0.271290  |Good |
 | -2.409751 |0.486870 | 0.346921 |-2.495099 | -0.892213 | 2.067549 | 0.307325  |Good |
 | -0.357607 |1.483176 | 1.568452 |-2.645145 | -0.647267 |3.090643	| 1.427322  |Good |
 | -0.868524 |1.566201 | 1.889605 |-1.273761 | -1.006278 |1.873001	| 0.477862  |Good |
 | 0.651825 |1.319199 | -0.022459 |-1.209709 | -1.430692 |1.078345	| 2.812442  |Good |


Tabel 1.

Tabel 1 menyajikan hasil *Exploratory Data Analysis* (EDA) dari deskripsi variabel. Dataset ini telah melalui proses *preprocessing* awal, termasuk pembersihan dan normalisasi.

- Dataset ini tersedia dalam format CSV (Comma-Separated Values).
- Dataset terdiri atas 8000 sampel dan 8 fitur.
- Dari total fitur, 7 memiliki tipe data float64, sedangkan 1 lainnya bertipe object.

### Variabel-variabel pada dataset adalah sebagai berikut:
Informasi dari dataframe diatas adalah sebagai berikut, yang terdiri dari 8 kolom. 

- **Size**: ukuran buah
- **Weight**: berat buah
- **Sweetness**: tingkat kemanisan buah
- **Softness**: kelembutan buah
- **HarvestTime**: waktu yang telah berlalu sejak buah dipanen
- **Ripeness**: tingkat kematangan buah
- **Acidity**: tingkat keasaman buah
- **Quality**: kualitas buah

pada label `Quality` dirubah menjadi `label` agar memudahkan dalam pengolahan data. 

### EDA - Univariate Analysis

![Analisis Univariat (Data Kategori)](https://github.com/Primadya/predictiveanalyticsdicoding/blob/main/image/gambar%201.png)

Gambar 1.1. Analisis Univariat (Data Kategori) 

![Univariate Analysis](https://github.com/Primadya/predictiveanalyticsdicoding/blob/main/image/gambar%2012.png)

Gambar 1.2. Analisis Univariat (Data Numerik) 

 Berdasarkan _Gambar 1.1_ , dapat dilihat bahwa distribusi data katagorik _laebl_ yang terdiri dari _good_ dan _bad_ kualitas apel, yang mana nilai data **bad** terdiri dari `3994` dan **good** terdiri dari `4006`, yang mana menunjukan perbandingan data yang tidak terlalu jauh. 
 Pada _Gambar 1.2,_ untuk data numerik memiliki karakteristik, yaitu:
  Distribusi variabel numerik pada gambar di atas menunjukkan beberapa karakteristik penting yang mencerminkan sifat statistik dari dataset setelah melalui proses normalisasi, kemungkinan dengan metode z-score normalization. Berikut adalah hasil observasi dari masing-masing variabel:

- **Size**: Distribusi variabel ini menunjukkan bahwa ukuran rata-rata buah terletak di sekitar rentang -2 hingga 2, dengan persebaran data yang simetris. Rentang ini menunjukkan ukuran buah yang relatif seragam dalam dataset.
- **Weight**: Data berat buah juga memiliki distribusi yang simetris di sekitar nol, dengan sebagian besar nilai terletak antara -2 dan 2. Hal ini mengindikasikan bahwa rata-rata berat buah dalam dataset telah dinormalisasi, sehingga mendekati distribusi normal dengan rata-rata di sekitar nol.
- **Sweetness**: Tingkat kemanisan buah memiliki distribusi serupa, dengan nilai yang terkonsentrasi di antara -2 hingga 2. Simetri distribusi ini menunjukkan tingkat kemanisan yang terdistribusi secara merata.
- **Softness**: Distribusi kekerasan atau kelembutan buah menunjukkan sedikit asimetri, dengan puncak distribusi yang tidak sepenuhnya simetris, mengindikasikan variasi yang lebih besar dalam tekstur buah.
- **HarvestTime** dan **Ripeness**: Kedua variabel ini memiliki pola distribusi yang simetris dan terkonsentrasi di sekitar nol, menunjukkan bahwa waktu panen dan tingkat kematangan buah cenderung terdistribusi secara merata, tanpa ada bias yang signifikan.
- **Acidity**: Distribusi variabel tingkat keasaman juga simetris di sekitar nol, dengan rentang antara -2 hingga 2. Hal ini menunjukkan bahwa keasaman buah dalam dataset memiliki penyebaran yang relatif seragam.

Berdasarkan pola distribusi ini, dapat disimpulkan bahwa dataset telah dinormalisasi menggunakan metode z-score normalization, di mana setiap nilai data dikurangi dengan nilai rata-rata (mean) dan kemudian dibagi dengan standar deviasi. Proses ini menghasilkan distribusi dengan rata-rata mendekati nol dan standar deviasi mendekati satu untuk setiap variabel, sehingga memungkinkan analisis yang lebih komparatif antar variabel.


### EDA - Multivariate Analysis

![Multivariate Analysis](https://github.com/Primadya/predictiveanalyticsdicoding/blob/main/image/gambar%2021.png)


Gambar 2.1. Analisis Multivariat

![Multivariate Analysis](https://github.com/Primadya/predictiveanalyticsdicoding/blob/main/image/gambar%2022.png)


Gambar 2.2. Analisis Matriks Korelasi

Pada _Gambar 2.1. Analisis Multivariat_, matriks scatterplot yang menunjukkan hubungan antara delapan variabel: "Size," "Weight," "Sweetness," "Softness," "HarvestTime," "Ripeness," dan "Acidity." Histogram di diagonal memperlihatkan distribusi masing-masing variabel, sementara scatterplot di luar diagonal menunjukkan hubungan antar-variabel. Sebagian besar scatterplot menunjukkan pola titik yang menyebar dan berbentuk bundar, menandakan bahwa tidak ada korelasi yang kuat atau pola linier antara variabel-variabel ini, sehingga variabel-variabel tersebut tampak cukup independen satu sama lain. Secara keseluruhan, plot ini menunjukkan bahwa tidak ada hubungan atau pola signifikan di antara variabel-variabel yang dianalisis.

Pada _Gambar 2.2_ Matriks korelasi pada gambar di atas menunjukkan hubungan linier antara variabel numerik dalam dataset, diukur menggunakan koefisien korelasi Pearson yang berkisar antara -1 hingga 1. Nilai koefisien positif (ditandai dengan warna merah) menunjukkan korelasi positif, di mana peningkatan nilai pada satu variabel cenderung diikuti oleh peningkatan pada variabel lainnya. Sebaliknya, koefisien negatif (ditandai dengan warna biru) menunjukkan korelasi negatif, di mana peningkatan nilai pada satu variabel berkaitan dengan penurunan pada variabel lainnya.

Beberapa temuan utama dari matriks korelasi ini adalah sebagai berikut:

1. **Size dan HarvestTime** memiliki korelasi positif yang cukup kuat (0,58), mengindikasikan bahwa ukuran buah yang lebih besar cenderung membutuhkan waktu lebih lama hingga mencapai masa panen. Korelasi ini menunjukkan adanya keterkaitan antara perkembangan ukuran buah dan waktu panennya.

2. **Weight dan Sweetness** menunjukkan korelasi positif moderat (0,4), yang mengindikasikan bahwa buah dengan bobot lebih besar cenderung memiliki tingkat kemanisan yang lebih tinggi. Hal ini mungkin terkait dengan akumulasi gula yang meningkat seiring pertambahan massa buah.

3. **Ripeness dan Acidity** memiliki korelasi negatif sebesar -0,35. Korelasi ini menunjukkan bahwa buah yang lebih matang cenderung memiliki tingkat keasaman yang lebih rendah, yang dapat mengindikasikan bahwa keasaman berkurang seiring proses pematangan.

4. **Size dan Sweetness** memiliki korelasi negatif (-0,27), yang menunjukkan bahwa buah dengan ukuran yang lebih besar cenderung memiliki tingkat kemanisan yang lebih rendah, sebuah indikasi potensi hubungan invers antara ukuran fisik dan karakteristik rasa buah.

5. Mayoritas variabel lainnya menunjukkan korelasi yang lemah atau mendekati nol, menandakan bahwa tidak terdapat hubungan linier yang signifikan antar variabel tersebut dalam konteks ini.

Analisis korelasi ini memberikan wawasan mengenai potensi hubungan antar variabel, yang dapat menjadi dasar untuk analisis lebih lanjut dalam mengeksplorasi faktor-faktor yang memengaruhi karakteristik buah dalam dataset ini.

## Data Preparation
Dalam tahap *Data Preparation*, dilakukan beberapa aktivitas seperti *Data Gathering*, *Data Assessing*, dan *Data Cleaning*. Pada *Data Gathering*, data diimpor dalam format yang sesuai agar dapat diolah dengan baik menggunakan dataframe Pandas. Tahap *Data Assessing* mencakup pemeriksaan beberapa aspek, termasuk: duplikasi data (data yang identik dengan entri lainnya), nilai yang hilang (*missing values*), dan nilai ekstrem (*outliers*) yang menyimpang dari pola umum data. 

Selama *Data Cleaning*, beberapa langkah dilakukan, antara lain:
- Mengubah tipe kolom agar sesuai dengan kebutuhan analisis (*Converting Column Type*).
- Membagi data menjadi data latih dan data uji menggunakan *Train Test Split*.
- Melakukan normalisasi untuk menyelaraskan rentang nilai semua fitur atau atribut, sehingga memiliki skala yang sebanding.

Dalam proyek ini, tidak ditemukan duplikasi data dan *missing value*. Sedangkan, untuk *outliers*, metode *dropping* berbasis *Interquartile Range* (IQR) digunakan, dengan menghitung IQR sebagai selisih antara kuartil ketiga (Q3) dan kuartil pertama (Q1), sesuai dengan rumus berikut:

$$IQR = Q_3 - Q_1$$

- Q1 adalah kuartil pertama
- Q3 adalah kuartil ketiga

Setelah menghapus *outliers* dengan metode IQR, jumlah data berkurang dari `8.000` menjadi `7.645`. Pembagian data latih dan data uji dilakukan dengan fungsi *Train Test Split* dari library *sklearn.model_selection*, dengan rasio 80:20 dan *random state* sebesar 42. Selain itu, normalisasi dilakukan menggunakan *MinMaxScaler* dari library *sklearn.preprocessing* untuk menyelaraskan skala dataset. Seluruh proses ini bertujuan untuk menghasilkan model yang optimal.

## Modeling
- Random Forest
   Random Forest sangat efisien dalam menangani dataset berdimensi tinggi dan robust terhadap nilai ekstrem (outlier). Algoritma ini meningkatkan akurasi prediksi dengan teknik ensemble, tetapi dapat rentan terhadap overfitting pada dataset kecil dan membutuhkan waktu komputasi yang tinggi.

- Gradient Boosting
   Gradient Boosting efektif pada dataset kompleks dan mampu menangani variasi data dengan baik. Namun, algoritma ini memerlukan waktu komputasi yang tinggi dan lebih mudah mengalami overfitting dibandingkan dengan Random Forest.

- Support Vector Machine (SVM)
   SVM memberikan akurasi prediksi yang tinggi dan mampu menangani dataset berdimensi tinggi. Meskipun begitu, SVM membutuhkan waktu komputasi yang signifikan dan sensitif terhadap pilihan kernel yang digunakan.

- K-Nearest Neighbors (KNN)
   KNN adalah algoritma yang sederhana dan intuitif, cocok untuk klasifikasi dan regresi. Namun, algoritma ini memerlukan memori dan waktu komputasi yang besar, serta sensitif terhadap nilai-nilai ekstrem (outlier).

- Logistic Regression
   Logistic Regression mudah diinterpretasikan dan efektif untuk masalah linier. Sayangnya, model ini kurang akurat pada dataset yang kompleks atau non-linear dan mungkin memerlukan algoritma yang lebih canggih.

## Evaluation
Pada tahap evaluasi model, metrik yang digunakan adalah *accuracy*, yaitu ukuran yang menggambarkan persentase prediksi yang benar dari total prediksi yang dilakukan. *Accuracy* diperoleh dengan membandingkan jumlah prediksi benar dengan jumlah total prediksi, sesuai dengan rumus berikut:

$$\text{Accuracy} = \frac{\text{TP + TN}}{\text{TP + TN + FP + FN}} \times 100\%$$

**Penjelasan Komponen:**
- **TP (True Positive):** Jumlah data positif yang berhasil diklasifikasikan dengan benar sebagai positif.
- **TN (True Negative):** Jumlah data negatif yang berhasil diklasifikasikan dengan benar sebagai negatif.
- **FP (False Positive):** Jumlah data negatif yang salah diklasifikasikan sebagai positif (Kesalahan Tipe I).
- **FN (False Negative):** Jumlah data positif yang salah diklasifikasikan sebagai negatif (Kesalahan Tipe II).

Rumus ini menghitung rasio antara jumlah data yang diklasifikasikan dengan benar (TP dan TN) dengan jumlah keseluruhan data yang dievaluasi, kemudian mengalikannya dengan 100% untuk menyajikan hasil dalam bentuk persentase.

Di bawah ini adalah hasil *accuracy* dari lima model yang digunakan dalam proyek ini, yaitu *Random Forest*, *Gradient Boosting*, *Support Vector Machine (SVM)*, *K-Nearest Neighbors (KNN)*, dan *Logistic Regression*:

| Model                        | Accuracy |
|------------------------------|----------|
| K-Nearest Neighbors (KNN)    | 0.98     |
| Random Forest                | 0.97     |
| Support Vector Machine (SVM) | 0.99     |
| Gradient Boosting            | 0.95     |
| Logistic Regression          | 0.87     |


![Plot Akurasi](https://github.com/Primadya/predictiveanalyticsdicoding/blob/main/image/gambar%203.png)

Analisis Hasil:

- Support Vector Machine (SVM) memiliki akurasi tertinggi di antara semua model yang diuji, mencapai 0.99. Ini menunjukkan bahwa SVM memiliki kemampuan yang sangat baik dalam mengidentifikasi pola dalam dataset dan memisahkan kelas dengan margin yang optimal.
- K-Nearest Neighbors (KNN) juga menunjukkan kinerja yang sangat baik dengan akurasi sebesar 0.98. Akurasi yang tinggi pada KNN menunjukkan bahwa untuk dataset ini, pendekatan berbasis tetangga terdekat mampu menangkap hubungan antara data secara efektif.
- Random Forest mencapai akurasi 0.97, yang juga sangat tinggi. Sebagai metode ensemble yang menggabungkan prediksi dari banyak decision tree, Random Forest efektif dalam menangani variasi data yang tinggi dan tidak sensitif terhadap outlier.
- Gradient Boosting memiliki akurasi sebesar 0.95, sedikit lebih rendah dibandingkan SVM, KNN, dan Random Forest. Meskipun akurasinya tinggi, metode Gradient Boosting cenderung rentan terhadap overfitting jika tidak disetel dengan hati-hati, yang dapat menjelaskan performa yang sedikit lebih rendah.
- Logistic Regression memiliki akurasi terendah, yaitu 0.87, mengindikasikan bahwa model linier ini mungkin kurang mampu menangani dataset yang kompleks atau memiliki fitur non-linear yang kuat. Logistic Regression umumnya efektif untuk masalah klasifikasi sederhana, tetapi mungkin tidak optimal jika data memiliki pola yang lebih kompleks.

Secara keseluruhan, hasil ini menunjukkan bahwa Support Vector Machine (SVM) adalah model dengan akurasi tertinggi dalam proyek ini, diikuti oleh KNN dan Random Forest. Pemilihan model yang optimal, bagaimanapun, harus mempertimbangkan selain akurasi, juga metrik lain seperti precision, recall, dan F1 score, serta analisis lebih lanjut terhadap karakteristik dataset.



## Referensi
1. [Aurelia, R., Kurniati, D., & Hutajulu, J. P. (2022). Daya Saing Ekspor Pisang Indonesia Di Negara Tujuan Ekspor Periode 2000-2019. Jurnal Agribisnis Indonesia (Journal of Indonesian Agribusiness), 10(2), 335-349.](https://journal.ipb.ac.id/index.php/jagbi/article/view/36753)
2. [Fadilah, L. (2018). Klasifikasi Random Forest pada data imbalanced (Bachelor's thesis, Fakultas Sains dan Teknologi UIN Syarif Hidayatullah Jakarta).](https://repository.uinjkt.ac.id/dspace/handle/123456789/55034)
3. [Suryana, S. E., Warsito, B., & Suparti, S. (2021). Penerapan Gradient Boosting Dengan Hyperopt Untuk Memprediksi Keberhasilan Telemarketing Bank. Jurnal Gaussian, 10(4), 617-623.](https://ejournal3.undip.ac.id/index.php/gaussian/article/view/31335)
4. [Handayani, P. K. (2021). Penerapan Algoritma Support Vector Machine (Svm) Untuk Analisis Pola Klasifikasi Pada Parkinson’S Dataset. Indonesian Journal of Technology, Informatics and Science (IJTIS), 3(1), 31-35.](https://jurnal.umk.ac.id/index.php/ijtis/article/download/7530/pdf)
5. [Isnain, A. R., Supriyanto, J., & Kharisma, M. P. (2021). Implementation of K-Nearest Neighbor (K-NN) algorithm for public sentiment analysis of online learning. IJCCS (Indonesian Journal of Computing and Cybernetics Systems), 15(2), 121-130.](https://journal.ugm.ac.id/ijccs/article/view/65176)
6. [Setyati, W. A., Sunaryo, S., Rezagama, A., Widodo, A. K., & Yulianto, M. F. A. (2020). PENERAPAN REGRESI LOGISTIK DALAM PENENTUAN FAKTOR YANG MEMPENGARUHI JUMLAH WISATAWAN ECOTOURISM DESA BEDONO. Jurnal Enggano, 5(1), 11-22.](https://core.ac.uk/download/pdf/327105237.pdf)


</div>
