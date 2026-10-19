Aplikasi Manajemen Toko Sepatu (Shoe Store Management System)

Aplikasi berbasis web sederhana menggunakan PHP (Native) dan MySQL untuk mengelola inventaris, transaksi stok, serta autentikasi pengguna pada toko sepatu.

Struktur Direktori & File Proyek

toko_sepatu/
├── config/
│   └── database.php          # Konfigurasi koneksi ke database MySQL
├── helpers/
│   ├── auth.php              # Helper fungsi autentikasi & proteksi halaman
│   ├── escape.php            # Helper keamanan (sanitasi input XSS)
│   └── views/
│       ├── header.php        # Komponen header umum
│       └── footer.php        # Komponen footer umum
├── public/
│   ├── dashboard.php         # Halaman utama / ringkasan inventaris
│   ├── login.php             # Halaman autentikasi/masuk pengguna
│   ├── logout.php            # Fungsi untuk mengakhiri sesi pengguna
│   ├── products.php          # Daftar produk sepatu
│   ├── product_add.php       # Form penambahan produk sepatu baru
│   ├── product_edit.php      # Form pengubahan data produk sepatu
│   ├── product_delete.php    # Proses penghapusan produk sepatu
│   └── stock_transaction.php # Pengelolaan transaksi stok (masuk/keluar)
├── views/
│   ├── header.php            # Template tampilan header
│   └── footer.php            # Template tampilan footer
└── schema.sql                # Skrip struktur database & tabel


Fitur Utama

Autentikasi Pengguna (public/login.php, public/logout.php)

Keamanan akses menggunakan pembatas sesi (helpers/auth.php).

Proteksi penginputan data sensitif menggunakan fungsi sanitasi (helpers/escape.php).

Manajemen Inventaris / Produk (public/products.php)

Tambah Produk (product_add.php): Menambahkan sepatu baru ke katalog.

Edit Produk (product_edit.php): Memperbarui informasi produk (nama, harga, deskripsi, dll.).

Hapus Produk (product_delete.php): Menghapus stok/produk dari database.

Transaksi Stok (public/stock_transaction.php)

Mencatat penambahan atau pengurangan jumlah stok barang secara realtime.

Dashboard Utama (public/dashboard.php)

Menampilkan ringkasan informasi toko dan stok secara visual dan terorganisir.