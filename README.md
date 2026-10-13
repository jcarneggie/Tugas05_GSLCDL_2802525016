# Transfer Learning untuk Klasifikasi Citra Oxford-IIIT Pet

## Deskripsi

Repository ini berisi implementasi tugas Take Home Sesi 05
Advanced CNNs and Transfer Learning.

Eksperimen dilakukan untuk mengevaluasi efektivitas transfer learning
pada kondisi data terbatas menggunakan arsitektur ResNet-18.

## Dataset

Dataset yang digunakan:
Oxford-IIIT Pet Dataset

Subset:
10 kelas ras kucing dan anjing.

Preprocessing:
- Resize 224x224
- ImageNet normalization
- Data augmentation pada training set

## Model

Arsitektur utama:
- ResNet-18

Eksperimen:

### B1 - From Scratch
ResNet-18 dilatih dari inisialisasi acak.

### B2 - Feature Extraction
Backbone pretrained ImageNet dibekukan.
Hanya classifier head yang dilatih.

### B3 - Progressive Fine-Tuning
Layer4 dan classifier head dibuka dengan differential learning rate.

### B4 - Data Augmentation Control
Perbandingan training dengan dan tanpa augmentation.

## Hasil Singkat

| Experiment | Macro F1 |
|------------|----------|
| B1 Scratch | 0.1579 |
| B2 Feature Extraction | 0.8125 |
| B3 Fine Tuning | 0.7928 |
| B4 Without Augmentation | 0.7688 |

Feature extraction memberikan performa terbaik pada eksperimen ini.

## Environment

Eksperimen dijalankan menggunakan:
- Google Colab
- NVIDIA Tesla T4 GPU
- PyTorch
- torchvision

## Cara Menjalankan

1. Buka notebook pada Google Colab.
2. Aktifkan GPU runtime.
3. Jalankan cell secara berurutan.

## Author

Nama:
NIM:
