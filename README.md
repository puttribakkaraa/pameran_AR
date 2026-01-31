# MTM 3D Exhibition AR System

Project ini menghadirkan pengalaman Augmented Reality untuk pameran MTM menggunakan WebAR.

## 📁 Struktur Folder

Pastikan folder `models` berisi file 3D Anda:

```
p:\pameran_mtm_3d\
├── models/
│   ├── Lower Die Finisher.glb  <-- WAJIB ADA
│   └── v8_engine_internals.glb <-- WAJIB ADA
├── index.html
├── qr-codes.html
├── css/...
└── products/...
```

## 🚀 Cara Menjalankan

### 1. Setup Model 3D
Copy file `.glb` Anda ke dalam folder `models/`. Pastikan nama filenya PERSIS seperti di atas.

### 2. Test Lokal
Karena masalah security browser, WebAR/Camera mungkin tidak jalan kalau hanya double-click HTML.
Gunakan extension VS Code **"Live Server"** atau jalankan local server python:
```bash
python -m http.server
```
Lalu buka `localhost:8000` di browser.

### 3. Deploy ke Internet (Gratis)
Agar pengunjung bisa scan QR, website harus online. Gunakan **GitHub Pages**:

1. **Upload ke GitHub**
   - Buat repository baru di GitHub.com
   - Upload semua file project ini ke repository tersebut

2. **Aktifkan GitHub Pages**
   - Buka Settings repository -> **Pages**
   - Source: pilih branch `main` / `master`
   - Save. Tunggu 1-2 menit hingga dapat URL (misal: `https://username.github.io/repo-name`)

3. **Generate QR Code**
   - Setelah dapat URL GitHub Pages, buka `qr-codes.html`
   - Masukkan URL Anda disana (misal: `https://username.github.io/repo-name`)
   - Klik **Generate** dan Download QR Code untuk diprint di poster.

## 📱 Cara Pakai di Pameran
1. Pengunjung scan QR Code di poster.
2. Halaman produk terbuka.
3. Pengunjung klik tombol **View in AR**.
4. Kamera terbuka, arahkan ke meja/lantai untuk menaruh model 3D.
