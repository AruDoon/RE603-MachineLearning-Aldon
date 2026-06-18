# Repository RE-603 Machine Learning ALDON

---
## Keterangan Info Pemilik Repo 
Nama     : Aldon Zufar Putra Twyn <br>
NIM      : 4222301042 <br>
Kelas    : Robotika - B Pagi <br>
Semester : 6 <br>
Prodi    : Robotika <br>

### Latest Update Repository 
Peyelesaian Tugas **Practive Week-9 Penggunaan MLP pada dataset Iris** `Week-9 [MLP]` dan juga **Practice Week-10 Penggunaan vision CNN untuk mendeteksi jenis Sampah** `Week-10 [CNN]`  

---
---

# Week-9 Result Recap

```
📁 Week-9 [Iris Dataset MLP]/
├── MLP_Iris_Activation_Comparison.ipynb   # Notebook utama
├── iris.csv                               # Dataset Iris
└── README.md                              
```
## Konfigurasi Model

```
Arsitektur  : Input(4) → Hidden(64) → Hidden(32) → Output(3)
Solver      : Adam
Learning Rate : 0.001
Max Epoch   : 500
Train/Test  : 80% / 20%
Normalisasi : StandardScaler
Evaluasi    : 5-Fold Cross Validation
```

## 📊 Hasil Perbandingan Performa

| Fungsi Aktivasi | Accuracy | Precision | Recall | F1-Score | CV Mean | CV Std |
|----------------|----------|-----------|--------|----------|---------|--------|
| **Sigmoid** ✅ | 0.9667 | 0.9697 | 0.9667 | 0.9666 | 0.9533 | 0.0340 |
| Tanh | 0.9667 | 0.9697 | 0.9667 | 0.9666 | 0.9733 | 0.0267 |
| ReLU | 0.9667 | 0.9697 | 0.9667 | 0.9666 | 0.9600 | 0.0249 |

> ✅ **Sigmoid** dipilih sebagai fungsi aktivasi terbaik berdasarkan F1-Score tertinggi pada data uji.

---
---

# Week-10 Result Recap

```
Week-10 [CNN]/
│
├── archive/
│   └── TrashType_Image_Dataset/
│       ├── cardboard/
│       ├── glass/
│       ├── metal/
│       ├── paper/
│       ├── plastic/
│       └── trash/
│
├── CNN_Trash_Classification.ipynb   ← notebook utama
├── best_model.keras                 ← model terbaik (disimpan otomatis saat training)
├── CNN_TrashClassifier_final.keras  ← model final setelah training selesai
│
├── distribusi_kelas.png             ← grafik distribusi jumlah gambar per kelas
├── contoh_gambar.png                ← contoh gambar dari setiap kelas
├── augmentasi.png                   ← contoh hasil augmentasi data
├── step1_pixel_matrix.png           ← visualisasi gambar sebagai matriks angka
├── training_history.png             ← grafik loss & accuracy selama training
├── confusion_matrix.png             ← confusion matrix hasil evaluasi
├── prediksi_output.png              ← contoh output prediksi satu gambar
└── prediksi_grid.png                ← prediksi pada contoh gambar per kelas
```

- **Sumber:** [Trash Type Image Dataset — Kaggle](https://www.kaggle.com/datasets/farzadnekouei/trash-type-image-dataset)
- **Total gambar:** 2.527 gambar
- **Jumlah kelas:** 6

| Kelas | Jumlah | Proporsi |
|-------|--------|----------|
| cardboard | 403 | 15.9% |
| glass | 501 | 19.8% |
| metal | 410 | 16.2% |
| paper | 594 | 23.5% |
| plastic | 482 | 19.1% |
| trash | 137 | 5.4% |

![Distribusi Kelas](<Week-10 [CNN] (COMPLETED)/distribusi_kelas.png>)

![Contoh Gambar](<Week-10 [CNN] (COMPLETED)/contoh_gambar.png>)

---

## 📈 Hasil Training

![Training History](training_history.png)

| Metrik | Nilai |
|--------|-------|
| Validation Accuracy | **67.37%** |
| Training Platform | CPU (Intel) — TensorFlow 2.21.0 |

![Confusion Matrix](<Week-10 [CNN] (COMPLETED)/confusion_matrix.png>)

---
---