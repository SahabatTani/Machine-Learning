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

## Dataset Structures

- **Train** : Data latih, digunakan oleh model saat training.
- **Validation** : Data validasi, digunakan untuk evaluasi kinerja model selama training.
- **Test** : Data pengujian akhir, digunakan untuk menguji model setelah training selesai.

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

---

## 📚 Library Overview

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
