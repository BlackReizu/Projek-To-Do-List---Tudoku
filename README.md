# Tudoku - Aplikasi Todo List

Aplikasi Todo List yang dibangun menggunakan Laravel. Aplikasi ini dirancang untuk mencatat tugas harian dengan antarmuka yang bersih, fungsionalitas yang cepat, dan fitur manajemen tugas yang praktis.

## Fitur Utama

- Manajemen Tugas: Tambah, edit, hapus, dan tandai tugas selesai.
- Smart Progress Dashboard: Menampilkan ringkasan tugas yang selesai dan belum selesai beserta persentase progres harian secara visual.
- Quick Add & Keyboard Shortcut: Gunakan tombol garis miring ( / ) atau kombinasi Ctrl+K untuk langsung memfokuskan kursor ke input tugas baru.
- Prioritas & Tenggat Waktu: Atur tingkat prioritas (Rendah, Sedang, Tinggi) dan batas waktu penyelesaian untuk setiap tugas.
- Filter Tugas: Urutkan tampilan tugas berdasarkan status aktif, selesai, prioritas tinggi, atau tugas yang melewati tenggat waktu.

## Persyaratan Sistem

Pastikan sistem Anda telah terpasang perangkat lunak berikut sebelum menjalankan aplikasi:

- PHP versi 8.1 atau yang lebih baru
- Composer
- Database (MySQL, PostgreSQL, atau SQLite)

## Cara Instalasi dan Eksekusi

Berikut adalah langkah-langkah untuk menjalankan aplikasi ini di komputer Anda.

### 1. Persiapan Direktori
Buka terminal atau command prompt, lalu arahkan (cd) ke dalam direktori proyek aplikasi ini.

### 2. Instalasi Dependensi
Jalankan perintah berikut untuk mengunduh semua pustaka PHP yang dibutuhkan oleh Laravel:

```bash
composer install
```

### 3. Pengaturan Konfigurasi (Environment)
Buat salinan file konfigurasi bawaan agar aplikasi memiliki pengaturan lokalnya sendiri. Jalankan perintah:

```bash
cp .env.example .env
```
*(Catatan: Untuk pengguna Windows Command Prompt, Anda bisa menggunakan perintah `copy .env.example .env`)*

### 4. Pembuatan Application Key
Buat kunci enkripsi unik untuk keamanan aplikasi Anda dengan perintah:

```bash
php artisan key:generate
```

### 5. Pengaturan Database
Buka file `.env` yang baru saja dibuat menggunakan program teks editor. Cari bagian konfigurasi database (biasanya dimulai dengan teks `DB_CONNECTION`) dan sesuaikan dengan database yang Anda siapkan.

Jika Anda ingin cara yang paling cepat untuk mencoba aplikasi tanpa mengatur server database tambahan, Anda bisa menggunakan basis data SQLite. Caranya, ubah konfigurasi database di file `.env` menjadi persis seperti ini:

```env
DB_CONNECTION=sqlite
```
(Hapus atau berikan tanda pagar `#` pada baris DB_HOST, DB_PORT, DB_DATABASE, DB_USERNAME, dan DB_PASSWORD).

Setelah pengaturan database sesuai, jalankan perintah migrasi untuk membuat tabel-tabel ke dalam database:

```bash
php artisan migrate
```

### 6. Menjalankan Aplikasi
Langkah terakhir, jalankan server pengembangan bawaan dari Laravel dengan perintah:

```bash
php artisan serve
```

Aplikasi sekarang sudah berjalan. Buka web browser Anda dan kunjungi alamat `http://localhost:8000` untuk mulai menggunakan aplikasi.
