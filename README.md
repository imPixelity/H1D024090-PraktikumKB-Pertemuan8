## Rock Paper Scissors Classification

Klasifikasi gambar Rock, Paper, Scissors menggunakan Convolutional Neural Network (CNN) dengan TensorFlow/Keras.

### Deskripsi

Model ini memprediksi gestur tangan (Rock, Paper, Scissors) dari gambar menggunakan CNN dengan 3 layer konvolusi.

### Arsitektur Model

```
Conv2D(32) → MaxPooling → Conv2D(64) → MaxPooling → Conv2D(128) → MaxPooling → Flatten → Dense(512) → Dense(3, Softmax)
```

### Struktur Direktori

```
├── main.py
└── rockpaperscissors/
    ├── rock/
    ├── paper/
    └── scissors/
```

### Cara Pakai

**1. Install dependensi**

```bash
pip install tensorflow numpy pandas
```

**2. Siapkan dataset** di folder `rockpaperscissors/` dengan subfolder per kelas

**3. Jalankan**

```bash
python main.py
```

### Detail Training

| Parameter | Nilai |
|---|---|
| Input size | 150 × 150 px |
| Batch size | 32 |
| Epochs | 10 |
| Split | 80% train / 20% validasi |
| Optimizer | Adam |
| Loss | Categorical Crossentropy |

### Output

- Summary arsitektur model
- Akurasi & loss per epoch
- Hasil evaluasi pada data validasi
- Probabilitas prediksi tiap kelas
