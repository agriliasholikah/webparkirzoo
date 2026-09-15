
🦁 Zoo Parking --- Sistem Informasi Parkir Kebun Binatang
Zoo Parking adalah aplikasi web untuk mengelola sistem parkir
kendaraan di area kebun binatang. Sistem ini membantu
pelanggan/pengunjung, petugas, admin, dan owner dalam proses
reservasi, pengelolaan kendaraan, area parkir, pembayaran, monitoring,
dan laporan transaksi.

🔗 Link Project
🌐 Website Zoo Parking: https://zooparkir.infinityfree.me/

🎨 Wireframe / Mockup UI, UX Design, Flowchart/User Flow, ERD &
Basis Data: https://agriliasholikah.github.io/mockupui/

💻 Repository GitHub:
https://github.com/agriliasholikah/webparkirzoo

📌 Tentang Project
Zoo Parking merupakan sistem informasi manajemen parkir berbasis web
yang digunakan untuk membuat proses parkir lebih mudah, cepat, dan
terorganisir.

Sistem memiliki beberapa peran pengguna:

Role Fungsi

👨‍💼 Admin Mengelola user, tarif, area parkir,
dan melihat log aktivitas.

👮 Petugas Mengelola kendaraan masuk/keluar,
parkir umum, reservasi, pembayaran,
karcis, dan struk.

📊 Owner Melihat rekap dan laporan transaksi
parkir serta reservasi.

✨ Fitur Utama
👨‍💼 Admin
Dashboard admin

Melihat jumlah kendaraan parkir

Melihat kapasitas dan slot area parkir

Mengelola area parkir

Menambah dan mengubah area parkir

Mengatur kapasitas area parkir

Mengatur tarif kendaraan

Mengelola user

Mengatur role user: Admin, Owner, Petugas, dan Pelanggan

Melihat log aktivitas sistem

👮 Petugas
Dashboard petugas

Parkir umum

Input kendaraan masuk

Input nomor plat, jenis kendaraan, warna, dan pemilik

Memilih area parkir

Mengecek kapasitas area

Mencegah kendaraan masuk jika area penuh

Kendaraan keluar

Menghitung biaya parkir

Pembayaran Tunai, Non Tunai, dan QRIS

Cetak karcis parkir umum

Konfirmasi reservasi online

Cetak karcis khusus reservasi

Pembayaran kendaraan reservasi

Cetak struk pembayaran

Melihat riwayat transaksi

👤 Pelanggan / Pengunjung
Registrasi akun

Login

Melihat ketersediaan area parkir

Melakukan reservasi parkir online

Mengisi nama pemesan

Mengisi nomor plat

Memilih jenis kendaraan

Memilih area parkir

Mendapatkan kode booking

Melihat status reservasi

Melihat riwayat reservasi sendiri

📊 Owner
Dashboard owner

Melihat rincian transaksi parkir

Melihat riwayat parkir harian

Melihat riwayat reservasi

Rekap laporan

Filter laporan berdasarkan periode

Pilihan periode: bulan ini, bulan lalu, atau semua data

Cetak / PDF laporan

🏠 Halaman Utama
Informasi Zoo Parking

Status ketersediaan parkir

Statistik ketersediaan area

Informasi tarif

Panduan parkir

FAQ

Ulasan dan rating pengunjung

Akses login petugas/admin

🔄 Alur Sistem
Parkir Umum
Kendaraan Datang
       ↓
Input Data Kendaraan
       ↓
Pilih Area Parkir
       ↓
Cek Kapasitas
       ↓
Kapasitas Tersedia?
   ↓             ↓
  Ya           Tidak
   ↓             ↓
Kendaraan      Pesan Error
Masuk
   ↓
Cetak Karcis
   ↓
Kendaraan Parkir
   ↓
Kendaraan Keluar
   ↓
Hitung Biaya
   ↓
Pilih Metode Pembayaran
   ↓
Pembayaran
   ↓
Cetak Struk
   ↓
Transaksi Selesai
Reservasi Online
Pelanggan
   ↓
Login / Registrasi
   ↓
Reservasi Online
   ↓
Pilih Kendaraan & Area
   ↓
Kode Booking
   ↓
Kendaraan Datang
   ↓
Petugas Validasi Kode Booking
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
Reservasi Selesai
💰 Sistem Tarif Parkir
Tarif disimpan pada tabel tb_tarif berdasarkan jenis kendaraan.

Contoh:

Jenis Kendaraan Tarif per Jam

Motor Rp5.000
Mobil Rp10.000
Lainnya Mengikuti konfigurasi sistem

Sistem juga menyediakan tarif maksimal sehingga biaya parkir dapat
dibatasi sesuai konfigurasi.

🅿️ Manajemen Area Parkir
Setiap area memiliki:

Nama area

Kapasitas

Jumlah kendaraan yang sedang terisi

Ketika kendaraan masuk:

Terisi + 1
Ketika kendaraan keluar:

Terisi - 1
Sistem melakukan pengecekan kapasitas agar kendaraan tidak masuk ketika
area sudah penuh.

🗄️ Basis Data
Project menggunakan MySQL.

Tabel yang terdeteksi digunakan oleh sistem:

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
Menyimpan data akun pengguna dan role.

Field utama yang digunakan antara lain:

id_user

nama_lengkap

username

email

password

role

Role yang digunakan sistem mencakup:

admin
petugas
owner
pelanggan
pengunjung
user
tb_kendaraan
Menyimpan data kendaraan:

id_kendaraan

plat_nomor

jenis_kendaraan

warna

pemilik

id_user

tb_area_parkir
Menyimpan data area parkir:

id_area

nama_area

kapasitas

terisi

tb_parkir
Menyimpan transaksi kendaraan:

id_parkir

id_kendaraan

id_area

id_reservasi

id_user

waktu_masuk

waktu_keluar

status

biaya_total

metode_pembayaran

denda

Status parkir:

parkir
selesai
tb_reservasi
Menyimpan reservasi pelanggan:

id_reservasi

kode_booking

nama_pemesan

plat_nomor

id_area

jenis_kendaraan

status

tgl_reservasi

warna_kendaraan

Status reservasi:

booked
digunakan
selesai
batal
tb_tarif
Menyimpan konfigurasi tarif:

jenis_kendaraan

tarif_per_jam

tarif_maksimal

tb_log_aktivitas
Mencatat aktivitas pengguna dalam sistem, termasuk user yang melakukan
aktivitas, jenis aktivitas, dan waktu aktivitas.

tb_ulasan
Digunakan untuk menyimpan ulasan/rating pengunjung pada halaman utama.

tb_faq
Menyimpan pertanyaan dan jawaban FAQ yang ditampilkan pada halaman
utama.

📂 Struktur Project
Berdasarkan file project yang diberikan, struktur sebenarnya adalah:

sistem_parkir/
│
├── admin_log.php
├── admin_tarif.php
├── admin_user.php
│
├── cetak_karcis.php
├── cetak_karcis_reservasi.php
├── cetak_struk.php
│
├── dashboard_admin.php
├── dashboard_owner.php
├── dashboard_petugas.php
├── dashboard_user.php
│
├── get_stats_parkir.php
├── index.php
├── koneksi.php
├── login.php
├── logout.php
├── pembayaran_berhasil.php
├── qr.jpeg
└── register.php
Struktur di atas disesuaikan dengan file project yang digunakan, bukan
struktur folder contoh.

🛠️ Teknologi
PHP

MySQL

HTML5

CSS3

JavaScript

Bootstrap 5

Font Awesome

Chart.js

SweetAlert2

XAMPP untuk local development

InfinityFree untuk hosting

🎨 Dokumentasi UI/UX
Dokumentasi perancangan sistem tersedia pada:

👉 https://agriliasholikah.github.io/mockupui/

Dokumentasi meliputi:

Wireframe / Mockup UI

UX Design (User Experience)

Flowchart / User Flow

ERD (Entity Relationship Diagram)

Basis Data / Struktur Tabel

🚀 Cara Menjalankan Secara Lokal
1. Siapkan XAMPP
Aktifkan:

Apache
MySQL
2. Letakkan Project
Masukkan folder project ke:

xampp/htdocs/sistem_parkir/
3. Buat Database
Buka:

http://localhost/phpmyadmin
Buat database sesuai konfigurasi pada koneksi.php.

4. Konfigurasi Database
Sesuaikan:

$host
$user
$password
$database
pada:

koneksi.php
5. Jalankan
Buka:

http://localhost/sistem_parkir/
🌐 Hosting
Project dapat digunakan pada hosting yang mendukung PHP dan MySQL.

Website yang digunakan:

https://zooparkir.infinityfree.me/

Untuk deployment, konfigurasi koneksi database harus disesuaikan dengan
database hosting.

Jangan menyimpan password database asli pada repository GitHub publik.

🔐 Keamanan
Beberapa hal yang perlu diperhatikan:

Gunakan password database yang aman.

Jangan menyimpan credential database asli di repository publik.

Validasi input pengguna.

Gunakan autentikasi session.

Batasi akses berdasarkan role.

Gunakan prepared statement untuk query database.

Jangan menampilkan informasi error database secara langsung kepada
pengguna.

🎯 Tujuan Project
Zoo Parking dibuat untuk:

Mempermudah pengelolaan parkir.

Mengurangi pencatatan manual.

Mempermudah petugas mengelola kendaraan.

Mengetahui kapasitas area parkir.

Mempermudah reservasi parkir online.

Mempermudah proses pembayaran.

Menyediakan informasi dan laporan transaksi.

Menyimpan data parkir secara terstruktur.

🔮 Pengembangan Selanjutnya
Beberapa pengembangan yang dapat dilakukan:

📱 Tampilan lebih responsif untuk smartphone

🔔 Notifikasi reservasi

🎫 QR Code pada tiket

📷 Pengenalan plat nomor kendaraan

💳 Payment gateway

📧 Notifikasi email

📱 Notifikasi WhatsApp

📈 Laporan transaksi yang lebih lengkap

🖨️ Dukungan printer thermal

👨‍💻 Developer
Zoo Parking

Sistem Informasi Parkir Kebun Binatang berbasis web.

📄 Lisensi
Project ini dibuat untuk keperluan pembelajaran, tugas, dan
pengembangan sistem informasi parkir
