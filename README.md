# SahabatTani-ML  
Platform SahabatTani menggunakan pendekatan satu model untuk setiap jenis tanaman. Artinya, masing-masing tanaman memiliki model deteksi penyakit yang dikembangkan secara khusus berdasarkan dataset dan karakteristik penyakitnya, guna memastikan akurasi dan kinerja yang optimal.

---

## Dataset  
Dataset yang digunakan untuk training dan evaluasi model dapat diunduh disini:
- [*Dataset Penyakit Tanaman Padi*](https://www.kaggle.com/datasets/loki4514/rice-leaf-diseases-detection)
- [*Dataset Penyakit Tanaman Jagung*](https://www.kaggle.com/datasets/smaranjitghose/corn-or-maize-leaf-disease-dataset)
- [*Dataset Penyakit Tanaman Singkong*](https://www.kaggle.com/datasets/dipoyonoarga/dataset-singkong)
- [*Dataset Penyakit Tanaman Mangga*](https://www.kaggle.com/datasets/aryashah2k/mango-leaf-disease-dataset) 

---
## Categories of Plant Disease:  
### Tanaman Padi
1. *Brown Spot*  
   - *Indikasi*: Bercak bulat atau oval cokelat dengan pusat terang pada daun dan gabah, mengganggu fotosintesis dan menurunkan kualitas hasil panen.
   - *Penyebab*: Jamur Bipolaris oryzae pada kondisi lembap dan benih terinfeksi.  
   - *Solusi*: Gunakan benih sehat, perbaiki nutrisi tanah (K dan P), tanam varietas tahan, semprot fungisida saat gejala awal.
 
2. *Neck Blast*  
   - *Indikasi*: Leher malai hitam/cokelat gelap, malai kering dan tidak terisi.
   - *Penyebab*:  Jamur Magnaporthe oryzae pada fase berbunga.
   - *Solusi*: Gunakan varietas tahan, hindari kelembapan tinggi, hindari pupuk N berlebih, semprot fungisida sistemik.

3. *Leaf Scald*  
   - *Indikasi*: Bercak cokelat tua atau ungu, tengah abu-abu, lesi memanjang pada daun.  
   - *Penyebab*:  Jamur Microdochium oryzae, muncul pada kelembapan tinggi.
   - *Solusi*: Gunakan varietas tahan, jaga sanitasi, hindari pupuk N berlebih, gunakan fungisida saat gejala awal.

4. *Narrow Brown Leaf Spot*  
   - *Indikasi*: Bercak sempit memanjang cokelat/keabu-abuan, menyebabkan daun mengering.
   - *Penyebab*:  Jamur Cercospora oryzae, diperparah kelembapan dan kurang hara.
   - *Solusi*:  Gunakan varietas tahan, perbaiki pemupukan (K dan P), jaga sirkulasi udara, gunakan fungisida.

5. *Sheath Blight*  
   - *Indikasi*: Bercak oval hijau pada pelepah yang membesar, disertai miselium putih. 
   - *Penyebab*: Jamur Rhizoctonia solani, muncul pada lahan lembap dan padat.
   - *Solusi*: Gunakan varietas tahan, hindari pupuk N berlebih, atur jarak tanam, semprot fungisida.
 
6. *Tungro*  
   - *Indikasi*: Daun menguning dari ujung, tanaman kerdil, kasar, dan mati cepat. 
   - *Penyebab*: Virus RTBV dan RTSV yang disebarkan wereng hijau.
   - *Solusi*: Gunakan varietas tahan, kendalikan wereng, tanam serempak, lakukan rotasi tanaman.
  
7. *Hispa*  
   - *Indikasi*: Daun bergaris putih transparan, menggulung dan rusak berat.
   - *Penyebab*:  Serangga Dicladispa armigera.  
   - *Solusi*: Tanam serempak, buang tanaman rusak, gunakan insektisida nabati/kimia.
8. *Bacterial Leaf Blight*  
   - *Indikasi*: Daun menguning dari ujung, muncul bercak berair yang mengering.  
   - *Penyebab*:Bakteri Xanthomonas oryzae pv. oryzae.
   - *Solusi*:  Gunakan varietas tahan, benih sehat, hindari pupuk N berlebih, semprot bakterisida.

9. *Leaf Blast*  
   - *Indikasi*: Bercak belah ketupat abu-abu dengan pinggir cokelat, daun mengering. 
   - *Penyebab*: Jamur Magnaporthe oryzae.
   - *Solusi*: Gunakan varietas tahan, hindari tanam saat musim hujan puncak, semprot fungisida saat awal gejala.

### Tanaman Jagung
1. *Gray Leaf Spot*  
   - *Indikasi*: Bercak persegi panjang sempit berwarna abu-abu keperakan atau cokelat pada daun, awalnya muncul di daun bawah lalu menyebar ke atas. Infeksi berat menyebabkan daun mati dan menurunkan hasil panen.  
   - *Penyebab*: Jamur Cercospora zeae-maydis, berkembang di cuaca hangat dan lembap.
   - *Solusi*: Gunakan varietas tahan, lakukan rotasi tanaman, atur jarak tanam, dan aplikasikan fungisida sistemik saat gejala awal muncul.
2. *Common Rust*  
   - *Indikasi*:  Pustula cokelat keemasan berbentuk oval kecil di permukaan daun. Daun menguning, nekrosis, dan kering pada infeksi berat. 
   - *Penyebab*: Jamur Puccinia sorghi, menyebar lewat spora dan tumbuh optimal pada kelembapan tinggi dan suhu 15–25°C. 
   - *Solusi*: Gunakan varietas tahan, lakukan rotasi tanaman, atur sirkulasi udara, bersihkan sisa tanaman, dan aplikasikan fungisida.
 
3. *Blight*  
   - *Indikasi*: NCLB menyebabkan lesi panjang keabu-abuan ("cerutu"), SCLB menyebabkan bercak kecil cokelat muda. Infeksi berat mengeringkan daun. 
   - *Penyebab*: Jamur Exserohilum turcicum (NCLB) dan Bipolaris maydis (SCLB), berkembang di lingkungan lembap. 
   - *Solusi*: Gunakan varietas tahan, rotasi tanaman, bersihkan sisa tanaman, hindari penanaman berdekatan, dan gunakan fungisida saat gejala awal muncul.

### Tanaman Singkong
1. *Bacterial Blight*  
   - *Indikasi*: Bercak basah pada daun, daun keriting dan gugur, luka gelap di batang, hingga pembusukan batang.  
   - *Penyebab*:  Bakteri Xanthomonas axonopodis pv. manihotis, menyebar lewat air, alat, dan bahan tanam terinfeksi.  
   - *Solusi*: Gunakan stek sehat, pangkas bagian terinfeksi, jaga kebersihan alat, rotasi tanaman, serta semprot bakterisida berbahan tembaga saat awal gejala atau musim hujan.
   
2. *Blight*  
   - *Indikasi*: Bercak lonjong atau kecil kecokelatan yang menyebar cepat, menyebabkan daun kering total.
   - *Penyebab*:  Jamur Exserohilum turcicum (NCLB) dan Bipolaris maydis (SCLB).
   - *Solusi*: Gunakan varietas tahan, lakukan rotasi, bersihkan sisa tanaman, dan semprot fungisida sejak gejala awal.

3. *Green Mottle*  
   - *Indikasi*: Belang hijau tak beraturan, daun keriting, tanaman kerdil. 
   - *Penyebab*: Virus CGMV, ditularkan melalui stek terinfeksi dan serangga penghisap.
   - *Solusi*: Gunakan stek sehat, buang tanaman terinfeksi, dan semprot insektisida untuk kendalikan vektor.

4. *Brown Streak Disease*  
   - *Indikasi*: Daun menguning di tulang daun, umbi bergaris cokelat kehitaman dan membusuk, pertumbuhan terhambat. 
   - *Penyebab*: Virus CBSV atau UCBSV, ditularkan oleh kutu putih dan stek terinfeksi.  
   - *Solusi*: Gunakan varietas tahan, tanam stek sehat, cabut tanaman terinfeksi berat, lakukan rotasi, dan kendalikan kutu putih dengan insektisida.
 
5. *Mosaic Disease*  
   - *Indikasi*: Pola mosaik hijau tua-muda, daun keriting, tanaman kerdil dan bercabang, umbi kecil. 
   - *Penyebab*: Virus CMV, disebarkan oleh kutu putih dan bahan tanam.  
   - *Solusi*: Gunakan varietas tahan, stek sehat, musnahkan tanaman sakit, bersihkan alat dan lahan, serta semprot insektisida untuk kendalikan vektor.

### Tanaman Mangga
1. *Anthracnose (Antraknosa)*  
   - *Indikasi*: Bercak hitam atau coklat pada daun, buah rontok.  
   - *Penyebab*: Jamur Colletotrichum gloeosporioides.  
   - *Solusi*: Pangkas bagian yang terinfeksi, hindari kelembapan tinggi. 

2. *Bacterial Canker (Kanker Bakteri)*  
   - *Indikasi*: Luka berair pada batang atau daun, kadang bau busuk.  
   - *Penyebab*: Bakteri Xanthomonas campestris.  
   - *Solusi*: Pangkas bagian terinfeksi, semprot dengan antibiotik.
   
3. *Cutting Weevil (Kumbang Pemotong)*  
   - *Indikasi*: Ujung daun atau tunas muda tampak digigit atau terpotong.  
   - *Penyebab*: Serangga Deporaus marginatus.
   - *Solusi*: Pangkas bagian terinfeksi, semprot dengan antibiotik.

4. *Die Black (Daun Mati Menghitam)*  
   - *Indikasi*: Daun menghitam dan mengering, sering mulai dari tepi daun.
   - *Penyebab*: Kekeringan ekstrem, penyakit sekunder.
   - *Solusi*: Perbaiki sistem irigasi, periksa kemungkinan infeksi lain.
 
5. *Gall Midge (Lalat Empedu)*  
   - *Indikasi*: Daun menggulung atau bengkak, tunas tidak berkembang.
   - *Penyebab*: Serangga Procontarinia matteianar.
   - *Solusi*: Buang daun terinfeksi, semprot insektisida sebelum musim hujan.
 
6. *Powdery Mildew (Embun Tepung)*  
   - *Indikasi*: Lapisan putih seperti bedak di permukaan daun, tunas muda mati.
   - *Penyebab*: Jamur Oidium mangiferae.
   - *Solusi*: Semprot fungisida, pangkas tanaman agar sirkulasi udara baik.

7. *Scooty Mould (Jelaga Hitam)*  
   - *Indikasi*: Lapisan hitam seperti jelaga di permukaan daun.
   - *Penyebab*: Pertumbuhan jamur pada ekskresi serangga (misal: kutu daun).
   - *Solusi*: Kendalikan serangga penyebab, bersihkan daun.
---

## Model Architecture
### 1. Model Architecture untuk Deteksi Penyakit Padi
Model deteksi penyakit daun padi dibangun menggunakan pendekatan **transfer learning** dengan arsitektur **MobileNet** sebagai _feature extractor_. MobileNet digunakan tanpa lapisan atas (_include_top=False_) dan dimuat dengan bobot pralatih dari ImageNet, sehingga mampu mengekstraksi fitur visual dari gambar daun secara efisien. Di atas MobileNet, ditambahkan lapisan klasifikasi berupa `Flatten`, `Dense` dengan 256 neuron beraktivasi ReLU, `Dropout` sebesar 0.5 untuk mengurangi overfitting, serta `Dense` akhir dengan 10 neuron beraktivasi `softmax` sebagai output layer. Model ini menerima input citra berukuran 224x224 piksel dan mengklasifikasikannya ke dalam sepuluh kategori penyakit seperti `rice_bacterial_leaf_blight`, `rice_leaf_blast`, `rice_tungro`, dan lainnya.
<div align="center">
  <img src="https://github.com/SahabatTani/Machine-Learning/blob/main/Rice%20Leaf%20Disease%20Detection%20Model/arsitektur.png?raw=true" alt="Arsitektur Model Padi" width="300"/>
</div>

##### Penjelasan Layer Tambahan

- **`Flatten`**  
  Mengubah output tensor 3D dari MobileNet menjadi vektor 1D agar dapat diproses oleh layer fully connected.
- **`Dense(256, activation='relu')`**  
  Layer fully connected dengan 256 neuron dan fungsi aktivasi ReLU untuk menangkap hubungan non-linear antar fitur.
- **`Dropout(0.5)`**  
  Mengurangi risiko overfitting dengan menonaktifkan 50% neuron secara acak saat training.
- **`Dense(10, activation='softmax')`**  
  Layer output dengan 10 neuron (untuk 10 kelas penyakit) dan aktivasi softmax untuk menghasilkan probabilitas prediksi per kelas.

### 2. Model Architecture untuk Deteksi Penyakit Jagung
Model deteksi penyakit daun jagung dibangun menggunakan arsitektur konvolusional bertingkat yang terdiri dari empat blok utama Conv2D, masing-masing diikuti oleh BatchNormalization dan MaxPooling2D. Model menerima input citra berukuran 256x256 piksel dengan 3 saluran warna. Blok pertama dimulai dengan Conv2D berisi 32 filter, diikuti normalisasi batch dan pooling, yang menghasilkan fitur berukuran 127x127x32. Blok-blok berikutnya secara bertahap menambah kedalaman fitur menjadi 64, 128, hingga 128 channel, sambil mengurangi resolusi spasial menjadi 14x14 piksel.

Setelah ekstraksi fitur, dilakukan GlobalAveragePooling2D untuk meratakan dimensi spasial, diikuti oleh lapisan Dropout sebesar 0.5 guna mencegah overfitting. Selanjutnya, dua lapisan Dense digunakan, masing-masing dengan 64 neuron ReLU dan 4 neuron softmax sebagai output layer. Model ini mengklasifikasikan citra daun jagung ke dalam empat kategori penyakit, seperti  `gray_leaf Spot`, `common_rust`, dan `blight`.

<div align="center">
  <img src="https://raw.githubusercontent.com/SahabatTani/Machine-Learning/refs/heads/main/Corn%20Leaf%20Disease%20Detection%20Model/model_architecture.png" alt="Arsitektur Model Jagung" width="300"/>
</div>


---


## Tools dan Libraries

- **Kaggle Notebook**: Lingkungan untuk eksekusi kode Jupyter Notebook berbasis cloud dengan akses ke GPU/TPU secara gratis
- **os, shutil**: Untuk operasi file dan folder, seperti membuat, memindahkan, atau menghapus direktori.
- **re**: Digunakan untuk pencocokan pola dengan regular expressions.
- **random**: Untuk pengacakan data, misalnya saat split dataset atau augmentasi.
- **NumPy (`np`)**: Operasi numerik dan manipulasi array multidimensi.
- **Pandas (`pd`)**: Manipulasi dan analisis data berbasis tabel (DataFrame).
- **Matplotlib (`plt`, `mpimg`)**: Visualisasi data dan citra seperti grafik akurasi dan loss.
- **Seaborn (`sns`)**: Visualisasi statistik seperti confusion matrix dengan tampilan yang lebih estetis.
- **PIL (Image)**: Membaca dan memproses gambar.
- **TensorFlow (`tf`)**: Framework utama untuk machine learning dan deep learning.
- **Keras (dari TensorFlow)**: 
  - `preprocessing`: Untuk augmentasi dan pemrosesan gambar.
  - `layers`: Membangun layer-layer CNN seperti Conv2D, Dense, dsb.
  - `models`: Untuk membuat dan memuat model.
  - `optimizers`: Untuk mengatur algoritma optimasi seperti Adam.
  - `applications`: Menggunakan arsitektur pretrained seperti MobileNet.
  - `callbacks`: Mengatur strategi pelatihan seperti EarlyStopping.
- **Scikit-learn (`sklearn`)**: 
  - `train_test_split`: Memisahkan dataset.
  - `metrics`: Mengukur performa model (confusion matrix, klasifikasi).
  - `utils`: Menghitung class weight untuk dataset tidak seimbang.
- **google.colab.files**: Untuk mengunggah atau mengunduh file di lingkungan Google Colab.
- **tensorflowjs**: Mengkonversi model Keras ke format TensorFlow.js agar dapat dijalankan di browser.
- **warnings**: Untuk menonaktifkan peringatan selama eksekusi kode.
