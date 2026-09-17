# DIT

Sistem manajemen absensi, inventory, peminjaman barang, pengajuan maintenance, dan pendukung operasional internal DIT.

## Fitur Utama

- Absensi dan manajemen karyawan
- Inventory barang dan stok
- Peminjaman barang
- Pengajuan maintenance
- Notifikasi email dan OAuth login
- Dashboard admin dan teknisi
- Integrasi Cloudflare Tunnel untuk akses publik sementara

## Struktur Proyek

- `index.php` — halaman login
- `dashboard.php` — dashboard utama
- `inventory.php` — pengelolaan barang dan stok
- `pengajuan.php` — pengajuan peminjaman dan maintenance
- `includes/` — konfigurasi dan helper aplikasi
- `database/` — SQL backup dan struktur database
- `PHPMailer-master/` — library email
- `uploads/` — file upload aplikasi

## Persyaratan

- PHP 8.0+
- MySQL / MariaDB
- Apache atau XAMPP
- Composer

## Setup

1. Clone atau unduh repo ini ke folder web server Anda.
2. Pastikan aplikasi berada di direktori web seperti:
   - `C:/xampp/htdocs/DIT`
3. Import database yang diperlukan dari folder `database/`.
4. Konfigurasi database di file `includes/config.php`.
5. Konfigurasi OAuth dan email pada file yang relevan seperti:
   - `oauth_config.php`
   - `includes/email_config.php`
6. Jalankan aplikasi melalui browser:
   - `http://localhost/DIT/`

## Environment & Keamanan

- Jangan commit credential asli ke repositori publik.
- Gunakan environment variable atau file konfigurasi lokal untuk password dan secret.
- Pastikan file `oauth_config.php` dan email config tidak di-publish tanpa masking secret.

## Deploy / Akses Publik

Untuk akses publik sementara, proyek ini juga dapat di-expose via Cloudflare Tunnel. Sesuaikan URL public serta konfigurasi OAuth dengan URL aktif yang digunakan.

## Lisensi

Proyek ini dilisensikan di bawah MIT License. Lihat file [LICENSE](LICENSE).

## Keamanan

Lihat [SECURITY.md](SECURITY.md) untuk panduan pelaporan keamanan.

## Kontribusi

Pull request disambut. Pastikan perubahan sudah dites dan dokumentasi diperbarui bila diperlukan.
