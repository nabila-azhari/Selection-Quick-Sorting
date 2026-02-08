# README – Analisis Perbandingan Sorting Video (Quick Sort vs Selection Sort)

## Deskripsi Proyek

Proyek ini merupakan implementasi **perbandingan algoritma sorting rekursif dan iteratif** menggunakan data video acak.
Dua algoritma yang dibandingkan:

* **Quick Sort (rekursif)** → digunakan untuk mengurutkan video berdasarkan jumlah penonton.
* **Selection Sort (iteratif)** → digunakan sebagai pembanding performa.

Setelah proses pengurutan, sistem akan:

1. Mengambil **30 video teratas** berdasarkan jumlah penonton.
2. Mengelompokkan video ke dalam kategori:

   * `music`
   * `gaming`
   * `film`
3. Mengukur **waktu eksekusi** masing-masing algoritma.
4. Menampilkan:

   * Tabel runtime
   * Grafik perbandingan performa

---

## Struktur Program

### 1. Kelas `Video`

Merepresentasikan objek video dengan atribut:

* `title` → Judul video
* `category` → Kategori video
* `viewers` → Jumlah penonton

---

### 2. Fungsi Utama

#### a. Generate Data

```python
generate_random_videos(n)
```

Membuat **n video acak** dengan:

* Kategori acak (`music`, `gaming`, `film`)
* Jumlah penonton acak (1.000 – 1.000.000)

---

#### b. Algoritma Sorting

**Quick Sort (Rekursif)**

```python
quick_sort(videos)
```

* Pendekatan divide and conquer
* Kompleksitas rata-rata: **O(n log n)**

**Selection Sort (Iteratif)**

```python
selection_sort(videos)
```

* Membandingkan elemen satu per satu
* Kompleksitas: **O(n²)**

---

#### c. Kategorisasi Video

```python
categorize_videos(videos)
```

Mengelompokkan video ke:

* Music
* Gaming
* Film

---

#### d. Sorting + Kategorisasi

**Rekursif**

```python
sort_and_categorize_recursive(videos)
```

**Iteratif**

```python
sort_and_categorize_iterative(videos)
```

Keduanya:

* Mengurutkan video
* Mengambil **Top 30**
* Mengelompokkan berdasarkan kategori

---

### 3. Analisis Runtime

Program menguji beberapa ukuran input:

```
[100, 250, 400, 550, 700, 850, 1000, 1150, 1300, 1450]
```

Untuk setiap ukuran:

* Mengukur waktu **Quick Sort**
* Mengukur waktu **Selection Sort**
* Menyimpan hasil dalam **pandas DataFrame**
* Menampilkan **grafik matplotlib**

---

## Cara Menjalankan

### 1. Install Dependensi

```bash
pip install matplotlib pandas
```

### 2. Jalankan Program

```bash
python nama_file.py
```

Program akan:

* Menampilkan tabel runtime di terminal
* Menampilkan grafik perbandingan performa

---

## Hasil yang Diharapkan

* **Quick Sort** jauh lebih cepat untuk data besar.
* **Selection Sort** memiliki waktu eksekusi meningkat drastis seiring ukuran input.
* Grafik menunjukkan:

  * Kurva Quick Sort relatif landai.
  * Kurva Selection Sort meningkat tajam.

---

## Tujuan Pembelajaran

Proyek ini bertujuan untuk:

* Memahami perbedaan **rekursif vs iteratif**
* Menganalisis **kompleksitas algoritma sorting**
* Menggunakan **Python untuk eksperimen runtime**
* Memvisualisasikan performa algoritma dengan **matplotlib**

---

## Pengembangan Selanjutnya

Beberapa ide pengembangan:

* Menambahkan algoritma lain:

  * Merge Sort
  * Heap Sort
  * Bubble Sort
* Menggunakan **data nyata** (misalnya dataset YouTube).
* Menyimpan hasil analisis ke **CSV atau Excel**.
* Membuat **visualisasi interaktif** dengan Plotly.

---

## Penulis

Proyek ini dibuat untuk keperluan **pembelajaran analisis dan kompleksitas algoritma** menggunakan Python.
