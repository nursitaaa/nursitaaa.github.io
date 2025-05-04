---
layout: post
title: "Menambahkan Audio di HTML"
---

Berikut adalah penjelasan tentang cara Menambahkan Audio di HTML.


<audio controls>
  <source src="/assets/audio/short-8-228137.mp3" type="audio/mpeg">
  <source src="/assets/audio/short-8-228137.ogg" type="audio/ogg">
  Browser kamu tidak mendukung pemutar audio.
</audio>

Menambahkan elemen audio ke halaman web bisa menjadi cara yang efektif untuk meningkatkan keterlibatan pengguna. Kamu mungkin ingin memainkan musik latar, podcast, atau mungkin efek suara tertentu. Dalam artikel ini, kami akan membahas cara menambahkan audio ke halaman webmu menggunakan kode HTML dasar.

## Menggunakan Elemen Audio HTML
    HTML5 memperkenalkan elemen <audio> yang membuat penambahan suara atau musik menjadi cukup mudah. Berikut adalah cara paling dasar untuk melakukannya:
    ```
    <audio src="namafile.mp3" controls></audio>
    ```
    Elemen audio perlu sumber file, yang ditentukan oleh atribut src. Nilai dari atribut ini adalah path dari file audio yang ingin kamu mainkan. Jika file audio berada dalam direktori yang sama dengan file HTML, kamu hanya perlu memberikan nama file.

    Atribut controls adalah opsi yang memungkinkan pengguna untuk mengontrol pemutaran audio. Mereka dapat memutar, menjeda, atau menavigasi track audio. Jika kamu menghilangkan atribut ini, audio akan tetap ada, tetapi pengguna tidak akan memiliki cara untuk memainkannya.

## Atribut Tambahan
    Ada beberapa atribut lain yang dapat kamu tambahkan ke dalam elemen <audio> yang dapat memberikan lebih banyak kontrol terhadap cara kerja audio.

    **Loop**
    Atribut loop akan membuat audio secara otomatis memutar ulang ketika mencapai akhir track.
    ```
    <audio src="namafile.mp3" controls loop></audio>
    ```
    **Autoplay**
    Jika kamu menginginkan audio otomatis dimainkan saat halaman dimuat, kamu bisa menggunakan atribut autoplay. Namun, berhati-hatilah karena ini dapat menjadi gangguan bagi beberapa pengguna.
    ```
    <audio src="namafile.mp3" controls autoplay></audio>
    ```
    **Muted**
    Atribut muted akan mematikan suara secara default saat halaman dimuat. Pengguna masih bisa mengontrol volume jika atribut controls digunakan.
    ```
    <audio src="namafile.mp3" controls muted></audio>
    ```

---

## Menggunakan Format Audio yang Berbeda
    Tidak semua browser mendukung semua format file audio. Untuk memastikan audio dapat dimainkan di sebagian besar browser, disarankan untuk menyertakan beberapa format file audio yang berbeda. Untuk melakukan ini, kamu perlu mengganti atribut src dengan elemen <source>:
    ```
    <audio controls>
    <source src="namafile.mp3" type="audio/mpeg">
    <source src="namafile.ogg" type="audio/ogg">
    </audio>
    ```
    Jika browser tidak dapat memainkan file MP3, maka akan mencoba memainkan file OGG.

---

Demikianlah cara menambahkan audio ke halaman webmu menggunakan HTML. Dengan pengetahuan ini, kamu sekarang bisa lebih kreatif dalam mengembangkan halaman webmu. Selamat mencoba!