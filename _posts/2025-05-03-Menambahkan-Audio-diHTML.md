---
layout: post
title: "Menambahkan Audio di HTML"
---

Berikut adalah materi lengkap tentang **Menambahkan Audio di HTML** :


# 🎵 Menambahkan Audio di HTML

Menambahkan elemen audio ke halaman web bisa menjadi cara yang efektif untuk meningkatkan keterlibatan pengguna. Kamu mungkin ingin menambahkan musik latar, podcast, atau efek suara tertentu.

Dalam artikel ini, kita akan membahas cara menambahkan audio ke halaman web menggunakan kode HTML dasar.

---

## 🔊 Menggunakan Elemen `<audio>`

HTML5 memperkenalkan elemen `<audio>` yang membuat penambahan suara atau musik menjadi sangat mudah. Berikut adalah cara paling dasar penggunaannya:

```
<audio src="namafile.mp3" controls></audio>
```

📌 **Penjelasan:**
<div class="bubble">
* `src="namafile.mp3"`: menentukan file audio yang akan diputar.
</div>
<div class="bubble">
* `controls`: menampilkan kontrol seperti play, pause, volume, dll.
</div>

Jika file audio berada di folder yang sama dengan file HTML, kamu cukup menuliskan nama file-nya saja. Tanpa atribut `controls`, pengguna tidak akan bisa mengontrol audio.

---

## ⚙️ Atribut Tambahan `<audio>`

Kamu bisa menambahkan atribut lain untuk mengatur perilaku audio:

### 🔁 Loop

Audio akan otomatis mengulang setelah selesai.

```
<audio src="namafile.mp3" controls loop></audio>
```

### ▶️ Autoplay

Audio langsung dimainkan saat halaman dimuat. ⚠️ Bisa mengganggu pengguna, gunakan dengan bijak.

```
<audio src="namafile.mp3" controls autoplay></audio>
```

### 🔇 Muted

Audio dimulai dalam keadaan tidak bersuara.

```
<audio src="namafile.mp3" controls muted></audio>
```

---

## 🎧 Mendukung Berbagai Format Audio

Tidak semua browser mendukung format audio yang sama. Oleh karena itu, sebaiknya gunakan beberapa format sekaligus menggunakan elemen `<source>`:

```
<audio controls>
  <source src="namafile.mp3" type="audio/mpeg">
  <source src="namafile.ogg" type="audio/ogg">
</audio>
```

Jika browser tidak bisa memutar MP3, maka akan mencoba memutar versi OGG.

---

## 📝 Kesimpulan

Dengan elemen `<audio>`, kamu bisa dengan mudah menambahkan audio ke halaman HTML. Gunakan atribut seperti:
<div class="bubble">
* `controls`: untuk kontrol pengguna
</div>
<div class="bubble">
* `loop`: untuk mengulang otomatis
</div>
<div class="bubble">
* `autoplay`: untuk memulai otomatis
</div>
<div class="bubble">
* `muted`: untuk mulai dalam keadaan senyap
</div>

Dan jangan lupa untuk menyertakan **beberapa format audio** agar mendukung berbagai browser.

---
