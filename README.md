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

| No. | Skenario | Input atau Tindakan | Hasil yang Diharapkan | Bukti Screenshot |
| :---: | :--- | :--- | :--- | :---: |
| 1 | **Tambah produk** | Memilih menu 2, memasukkan produk baru `Chiken Curry`, harga `25000`, stok `15` | Produk `Chiken Curry` berhasil disimpan dan muncul dalam daftar produk (Menu 1) | ![Screenshot1.png](Tampilan%20Program-UTS/Screenshot1.png) |
| 2 | **Transaksi** | Memilih menu 4, membeli `Nasi Goreng` (3 pcs), `Es Teh Manis` (3 pcs) dan `Gorengan` (1 pcs) dalam 1 transaksi | Subtotal tiap barang dan total pembayaran terhitung dengan akurat pada struk | ![Screenshot2.1.png](Tampilan%20Program-UTS/Screenshot2.1.png) |
| 3 | **Pembaruan stok** | Memeriksa data produk (Menu 1) setelah menyelesaikan transaksi pada skenario 2 | Stok `Nasi Goreng`, `Es Teh` & `Gorengan` berkurang, jumlah terjual bertambah | ![Screenshot3.png](Tampilan%20Program-UTS/Screenshot3.png) |
| 4 | **Stok tidak cukup** | Memilih menu 4, membeli `Mie Ayam` sejumlah `6` unit (melebihi stok yang ada = 3) | Transaksi ditolak dengan pesan peringatan; jumlah stok barang tetap/tidak berubah | ![Screenshot4.png](Tampilan%20Program-UTS/Screenshot4.png) |
| 5 | **Laporan** | Memilih menu 8 (Laporan Penjualan) | Total unit terjual, total pendapatan kantin, & produk terlaris dihitung dengan benar | ![Screenshot5.png](Tampilan%20Program-UTS/Screenshot5.png) |
| 6 | **Pengurutan** | Memilih menu 7, urutkan berdasarkan harga termurah dan jumlah penjualan terbanyak  | Urutan posisi produk pada daftar berubah sesuai dengan metode pengurutan yang dipilih (Jumlah penjualan terbanyak) | ![Screenshot6.png](Tampilan%20Program-UTS/Screenshot6.png) |
| 7 | **Pencarian dan stok** | Memilih menu 6 (Cari produk `Nasi Goreng`) dan menu 9 (Cek stok < 5) `Mie Ayam` | Menampilkan hasil pencarian produk `Nasi` dan `Mie Ayam` daftar peringatan barang bersisa < 5 | ![Screenshot7.1.png](Tampilan%20Program-UTS/Screenshot7.1.png) & ![Screenshot7.2.png](Tampilan%20Program-UTS/Screenshot7.2.png) |

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
