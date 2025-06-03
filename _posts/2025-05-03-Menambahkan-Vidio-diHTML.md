---
layout: post
title: "Menambahkan Vidio di HTML"
---

Berikut adalah penjelasan tentang cara Menambahkan Vidio di HTML.

<video width="640" height="360" controls>
  <source src="\nursitaaa\assets\vidio\mov_bbb.mp4" type="video/mp4">
  Browser Anda tidak mendukung elemen video.
</video>


Menambahkan video ke dalam website HTML dapat meningkatkan interaktivitas dan daya tarik bagi pengunjung. Dengan kemajuan HTML5, proses ini menjadi lebih sederhana dan efisien. Kamu dapat menyematkan video langsung ke halaman web tanpa memerlukan plugin eksternal. Artikel ini akan membahas cara memasukkan video ke website HTML menggunakan tag <video>, termasuk struktur dasar dan atribut penting yang perlu diperhatikan.

## Prasyarat

    Sebelum memulai, ada beberapa hal yang perlu kamu siapkan:

    1. Video yang ingin ditambahkan.  
    2. Pastikan kamu memiliki hak untuk menyebarkan video tersebut.  
    3. Editor teks, seperti Notepad atau lebih baik lagi, editor teks khusus untuk coding seperti Sublime Text, Visual Studio Code, Notepad++, dll.


---

## Pengenalan Tag Video

    HTML 5 memperkenalkan tag `<video>` yang dapat digunakan untuk embed video ke dalam halaman HTML. Tag ini sangat fleksibel dan mendukung berbagai format video, termasuk MP4, WebM, dan Ogg.

    Tag <video> dalam HTML5 digunakan untuk menyematkan konten video langsung ke dalam halaman web. Penggunaan tag ini memungkinkan kamu menampilkan video tanpa memerlukan plugin tambahan, sehingga kompatibilitas dan aksesibilitas situs meningkat. Sebelum menambahkan video, pastikan format file video yang digunakan didukung oleh browser, seperti MP4, WebM, atau OGG.

---
---

### Struktur Dasar Tag <video>

    Struktur dasar tag <video> melibatkan pembukaan tag <video>, penentuan sumber video menggunakan tag <source>, dan penutupan tag </video>. Berikut contoh sederhana:
    ```
    <video width="640" height="360" controls>

    <source src="video-sample.mp4" type="video/mp4">

    <source src="video-sample.webm" type="video/webm">

    Browser kamu tidak mendukung tag video.

    </video>
    ```

    Dalam contoh di atas, atribut width dan height menentukan ukuran pemutar video, sedangkan controls menambahkan kontrol pemutaran seperti play, pause, dan volume. Tag <source> digunakan untuk menentukan sumber video dengan atribut src sebagai lokasi file dan type sebagai format file. Menambahkan beberapa tag <source> dengan format berbeda memastikan kompatibilitas dengan berbagai browser.


---
---

### Atribut Penting dalam Tag <video>
    Tag <video> memiliki beberapa atribut yang dapat disesuaikan untuk mengontrol perilaku dan tampilan video di halaman web. Berikut beberapa atribut penting yang sering digunakan:

    src untuk Menentukan Sumber Video
    Atribut src digunakan untuk menentukan URL sumber video yang akan diputar. Namun, praktik terbaik adalah menggunakan tag <source> di dalam tag <video> untuk mendefinisikan sumber video, memungkinkan penambahan beberapa format video untuk kompatibilitas yang lebih baik. Contoh:

    ```
    <video controls>

    <source src="video-sample.mp4" type="video/mp4">

    <source src="video-sample.webm" type="video/webm">

    Browser kamu tidak mendukung tag video.

    </video>
    ```

    Ketika menambahkan beberapa sumber video dalam format berbeda, browser akan memilih format yang didukungnya, sehingga video dapat diputar dengan baik.

---
---

## Cara Menambahkan Video

    Berikut adalah langkah-langkah untuk menambahkan video ke halaman HTML:

 1. Siapkan Tag Video

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
