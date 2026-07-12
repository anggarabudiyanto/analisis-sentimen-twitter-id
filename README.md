# Analisis Sentimen — Twitter/X (Bahasa Indonesia)

Pipeline end-to-end untuk klasifikasi sentimen teks berbahasa Indonesia dari data Twitter/X: scraping, preprocessing, pelabelan, hingga pelatihan model (klasik ML + LSTM Bidirectional).

## Struktur Proyek

| File | Deskripsi |
|---|---|
| `01_scraping.ipynb` | Scraping tweet berdasarkan keyword (negatif & netral), autentikasi via Colab Secrets. |
| `02_pelatihan_model.ipynb` | Preprocessing, feature engineering (TF-IDF / Word2Vec), pelatihan model klasik & LSTM Bidirectional. |
| `dataset_final.csv` | Dataset hasil scraping — **sudah dianonimkan** (nama & mention pengguna di-mask). |
| `requirements.txt` | Daftar dependensi Python. |

## Setup

```bash
pip install -r requirements.txt
```

Notebook dirancang untuk dijalankan di **Google Colab** (memanfaatkan `google.colab.userdata` untuk token, dan opsional GPU RAPIDS/cuDF untuk akselerasi).

## Catatan Privasi

Kolom `full_text` pada dataset telah melalui proses anonimisasi:
- Prefiks nama pengguna (`Nama: ...`) dihapus.
- Mention (`@username`) diganti menjadi `@user`.

Dataset ini disediakan untuk tujuan riset/edukasi. Jika Anda menemukan data yang masih dapat mengidentifikasi individu, silakan buka issue.

## Lisensi

Belum ditentukan — tambahkan `LICENSE` sesuai kebutuhan (mis. MIT untuk kode, CC-BY-NC untuk data).
