# Credit Risk Prediction

## 📌 Deskripsi
Credit Risk Prediction adalah proyek yang bertujuan untuk menentukan apakah seorang nasabah layak mendapatkan pinjaman atau tidak berdasarkan parameter yang diberikan. Model ini menggunakan algoritma **Decision Tree** yang telah dioptimasi dengan **Hyperparameter Tuning, Synthetic Minority Oversampling Technique (SMOTE), dan K-Fold Cross Validation** untuk meningkatkan akurasi serta mengatasi masalah overfitting dan ketidakseimbangan data.

## 📊 Fitur Utama
- **Prediksi Risiko Gagal Bayar**: Menentukan apakah nasabah dapat diberikan pinjaman.
- **Optimasi Model**: Menggunakan **Hyperparameter Tuning (Grid Search)** untuk meningkatkan performa model.
- **Penanganan Ketidakseimbangan Data**: Menggunakan **SMOTE** untuk mengatasi distribusi kelas yang tidak merata.
- **Validasi Model**: Menggunakan **K-Fold Cross Validation (k=5)** untuk memastikan stabilitas model.
- **Deployable Model**: Model dapat diekspor dan digunakan kembali dalam aplikasi web atau API.

## 🛠 Teknologi yang Digunakan
- **Python** (scikit-learn, pandas, numpy, matplotlib, seaborn)
- **Machine Learning** (Decision Tree)
- **Data Preprocessing** (SMOTE, Feature Selection)
- **Model Evaluation** (Accuracy, Precision, Recall, F1-score)
- **Deployment** (Flask/FastAPI untuk API jika diperlukan)

## 🔧 Cara Menggunakan

### 1. Instalasi Dependensi
Pastikan Anda memiliki **Python 3.8+** dan instal pustaka yang dibutuhkan:
```bash
pip install -r requirements.txt
```

### 2. Menjalankan Model
Jalankan model menggunakan skrip utama:
```bash
python train_model.py
```

### 3. Menyimpan dan Memuat Model
Untuk menyimpan model setelah pelatihan:
```python
import joblib
joblib.dump(model, 'credit_risk_model.pkl')
```
Untuk memuat kembali model:
```python
model = joblib.load('credit_risk_model.pkl')
```

### 4. Menggunakan Model untuk Prediksi
```python
input_data = [[30, 5000000, 2, 1, 0]]  # Contoh input
prediction = model.predict(input_data)
print("Hasil Prediksi:", "Disetujui" if prediction[0] == 1 else "Ditolak")
```

## 🚀 Deployment (Opsional)
Model ini dapat diintegrasikan dengan aplikasi web menggunakan Flask atau FastAPI.

## 📌 Lisensi
Proyek ini dibuat untuk keperluan penelitian dan edukasi. Bebas digunakan dengan menyertakan atribusi.


