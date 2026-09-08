# 🍎🥦 Fruit & Vegetable Classification using MobileNetV2

![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-D00000?style=for-the-badge&logo=keras&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)

Proyek ini merupakan **Tugas Besar Pengolahan Citra Digital (PCD)** yang bertujuan untuk mengklasifikasikan berbagai jenis buah dan sayuran menggunakan arsitektur **MobileNetV2** berbasis Transfer Learning, dengan penerapan pemrosesan kontras citra (*Contrast Image Processing*) pada dataset pelatihan.

---

## 👥 Anggota Tim

| Nama | NIM |
| :--- | :--- |
| **Muhammad Hafiz Shakil** | 1301213111 |
| **Abraham Roy Rudianto** | 1301213202 |

---

## 📌 Fitur Utama & Alur Kerja

1. **Image Preprocessing & Contrast Enhancement**:
   - Memproses citra asli untuk meningkatkan kualitas visual dan ketajaman fitur objek melalui penyesuaian kontras citra (`train_contrast`).
2. **Data Pipeline & Augmentasi**:
   - Menggunakan `ImageDataGenerator` untuk augmentasi data citra dan normalisasi skala piksel.
3. **Transfer Learning dengan MobileNetV2**:
   - Memanfaat arsitektur ringan dan efisien MobileNetV2 yang telah di-pretrained pada ImageNet untuk ekstraksi fitur citra secara optimal.
4. **Optimasi Pelatihan Model (Callbacks)**:
   - `ModelCheckpoint`: Menyimpan bobot (*weights*) model terbaik selama proses pelatihan.
   - `EarlyStopping`: Mencegah *overfitting* secara otomatis jika performa validasi stagnan.
   - `ReduceLROnPlateau`: Menurunkan *learning rate* secara otomatis saat metrik evaluasi berada di fase plateau.
5. **Evaluasi Komprehensif**:
   - Pengujian performa menggunakan *Confusion Matrix* dan *Classification Report* (Precision, Recall, F1-Score, dan Accuracy).

---

## 📁 Struktur Dataset

Dataset disimpan dalam folder `dataset_pcd/` dengan struktur sebagai berikut:

```text
dataset_pcd/
├── train/              # Data latih asli
├── train_contrast/     # Data latih hasil peningkatan kontras (Image Processing)
├── validation/         # Data validasi pelatihan
└── test/               # Data pengujian akhir
```
---

## 🛠️ Modul & Library yang Digunakan

* **Deep Learning**: TensorFlow, Keras (`MobileNetV2`, `ImageDataGenerator`, `Callbacks`)
* **Pengolahan Citra**: OpenCV (`cv2`)
* **Pengolahan Data & Statistik**: NumPy, Pandas
* **Visualisasi Data**: Matplotlib, Seaborn
* **Evaluasi**: Scikit-Learn (`classification_report`, `confusion_matrix`)

---

## 🚀 Cara Menjalankan Notebook

### 1. Prasyarat (*Prerequisites*)

Pastikan Anda memiliki Python 3.8+ dan Jupyter Notebook/Google Colab. Install dependensi berikut:

```bash
pip install tensorflow opencv-python numpy pandas matplotlib seaborn scikit-learn termcolor

```

### 2. Menjalankan Kode

1. Clone repositori ini atau unduh file notebook `.ipynb`.
2. Pastikan direktori `dataset_pcd` berada di jalur (*path*) yang sesuai.
3. Buka notebook dan jalankan sel kode secara berurutan:
* **Langkah 1**: Import Library & Load Dataset.
* **Langkah 2**: Image Processing Contrast Enhancement.
* **Langkah 3**: Pembentukan Data Generator (Train, Validation, Test).
* **Langkah 4**: Inisialisasi Model MobileNetV2 & Pelatihan Model.
* **Langkah 5**: Evaluasi dan Visualisasi Hasil Klasifikasi.



---

## 📊 Hasil dan Evaluasi

Evaluasi dilakukan pada folder `test` menggunakan grafik akurasi/loss serta metrik pengukuran:

* **Confusion Matrix**: Menilai sebaran prediksi yang benar dan salah per kelas buah/sayur.
* **Classification Report**: Mengukur metrik *Precision*, *Recall*, dan *F1-Score*.

---
