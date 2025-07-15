---
layout: post
title: "Bootstrap"
---


Berikut adalah materi lengkap tentang **Bootstrap** :

# 📚 Bootstrap

**Bootstrap** adalah framework CSS paling populer yang digunakan untuk membangun tampilan website modern dan responsif dengan cepat. Dikembangkan oleh tim Twitter, Bootstrap menyediakan berbagai **komponen siap pakai** seperti tombol, form, navbar, grid, dan lainnya.

---

## 🧰 Kelebihan Bootstrap
<div class="bubble">
- ✅ Responsif di semua ukuran layar (mobile-first)  
</div>
<div class="bubble">
- ✅ Hemat waktu karena komponen sudah tersedia  
</div>
<div class="bubble">
- ✅ Dokumentasi lengkap & komunitas luas  
</div>
<div class="bubble">
- ✅ Mendukung customisasi dengan class bawaan  
</div>

---

## 📦 Cara Menggunakan Bootstrap

### 🔗 1. Menggunakan CDN (Online)

Tambahkan baris ini di dalam `<head>` file HTML:

```
<!-- Bootstrap 5 CDN -->
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
```

### 💾 2. Unduh File Manual
<div class="bubble">
* Kunjungi [getbootstrap.com](https://getbootstrap.com)
</div>
<div class="bubble">
* Klik “Download”
</div>
<div class="bubble">
* Hubungkan file CSS & JS ke dokumen HTML
</div>

---

## 🧱 Struktur Grid Sistem (Layout)

Bootstrap menggunakan sistem **grid 12 kolom**. Contoh penggunaan:

```
<div class="container">
  <div class="row">
    <div class="col-4">Kolom 1</div>
    <div class="col-4">Kolom 2</div>
    <div class="col-4">Kolom 3</div>
  </div>
</div>
```
<div class="bubble">
📌 *Gunakan `.container` untuk membungkus konten, dan `.row` sebagai baris sebelum `.col-*`.*
</div>
---

## 🧩 Komponen Dasar Bootstrap

### 1. 🔘 Tombol

```
<button class="btn btn-primary">Tombol Biru</button>
<button class="btn btn-success">Tombol Hijau</button>
<button class="btn btn-danger">Hapus</button>
```

---

### 2. 📥 Formulir

```
<form>
  <div class="mb-3">
    <label for="email" class="form-label">Email:</label>
    <input type="email" class="form-control" id="email">
  </div>
  <button type="submit" class="btn btn-primary">Kirim</button>
</form>
```

---

### 3. 📌 Alert

```
<div class="alert alert-warning" role="alert">
  Ini adalah peringatan!
</div>
```

---

## 📱 Responsivitas

Gunakan class untuk mengatur tampilan berdasarkan ukuran layar:
<div class="bubble">
* `d-none d-md-block`: Elemen hanya tampil di layar **medium ke atas**
</div>
<div class="bubble">
* `col-sm-6 col-md-4`: Ukuran kolom **berubah sesuai lebar layar**
</div>

---

## 🎯 Tips Styling Cepat

Berikut adalah class-class utility yang sering digunakan:
<div class="bubble">
* `text-center`: Teks rata tengah
</div>
<div class="bubble">
* `mt-3`, `mb-2`: Margin atas 3, margin bawah 2
</div>
<div class="bubble">
* `bg-primary`: Latar belakang biru
</div>
<div class="bubble">
* `text-white`: Teks berwarna putih
</div>
<div class="bubble">
* `rounded`: Sudut elemen melengkung
</div>

---

## 🔚 Kesimpulan

Dengan **Bootstrap**, kamu bisa membuat tampilan website yang rapi, modern, dan profesional **tanpa harus menulis CSS dari nol**. Cukup pahami:
<div class="bubble">
* Grid System
</div>
<div class="bubble">
* Komponen Dasar
</div>
<div class="bubble">
* Class Utility
</div>

Maka proses pengembangan website akan jauh lebih cepat dan efisien!

```