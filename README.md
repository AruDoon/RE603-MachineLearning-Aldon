# Repository RE-603 Machine Learning ALDON

## Keterangan Info Pemilik Repo 
Nama     : Aldon Zufar Putra Twyn <br>
NIM      : 4222301042 <br>
Kelas    : Robotika - B Pagi <br>
Semester : 6 <br>
Prodi    : Robotika <br>

> ## Latest Update Repository 
> Peyelesaian Tugas **Practive Week-13/14 Penggunaan Transfer Learning pada dataset Sampah** `Week-13&14 [TransferLearning and Validation]`

---

# Week-13/14 Result Recap

## Hasil Training

![Training History](<Week-13&14 [TransferLearning and Validation] (COMPLETED)/Pictures/tl_training_history.png>)

Garis hijau vertikal memisahkan Tahap 1 (Feature Extraction) dan Tahap 2 (Fine-Tuning).

| Metrik | Nilai |
|--------|-------|
| **Best Validation Accuracy** | **90.98%** |
| Final Train Accuracy | 95.35% |
| Final Val Accuracy | 89.12% |
| Final Train Loss | 0.1223 |
| Final Val Loss | 0.5697 |
| Training Platform | CPU — Intel i5 Gen 13, TensorFlow 2.21.0 |

---

## Week 14 — Deteksi & Penanganan Overfitting

### Diagnosis

| Kondisi | Train Acc | Val Acc | Diagnosis |
|---------|-----------|---------|-----------|
| Underfitting | 60% | 65% | Sama-sama rendah |
| Just Right | 85% | 82% | Gap kecil (normal) |
| Overfitting | 99% | 65% | **Gap besar!** |
| **Model Ini** | **95%** | **89%** | **✅ JUST RIGHT** |

**Gap accuracy: 6.22% ≤ 10% → Model generalisasi dengan baik, tidak overfitting.**

### Teknik Anti-Overfitting yang Diterapkan

![Overfitting Techniques](<Week-13&14 [TransferLearning and Validation] (COMPLETED)/Pictures/tl_overfitting_techniques.png>)

| Teknik | Implementasi |
|--------|-------------|
| **Dropout** | Rate 0.5 di head classifier |
| **Batch Normalization** | Di head classifier |
| **Data Augmentation** | Rotasi ±30°, flip, zoom, brightness |
| **Early Stopping** | patience=7, restore best weights |
| **ReduceLROnPlateau** | factor=0.5, patience=3 |
| **Class Weights** | Balanced — tangani imbalance trash (137 img) |
| **Fine-Tuning Bertahap** | Freeze → unfreeze pelan, cegah catastrophic forgetting |

---

## Evaluasi Model

![Confusion Matrix](<Week-13&14 [TransferLearning and Validation] (COMPLETED)/Pictures/tl_confusion_matrix.png>)

---

## Contoh Prediksi

![Prediksi Output](<Week-13&14 [TransferLearning and Validation] (COMPLETED)/Pictures/tl_prediksi_output.png>)

![Prediksi Grid](<Week-13&14 [TransferLearning and Validation] (COMPLETED)/Pictures/tl_prediksi_grid.png>)

---
![Contoh Gambar](<Pictures/tl_confusion_matrix.png>)