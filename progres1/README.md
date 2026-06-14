# PJBL-Sistem-Basis-Data
## LAPORAN PROGRES 1 - SISTEM BASIS DATA 

**Studi Kasus:** Sistem Manajemen Inventori Laboratorium 

**Kelompok:** 
1. Fikri Restu Nugraha (2501020109)
2. Virtuando Jagad Saputrana (2501020106)
3. Ramlan Leonardo Napitupulu (2501020102)
4. Almand Zaky S. (2501020114)


### 1. Deskripsi Studi Kasus 
Sistem Manajemen Inventori Laboratorium adalah sebuah sistem basis data yang dirancang untuk mengelola dan mendokumentasikan seluruh aset laboratorium. Sistem ini bertujuan untuk melacak ketersediaan barang, alat, dan bahan pratikum, serta mencatat secara terstruktur proses transaksi peminjaman dan pengembalian oleh civitas akademika di lingkungan kampus. 

### 2. Latar Belakang dan Tujuan Sistem
**Latar Belakang:** Sistem pencatatan inventori dan peminjaman alat di laboratorium saat ini masih dilakukan secara manual menggunakan buku besar. Hal ini menyebabkan data tidak terstruktur dan sulit diolah, rentan terhadap kehilangan data, serta menyulitkan laboran dalam memantau sirkulasi peminjaman dan mengecek ketersediaan stok barang secara *real-time*.  

**Tujuan:** Merancang database yang terstruktur untuk mengelola data inventori laboratorium.  
* Mengimplementasikan database menggunakan DBMS (MySQL/PostgreSQL) untuk menggantikan pencatatan manual.  
* Menghasilkan query untuk kebutuhan laporan, seperti laporan stok barang dan riwayat peminjaman alat.  

### 3. Identifikasi Aktor 
Pihak yang akan berinteraksi dengan sistem ini meliputi: 
1. **Laboran / Admin:** Aktor yang memiliki hak akses penuh untuk mengelola data master (barang, kategori, anggota) dan mencatat transaksi peminjaman/pengembalian. 
2. **Peminjam (Mahasiswa/Dosen):** Aktor yang melakukan peminjaman alat laboratorium. 
3. **Kepala Laboratorium:** Aktor yang melihat laporan rekapitulasi inventori dan aktivitas peminjaman. 

### 4. Kebutuhan Fungsional 
Sistem basis data ini harus memiliki fungsionalitas sebagai berikut:
1. Sistem dapat menambahkan data barang atau alat laboratorium baru ke dalam inventori.
2. Sistem dapat menampilkan daftar seluruh barang beserta jumlah stok saat ini. 
3. Sistem dapat memperbarui (mengedit) informasi detail dan jumlah stok barang. 
4. Sistem dapat menghapus data barang yang sudah rusak atau afkir. 
5. Sistem dapat mengelola (tambah, tampil, edit, hapus) data profil anggota peminjam. 
6. Sistem dapat mencatat transaksi peminjaman alat beserta tanggal pinjam. 
7. Sistem dapat mencatat transaksi pengembalian alat beserta tanggal kembali dan kondisi barang. 
8. Sistem dapat mengurangi stok barang secara otomatis saat dipinjam dan menambah stok saat dikembalikan. 
9. Sistem dapat menampilkan daftar barang yang statusnya sedang dipinjam (belum dikembalikan). 
10. Sistem dapat menghasilkan laporan riwayat transaksi peminjaman dalam rentang waktu tertentu. 

### 5. Kebutuhan Data 
Entitas data yang dibutuhkan untuk membangun basis data ini meliputi: 
* **Data Barang:** Menyimpan informasi ID Barang, Nama Barang, Spesifikasi, dan Stok. 
* **Data Kategori Barang:** Menyimpan klasifikasi barang (misal: Alat Kaca, Elektronik, Bahan Kimia). 
* **Data Anggota:** Menyimpan informasi ID Anggota (NIM/NIDN), Nama, dan Kontak peminjam. 
* **Data Laboran:** Menyimpan informasi staf yang bertugas melayani transaksi. 
* **Data Transaksi Peminjaman:** Menyimpan ID Transaksi, Tanggal Pinjam, Tanggal Kembali, dan status transaksi. 
* **Data Detail Transaksi:** Menyimpan detail barang apa saja dan berapa jumlah yang dipinjam dalam satu transaksi. 

### 6. Diagram Proses (Use Case/Flowchart) 

 
### 6. Pembagian Tugas Anggota 
* **Restu:** Menyusun Deskripsi studi kasus, membuat dan mengelola repository GitHub kelompok, serta merapikan Pembagian tugas anggota. 
* **Almand:** Menyusun Latar belakang dan tujuan sistem.  
* **Ando:** Menganalisis Identifikasi aktor dan membuat Diagram proses (Use Case/Flowchart).  
* **Ramlan:** Merumuskan Kebutuhan fungsional (minimal 10 kebutuhan) dan menentukan Kebutuhan data.
