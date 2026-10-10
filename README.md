# AR Preventive Maintenance — Demo

File: `index.html` (app), `jsQR.js` + `qrcode.js` (library lokal), `demo-sheet.png` / `demo-sheet-A4.pdf` (lembar target), `qr-*.png` (QR saja).

## Deploy ke GitHub Pages
1. Upload semua file (kecuali zip) ke repo, root folder.
2. Settings → Pages → Source: *Deploy from a branch* → `main` / `(root)` → Save.
3. Tunggu ±1 menit, buka `https://<username>.github.io/<repo>/` di HP (wajib HTTPS agar kamera jalan).

## Cara coba
1. Buka `demo-sheet-A4.pdf` untuk dicetak (skala 100%), atau tampilkan `demo-sheet.png` fullscreen di laptop/monitor.
2. Buka link di HP, izinkan kamera, arahkan ke lembar dari jarak ±25–35 cm sampai seluruh lembar masuk layar.
3. Callout 1–6 muncul menempel di kotak bagian mesin. Tap untuk isi checksheet.

## Admin: mesin baru & cetak QR
- Tombol **Admin** → *+ Mesin baru*: isi kode, nama, ukuran QR (cm), lalu tiap titik inspeksi (nama, x/y dalam cm dari **pusat QR**, daftar item). Preview posisi tampil langsung.
- **Unduh QR (siap cetak)** menghasilkan PNG 300 dpi dengan ukuran fisik persis sesuai input. Cetak skala 100% — kalau ukuran cetak beda, posisi callout meleset.
- Konfigurasi tersimpan di browser perangkat itu. Agar semua tablet/HP memakai mesin yang sama: **Ekspor machines.json** → taruh di root repo (sejajar index.html) → commit. Aplikasi memuat file itu otomatis.
- Format item checksheet: satu baris per item. Item OK/NG: `Level oli normal`. Item angka: `Suhu oli | 35 | 55 | °C`.
