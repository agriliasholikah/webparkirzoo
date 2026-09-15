🦁 Zoo Parking — Sistem Informasi Parkir Kebun Binatang

Aplikasi web Zoo Parking merupakan sistem informasi manajemen parkir berbasis web yang digunakan untuk mengelola kendaraan, area parkir, reservasi online, pembayaran, serta riwayat transaksi parkir.

🌐 Link Project

🎨 Wireframe / Mockup UI/UX: Lihat Mockup UI

🅿️ Website Zoo Parking: Buka Website Zoo Parking

💻 Repository GitHub: Lihat Repository

📌 Tentang Project

Sistem ini dibuat untuk membantu proses pengelolaan parkir agar lebih mudah, cepat, dan terorganisir.

Zoo Parking memiliki 4 jenis pengguna dengan hak akses yang berbeda:

Role

Deskripsi

👨‍💼 Admin

Mengelola data pengguna, tarif, area parkir, serta informasi sistem.

👮 Petugas

Mengelola kendaraan masuk/keluar, reservasi, pembayaran, dan transaksi parkir.

📊 Owner

Melihat dashboard, transaksi, riwayat parkir, reservasi, dan laporan.

👤 Pelanggan

Melakukan reservasi parkir online dan melihat riwayat reservasi.

✨ Fitur Utama

👨‍💼 Admin

#Dashboard admin

*Melihat jumlah kendaraan yang sedang parkir

*Melihat kapasitas dan ketersediaan area parkir

Mengelola pengguna dan role

Mengelola tarif parkir

Mengelola area parkir

Menambah dan mengubah area parkir

Melihat log aktivitas sistem

👮 Petugas

Dashboard petugas

Parkir umum

Input kendaraan masuk

Proses kendaraan keluar

Pencarian kendaraan berdasarkan nomor plat

Pengelolaan area parkir

Pengelolaan reservasi online

Konfirmasi kode booking

Cetak karcis parkir

Cetak karcis khusus reservasi

Proses pembayaran

Metode pembayaran:

Tunai

Non Tunai

QRIS

Cetak struk pembayaran

Melihat riwayat transaksi

📊 Owner

Dashboard owner

Melihat transaksi parkir

Melihat riwayat parkir

Melihat riwayat reservasi

Rekap laporan parkir

Filter laporan berdasarkan periode

Melihat informasi pendapatan

Mencetak laporan

👤 Pelanggan

Melihat informasi parkir

Melihat ketersediaan area parkir

Melakukan reservasi parkir online

Mendapatkan kode booking

Melihat status reservasi

Melihat riwayat reservasi

🎫 Alur Reservasi Online

Pelanggan melakukan reservasi
          ↓
   Mendapat kode booking
          ↓
   Kendaraan datang
          ↓
Petugas memasukkan kode booking
          ↓
   Validasi reservasi
          ↓
 Konfirmasi reservasi
          ↓
 Cetak karcis reservasi
          ↓
    Kendaraan parkir
          ↓
    Kendaraan keluar
          ↓
      Pembayaran
          ↓
      Cetak struk
          ↓
   Reservasi selesai

🅿️ Alur Parkir Umum

Kendaraan datang
       ↓
Input nomor plat
       ↓
Pilih jenis kendaraan
       ↓
Pilih area parkir
       ↓
Cek kapasitas area
       ↓
Kendaraan masuk
       ↓
Cetak karcis
       ↓
Kendaraan parkir
       ↓
Kendaraan keluar
       ↓
Hitung biaya parkir
       ↓
Pembayaran
       ↓
Cetak struk
       ↓
Transaksi selesai

💰 Sistem Tarif Parkir

Tarif parkir dapat dikonfigurasi berdasarkan jenis kendaraan.

Jenis Kendaraan

Tarif

🏍️ Motor

Rp5.000

🚗 Mobil

Rp10.000

🚙 Lainnya

Mengikuti konfigurasi sistem

Sistem juga mendukung tarif maksimal sehingga biaya parkir dapat dibatasi sesuai konfigurasi tarif.

🅿️ Manajemen Area Parkir

Setiap area parkir memiliki informasi:

Nama area

Kapasitas

Jumlah kendaraan yang sedang parkir

Ketersediaan slot

Ketika kendaraan masuk, jumlah kendaraan pada area akan bertambah:

Terisi + 1

Ketika kendaraan keluar:

Terisi - 1

Sistem juga melakukan pengecekan kapasitas agar kendaraan tidak dapat masuk apabila area parkir sudah penuh.

🗄️ Database

Project ini menggunakan MySQL.

Tabel utama yang digunakan:

tb_user
tb_kendaraan
tb_area_parkir
tb_parkir
tb_reservasi
tb_tarif
tb_log_aktivitas
tb_ulasan
tb_faq

tb_user

Menyimpan data pengguna dan role sistem.

tb_kendaraan

Menyimpan informasi kendaraan:

Nomor plat

Jenis kendaraan

Warna

Pemilik

Pengguna kendaraan

tb_area_parkir

Menyimpan informasi area:

Nama area

Kapasitas

Jumlah kendaraan yang sedang parkir

tb_parkir

Menyimpan transaksi parkir:

ID parkir

Kendaraan

Area parkir

Reservasi

Petugas

Waktu masuk

Waktu keluar

Status parkir

Total biaya

Metode pembayaran

Denda

tb_reservasi

Menyimpan data reservasi:

Kode booking

Nama pemesan

Nomor plat

Jenis kendaraan

Area parkir

Tanggal reservasi

Status reservasi

tb_tarif

Menyimpan tarif parkir berdasarkan jenis kendaraan.

🔐 Hak Akses Pengguna

Role

Akses Utama

Admin

Pengguna, tarif, area parkir, dashboard, log

Petugas

Parkir umum, reservasi, kendaraan masuk/keluar, pembayaran, struk

Owner

Dashboard, transaksi, riwayat, reservasi, laporan

Pelanggan

Reservasi online dan riwayat reservasi

📂 Struktur Project

Struktur file utama project:

sistem_parkir/
│
├── index.php
├── login.php
├── register.php
├── logout.php
├── koneksi.php
│
├── dashboard_admin.php
├── dashboard_petugas.php
├── dashboard_owner.php
├── dashboard_user.php
│
├── admin_user.php
├── admin_tarif.php
├── admin_log.php
│
├── cetak_karcis.php
├── cetak_karcis_reservasi.php
├── cetak_struk.php
├── pembayaran_berhasil.php
│
├── get_stats_parkir.php
└── qr.jpeg

🛠️ Teknologi yang Digunakan

PHP — Backend dan proses sistem

MySQL — Database

HTML5 — Struktur halaman

CSS3 — Tampilan antarmuka

JavaScript — Interaksi halaman

Bootstrap 5.3 — Komponen dan responsive layout

Font Awesome 6.4 — Ikon

Chart.js — Grafik dan statistik

SweetAlert2 — Notifikasi

XAMPP — Local development

InfinityFree — Hosting

🔄 Status Data

Status Parkir

parkir
selesai

Status Reservasi

booked
digunakan
selesai
batal

🚀 Cara Menjalankan Project

1. Clone Repository

git clone https://github.com/agriliasholikah/webparkirzoo.git

Masuk ke folder project:

cd webparkirzoo

2. Jalankan XAMPP

Aktifkan:

Apache
MySQL

Kemudian letakkan project di:

htdocs/
└── webparkirzoo/

3. Buat Database

Buka:

http://localhost/phpmyadmin

Buat database sesuai dengan konfigurasi pada koneksi.php.

4. Konfigurasi Database

Sesuaikan file:

koneksi.php

dengan konfigurasi MySQL pada komputer/server.

5. Jalankan Project

Buka browser:

http://localhost/webparkirzoo/

🌐 Hosting

Project dapat dijalankan pada hosting yang mendukung:

PHP

MySQL

phpMyAdmin

File Manager

Project Zoo Parking saat ini menggunakan InfinityFree sebagai hosting.

Jangan menyimpan username, password database, atau credential penting lainnya di repository GitHub publik.

📸 Tampilan Aplikasi

Screenshot aplikasi dapat ditambahkan ke repository, kemudian ditampilkan pada README menggunakan format:

![Login](screenshots/login.png)

![Dashboard Admin](screenshots/dashboard-admin.png)

![Dashboard Petugas](screenshots/dashboard-petugas.png)

![Pembayaran](screenshots/pembayaran.png)

![Cetak Struk](screenshots/cetak-struk.png)

🎯 Tujuan Project

Project Zoo Parking dibuat untuk:

Mempermudah pengelolaan parkir.

Mengurangi pencatatan kendaraan secara manual.

Mempermudah petugas mengelola kendaraan masuk dan keluar.

Mengetahui kapasitas area parkir.

Mengelola reservasi parkir secara online.

Mempermudah proses pembayaran.

Menyimpan riwayat transaksi secara terstruktur.

Membantu owner dalam melihat laporan parkir.

🔮 Pengembangan Selanjutnya

Beberapa pengembangan yang dapat dilakukan:

📱 Peningkatan tampilan responsive smartphone

🔔 Notifikasi otomatis

🎫 QR Code pada tiket parkir

📷 Pengenalan nomor plat kendaraan

💳 Integrasi payment gateway

📧 Notifikasi email reservasi

📱 Notifikasi WhatsApp

📈 Laporan transaksi berdasarkan tanggal

🖨️ Dukungan printer thermal

👨‍💻 Developer

Zoo Parking

Sistem Informasi Parkir Kebun Binatang berbasis web.

📄 Lisensi

Project ini dibuat untuk keperluan pembelajaran, tugas, dan pengembangan sistem informasi parkir.

Silakan dikembangkan dan disesuaikan dengan kebutuhan.
