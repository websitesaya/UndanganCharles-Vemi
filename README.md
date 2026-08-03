# Undangan Pernikahan Digital — Charles & Vemiresiyani

## 1. Struktur folder
```
index.html        -> halaman undangan utama
generator.html     -> alat pembuat link undangan personal + share WhatsApp
style.css          -> semua styling
script.js          -> semua interaksi (tirai, salju, musik, countdown, galeri, ucapan)
assets/images/     -> taruh semua foto di sini
assets/audio/      -> taruh file lagu di sini
```

## 2. Foto yang perlu Anda tambahkan (wajib, nama file harus sama persis)
Taruh di dalam folder `assets/images/`:
- `Latar.jpg` — foto latar belakang opening screen (bagian bawah foto otomatis digelapkan agar teks terbaca)
- `Mempelai_Pria.jpg` — foto Charles
- `Mempelai_Wanita.jpg` — foto Vemiresiyani
- `Foto1.jpg` s/d `Foto10.jpg` — 10 foto prewedding untuk galeri

**Alur opening screen:** halaman pertama tampil dengan foto `Latar.jpg` + tombol "Buka Undangan".
Setelah tombol diklik, tirai baru muncul menutup lalu terbuka mengungkap undangan — bukan
tampil dari awal.

## 3. Lagu
Taruh file lagu di `assets/audio/` dengan nama persis:
`Westlife - Beautiful in white (Lyrics).mp3`

## 4. Ucapan & Doa bersama (JSONBin)
Supaya ucapan dari semua tamu bisa saling terlihat, buka `script.js` dan isi:
1. Daftar gratis di https://jsonbin.io
2. Buat bin baru dengan isi awal: `[]`
3. Salin **Bin ID** → tempel ke `JSONBIN_BIN_ID`
4. Salin **X-Master-Key** (menu API Keys) → tempel ke `JSONBIN_API_KEY`

Selama kedua nilai itu belum diisi, halaman ucapan akan menampilkan pesan "fitur belum aktif".

## 5. Cek / ubah tanggal & lokasi
Semua detail acara ada langsung di `index.html` (mudah dicari & diedit teks-nya).
Countdown menuju Pemberkatan diatur di `script.js` pada `CONFIG.WEDDING_DATE`.

> Catatan: pada data resepsi Anda menuliskan tahun **2016**, sedangkan pemberkatan **2026**
> pada tanggal yang sama (28 Agustus). Saya asumsikan resepsi juga di **2026** — silakan
> koreksi di bagian "Resepsi" pada `index.html` bila keliru.

Link Google Maps untuk Pemberkatan & Resepsi memakai pencarian otomatis berdasarkan alamat
(karena link maps spesifik belum diberikan). Ganti `href` pada tombol `#mapsPemberkatan` dan
`#mapsResepsi` di `index.html` dengan link Google Maps asli bila sudah ada.

## 6. Cara pakai generator.html
1. Buka `generator.html` di browser
2. Isi "Link Undangan" dengan alamat `index.html` **setelah** di-hosting (contoh: `https://nama-domain.com/index.html`)
3. Isi daftar nama tamu (satu nama per baris)
4. Klik **Buat Link Undangan** → klik **Bagikan via WhatsApp** untuk tiap tamu

## 7. Hosting
Upload seluruh folder ini (termasuk `assets/`) ke hosting statis apa pun, misalnya:
- Netlify / Vercel (drag & drop folder)
- GitHub Pages
- Hosting cPanel biasa

Pastikan struktur folder & nama file tetap sama persis seperti di atas.
