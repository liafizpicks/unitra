# UNITRA — Website Katalog Mobil Bekas

Website statis responsif untuk GitHub Pages. Fitur: katalog harga, pencarian/filter, detail unit, status tersedia/terjual, dan tombol WhatsApp otomatis.

## Publikasi di GitHub Pages
1. Masuk ke https://github.com dan buat repository baru bernama `unitra`.
2. Pilih **Public** jika memakai GitHub Free.
3. Di repository, pilih **Add file → Create new file**, beri nama `index.html`, lalu tempel isi file `index.html` dari paket ini dan klik **Commit changes**. (Atau unggah semua file dalam ZIP setelah diekstrak.)
4. Buka **Settings → Pages**.
5. Di bagian **Build and deployment**, pilih **Deploy from a branch**.
6. Pilih branch `main`, folder `/(root)`, lalu klik **Save**.
7. Tunggu proses publikasi. URL umumnya `https://USERNAME.github.io/unitra/`, ganti `USERNAME` dengan username GitHub milikmu. Publikasi pertama bisa memerlukan beberapa menit.

Panduan resmi GitHub: https://docs.github.com/en/pages/quickstart

## Nomor WhatsApp
Sudah diset di `index.html`:
`const WHATSAPP_NUMBER = "628156148016";`
Nomor 08156148016 dikonversi ke format internasional untuk tautan WhatsApp.

## Mengubah stok, harga, dan status
Di `index.html`, cari `const UNITS = [`.
- `price`: angka rupiah tanpa titik, misalnya `85000000`
- `status`: `"Tersedia"` atau `"Terjual"`
- `description`: deskripsi unit
- `year`, `fuel`, `transmission`, `category`: spesifikasi unit

Untuk menambah unit, salin salah satu objek unit di dalam daftar, tempel sebelum penutup `];`, lalu ubah semua datanya. Pastikan setiap unit memiliki `id` yang unik.

## Memasukkan foto asli kendaraan
Buat folder `assets` di repository dan unggah foto asli, misalnya `assets/colt-diesel.jpg`. Ubah `image: ""` pada data unit menjadi `image: "assets/colt-diesel.jpg"`. Gunakan foto unit yang benar-benar dijual dan punya izin untuk dipublikasikan. Jika foto belum diisi, situs akan menampilkan ilustrasi placeholder.

## Sebelum dibagikan ke calon pembeli
- Ganti placeholder dengan foto asli unit.
- Pastikan harga Gran Max Rp109.000.000 sudah sesuai persetujuan pemilik sebelum dipublikasikan.
- Pastikan stok/status dan deskripsi akurat.
- Konfirmasi kondisi, dokumen, pajak/KIR, dan ketersediaan sebelum transaksi.
- GitHub Pages merupakan situs publik; jangan unggah STNK, KTP, alamat pribadi, atau dokumen sensitif.
