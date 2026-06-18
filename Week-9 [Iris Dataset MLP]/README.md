# 🌸 MLP Iris — Perbandingan Fungsi Aktivasi
**Tugas Mata Kuliah:** Machine Learning  
**Topik:** Perbandingan Performa Multi-Layer Perceptron (MLP) menggunakan 3 Fungsi Aktivasi pada Dataset Iris

---

## Deskripsi

Proyek ini membandingkan performa model **Multi-Layer Perceptron (MLP)** pada dataset klasifikasi Iris dengan menggunakan tiga fungsi aktivasi yang berbeda:

| # | Fungsi Aktivasi | Deskripsi |
|---|----------------|-----------|
| 1 | **Sigmoid** | Memetakan output ke rentang (0, 1), cocok untuk klasifikasi biner |
| 2 | **Tanh** | Memetakan output ke rentang (-1, 1), zero-centered |
| 3 | **ReLU** | Mengembalikan nilai maksimum antara 0 dan input, efisien dan cepat konvergen |

Semua model menggunakan arsitektur dan hyperparameter yang **sama persis**, hanya fungsi aktivasinya yang berbeda, sehingga perbandingan bersifat adil dan terkontrol.

---

## Struktur File

```
📁 Week-9 [Iris Dataset MLP]/
├── MLP_Iris_Activation_Comparison.ipynb   # Notebook utama
├── iris.csv                               # Dataset Iris
└── README.md                              
```

---

## Dataset

- **Nama:** Iris Dataset
- **Sumber:** [Kaggle — Iris Dataset](https://www.kaggle.com/datasets/uciml/iris)
- **Jumlah data:** 150 sampel
- **Fitur:** `sepal_length`, `sepal_width`, `petal_length`, `petal_width`
- **Kelas:** `setosa`, `versicolor`, `virginica` (masing-masing 50 sampel)

---

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

---

## 📊 Hasil Perbandingan Performa

| Fungsi Aktivasi | Accuracy | Precision | Recall | F1-Score | CV Mean | CV Std |
|----------------|----------|-----------|--------|----------|---------|--------|
| **Sigmoid** ✅ | 0.9667 | 0.9697 | 0.9667 | 0.9666 | 0.9533 | 0.0340 |
| Tanh | 0.9667 | 0.9697 | 0.9667 | 0.9666 | 0.9733 | 0.0267 |
| ReLU | 0.9667 | 0.9697 | 0.9667 | 0.9666 | 0.9600 | 0.0249 |

> ✅ **Sigmoid** dipilih sebagai fungsi aktivasi terbaik berdasarkan F1-Score tertinggi pada data uji.

---

## Kesimpulan

Ketiga fungsi aktivasi menghasilkan akurasi yang sangat kompetitif pada dataset Iris (**96.67%**). Pada dataset yang kecil dan terstruktur seperti Iris, perbedaan performa antar fungsi aktivasi cenderung minimal. Namun secara keseluruhan:

- **Sigmoid** unggul sedikit pada data uji berdasarkan F1-Score.
- **Tanh** menunjukkan CV Mean tertinggi (0.9733), mengindikasikan generalisasi yang lebih stabil.
- **ReLU** konvergen lebih cepat (iterasi lebih sedikit) tetapi sedikit lebih bervariasi pada cross-validation.

---

## 🛠️ Library yang Digunakan

- `numpy` — operasi numerik
- `pandas` — manipulasi data
- `matplotlib` & `seaborn` — visualisasi
- `scikit-learn` — preprocessing, model MLP, dan evaluasi

---

Dataset **IRIS** dapat di Download melalui tombol di bawah ini: <br>
[![IRIS Dataset](https://img.shields.io/badge/KAGGLE-IRIS_Dataset-blue?style=for-the-badge)](https://www.kaggle.com/datasets/himanshunakrani/iris-dataset)