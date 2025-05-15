# Rock-Paper-Scissors Classification Project 🪨📄✂️
---

## 📚 Deskripsi Proyek

Proyek ini bertujuan untuk membangun sistem klasifikasi gambar sederhana menggunakan **Deep Learning** dengan arsitektur **Transfer Learning** (menggunakan MobileNetV2).  
Gambar yang diklasifikasikan terdiri dari tiga kategori: **Rock**, **Paper**, dan **Scissors**.

Model yang dilatih kemudian akan diintegrasikan ke dalam aplikasi backend berbasis **FastAPI**, serta frontend berbasis **Streamlit**, sehingga bisa menerima gambar dan memberikan hasil prediksi secara real-time.

---

## 🛠️ Teknologi yang Digunakan

- **TensorFlow / Keras** — Untuk membangun dan melatih model klasifikasi gambar.
- **FastAPI** — Untuk membangun backend REST API.
- **Uvicorn** — Sebagai ASGI server untuk menjalankan FastAPI.
- **Streamlit** — Untuk frontend berbasis web.
- **PIL (Pillow)** — Untuk memproses gambar.
- **NumPy** — Untuk manipulasi data numerik.
- **scikit-learn** — Untuk evaluasi model (classification report, confusion matrix).

---

## 📂 Struktur Folder Proyek

```
project-root/
├── backend/
│   ├── main.py           # Kode backend FastAPI
│   └── requirements.txt  # Dependencies backend
├── frontend/
│   ├── main.py           # Kode frontend Streamlit
│   └── requirements.txt  # Dependencies frontend
├── model/
│   └── best_transfer.h5  # Model hasil training
├── dataset/
│   ├── rock/
│   ├── paper/
│   └── scissors/
├── README.md
```

---

## 🚀 Langkah Penggunaan

### 1. Clone Repository

```bash
git clone https://github.com/furqanx/Tugas-Pembelajaran-Mesin.git
cd Tugas-Pembelajaran-Mesin
```

### 2. Siapkan Environment Python

Disarankan menggunakan **Python 3.9–3.11**.

Install dependencies backend:

```bash
cd backend/
pip install -r requirements.txt
```

Install dependencies frontend:

```bash
cd ../frontend/
pip install -r requirements.txt
```

### 3. Download Dataset

Unduh dataset Rock-Paper-Scissors dari Kaggle:  
🔗 [Rock-Paper-Scissors Dataset – Kaggle](https://www.kaggle.com/datasets/drgfreeman/rockpaperscissors)

Setelah download dan ekstrak:
- Susun dataset ke dalam folder:

```
dataset/
├── rock/
├── paper/
└── scissors/
```

### 4. Jalankan Aplikasi

Jalankan frontend:

```bash
cd frontend/
streamlit run main.py
```

Streamlit akan berjalan di `http://localhost:8501/`

Lalu jalankan backend:

```bash
cd ../backend/
uvicorn main:app --host 0.0.0.0 --port 8000 --reload
```

Server akan berjalan di `http://localhost:8000/`

---

## 🎯 Tujuan Pembelajaran

- Memahami alur kerja training dan deployment model machine learning.
- Membiasakan diri mengintegrasikan model ke dalam aplikasi backend nyata.
- Melatih kerapihan penyusunan struktur proyek dan dokumentasi.

---

## 📋 Catatan Penting

- Pastikan struktur dataset rapi dan sesuai.
- Pastikan preprocessing konsisten antara training dan backend inference.
- Jangan lupa untuk mengisi seluruh bagian `TODO` yang ada dalam kode.
