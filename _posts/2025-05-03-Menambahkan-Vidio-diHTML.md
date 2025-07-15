---
layout: post
title: "Menambahkan Video di HTML"
---

Berikut adalah materi lengkap tentang **Menambahkan Vidio di HTML** :


# 🎬 Menambahkan Video di HTML

Menambahkan video ke dalam website HTML dapat meningkatkan **interaktivitas dan daya tarik pengguna**. Dengan adanya HTML5, kini kamu dapat menyematkan video langsung ke halaman web **tanpa plugin tambahan**.

Artikel ini akan membahas cara menggunakan tag `<video>`, atribut penting, dan praktik terbaik dalam menyisipkan video.

---

## 📌 Prasyarat

Sebelum mulai, pastikan kamu sudah memiliki:
<div class="bubble">
1. File video yang ingin ditampilkan  
</div>
<div class="bubble">
2. Hak atau izin untuk menggunakan video tersebut  
</div>
<div class="bubble">
3. Editor teks seperti VS Code, Sublime Text, atau Notepad++  
</div>

---

## 🔍 Pengenalan Tag `<video>`

HTML5 memperkenalkan tag `<video>` untuk menyematkan video langsung ke dalam halaman web.

Format yang umum digunakan:
<div class="bubble">
- WebM
</div>
<div class="bubble">
- Ogg
</div>

Keuntungan:
<div class="bubble">
- Tidak butuh plugin tambahan
</div>
<div class="bubble">
- Kompatibel di banyak browser modern
</div>

---

## 🧱 Struktur Dasar Tag `<video>`

Berikut adalah contoh struktur dasar untuk menambahkan video:

```
<video width="640" height="360" controls>
  <source src="video-sample.mp4" type="video/mp4">
  <source src="video-sample.webm" type="video/webm">
  Browser kamu tidak mendukung tag video.
</video>
```

📌 Penjelasan:
<div class="bubble">
* width & height: menentukan ukuran player
</div>
<div class="bubble">
* `controls`: menampilkan tombol kontrol (play, pause, volume)
</div>
<div class="bubble">
* `source`: untuk menyisipkan file video
</div>
<div class="bubble">
* Pesan alternatif ditampilkan jika browser tidak mendukung video
</div>

---

## ⚙️ Atribut Penting `<video>`

Berikut beberapa atribut yang bisa digunakan untuk mengatur perilaku video:
<div class="bubble">
* `controls`: Menampilkan kontrol video
</div>
<div class="bubble">
* `autoplay`: Memutar otomatis saat halaman dimuat
</div>
<div class="bubble">
* `loop`: Memutar ulang setelah selesai
</div>
<div class="bubble">
* `muted`: Memulai dalam keadaan tanpa suara
</div>

### Contoh Lengkap:

```
<video width="640" height="360" controls autoplay loop muted>
  <source src="/assets/vidio/mov_bbb.mp4" type="video/mp4">
  Browser Anda tidak mendukung elemen video.
</video>
```
<div class="bubble">
> ⚠️ Catatan: Autoplay hanya bekerja jika video dalam keadaan muted.
</div>
---

## 🧪 Langkah-Langkah Menambahkan Video

### 1. Siapkan Struktur HTML

Buat file HTML dan tambahkan tag `<video>` di bagian yang diinginkan.

```
<video width="640" height="360" controls>
```

### 2. Tambahkan Sumber Video

Gunakan tag `<source>` untuk menentukan lokasi dan jenis file video:

```
<source src="/assets/vidio/mov_bbb.mp4" type="video/mp4">
<source src="/assets/vidio/mov_bbb.webm" type="video/webm">
```

### 3. Tambahkan Pesan Alternatif

Pesan ini akan muncul jika browser tidak mendukung tag `<video>`:

```
Browser Anda tidak mendukung elemen video.
```

### 4. Simpan dan Jalankan

Simpan file HTML dan buka di browser. Video seharusnya sudah tampil dan bisa dijalankan.

---

## 🧾 Format File yang Didukung

Beberapa format video yang didukung oleh browser:
<div class="bubble">
* ✅ **MP4**: Paling umum dan kompatibel
</div>
<div class="bubble">
* ✅ **WebM**: Ukuran kecil, ideal untuk performa
</div>
<div class="bubble">
* ✅ **Ogg**: Alternatif tambahan
</div>

### Contoh:

```
<video controls>
  <source src="video.mp4" type="video/mp4">
  <source src="video.webm" type="video/webm">
  <source src="video.ogg" type="video/ogg">
  Browser Anda tidak mendukung pemutar video.
</video>
```

---

## ✅ Kesimpulan

Dengan HTML5, kamu bisa menyematkan video dengan mudah dan fleksibel. Gunakan tag `<video>` dengan atribut dan format yang sesuai agar kontenmu tampil menarik dan kompatibel di berbagai perangkat.

---