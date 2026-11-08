# 🧠 UTS Deep Learning: Analisis Sentimen Twitter menggunakan LSTM

Repositori ini dibuat untuk memenuhi Tugas / Ujian Tengah Semester (UTS) mata kuliah Deep Learning. Proyek ini berfokus pada pembangunan model *Deep Learning* menggunakan arsitektur **Long Short-Term Memory (LSTM)** untuk mengklasifikasikan sentimen opini publik berdasarkan data teks Twitter.

## 👤 Informasi Mahasiswa
- **Nama**  : Arif Rizki Kurniadi
- **NIM**   : 202432089
- **Kelas** : Deep Learning - B

---

## 📖 Deskripsi Permasalahan
Dataset yang digunakan berisi 1,6 juta *tweet* yang sangat bising—penuh dengan *slang*, singkatan, kesalahan ketik, dan tata bahasa yang tidak baku—sehingga menciptakan masalah skalabilitas dan kompleksitas tinggi. Mengurai dan menyimpulkan jutaan opini publik yang tidak terstruktur ini secara manual adalah hal yang mustahil. Oleh karena itu, dibutuhkan sistem komputasi cerdas yang mampu membaca secepat kilat sekaligus memahami konteks di balik bahasa sehari-hari yang acak-acakan tersebut.

## 🎯 Tujuan Pemodelan & Pemilihan Algoritma
Tujuan utama pemodelan ini adalah menciptakan sistem yang mengotomatisasi klasifikasi polaritas sentimen (positif atau negatif) dengan mengekstraksi makna semantik dan pola urutan dari teks. 

**Mengapa memilih LSTM?**
Algoritma **Long Short-Term Memory (LSTM)** dipilih karena kemampuannya yang sangat superior dalam menangani data sekuensial (berurutan) seperti bahasa. Mekanisme sel memori dan gerbang (*gates*) pada LSTM memungkinkannya mengingat konteks krusial dari awal kalimat (misalnya kata negasi seperti "tidak") dan menghubungkannya dengan kata di akhir kalimat. Hal ini memecahkan masalah "amnesia" (*vanishing gradient*) yang sering dialami algoritma lain, memastikan model dapat menyimpulkan sentimen dengan akurasi tinggi layaknya manusia yang membaca kalimat secara utuh.

## 📊 Tentang Dataset (Sentiment140)
Proyek ini menggunakan [Sentiment140 Dataset](https://www.kaggle.com/datasets/kazanova/sentiment140), sebuah korpus *benchmark* NLP dari Stanford University.
- **Total Data:** 1.600.000 baris teks *tweet* berbahasa Inggris.
- **Pelabelan:** Dilakukan secara otomatis menggunakan deteksi *emoticon* (*distant supervision*), di mana *emoticon* tersebut kemudian dihapus dari teks mentah.
- **Target Klasifikasi:** Biner.
  - `0` = Sentimen Negatif
  - `4` = Sentimen Positif
- **Fitur Utama:** Dalam pemodelan ini, fokus utama ekstraksi fitur (X) dilakukan pada kolom `text`, dan prediksi (Y) pada kolom `target`.

## 🛠️ Kebutuhan Sistem & Library (Prerequisites)
Pastikan Anda telah menginstal *library* berikut sebelum menjalankan *notebook* atau *script* di dalam repositori ini:
```bash
pip install pandas numpy matplotlib seaborn
pip install scikit-learn nltk
pip install tensorflow keras
```

## 🚀 Cara Menjalankan Proyek
1. *Clone* repositori ini ke dalam mesin lokal Anda:
   ```bash
   git clone https://github.com/aripp996/UTS_DEEPL_B_202432089_Arif-Rizki-Kurniadi.git
   ```
2. Unduh dataset Sentiment140 dari Kaggle dan letakkan file `.csv` ke dalam folder repositori (atau sesuai dengan jalur/direktori yang diarahkan di dalam kode).
3. Buka dan jalankan file *Jupyter Notebook* (misalnya `Notebook_UTS.ipynb`) secara berurutan, mulai dari tahapan *Data Preprocessing*, *Modeling*, hingga *Evaluation*.

## 📈 Hasil dan Evaluasi
*(Bagian ini dapat Anda isi nanti dengan ringkasan metrik akurasi, *loss*, atau grafik *confusion matrix* yang dihasilkan oleh model LSTM Anda setelah proses *training* selesai).*

---
*Dibuat untuk keperluan evaluasi akademik - 2024*
