# webparkirzoo# 🦁 Zoo Parking — Sistem Informasi Parkir Kebun Binatang

**Zoo Parking** adalah aplikasi web untuk mengelola sistem parkir kendaraan di area kebun binatang. Aplikasi ini dibuat untuk membantu petugas dan admin dalam mengelola kendaraan masuk dan keluar, area parkir, reservasi online, pembayaran, serta riwayat transaksi parkir.

## 📌 Tentang Project

Sistem ini menyediakan pengelolaan parkir secara terkomputerisasi sehingga proses pencatatan kendaraan dan transaksi parkir menjadi lebih mudah, cepat, dan terorganisir.

Aplikasi memiliki dua jenis pengguna utama:

* 👨‍💼 **Admin** — mengelola data sistem dan area parkir.
* 👮 **Petugas** — mengelola kendaraan masuk, kendaraan keluar, reservasi, dan pembayaran.

---

## ✨ Fitur Utama

### 👨‍💼 Admin

* Dashboard admin
* Melihat jumlah kendaraan yang sedang parkir
* Melihat kapasitas area parkir
* Mengelola area parkir
* Menambah area parkir
* Mengubah data area parkir
* Mengatur kapasitas area parkir
* Melihat informasi parkir

### 👮 Petugas

* Dashboard petugas
* Parkir umum
* Pencatatan kendaraan masuk
* Pencatatan kendaraan keluar
* Pencarian kendaraan berdasarkan nomor plat
* Pengelolaan parkir berdasarkan area
* Pengelolaan reservasi online
* Konfirmasi reservasi
* Pencatatan kendaraan reservasi
* Pembayaran parkir
* Pilihan metode pembayaran:

  * Tunai
  * Non Tunai
  * QRIS
* Cetak karcis parkir
* Cetak karcis khusus reservasi
* Cetak struk pembayaran
* Riwayat transaksi parkir

### 🎫 Reservasi Online

Sistem mendukung reservasi parkir secara online.

Alur reservasi:

```text
Pelanggan melakukan reservasi
          ↓
   Mendapat kode booking
          ↓
   Petugas menerima kendaraan
          ↓
Petugas memasukkan kode booking
          ↓
   Reservasi dikonfirmasi
          ↓
     Cetak karcis
          ↓
      Kendaraan parkir
          ↓
   Kendaraan keluar
          ↓
      Pembayaran
          ↓
    Cetak struk
```

---

## 💰 Sistem Tarif Parkir

Tarif parkir dapat dibedakan berdasarkan jenis kendaraan.

Contoh:

| Jenis Kendaraan |                        Tarif |
| --------------- | ---------------------------: |
| Motor           |                      Rp5.000 |
| Mobil           |                     Rp10.000 |
| Lainnya         | Mengikuti konfigurasi sistem |

Sistem juga dapat menggunakan tarif maksimal sehingga biaya parkir tidak melebihi batas yang telah ditentukan.

---

## 🅿️ Manajemen Area Parkir

Setiap area parkir memiliki:

* Nama area
* Kapasitas
* Jumlah kendaraan yang sedang menggunakan area

Sistem akan memperbarui jumlah kendaraan ketika:

**Kendaraan masuk:**

```text
Terisi + 1
```

**Kendaraan keluar:**

```text
Terisi - 1
```

Sistem juga mencegah kendaraan masuk apabila kapasitas area sudah penuh.

---

## 🗄️ Database

Project ini menggunakan **MySQL**.

Beberapa tabel utama yang digunakan:

```text
tb_user
tb_kendaraan
tb_parkir
tb_area_parkir
tb_reservasi
tb_tarif
```

### `tb_parkir`

Digunakan untuk menyimpan transaksi kendaraan yang masuk dan keluar.

Contoh data yang disimpan:

* ID parkir
* Kendaraan
* Area parkir
* Reservasi
* Petugas
* Waktu masuk
* Waktu keluar
* Status parkir
* Total biaya
* Metode pembayaran
* Denda

### `tb_kendaraan`

Menyimpan informasi kendaraan:

* Nomor plat
* Jenis kendaraan
* Warna
* Pemilik

### `tb_area_parkir`

Menyimpan informasi area parkir:

* Nama area
* Kapasitas
* Jumlah kendaraan yang sedang parkir

### `tb_reservasi`

Menyimpan data reservasi:

* Kode booking
* Nama pemesan
* Nomor plat
* Jenis kendaraan
* Area parkir
* Tanggal reservasi
* Status reservasi

### `tb_tarif`

Menyimpan tarif berdasarkan jenis kendaraan.

---

## 🛠️ Teknologi yang Digunakan

Project ini dibuat menggunakan:

* **PHP**
* **MySQL**
* **HTML5**
* **CSS3**
* **JavaScript**
* **Bootstrap** *(jika digunakan pada project)*
* **XAMPP / Laragon** untuk local development
* **InfinityFree** untuk hosting

---

## 📂 Struktur Project

Struktur file utama project:

```text
Zoo-Parking/
│
├── koneksi.php
├── login.php
│
├── dashboard_admin.php
├── dashboard_petugas.php
│
├── cetak_karcis.php
├── cetak_karcis_reservasi.php
├── cetak_struk.php
│
├── admin/
│   └── ...
│
├── assets/
│   ├── css/
│   ├── js/
│   └── images/
│
└── database/
    └── zoo_parking.sql
```

> Struktur folder dapat berbeda tergantung versi project yang digunakan.

---

## 🔐 Sistem Login & Hak Akses

Sistem menggunakan autentikasi berbasis session.

### Admin

Admin memiliki akses untuk mengelola data dan area parkir.

```text
Login
  ↓
Dashboard Admin
  ↓
Manajemen Area Parkir
  ↓
Pengelolaan Sistem
```

### Petugas

Petugas memiliki akses untuk mengelola operasional parkir.

```text
Login
  ↓
Dashboard Petugas
  ↓
Parkir Umum / Reservasi
  ↓
Kendaraan Masuk
  ↓
Kendaraan Keluar
  ↓
Pembayaran
  ↓
Cetak Struk
```

---

## 🔄 Alur Parkir Umum

```text
Kendaraan Datang
       ↓
Input Nomor Plat
       ↓
Pilih Jenis Kendaraan
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
Transaksi Selesai
```

---

## 🔄 Alur Parkir Reservasi

```text
Reservasi Online
       ↓
Kode Booking
       ↓
Kendaraan Datang
       ↓
Petugas Memasukkan Kode Booking
       ↓
Validasi Reservasi
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
```

---

## 📊 Status Data

### Status Parkir

```text
parkir
selesai
```

### Status Reservasi

```text
booked
digunakan
selesai
batal
```

---

## 🚀 Cara Menjalankan Project

### 1. Clone Repository

```bash
git clone https://github.com/USERNAME/NAMA-REPOSITORY.git
```

Masuk ke folder project:

```bash
cd NAMA-REPOSITORY
```

### 2. Jalankan Web Server

Jika menggunakan XAMPP:

```text
htdocs/
└── Zoo-Parking/
```

Kemudian aktifkan:

* Apache
* MySQL

### 3. Buat Database

Buka:

```text
http://localhost/phpmyadmin
```

Buat database baru, misalnya:

```text
zoo_parking
```

Kemudian import file:

```text
database/zoo_parking.sql
```

### 4. Konfigurasi Database

Sesuaikan file:

```text
koneksi.php
```

Contoh konfigurasi:

```php
$host = "localhost";
$user = "root";
$password = "";
$database = "zoo_parking";
```

Sesuaikan username, password, dan nama database dengan konfigurasi komputer/server.

### 5. Jalankan Project

Buka browser:

```text
http://localhost/Zoo-Parking/
```

---

## 🌐 Hosting

Project dapat di-host menggunakan hosting yang mendukung:

* PHP
* MySQL
* phpMyAdmin
* File Manager

Contoh hosting yang dapat digunakan:

**InfinityFree**

Setelah upload file project, sesuaikan konfigurasi `koneksi.php` dengan database hosting.

> Jangan upload password database asli ke repository GitHub publik.

---

## 🔒 Keamanan

Beberapa hal yang perlu diperhatikan sebelum project digunakan pada production:

* Gunakan password database yang aman.
* Jangan menyimpan credential database di repository publik.
* Gunakan prepared statement untuk query database.
* Validasi input pengguna.
* Gunakan session authentication untuk halaman yang membutuhkan login.
* Batasi hak akses berdasarkan role.
* Jangan menampilkan informasi error database kepada pengguna secara langsung.

---

## 📸 Tampilan Aplikasi

Tambahkan screenshot aplikasi pada folder:

```text
screenshots/
├── login.png
├── dashboard-admin.png
├── dashboard-petugas.png
├── parkir-umum.png
├── reservasi.png
├── pembayaran.png
└── cetak-struk.png
```

Kemudian tampilkan di README:

```markdown
![Login](screenshots/login.png)

![Dashboard Petugas](screenshots/dashboard-petugas.png)

![Pembayaran](screenshots/pembayaran.png)
```

---

## 🎯 Tujuan Project

Project **Zoo Parking** dibuat untuk:

* Mempermudah pengelolaan parkir.
* Mengurangi pencatatan manual.
* Mempermudah petugas dalam mengelola kendaraan.
* Mengetahui kapasitas area parkir.
* Mengelola reservasi parkir.
* Mempermudah proses pembayaran.
* Menyimpan riwayat transaksi secara terstruktur.

---

## 🔮 Pengembangan Selanjutnya

Beberapa fitur yang dapat dikembangkan:

* 📱 Tampilan responsive untuk smartphone
* 📊 Grafik statistik parkir
* 🔔 Notifikasi otomatis
* 🎫 QR Code pada tiket parkir
* 📷 Pengenalan plat nomor kendaraan
* 💳 Integrasi payment gateway
* 📧 Notifikasi email reservasi
* 📱 Notifikasi WhatsApp
* 📈 Laporan transaksi berdasarkan tanggal
* 🖨️ Dukungan printer thermal
* 👥 Manajemen pengguna dan role yang lebih lengkap

---

## 👨‍💻 Developer

**Zoo Parking**

Sistem Informasi Parkir Kebun Binatang berbasis web.

---

## 📄 Lisensi

Project ini dibuat untuk keperluan **pembelajaran, tugas, dan pengembangan sistem informasi parkir**.

Silakan dikembangkan dan disesuaikan dengan kebutuhan.
