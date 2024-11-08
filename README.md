# Laporan Proyek Machine Learning - Nauval Dwi Primadya

<div align="justify">


## Domain Proyek
Domain yang dipilih untuk proyek *machine learning* ini adalah **Pertanian**, dengan judul **Predictive Analytics: Kualitas Buah Pisang**


![Foto Buah Pisang](https://github.com/Primadya/predictiveanalyticsdicoding/blob/main/image/buahpisang.jpg?raw=true)


Indonesia merupakan salah satu produsen pisang utama di Asia Tenggara dengan produksi tahunan yang mencapai sekitar 8 juta ton, menjadikannya komoditas pertanian bernilai tinggi yang memberikan kontribusi penting terhadap perekonomian nasional. Pisang memiliki nilai ekonomis yang besar bagi petani lokal, namun industri ini menghadapi tantangan signifikan dalam menjaga mutu produk. Mutu pisang dapat mengalami penurunan akibat sejumlah faktor, seperti ukuran buah yang tidak sesuai standar, tingkat kematangan yang tidak optimal, dan tekstur yang tidak memenuhi kualitas ideal. Penurunan mutu ini dapat menimbulkan dampak ekonomi yang merugikan, baik bagi petani maupun distributoraatan [[1](https://journal.ipb.ac.id/index.php/jagbi/article/view/36753)].
Predictive analytics dalam sektor pisang menunjukkan potensi besar dalam meningkatkan nilai komoditas ini. Teknologi ini dapat membantu petani dengan menjaga kualitas hasil panen, yang pada akhirnya dapat meningkatkan pendapatan mereka. Selain itu, distributor diuntungkan melalui pengurangan risiko kerugian dan peningkatan efisiensi dalam manajemen rantai pasokan. Dari sisi konsumen, teknologi ini memungkinkan akses terhadap pisang berkualitas tinggi dengan harga yang lebih stabil.

## Business Understanding

Pengembangan model prediksi kualitas buah pisang memiliki potensi signifikan untuk memberikan manfaat bagi berbagai pemangku kepentingan, termasuk petani dan distributor. Model ini dapat berfungsi untuk meningkatkan mutu hasil panen pisang, memperkuat nilai ekonomi buah, serta meningkatkan tingkat kepercayaan konsumen. Sebagai contoh, akurasi prediksi kualitas pisang yang tinggi dapat mendukung petani dalam melakukan seleksi buah secara lebih efektif dan memungkinkan penentuan harga jual yang lebih presisi di masa mendatang.

### Problem Statements

Berdasarkan latar belakang yang telah dijelaskan, berikut ini adalah perincian masalah yang dapat diatasi dalam proyek ini:

1. Bagaimana cara mengembangkan model *machine learning* untuk memprediksi kualitas pisang berdasarkan data visual dan sensorik?
2. Model seperti apa yang mampu mencapai tingkat akurasi prediksi tertinggi?
3. Bagaimana penerapan model ini dapat mendukung petani dan distributor dalam meningkatkan kualitas serta nilai ekonomi dari buah pisang?

### Goals

Berikut adalah tujuan atau hasil yang diharapkan dari masing-masing pertanyaan dalam proyek ini:

1. **Pengembangan model *machine learning* untuk memprediksi kualitas pisang**
   - Menghasilkan model *machine learning* yang dapat menganalisis data untuk memprediksi kualitas pisang secara akurat. Model ini diharapkan mampu mengidentifikasi faktor-faktor yang memengaruhi kualitas pisang sehingga dapat membantu dalam proses seleksi dan pemantauan kualitas.

2. **Menentukan model dengan akurasi prediksi terbaik**
   - Menemukan model yang memiliki tingkat akurasi paling tinggi melalui evaluasi berbagai algoritma *machine learning*. Model terbaik akan diidentifikasi berdasarkan hasil uji akurasi dan konsistensinya dalam memprediksi kualitas pisang di berbagai kondisi.

3. **Mengoptimalkan kualitas dan nilai jual pisang bagi petani dan distributor**
   - Memberikan solusi bagi petani dan distributor untuk meningkatkan kualitas pisang melalui panduan pemilahan dan pengelolaan buah berdasarkan prediksi model. Dengan demikian, model ini diharapkan membantu meningkatkan nilai jual pisang, mengurangi buah yang rusak atau tidak layak jual, dan memperbaiki efisiensi rantai pasokan.

### Solution Statements

Untuk mencapai tujuan di atas, beberapa langkah strategis direncanakan:

1. **Analisis dan Visualisasi Data**
   - Melakukan analisis data secara mendalam melalui analisis univariat dan multivariat untuk memahami karakteristik data.
   - Melakukan visualisasi data untuk memperoleh pemahaman komprehensif, termasuk identifikasi matriks korelasi antar fitur dan deteksi keberadaan outlier yang berpotensi memengaruhi hasil model.

2. **Pembersihan Data dan Normalisasi**
   - Melakukan pembersihan data (*data cleaning*) dengan menghapus nilai-nilai yang tidak valid dan mengatasi outlier. Selanjutnya, data dinormalisasi untuk memastikan setiap fitur berada pada skala yang seragam dan dapat mendukung prediksi yang optimal.

3. **Pengembangan Model *Machine Learning***
   - Mengembangkan beberapa variasi model *machine learning* untuk memprediksi kualitas pisang dan melakukan perbandingan performa untuk memilih model terbaik. Model yang akan dievaluasi meliputi:
     - **Random Forest**: Metode ini menggabungkan beberapa pohon keputusan untuk meningkatkan akurasi dan mengurangi masalah *overfitting* [[2](https://repository.uinjkt.ac.id/dspace/handle/123456789/55034)]. Random Forest cocok untuk klasifikasi multikelas dan mampu menangani data yang tidak seimbang dengan baik.
     - **Gradient Boosting**: Teknik ini menggabungkan beberapa pohon keputusan kecil secara iteratif untuk mendapatkan model yang lebih akurat [[3](https://ejournal3.undip.ac.id/index.php/gaussian/article/view/31335)]. Gradient Boosting sering digunakan dalam tugas prediksi dan klasifikasi yang kompleks.
     - **Support Vector Machine (SVM)**: Algoritma ini bekerja dengan memaksimalkan jarak antar kelas dalam ruang fitur. SVM efektif dalam menangani klasifikasi linear dan non-linear, terutama dengan penggunaan kernel seperti linear, polynomial, dan RBF [[4](https://jurnal.umk.ac.id/index.php/ijtis/article/download/7530/pdf)].
     - **K-Nearest Neighbors (KNN)**: Algoritma ini mengklasifikasikan data berdasarkan tetangga terdekatnya. KNN sederhana dalam implementasi dan menghasilkan hasil yang memadai pada dataset yang lebih kecil [[5](https://journal.ugm.ac.id/ijccs/article/view/65176)].
     - **Logistic Regression**: Metode ini digunakan untuk prediksi hasil biner dan populer untuk klasifikasi berdasarkan variabel kategorial. Logistic Regression memiliki aplikasi luas di berbagai disiplin ilmu [[6](https://core.ac.uk/download/pdf/327105237.pdf)].

4. **Evaluasi dan Pemilihan Model Terbaik**
   - Model terbaik akan dipilih berdasarkan akurasi dan stabilitasnya dalam berbagai kondisi data. Model ini akan dievaluasi melalui metrik akurasi, presisi, recall, dan F1-score untuk memastikan performa yang andal.

5. **Penerapan dan Manfaat Model**
   - Mengimplementasikan model terbaik untuk mendukung petani dan distributor dalam mengelola kualitas pisang. Dengan memanfaatkan model ini, pemangku kepentingan dapat melakukan pemilahan dan pengelolaan buah yang lebih efektif, sehingga mengurangi risiko kerusakan dan meningkatkan nilai jual pisang.

Dengan mengikuti langkah-langkah ini, proyek ini diharapkan dapat menghasilkan model prediksi kualitas pisang yang akurat, yang bermanfaat bagi seluruh pemangku kepentingan dalam rantai pasokan pisang.

## Data Understanding

### EDA - Deskripsi Variabel

### Informasi Datasets

| Jenis      | Keterangan                                                                 |
|------------|-----------------------------------------------------------------------------|
| Title      | Banana Quality                                                             |
| Source     | [Kaggle](https://www.kaggle.com/datasets/l3llff/banana)                  |
| Maintainer | [l3LlFF](https://www.kaggle.com/l3llff)                                   |
| License    | [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0)                  |
| Visibility | Publik                                                                      |
| Tags       | _Earth and Nature, Education, Food, Data Visualization, Exploratory Data Analysis, Binary Classification_ |
| Usability  | 10.00                                                                      |

Berikut informasi pada dataset:

| Size       | Weight     | Sweetness | Softness  | HarvestTime | Ripeness   | Acidity   | Quality |
|------------|------------|-----------|-----------|-------------|------------|-----------|--------|
| -1.924968  | 0.468078   | 3.077832  | -1.472177 | 0.294799    | 2.435570   | 0.271290  | Good   |
| -2.409751  | 0.486870   | 0.346921  | -2.495099 | -0.892213   | 2.067549   | 0.307325  | Good   |
| -0.357607  | 1.483176   | 1.568452  | -2.645145 | -0.647267   | 3.090643   | 1.427322  | Good    |
| -0.868524  | 1.566201   | 1.889605  | -1.273761 | -1.006278   | 1.873001   | 0.477862  | Good   |
| 0.651825   | 1.319199   | -0.022459 | -1.209709 | -1.430692   | 1.078345   | 2.812442  | Good   |

**Tabel 1.** Hasil *Exploratory Data Analysis* (EDA) dari deskripsi variabel. Dataset ini telah melalui proses *preprocessing* awal yang mencakup pembersihan dan normalisasi.

- **Tipe Data**: Terdapat tujuh variabel bertipe `float64` dan satu variabel `Quality` yang bertipe `object`. Kolom `Quality` telah diubah menjadi `label` untuk memudahkan analisis.
- **Kondisi Data**:
  - **Missing Values**: Tidak ditemukan nilai yang hilang di seluruh kolom dataset.
  - **Duplicate Values**: Tidak ada data duplikat yang ditemukan.

Untuk outliers, metode dropping berbasis Interquartile Range (IQR) digunakan, dengan menghitung IQR sebagai selisih antara kuartil ketiga (Q3) dan kuartil pertama (Q1):

$$IQR = Q_3 - Q_1$$

Setelah menghapus outliers, jumlah data berkurang dari `8.000` menjadi `7.645`.

- **Distribusi Data**: Analisis univariat menunjukkan bahwa distribusi variabel numerik simetris dan mendekati normal setelah normalisasi. Untuk data kategorikal, distribusi kualitas _Good_ (4006) dan _Bad_ (3994) cukup seimbang.
  
- **Korelasi Antar Variabel**: Analisis menunjukkan beberapa korelasi moderat, seperti antara Size dan HarvestTime (0,58) serta Ripeness dan Acidity (-0,35). Sebagian besar variabel lainnya menunjukkan korelasi lemah.

### Variabel-variabel pada dataset adalah sebagai berikut:
Dataset terdiri dari 8 kolom:

- **Size**: ukuran buah
- **Weight**: berat buah
- **Sweetness**: tingkat kemanisan
- **Softness**: kelembutan
- **HarvestTime**: waktu pascapanen
- **Ripeness**: tingkat kematangan
- **Acidity**: tingkat keasaman
- **Quality**: kualitas buah (label ini dirubah menjadi `label`).

### EDA - Univariate Analysis

![Analisis Univariat (Data Kategori)](https://github.com/Primadya/predictiveanalyticsdicoding/blob/main/image/gambar%201.png?raw=true)

**Gambar 1.1.** Analisis Univariat (Data Kategori)

![Univariate Analysis](https://github.com/Primadya/predictiveanalyticsdicoding/blob/main/image/gambar%2012.png?raw=true)

**Gambar 1.2.** Analisis Univariat (Data Numerik)

Berdasarkan **Gambar 1.1**, distribusi data kategorik menunjukkan jumlah data **bad** sebanyak `3994` dan **good** sebanyak `4006`, dengan perbandingan yang hampir seimbang. 

Pada **Gambar 1.2**, distribusi variabel numerik mencerminkan karakteristik statistik setelah normalisasi. Berikut adalah hasil observasi dari masing-masing variabel:

- **Size**: ukuran rata-rata buah terletak di rentang -2 hingga 2, dengan persebaran simetris.
- **Weight**: distribusi berat buah simetris di sekitar nol, mayoritas nilai antara -2 dan 2.
- **Sweetness**: kemanisan juga terkonsentrasi di antara -2 hingga 2.
- **Softness**: menunjukkan sedikit asimetri, mencerminkan variasi tekstur.
- **HarvestTime** dan **Ripeness**: pola distribusi simetris sekitar nol.
- **Acidity**: tingkat keasaman simetris di sekitar nol, rentang antara -2 hingga 2.

Dari analisis ini, dataset dinyatakan telah dinormalisasi menggunakan metode z-score normalization, memungkinkan analisis komparatif antar variabel.

### EDA - Multivariate Analysis

![Multivariate Analysis](https://github.com/Primadya/predictiveanalyticsdicoding/blob/main/image/gambar%2021.png?raw=true)

**Gambar 2.1.** Analisis Multivariat

![Multivariate Analysis](https://github.com/Primadya/predictiveanalyticsdicoding/blob/main/image/gambar%2022.png?raw=true)

**Gambar 2.2.** Analisis Matriks Korelasi

Pada **Gambar 2.1**, matriks scatterplot menunjukkan hubungan antar delapan variabel, tanpa pola linier yang kuat. 

Di **Gambar 2.2**, matriks korelasi mengungkap hubungan linier variabel numerik. Temuan utama termasuk:

1. **Size dan HarvestTime** memiliki korelasi positif kuat (0,58).
2. **Weight dan Sweetness** menunjukkan korelasi positif moderat (0,4).
3. **Ripeness dan Acidity** memiliki korelasi negatif (-0,35).
4. **Size dan Sweetness** menunjukkan korelasi negatif (-0,27).
5. Sebagian besar variabel lain menunjukkan korelasi lemah.

Analisis ini memberikan wawasan tentang hubungan antar variabel yang dapat dieksplorasi lebih lanjut dalam penelitian karakteristik buah dalam dataset ini.


## Data Preparation
Pada tahap ini, dilakukan beberapa teknik persiapan data yang meliputi penghapusan *outlier*, pengubahan tipe kolom dan pemetaan nilai, pembagian data menjadi set latih dan uji, serta normalisasi data. Teknik ini digunakan agar dataset siap digunakan dalam proses pemodelan *machine learning*. Berikut penjelasan teknik yang digunakan:

### 1. Menghapus *Outlier* Berdasarkan IQR

*Outlier* adalah data yang nilainya berada jauh dari mayoritas nilai lainnya dalam dataset, sehingga dapat memengaruhi performa model dalam mengidentifikasi pola yang representatif. Teknik *Interquartile Range* (IQR) digunakan untuk mendeteksi dan menghapus *outlier* pada data numerik. Langkahnya sebagai berikut:

- Menghitung Kuartil Pertama (Q1) dan Kuartil Ketiga (Q3) dari data numerik.
- Menghitung IQR sebagai selisih antara Q3 dan Q1.
- Menentukan rentang normal dengan rumus (Q1 - 1.5 * IQR) hingga (Q3 + 1.5 * IQR). Data yang berada di luar rentang ini dianggap sebagai *outlier*.
- Menghapus data yang diidentifikasi sebagai *outlier*.

```python
# Memilih kolom numerik saja
df_numeric = df.select_dtypes(include=[float, int])

# Menghitung Q1, Q3, dan IQR
Q1 = df_numeric.quantile(0.25)
Q3 = df_numeric.quantile(0.75)
IQR = Q3 - Q1

# Menghapus *outlier* berdasarkan IQR
df_numeric_clean = df_numeric[~((df_numeric < (Q1 - 1.5 * IQR)) | (df_numeric > (Q3 + 1.5 * IQR))).any(axis=1)]

# Menggabungkan kembali dengan kolom non-numerik (jika ada)
df = df.loc[df_numeric_clean.index]

# Melihat hasil dataset tanpa *outlier*
print(df.head())
```
Penghapusan outlier membantu meningkatkan keakuratan model karena data yang digunakan menjadi lebih konsisten dan representatif.

### 2. Pengubahan Tipe Kolom dan Mapping Label
Kolom Quality diubah namanya menjadi label untuk memudahkan proses pemodelan, dan data pada kolom ini dimapping sehingga nilai kategorikal seperti "Good" dan "Bad" dikonversi menjadi nilai numerik. Hal ini memudahkan algoritma machine learning dalam melakukan proses perhitungan.
```python
# Mengubah nama kolom dan mapping label
df['label'] = df['Quality'].map({'Good': 1, 'Bad': 0})
print(df.head())
```
Mapping ini memastikan bahwa data dapat digunakan langsung oleh model, menghindari kesalahan interpretasi karena data kategorikal diubah menjadi bentuk yang dapat dihitung.

### 3. Pembagian Data (Train-Test Split)
Dataset dibagi menjadi dua bagian utama: data latih (training set) dan data uji (test set), dengan rasio 80:20. Ini dilakukan untuk memisahkan data yang akan digunakan untuk melatih model dan data yang akan digunakan untuk menguji performa model pada data baru yang tidak pernah dilihat sebelumnya. Penggunaan random_state dengan nilai tetap (misalnya, 42) memastikan bahwa pembagian data dapat direplikasi secara konsisten.
```python
from sklearn.model_selection import train_test_split

# Pisahkan fitur dan label
X = df.drop('label', axis=1)  # Menghapus kolom label dari dataset
y = df['label']

# Membagi data menjadi train dan test
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# Informasi jumlah data
print(f'Total datasets: {len(X)}')
print(f'Total data Latih: {len(X_train)}')
print(f'Total data Uji: {len(X_test)}')
```
Pembagian data ini penting untuk menghindari data leakage (kebocoran data), yaitu ketika model "belajar" dari data yang seharusnya menjadi bagian dari pengujian.

### 4. Normalisasi Data
Normalisasi dilakukan untuk menyelaraskan rentang nilai tiap fitur, sehingga model lebih mudah untuk beradaptasi dan menghindari bias akibat skala fitur yang berbeda-beda. MinMaxScaler digunakan untuk mengubah nilai fitur menjadi rentang antara 0 dan 1, yang membuat proses komputasi lebih efisien dan hasil prediksi lebih stabil.
```python
from sklearn.preprocessing import MinMaxScaler

# Menerapkan normalisasi pada data train dan test
scaler = MinMaxScaler()
scaler.fit(X_train)
X_train = scaler.transform(X_train)
X_test = scaler.transform(X_test)
```
Normalisasi membantu model mencapai hasil yang lebih akurat dengan meratakan nilai fitur, terutama untuk algoritma yang sensitif terhadap perbedaan skala, seperti regresi linier atau k-nearest neighbors.

Dengan tahapan data preparation di atas, dataset menjadi lebih bersih, konsisten, dan siap untuk digunakan dalam pemodelan. Hal ini bertujuan untuk memastikan bahwa model memiliki performa optimal dan dapat diandalkan dalam memprediksi kualitas pisang.
    
## Modeling

### Random Forest
- **Konfigurasi**  
  Random Forest dipilih karena kemampuannya dalam menangani dataset berdimensi tinggi dan ketahanannya terhadap nilai ekstrem. Model ini dikonfigurasi dengan parameter `n_estimators=100`, yang menunjukkan jumlah pohon yang dibangun, dan `max_depth=10`, yang membatasi kedalaman pohon untuk menghindari overfitting. Parameter `random_state=42` ditambahkan untuk menjaga konsistensi hasil eksperimen.

- **Cara Kerja**  
  Random Forest membangun sejumlah pohon keputusan secara acak dan menggabungkan hasil prediksi dari masing-masing pohon untuk meningkatkan akurasi. Dengan mengintegrasikan hasil dari beberapa pohon, teknik ini juga mengurangi risiko overfitting melalui rata-rata hasil prediksi.

- **Kelebihan**
  1. Mampu menangani data berdimensi tinggi dengan baik.
  2. Tahan terhadap outlier dan lebih stabil dibandingkan model pohon tunggal.
  3. Dapat mengelola data dengan berbagai tipe fitur.

- **Kelemahan**
  1. Memerlukan lebih banyak sumber daya komputasi karena keberadaan banyak pohon dalam ensemble.
  2. Interpretasi hasil lebih kompleks dibandingkan model pohon tunggal.

### Gradient Boosting
- **Konfigurasi**  
  Gradient Boosting menggunakan parameter `learning_rate=0.1`, yang mengontrol kontribusi setiap pohon baru dalam memperbaiki kesalahan model sebelumnya, dan `n_estimators=100`, yang menunjukkan jumlah pohon dalam ensemble. Penetapan `random_state=42` memastikan hasil eksperimen yang konsisten.

- **Cara Kerja**  
  Gradient Boosting beroperasi secara iteratif, di mana setiap model baru dirancang untuk memperbaiki kesalahan dari model sebelumnya. Dengan menambahkan model baru untuk mengatasi kesalahan, akurasi meningkat secara bertahap dengan setiap iterasi dalam ensemble.

- **Kelebihan**
  1. Sangat akurat, terutama pada data yang kompleks.
  2. Mengatasi masalah underfitting melalui proses iteratif.

- **Kelemahan**
  1. Rentan terhadap overfitting jika parameter tidak diatur dengan baik.
  2. Cenderung memerlukan waktu lebih lama dalam proses pelatihan dibandingkan dengan model lain.

### Support Vector Machine (SVM)
- **Konfigurasi**  
  SVM diterapkan dengan kernel RBF (`kernel='rbf'`) untuk mengakomodasi data berdimensi tinggi dan data non-linier. Parameter `C=1.0` digunakan sebagai regulasi untuk mengontrol margin antara kelas, sedangkan `gamma='scale'` menyesuaikan nilai gamma secara otomatis pada data kompleks. Fitur `probability=True` diaktifkan untuk memungkinkan prediksi probabilitas.

- **Cara Kerja**  
  SVM memisahkan data berdasarkan hyperplane yang memaksimalkan margin antar kelas. Kernel RBF memungkinkan model ini untuk menangani data dengan pola non-linier, sehingga memberikan fleksibilitas dalam pemisahan data.

- **Kelebihan**
  - Sangat efektif untuk data berdimensi tinggi.
  - Memiliki kinerja yang baik pada data dengan batas pemisah yang jelas.

- **Kelemahan**
  - Kurang efisien pada dataset besar dalam hal waktu dan memori.
  - Pemilihan parameter `C` dan `gamma` cukup sensitif dan dapat mempengaruhi hasil model secara signifikan.

### K-Nearest Neighbors (KNN)
- **Konfigurasi**  
  Nilai `K=5` dipilih setelah evaluasi kinerja model pada berbagai nilai K untuk mencapai akurasi optimal.

- **Cara Kerja**  
  KNN mengklasifikasikan sampel uji berdasarkan kelas mayoritas dari lima tetangga terdekat, yang memungkinkan klasifikasi berdasarkan kemiripan data. Pendekatan ini memfasilitasi klasifikasi berdasarkan kedekatan atau kemiripan dalam fitur data.

- **Kelebihan**
  1. Sederhana dan mudah diimplementasikan.
  2. Tidak memerlukan pelatihan, sehingga lebih cepat untuk diterapkan pada dataset kecil.

- **Kelemahan**
  1. Sensitif terhadap skala fitur dan outlier.
  2. Kurang efisien pada dataset besar karena harus menghitung jarak ke setiap titik data lain dalam dataset.

### Logistic Regression
- **Konfigurasi**  
  Logistic Regression digunakan sebagai model baseline yang sederhana dan mudah diinterpretasikan. Parameter `max_iter=1000` diatur untuk memungkinkan konvergensi pada dataset yang lebih besar, dan `random_state=42` digunakan untuk hasil yang konsisten.

- **Cara Kerja**  
  Logistic Regression menghasilkan probabilitas untuk klasifikasi biner dengan menggunakan fungsi sigmoid, dan bekerja optimal pada data dengan batas pemisah linier. Model ini menghasilkan prediksi probabilitas untuk setiap kelas, memungkinkan klasifikasi dengan interpretasi yang mudah.

- **Kelebihan**
  1. Mudah diinterpretasikan dan cukup cepat dalam proses pelatihan.
  2. Bekerja dengan baik pada data yang memiliki batas pemisah linier.

- **Kelemahan**
  1. Kurang efektif untuk data yang tidak linier.
  2. Lebih mungkin mengalami underfitting pada data yang kompleks dan berdimensi tinggi.

Setelah pemilihan model dan konfigurasi, setiap model dievaluasi menggunakan metrik seperti akurasi, presisi, recall, dan F1-score untuk menentukan model dengan performa terbaik pada dataset ini.

## Evaluation

Pada tahap evaluasi, metrik utama yang digunakan adalah akurasi (accuracy), yaitu metrik yang mengukur persentase prediksi yang benar dari keseluruhan prediksi yang dilakukan oleh model. Akurasi digunakan untuk memahami sejauh mana model mampu melakukan klasifikasi dengan benar, yaitu mengidentifikasi kualitas pisang dengan tepat berdasarkan data yang diberikan.

### Rumus Akurasi

Akurasi didefinisikan sebagai rasio dari prediksi yang benar terhadap seluruh prediksi yang dibuat oleh model. Rumus untuk menghitung akurasi adalah sebagai berikut:

$$\text{Accuracy} = \frac{\text{TP + TN}}{\text{TP + TN + FP + FN}} \times 100\%$$

di mana:

- **TP (True Positive)**: Jumlah data positif yang diklasifikasikan dengan benar sebagai positif.
- **TN (True Negative)**: Jumlah data negatif yang diklasifikasikan dengan benar sebagai negatif.
- **FP (False Positive)**: Jumlah data negatif yang salah diklasifikasikan sebagai positif. Ini dikenal sebagai Kesalahan Tipe I (False Alarm).
- **FN (False Negative)**: Jumlah data positif yang salah diklasifikasikan sebagai negatif. Ini dikenal sebagai Kesalahan Tipe II (Miss).

**Penjelasan**: Akurasi mengukur proporsi prediksi yang benar dari semua prediksi. Nilai akurasi yang lebih tinggi menunjukkan bahwa model secara konsisten dapat memprediksi kelas yang benar untuk data yang diuji. Misalnya, akurasi sebesar 0.98 berarti model dapat memprediksi dengan benar 98% dari keseluruhan data uji yang diberikan.

### Benchmarking Hasil Evaluasi Model

Untuk membandingkan performa model, dilakukan benchmarking berdasarkan beberapa metrik evaluasi utama, yaitu akurasi, presisi, recall, dan F1 score. Berikut adalah rangkuman hasil benchmarking untuk masing-masing model.

| Model                           | Cross-Validation Accuracy | Test Set Accuracy | Precision | Recall | F1 Score |
|---------------------------------|---------------------------|--------------------|-----------|--------|----------|
| **Support Vector Machine (SVM)**| 97.91%                    | **98.76%**         | **98.76%**| **98.76%**| **98.76%**|
| **K-Nearest Neighbors (KNN)**   | 97.83%                    | 98.04%             | 98.05%    | 98.04% | 98.04%   |
| **Random Forest**               | 96.29%                    | 96.86%             | 96.87%    | 96.86% | 96.86%   |
| **Gradient Boosting**           | 95.47%                    | 95.36%             | 95.37%    | 95.36% | 95.36%   |
| **Logistic Regression**         | 87.38%                    | 87.05%             | 87.05%    | 87.05% | 87.05%   |

### Analisis Benchmarking

- **Support Vector Machine (SVM)** memiliki performa terbaik di seluruh metrik, dengan test set accuracy mencapai 98.76%. Ini menunjukkan bahwa SVM sangat efisien dalam menangani data berdimensi tinggi dan pola non-linier pada dataset ini.
- **K-Nearest Neighbors (KNN)** mendekati performa SVM dengan akurasi 98.04%, menjadikannya pilihan yang kompetitif untuk klasifikasi pada dataset ini. Namun, KNN kurang efisien pada data besar dalam hal kecepatan prediksi.
- **Random Forest** juga menghasilkan hasil yang baik, dengan akurasi 96.86%. Model ini sangat kuat dalam menangani variabilitas data dan robust terhadap outlier.
- **Gradient Boosting** memberikan akurasi yang tinggi, namun sedikit lebih rendah dibandingkan SVM dan KNN. Dengan akurasi 95.36%, model ini menunjukkan stabilitas pada data kompleks, meskipun cenderung lebih lambat dalam proses pelatihan.
- **Logistic Regression** sebagai model baseline memberikan akurasi 87.05%. Meskipun sederhana dan mudah diinterpretasikan, model ini tidak seoptimal model lain dalam menangani data yang lebih kompleks.

### Catatan Visualisasi Akurasi

Pada gambar plot hasil akurasi, hasil akurasi ditampilkan dalam bentuk yang dibulatkan untuk memudahkan interpretasi. Pembulatan akurasi ini memberikan gambaran umum performa setiap model secara ringkas dan memudahkan perbandingan visual di antara model.

### Kesimpulan Benchmarking

Dari hasil benchmarking ini, **Support Vector Machine (SVM)** dan **K-Nearest Neighbors (KNN)** berada di posisi teratas, dengan SVM sebagai pilihan model terbaik untuk digunakan pada dataset ini. **Random Forest** dan **Gradient Boosting** juga menunjukkan hasil yang memadai, namun mungkin memerlukan lebih banyak sumber daya komputasi.


![Gambar Plot Akurasi](https://github.com/Primadya/predictiveanalyticsdicoding/blob/main/image/gambar%203.png?raw=true)



### Diskusi Hasil Proyek terhadap Problem Statement dan Goals

Hasil evaluasi model menunjukkan bahwa akurasi tinggi dari SVM, KNN, dan Random Forest dapat secara langsung mendukung tujuan ketiga proyek ini. Dengan model yang mampu memprediksi kualitas pisang secara akurat, petani dan distributor dapat:

- **Seleksi Buah yang Lebih Efisien**: Dengan akurasi model yang tinggi, petani dapat lebih percaya diri dalam memilih buah yang berkualitas untuk dipasarkan. Ini mengurangi risiko menjual buah yang tidak memenuhi standar kualitas.
  
- **Mengurangi Kerugian**: Dengan mengidentifikasi pisang yang tidak layak jual lebih awal, petani dapat mengurangi jumlah buah yang dibuang atau dijual dengan harga rendah, sehingga meningkatkan profitabilitas.

- **Meningkatkan Nilai Jual**: Dengan memisahkan buah berdasarkan kualitas dengan lebih baik, distributor dapat menawarkan produk yang lebih baik kepada konsumen, meningkatkan kepuasan pelanggan dan mempertahankan loyalitas di pasar.

Secara keseluruhan, hasil proyek ini menunjukkan bahwa pengembangan model prediksi tidak hanya berhasil mencapai akurasi yang tinggi, tetapi juga memberikan manfaat praktis bagi petani dan distributor. Dengan demikian, proyek ini memiliki potensi untuk meningkatkan kualitas dan nilai ekonomis buah pisang dalam rantai pasokan.



## Referensi
1. [Aurelia, R., Kurniati, D., & Hutajulu, J. P. (2022). Daya Saing Ekspor Pisang Indonesia Di Negara Tujuan Ekspor Periode 2000-2019. Jurnal Agribisnis Indonesia (Journal of Indonesian Agribusiness), 10(2), 335-349.](https://journal.ipb.ac.id/index.php/jagbi/article/view/36753)
2. [Fadilah, L. (2018). Klasifikasi Random Forest pada data imbalanced (Bachelor's thesis, Fakultas Sains dan Teknologi UIN Syarif Hidayatullah Jakarta).](https://repository.uinjkt.ac.id/dspace/handle/123456789/55034)
3. [Suryana, S. E., Warsito, B., & Suparti, S. (2021). Penerapan Gradient Boosting Dengan Hyperopt Untuk Memprediksi Keberhasilan Telemarketing Bank. Jurnal Gaussian, 10(4), 617-623.](https://ejournal3.undip.ac.id/index.php/gaussian/article/view/31335)
4. [Handayani, P. K. (2021). Penerapan Algoritma Support Vector Machine (Svm) Untuk Analisis Pola Klasifikasi Pada Parkinson’S Dataset. Indonesian Journal of Technology, Informatics and Science (IJTIS), 3(1), 31-35.](https://jurnal.umk.ac.id/index.php/ijtis/article/download/7530/pdf)
5. [Isnain, A. R., Supriyanto, J., & Kharisma, M. P. (2021). Implementation of K-Nearest Neighbor (K-NN) algorithm for public sentiment analysis of online learning. IJCCS (Indonesian Journal of Computing and Cybernetics Systems), 15(2), 121-130.](https://journal.ugm.ac.id/ijccs/article/view/65176)
6. [Setyati, W. A., Sunaryo, S., Rezagama, A., Widodo, A. K., & Yulianto, M. F. A. (2020). PENERAPAN REGRESI LOGISTIK DALAM PENENTUAN FAKTOR YANG MEMPENGARUHI JUMLAH WISATAWAN ECOTOURISM DESA BEDONO. Jurnal Enggano, 5(1), 11-22.](https://core.ac.uk/download/pdf/327105237.pdf)



</div>
