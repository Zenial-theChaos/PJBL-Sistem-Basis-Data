# Penjelasan Entitas
1. **KATEGORI_BARANG** Menyimpan klasifikasi atau pengelompokan jenis barang laboratorium, misalnya Alat Kaca, Elektronik, atau Bahan Kimia. Entitas ini berfungsi sebagai master kategori agar barang-barang dapat dikelola berdasarkan jenisnya.
2. **BARANG** Menyimpan data seluruh aset atau inventori laboratorium. Setiap barang memiliki nama, spesifikasi teknis, dan jumlah stok yang tersedia. Barang terhubung ke kategori melalui id_kategori sebagai foreign key.
3. **ANGGOTA** Menyimpan data pihak yang dapat melakukan peminjaman, yaitu mahasiswa atau dosen. id_anggota menggunakan NIM atau NIDN, jenis_anggota membedakan apakah dia mahasiswa atau dosen.
4. **LABORAN** Menyimpan data staf laboratorium yang bertugas melayani dan mencatat setiap transaksi peminjaman/pengembalian. Laboran berperan sebagai operator sistem.
5. **TRANSAKSI_PEMINJAMAN** Menyimpan data header dari setiap sesi peminjaman — siapa yang meminjam, siapa laboran yang bertugas, kapan dipinjam, kapan harus dikembalikan, dan status transaksinya (misal: dipinjam / dikembalikan).
6. **DETAIL_TRANSAKSI** Menyimpan rincian barang apa saja yang dipinjam dalam satu transaksi. Satu transaksi bisa mencakup banyak barang sekaligus, sehingga entitas ini berfungsi sebagai tabel jembatan antara transaksi dan barang.

# Penjelasan Relasi
| Relasi | Kardinalitas | Keterangan |
|--------|-------------|------------|
| `KATEGORI_BARANG` → `BARANG` | 1 ke banyak | Satu kategori dapat memiliki banyak barang |
| `ANGGOTA` → `TRANSAKSI_PEMINJAMAN` | 1 ke banyak | Satu anggota bisa melakukan banyak transaksi peminjaman |
| `LABORAN` → `TRANSAKSI_PEMINJAMAN` | 1 ke banyak | Satu laboran bisa mencatat banyak transaksi |
| `TRANSAKSI_PEMINJAMAN` → `DETAIL_TRANSAKSI` | 1 ke banyak | Satu transaksi terdiri dari banyak detail barang |
| `BARANG` → `DETAIL_TRANSAKSI` | 1 ke banyak | Satu barang bisa muncul di banyak detail transaksi berbeda |
