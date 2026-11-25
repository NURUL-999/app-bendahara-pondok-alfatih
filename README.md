# Alfatih - Bendahara

**Alfatih - Bendahara** adalah aplikasi web pencatatan dan pelaporan keuangan santri yang dirancang dengan antarmuka modern, intuitif, serta sistem multi-peran (**Admin** dan **Wali Santri**).

---

## Fitur Utama

1. **Sistem Autentikasi & Multi-Peran Otomatis**
   - **Login Otomatis Sesuai Peran:** Sistem mengenali hak akses akun secara internal saat pengguna masuk (*Admin* maupun *Wali Santri*).
   - **Create Account:** Pendaftaran akun baru dengan validasi kata sandi minimal 6 karakter serta syarat angka & simbol khusus untuk username Admin.
   - **Reset Password:** Pemulihan kata sandi mandiri menggunakan verifikasi Username dan Nama Lengkap terdaftar.
   - **Mode Demo:** Tombol akses cepat untuk mengecek seluruh fitur aplikasi tanpa perlu mendaftar akun terlebih dahulu.

2. **Hak Akses Tegas (Admin vs Wali Santri)**
   - **Admin:** Memiliki akses penuh pada menu **Beranda**, **Daftar Santri** (tambah/hapus santri satuan maupun massal, cek profil lengkap santri, serta input/edit/hapus catatan transaksi), dan **Hasil Laporan**.
   - **Wali Santri (*Read-Only*):** Hanya dapat memantau perkembangan keuangan khusus milik santri yang namanya sesuai dengan akun yang login, serta mengunduh laporan tanpa bisa mengubah data.

3. **Input & Perhitungan Otomatis**
   - Input nominal **Masuk** dan **Keluar** dilengkapi pemisah ribuan otomatis (titik) dengan batas minimal transaksi **Rp 5.000**.
   - Kolom **Jumlah** terhitung secara otomatis berdasarkan nominal yang diinput.

4. **Hasil Laporan & Ekspor Dokumen (Excel & PDF)**
   - Filter cepat berdasarkan nama santri maupun kolom pencarian tanggal/keterangan.
   - **Export Excel (`.xlsx`)** dan **Export PDF (`.pdf`)** langsung dari browser.
   - Nama file unduhan otomatis menyesuaikan nama **Wali Santri** yang sedang login (misalnya `Galih.pdf` / `Galih.xlsx`).
   - Format cetak PDF dilengkapi bagian tanda tangan **Mengetahui — Muhammad Galih Assyafi** tepat di posisi tengah bawah laporan.

---

## Struktur File Proyek

```text
alfatih-bendahara/
├── index.html      # Struktur utama antarmuka aplikasi (Login, Beranda, Daftar Santri, Hasil Laporan)
├── style.css       # Pengaturan tampilan kustom, animasi, dan tata letak cetak
├── script.js       # Logika aplikasi, manajemen peran, validasi form, dan generator Excel/PDF
└── README.md       # Dokumentasi panduan penggunaan dan deploy aplikasi
```

---

## Akun Pengujian Bawaan

| Peran | Nama Lengkap | Username | Kata Sandi |
| :--- | :--- | :--- | :--- |
| **Admin** | Riski | `riski_123` | `password123` |
| **Wali Santri** | Sahal | `sahal_123` | `password123` |
| **Wali Santri** | Galih | `galih_123` | `password123` |

---

## Cara Menjalankan & Deploy Website

### 1. Menjalankan di Komputer Lokal
1. Pastikan seluruh file (`index.html`, `style.css`, `script.js`) berada dalam satu folder yang sama.
2. Klik dua kali pada file `index.html` untuk membukanya langsung di browser (Chrome, Edge, Firefox, atau Safari).

### 2. Publikasi ke Hosting Online
Karena aplikasi ini berbasis HTML, CSS, dan JavaScript murni tanpa perlu konfigurasi server rumit, Anda dapat langsung mengunggah folder proyek ke layanan hosting berikut:
- **Netlify Drop:** Seret dan lepas folder proyek ke [app.netlify.com/drop](https://app.netlify.com/drop).
- **Vercel / Cloudflare Pages:** Hubungkan repositori atau unggah folder proyek untuk mendapatkan domain gratis.
- **GitHub Pages:** Upload semua file ke repositori GitHub, lalu aktifkan **Pages** pada menu *Settings*.
- **cPanel Hosting:** Unggah seluruh file ke dalam direktori `public_html`.