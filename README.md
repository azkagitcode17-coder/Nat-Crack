# Nat'Crack — CTF Utility Box

Nat'Crack adalah aplikasi web toolkit dekoder, konverter sandi, dan solver otomatis untuk kompetisi Capture The Flag (CTF) dan analisis kriptografi.

---

## 🚀 Panduan Menjalankan Proyek di VS Code (Komputer Lokal)

Jika saat dibuka di browser hanya muncul **layar putih (white screen)**, itu terjadi karena proyek ini menggunakan **React + TypeScript + Vite** yang **tidak bisa** dijalankan langsung dengan klik ganda file `index.html` atau ekstensi **Live Server**.

Ikuti langkah-langkah di bawah ini untuk menjalankannya dengan benar:

### 1. Pastikan Node.js Terinstall
Pastikan komputer Anda sudah terpasang Node.js (versi 18 atau lebih baru).
Cek di terminal:
```bash
node -v
npm -v
```

### 2. Buka Folder Proyek di VS Code
1. Buka aplikasi **VS Code**.
2. Klik menu **File** > **Open Folder...** lalu pilih folder hasil ekstrak / clone proyek ini.

### 3. Buka Terminal Terintegrasi VS Code
- Tekan tombol keyboard: ``Ctrl + ` `` (atau menu **Terminal** > **New Terminal**).

### 4. Install Dependensi (PENTING!)
Folder `node_modules` tidak disertakan saat download. Anda harus menginstallnya terlebih dahulu:
```bash
npm install
```
*Tunggu hingga proses instalasi paket selesai sampai muncul pesan sukses.*

### 5. Jalankan Server Pengembangan (Dev Server)
Ketik perintah berikut di terminal:
```bash
npm run dev
```
Setelah server aktif, akan muncul output:
```text
Nat'Crack Server running on http://0.0.0.0:3000
```

### 6. Buka di Browser
Buka browser Anda (Chrome / Edge / Firefox) dan kunjungi alamat:
```
http://localhost:3000
```
Aplikasi Nat'Crack akan langsung tampil normal tanpa layar putih!

---

## 🛠️ Perintah Tambahan

- **Build untuk Produksi:**
  ```bash
  npm run build
  ```
- **Menjalankan Hasil Build:**
  ```bash
  npm start
  ```
- **Cek Error TypeScript:**
  ```bash
  npm run lint
  ```

---

## ❓ Mengapa Terjadi White Screen?
1. **Membuka lewat Live Server / Klik ganda `index.html`**:
   Browser tidak mengenali syntax TypeScript (`.tsx`) tanpa proses kompilasi Vite. Anda harus menjalankan `npm run dev`.
2. **Belum menjalankan `npm install`**:
   Semua library React, Vite, Tailwind, dan modul kriptografi berada di `node_modules` yang perlu diunduh melalui `npm install`.
3. **Salah Port**:
   Pastikan membuka port **3000** (`http://localhost:3000`), bukan port 5173 atau 5500.
