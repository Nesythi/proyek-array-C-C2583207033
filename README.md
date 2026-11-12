# SISTEM MONITORING STOK DAN PENJUALAN KANTIN KAMPUS

## Identitas Mahasiswa

| Keterangan | Identitas |
|---|---|
| Nama | Nesythi Mus'idah |
| NIM | C2583207033 |
| Kelas | PTI3A  |
| Mata Kuliah | Algoritma dan Pemrograman lanjut |
| Nama Proyek | Kantin |
| Dosen Pengampu | Taofik Muhammad, M.Kom |

## 1. Deskripsi Proyek

Sistem Monitoring Stok dan Penjualan Kantin Kampus merupakan aplikasi berbasis console yang dibuat menggunakan bahasa pemrograman C.

Program ini bertujuan untuk membantu pengelola kantin dalam mengelola data produk, memantau persediaan stok, melakukan transaksi penjualan, serta mengetahui laporan hasil penjualan.

Program menggunakan array sebagai struktur data utama untuk menyimpan informasi produk selama program berjalan.

## 2. Daftar Fitur Program

Berikut fitur yang tersedia dalam program:

1. **Lihat Daftar Produk:** Menampilkan nama produk, harga, dan stok.
2. **Tambah Produk:** Menambahkan produk baru dengan kapasitas maksimal 50 produk.
3. **Ubah Produk:** Mengubah harga dan stok produk.
4. **Transaksi Penjualan:** Melakukan pembelian beberapa jenis produk dalam satu transaksi.
5. **Tambah Stok:** Menambahkan persediaan produk.
6. **Cari Produk:** Mencari produk berdasarkan nama.
7. **Urutkan Produk:** Mengurutkan produk berdasarkan harga termurah dan jumlah terjual terbanyak.
8. **Laporan Penjualan:** Menampilkan jumlah produk terjual, total unit, total pendapatan, dan produk terlaris.
9. **Cek Stok Menipis:** Menampilkan produk dengan stok kurang dari 5.
10. **Keluar:** Mengakhiri program.

## 3. Penerapan Array

Array digunakan sebagai struktur data utama untuk menyimpan informasi produk.

### A. Array Satu Dimensi

Array satu dimensi digunakan untuk menyimpan harga, stok, jumlah produk terjual, dan pendapatan.

Contoh kode:

```c
int harga[MAKS] = {15000, 10000, 5000, 18000, 4000};
int stok[MAKS] = {20, 15, 30, 10, 25};
int jumlahTerjual[MAKS] = {0, 0, 0, 0, 0};
int pendapatanProduk[MAKS] = {0};
```

### B. Array Karakter Dua Dimensi

Array karakter dua dimensi digunakan untuk menyimpan nama produk.

Contoh kode:

```c
char namaProduk[MAKS][PANJANG_NAMA] = {
    "Ayam Penyet",
    "Kentang Goreng",
    "Es Teh",
    "Kwetiau Goreng",
    "Air Mineral"
};
```

### C. Kapasitas Array

- Kapasitas maksimal: 50 produk.
- Jumlah produk awal: 5 produk.
- Panjang maksimal nama produk: 100 karakter.

## 4. Teknologi dan Konsep Pemrograman

Teknologi yang digunakan:
- Bahasa pemrograman C.
- Code::Blocks.
- Compiler GCC.

Konsep pemrograman yang diterapkan:
- Array satu dimensi dan dua dimensi.
- Percabangan `if`, `else`, dan `switch`.
- Perulangan `for` dan `do-while`.
- Fungsi.
- Pencarian produk.
- Pengurutan menggunakan Bubble Sort.
- Validasi input.

## 5. Cara Menjalankan Program

### A. Menggunakan Code::Blocks

1. Buka aplikasi Code::Blocks.
2. Pilih File → New → Empty File.
3. Masukkan source code program C.
4. Simpan dengan nama `sistem_monitoring_kantin.c`.
5. Pastikan ekstensi file adalah `.c`.
6. Tekan F9 atau pilih Build and Run.
7. Program akan berjalan pada jendela console.

### B. Menggunakan GCC

Kompilasi program menggunakan perintah:

```bash
gcc sistem_monitoring_kantin.c -o kantin
```

Jalankan program pada Windows:

```bash
kantin.exe
```

## 6. Dokumentasi Pengujian

Pengujian dilakukan untuk memastikan setiap fitur program berjalan sesuai dengan ketentuan tugas.

### Pengujian 1: Tambah Produk

**Tindakan:** Menambahkan produk baru dengan memasukkan nama, harga, dan stok.

**Hasil yang diharapkan:** Produk berhasil ditambahkan dan muncul pada daftar produk.

!<screnshot 1.jpeg> (screnshoot 2.jpeg)

### Pengujian 2: Transaksi Beberapa Produk

**Tindakan:** Melakukan pembelian beberapa jenis produk dalam satu transaksi.

**Hasil yang diharapkan:** Subtotal setiap produk dan total pembayaran ditampilkan dengan benar.

**Screenshot:**

![Transaksi](screenshots/02-transaksi.png)

### Pengujian 3: Pembaruan Stok

**Tindakan:** Melakukan transaksi penjualan.

**Hasil yang diharapkan:** Stok berkurang dan jumlah produk terjual bertambah.

**Screenshot:**

![Pembaruan Stok](screenshots/03-pembaruan-stok.png)

### Pengujian 4: Stok Tidak Mencukupi

**Tindakan:** Melakukan pembelian dengan jumlah melebihi stok yang tersedia.

**Hasil yang diharapkan:** Transaksi ditolak dan stok tetap tidak berubah.

**Screenshot:**

![Stok Tidak Cukup](screenshots/04-stok-tidak-cukup.png)

### Pengujian 5: Laporan Penjualan

**Tindakan:** Membuka menu laporan penjualan setelah melakukan transaksi.

**Hasil yang diharapkan:** Total unit terjual, total pendapatan, dan produk terlaris ditampilkan dengan benar.

**Screenshot:**

![Laporan Penjualan](screenshots/05-laporan-penjualan.png)

### Pengujian 6: Pengurutan Produk

**Tindakan:** Mengurutkan produk berdasarkan harga dan jumlah terjual.

**Hasil yang diharapkan:** Produk ditampilkan sesuai urutan yang dipilih.

**Screenshot:**

![Pengurutan Produk](screenshots/06-pengurutan.png)

### Pengujian 7: Pencarian dan Stok

**Tindakan:** Mencari produk berdasarkan nama dan memeriksa stok produk.

**Hasil yang diharapkan:** Produk ditemukan sesuai pencarian dan program menampilkan peringatan untuk stok kurang dari 5.

**Screenshot:**

![Pencarian dan Stok](screenshots/07-pencarian-stok.png)

## 7. Struktur Repository

Struktur folder repository GitHub:

```text
Proyek-Array-C-NIM/
|
|-- sistem_monitoring_kantin.c
|
|-- README.md
|
|-- screenshots/
    |
    |-- 01-tambah-produk.png
    |-- 02-transaksi.png
    |-- 03-pembaruan-stok.png
    |-- 04-stok-tidak-cukup.png
    |-- 05-laporan-penjualan.png
    |-- 06-pengurutan.png
    |-- 07-pencarian-stok.png
```

## 8. Kesimpulan

Melalui proyek ini, saya menerapkan konsep pemrograman bahasa C, khususnya penggunaan array, fungsi, percabangan, perulangan, pencarian, dan pengurutan.

Program ini dibuat untuk membantu pengelolaan data produk dan transaksi penjualan kantin agar lebih mudah dan terstruktur.

Selain itu, proyek ini menjadi sarana untuk memahami penerapan algoritma dan struktur data dalam menyelesaikan permasalahan sederhana di lingkungan sekitar.

---

**Program Studi Pendidikan Teknologi Informasi**  
**Universitas Muhammadiyah Tasikmalaya**  
**Tahun Akademik 2026/2027**
