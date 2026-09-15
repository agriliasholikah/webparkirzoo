🦁 Zoo Parking — Sistem Informasi Parkir Kebun Binatang
Sistem informasi manajemen parkir berbasis web untuk mengelola kendaraan, area parkir, reservasi, pembayaran, dan riwayat transaksi.

🌐 Link Project
Akses	Link
🎨 Wireframe / Mockup UI	Lihat Mockup UI
🅿️ Website Zoo Parking	Buka Website Zoo Parking
💻 Repository	GitHub Zoo Parking
📌 Tentang Project
Zoo Parking membantu proses pengelolaan parkir agar lebih mudah, cepat, dan terorganisir.

Sistem memiliki 4 jenis pengguna:

👨‍💼 Admin — mengelola data sistem, pengguna, tarif, dan area parkir.

👮 Petugas — mengelola kendaraan masuk/keluar, reservasi, pembayaran, dan transaksi.

📊 Owner — melihat dashboard dan informasi/laporan parkir.

👤 Pelanggan — melakukan reservasi parkir dan melihat informasi/riwayat reservasi.

✨ Fitur Utama
👨‍💼 Admin
Dashboard admin

Kelola pengguna

Kelola tarif parkir

Kelola area parkir

Melihat kapasitas area parkir

Melihat log aktivitas

👮 Petugas
Dashboard petugas

Parkir umum

Pencatatan kendaraan masuk

Pencatatan kendaraan keluar

Pengelolaan reservasi

Konfirmasi kode booking

Cetak karcis

Cetak karcis reservasi

Pembayaran parkir

Metode pembayaran: Tunai, Non Tunai, QRIS

Cetak struk

Riwayat transaksi

📊 Owner
Dashboard owner

Melihat statistik parkir

Melihat informasi transaksi

Memantau aktivitas sistem

👤 Pelanggan
Registrasi dan login

Reservasi parkir online

Mendapatkan kode booking

Melihat status reservasi

Melihat riwayat reservasi

Memberikan ulasan

🔄 Alur Parkir Umum
Kendaraan Datang
       ↓
Input Data Kendaraan
       ↓
Pilih Area Parkir
       ↓
Cek Kapasitas
       ↓
Kendaraan Masuk
       ↓
Cetak Karcis
       ↓
Kendaraan Parkir
       ↓
Kendaraan Keluar
       ↓
Hitung Biaya
       ↓
Pembayaran
       ↓
Cetak Struk
       ↓
Selesai
🎫 Alur Reservasi
Pelanggan Reservasi Online
          ↓
      Kode Booking
          ↓
    Kendaraan Datang
          ↓
  Petugas Validasi Booking
          ↓
   Konfirmasi Reservasi
          ↓
  Cetak Karcis Reservasi
          ↓
    Kendaraan Parkir
          ↓
    Kendaraan Keluar
          ↓
      Pembayaran
          ↓
      Cetak Struk
          ↓
        Selesai
💰 Tarif Parkir
Jenis Kendaraan	Tarif
🏍️ Motor	Rp5.000
🚗 Mobil	Rp10.000
🚙 Lainnya	Sesuai konfigurasi sistem
Sistem juga mendukung tarif maksimal sesuai konfigurasi database.

🅿️ Manajemen Area Parkir
Setiap area mempunyai:

Nama area

Kapasitas

Jumlah kendaraan terisi

Ketika kendaraan masuk:

Terisi + 1
Ketika kendaraan keluar:

Terisi - 1
Sistem mencegah kendaraan masuk apabila area sudah penuh.

🗄️ Basis Data
Project menggunakan MySQL.

Tabel utama:

tb_user
tb_kendaraan
tb_area_parkir
tb_parkir
tb_reservasi
tb_tarif
tb_log_aktivitas
tb_ulasan
tb_faq
Relasi utama
tb_user
   │
   ├── tb_kendaraan
   │
   ├── tb_parkir
   │
   └── tb_log_aktivitas

tb_kendaraan ─── tb_parkir
tb_area_parkir ─ tb_parkir
tb_reservasi ─── tb_parkir
tb_tarif ─────── tb_parkir
📊 Status Data
Status Parkir
parkir
selesai
Status Reservasi
booked
digunakan
selesai
batal
🛠️ Teknologi
PHP

MySQL

HTML5

CSS3

JavaScript

Bootstrap

XAMPP

InfinityFree

GitHub

📂 Struktur Project
sistem_parkir/
│
├── admin_log.php
├── admin_tarif.php
├── admin_user.php
├── cetak_karcis.php
├── cetak_karcis_reservasi.php
├── cetak_struk.php
├── dashboard_admin.php
├── dashboard_owner.php
├── dashboard_petugas.php
├── dashboard_user.php
├── get_stats_parkir.php
├── index.php
├── koneksi.php
├── login.php
├── logout.php
├── pembayaran_berhasil.php
├── qr.jpeg
└── register.php
🔐 Hak Akses
Role	Akses Utama
Admin	Data pengguna, tarif, area, log
Petugas	Parkir, reservasi, pembayaran, transaksi
Owner	Dashboard dan statistik
Pelanggan	Reservasi dan riwayat
🚀 Menjalankan Project
Install XAMPP.

Aktifkan Apache dan MySQL.

Simpan project ke:

C:/xampp/htdocs/sistem_parkir/
Buat database melalui:

http://localhost/phpmyadmin
Sesuaikan konfigurasi database pada koneksi.php.

Jalankan:

http://localhost/sistem_parkir/
🌐 Hosting
Website dapat dijalankan menggunakan hosting yang mendukung PHP dan MySQL.

Website: https://zooparkir.infinityfree.me/

Jangan menyimpan username atau password database asli di repository GitHub publik.

🎨 Dokumentasi UI/UX
Dokumentasi wireframe/mockup, UX design, flowchart/user flow, ERD, dan struktur basis data dapat dilihat di:

🔗 Lihat Wireframe / Mockup UI

🎯 Tujuan Project
Mempermudah pengelolaan parkir.

Mengurangi pencatatan manual.

Mempermudah petugas mengelola kendaraan.

Memantau kapasitas area parkir.

Mengelola reservasi online.

Mempermudah proses pembayaran.

Menyimpan riwayat transaksi secara terstruktur.

👨‍💻 Developer
Zoo Parking
Sistem Informasi Manajemen Parkir Kebun Binatang berbasis web.

📄 Lisensi
Project ini dibuat untuk keperluan pembelajaran, tugas, dan pengembangan sistem informasi parkir.

