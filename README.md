# 2418069DataCleansing-Enrichment
Data Cleansing &amp; Enrichment Implementation 
# Tugas Data Mining: Data Cleansing, Deduplikasi, dan Enrichment

**Nama:** ISA AL FAREL SAFARUDIN 
**NIM:** 2418069 
**Mata Kuliah:** Data Mining  

## Deskripsi Tugas
Repositori ini berisi pengerjaan tugas Data Mining yang berfokus pada prapemrosesan data (data preprocessing) menggunakan Python dan Pandas di Google Colab. Dataset yang digunakan adalah data mentah film IMDB (`messy_IMDB_dataset.xlsx`) yang memiliki berbagai anomali.

## Langkah-Langkah yang Dilakukan

### 1. Data Cleansing (Pembersihan Data)
* **Pembersihan Kolom:** Menghapus kolom kosong (`Unnamed: 8`) dan memperbaiki penamaan kolom agar standar (menghapus spasi dan karakter aneh).
* **Pembersihan Teks pada Angka:** Menghilangkan simbol dolar (`$`), koma, dan salah ketik huruf 'o' pada kolom `Income`, serta membersihkan karakter huruf pada kolom `Score` lalu mengubahnya menjadi tipe data `float`.
* **Standardisasi Format:** Menyeragamkan penulisan negara pada kolom `Country` (mengubah 'US' menjadi 'USA') dan memperbaiki format tanggal rilis.
* **Penanganan Missing Values:** Mengisi nilai kosong pada kolom `Duration` dengan nilai median, dan `Content Rating` dengan label 'Unknown'.

### 2. Deduplikasi Data
* Mengidentifikasi dan menghapus baris data yang ganda (duplikat) berdasarkan ID unik film (`Title_ID`), menyisakan data kemunculan pertama.

### 3. Data Enrichment (Pengayaan Data)
* **Ekstraksi Tahun:** Membuat kolom baru `Release_Year` yang diekstrak dari kolom tanggal rilis.
* **Kategorisasi Skor:** Membuat kolom baru `Score_Category` untuk mengelompokkan kualitas film menjadi 'High' (>= 8.5), 'Medium' (7.0 - 8.4), dan 'Low' (< 7.0) berdasarkan kolom `Score`.

## Cara Menjalankan Kode
1. Clone repositori ini atau unduh file `messy_IMDB_dataset.xlsx` dan file `.ipynb`.
2. Buka file `.ipynb` menggunakan Google Colab atau Jupyter Notebook.
3. Pastikan dataset berada di direktori yang sama dengan notebook, atau sesuaikan *path* pembacaan file di blok kode pertama.
4. Jalankan semua cell (Run All).

## Tools
* Python 3
* Pandas, Regex
* Google Colab
