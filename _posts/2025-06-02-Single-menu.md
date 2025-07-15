---
layout: post
title: "Single Menu"
---

Berikut adalah materi lengkap tentang **Single Menu** :


# 📌 Apa Itu Single Menu?

**Single Menu** adalah jenis antarmuka interaktif yang hanya memperbolehkan pengguna memilih satu aksi atau satu opsi dari beberapa pilihan yang tersedia. Menu ini umum digunakan dalam aplikasi web, desktop, maupun mobile — terutama saat pengguna perlu membuat **pilihan eksklusif**.

---

## 🧩 Jenis-Jenis Komponen Single Menu

### 1. 🎯 Radio Button

**Radio Button** digunakan ketika hanya **satu opsi** yang boleh dipilih dari sekumpulan opsi.

**Kapan digunakan?**
<div class="bubble">
- Pemilihan jenis kelamin  
</div>
<div class="bubble">
- Memilih metode pengiriman  
</div>

**Contoh HTML:**

```
<p>Jenis Kelamin:</p>
<input type="radio" name="gender" value="pria" id="pria">
<label for="pria">Pria</label>
<input type="radio" name="gender" value="wanita" id="wanita">
<label for="wanita">Wanita</label>
```

---

### 2. 🟢 Toggle Button

**Toggle Button** adalah tombol yang dapat mengubah status antara **aktif dan tidak aktif** (on/off).

**Fungsi:**
<div class="bubble">
* Mengaktifkan atau menonaktifkan fitur
</div>
<div class="bubble">
* Memberi pengalaman visual seperti saklar
</div>

**Contoh HTML:**

```
<button onclick="this.classList.toggle('aktif')">Toggle Fitur</button>
```

---

### 3. ☑️ Checkbox

**Checkbox** memungkinkan pengguna memilih **lebih dari satu opsi** secara bersamaan.

**Penggunaan Umum:**
<div class="bubble">
* Memilih hobi
</div>
<div class="bubble">
* Memilih layanan tambahan
</div>

**Contoh HTML:**

```
<p>Hobi:</p>
<input type="checkbox" id="membaca" name="hobi" value="Membaca">
<label for="membaca">Membaca</label>
<input type="checkbox" id="musik" name="hobi" value="Musik">
<label for="musik">Musik</label>
```

---

### 4. 📋 Dropdown (Select Menu)

**Dropdown** menyajikan opsi dalam bentuk daftar tarik-turun (**combo box**) yang hemat ruang.

**Keunggulan:**
<div class="bubble">
* Cocok untuk daftar panjang (misalnya daftar kota)
</div>
<div class="bubble">
* Menjaga antarmuka tetap rapi
</div>

**Contoh HTML:**

```
<label for="kota">Pilih Kota:</label>
<select name="kota" id="kota">
  <option value="medan">Medan</option>
  <option value="makassar">Makassar</option>
  <option value="bali">Bali</option>
</select>
```

---

## 📊 Tabel Perbandingan Komponen
Berikut adalah isi perbandingan **komponen Single Menu** yang sudah dirapikan **tanpa menggunakan tabel**, agar cocok untuk ditampilkan di markdown blog (misalnya di Jekyll):

---

## 📊 Perbandingan Komponen Single Menu

### 🎯 Radio Button

* **Pilihan Tunggal:** ✅ Ya
* **Pilihan Ganda:** ❌ Tidak
* **Bentuk Visual:** Lingkaran (bulat)
* **Contoh Penggunaan:** Memilih jenis kelamin, metode pengiriman

---

### ☑️ Checkbox

* **Pilihan Tunggal:** ❌ Tidak
* **Pilihan Ganda:** ✅ Ya
* **Bentuk Visual:** Kotak centang
* **Contoh Penggunaan:** Memilih hobi, layanan tambahan

---

### 📋 Dropdown (Select Menu)

* **Pilihan Tunggal:** ✅ Ya
* **Pilihan Ganda:** ❌ Tidak (kecuali dikustomisasi)
* **Bentuk Visual:** Daftar tarik-turun (combo box)
* **Contoh Penggunaan:** Memilih kota, negara, kategori

---

### 🟢 Toggle Button

* **Pilihan Tunggal / Ganda:** Bisa salah satu, tergantung konteks
* **Pilihan Ganda:** Bergantung penggunaan
* **Bentuk Visual:** Tombol geser atau switch
* **Contoh Penggunaan:** Mengaktifkan fitur, dark mode, pengaturan cepat

---

## 🔚 Kesimpulan

Setiap komponen **Single Menu** memiliki fungsinya masing-masing tergantung konteks aplikasi:
<div class="bubble">
* **Radio Button**: untuk pilihan tunggal
</div>
<div class="bubble">
* **Toggle Button**: untuk fitur aktif/nonaktif
</div>
<div class="bubble">
* **Checkbox**: untuk pilihan ganda
</div>
<div class="bubble">
* **Dropdown**: untuk pilihan tunggal dalam format ringkas
</div>

```


