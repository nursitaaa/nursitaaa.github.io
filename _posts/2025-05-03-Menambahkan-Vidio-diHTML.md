---
layout: post
title: "Menambahkan Vidio di HTML"
---

Berikut adalah penjelasan tentang cara Menambahkan Vidio di HTML.

<video width="640" height="360" controls>
  <source src="\assets\vidio\mov_bbb.mp4" type="video/mp4">
  Browser Anda tidak mendukung elemen video.
</video>

## Prasyarat

    Sebelum memulai, ada beberapa hal yang perlu kamu siapkan:

    1. Video yang ingin ditambahkan.  
    2. Pastikan kamu memiliki hak untuk menyebarkan video tersebut.  
    3. Editor teks, seperti Notepad atau lebih baik lagi, editor teks khusus untuk coding seperti Sublime Text, Visual Studio Code, Notepad++, dll.

---
---

## Pengenalan Tag Video

    HTML 5 memperkenalkan tag `<video>` yang dapat digunakan untuk embed video ke dalam halaman HTML. Tag ini sangat fleksibel dan mendukung berbagai format video, termasuk MP4, WebM, dan Ogg.

---
---

## Cara Menambahkan Video

    Berikut adalah langkah-langkah untuk menambahkan video ke halaman HTML:

        ### 1. Siapkan Tag Video

        Buka editor teks kamu dan buat struktur dasar HTML jika belum ada. Kemudian, tambahkan tag `<video>` ke bagian yang kamu ingin letakkan videonya.

        #### Contoh Dasar

        Gunakan tag `<video>` untuk menyematkan video ke halaman web:

        ```
        <video width="640" height="360" controls>
            
        ````

---
---


### 2. Tambahkan Source Video

    Selanjutnya, tambahkan tag `<source>` di dalam tag `<video>`. Tag ini digunakan untuk menunjukkan lokasi dan jenis file video.

    Misalnya, jika kamu memiliki file video bernama “videoKu.mp4” di folder yang sama dengan file HTML, maka isi tag `<source>` akan menjadi seperti ini:

    ```
    <source src="\assets\vidio\mov_bbb.mp4" type="video/mp4">
    Browser Anda tidak mendukung elemen video.
    </video>
    ```
---
---

### 3. Tambahkan Pesan Alternatif

    Pesan ini akan ditampilkan jika browser yang digunakan pengunjung tidak mendukung tag video. Tambahkan teks ini langsung setelah tag `<source>`.

    ```
    Browser Anda tidak mendukung elemen video.
    ```

---
---

### 4. Cek Hasilnya

    Simpan file HTML tersebut dan buka dengan browser. Jika semua langkah diikuti dengan benar, video harus sudah bisa muncul di halaman web.

    #### Menambahkan Kontrol Video

    Atribut `controls` pada tag `<video>` digunakan untuk menunjukkan kontrol video seperti play, pause, volume, dll. Jika kamu ingin menyembunyikannya, cukup hapus atribut ini.

---
---


### 5. Menambahkan Otomatis Play

    Jika kamu menginginkan videonya langsung diputar saat halaman dibuka, tambahkan atribut `autoplay` ke tag `<video>`. Contohnya seperti ini:

    Beberapa atribut lain yang bisa digunakan:

    * `autoplay`: Memutar otomatis saat halaman dimuat.
    * `loop`: Mengulang video setelah selesai.
    * `muted`: Memulai video tanpa suara.

    Contoh:

    ```
    <video width="640" height="360" controls autoplay loop muted>
    <source src="\assets\vidio\mov_bbb.mp4" type="video/mp4">
    </video>
    ```

    > Catatan: Autoplay hanya berfungsi jika video dalam keadaan *muted*.

---
---

## Format File yang Didukung

    * **MP4 (paling umum dan kompatibel)**
    * **WebM (ukuran lebih kecil, ideal untuk performa)**
    * **Ogg (alternatif tambahan)**

    ```
    <video controls>
    <source src="video.mp4" type="video/mp4">
    <source src="video.webm" type="video/webm">
    <source src="video.ogg" type="video/ogg">
    Browser Anda tidak mendukung pemutar video.
    </video>
    ```
