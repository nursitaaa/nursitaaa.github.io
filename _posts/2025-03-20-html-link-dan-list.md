---
layout : post
title : "HTML Link dan Lists"
---

berikut adalah penjelasan tentang link dan lists pada HTML.


![HTML Link dan Lists](/assets/images/link-dan-lists.jpeg)

### Penjelasan Link dan Lists Pada HTML

### **HTML Link (Tautan)**
      Link di HTML digunakan untuk menghubungkan satu halaman web dengan halaman web lain, atau untuk mengarahkan pengguna ke lokasi tertentu dalam halaman yang sama. Tautan dibuat menggunakan elemen `<a>` (anchor) dan atribut `href` yang menentukan URL tujuan.

      # Sintaks Dasar Link:
      ```html
      <a href="URL">Teks Tautan</a>
      ```
---
      - **`href`**: Atribut ini digunakan untuk menentukan URL atau alamat halaman yang akan dituju.
      - **Teks di antara tag `<a>` dan `</a>`**: Ini adalah teks atau konten yang akan muncul sebagai tautan yang dapat diklik oleh pengguna.

        #### Contoh Link:
        ```html
        <a href="https://www.google.com">Kunjungi Google</a>
        ```
        - Di atas, link ini akan mengarahkan pengguna ke **Google** saat diklik.

---
#### Link Internal dan Eksternal:
      - **Link Eksternal**: Tautan yang mengarah ke halaman web di luar situs Anda. Misalnya, tautan yang mengarah ke Google.
        ```html
        <a href="https://www.google.com">Kunjungi Google</a>
        ```
        ---

      - **Link Internal**: Tautan yang mengarah ke halaman lain di dalam situs yang sama. Anda hanya perlu menentukan jalur relatif, seperti:
        ```html
        <a href="about.html">Tentang Kami</a>
  ```
---

#### Link ke Bagian Tertentu dalam Halaman:
      Link juga dapat digunakan untuk menavigasi ke bagian tertentu dalam halaman yang sama, dengan menggunakan **id** pada elemen tujuan.

      Contoh:
      ```html
      <a href="#section1">Ke Bagian 1</a>

      <h2 id="section1">Bagian 1</h2>
      ```
      - Di atas, saat link diklik, pengguna akan dibawa ke bagian yang memiliki id `section1` dalam halaman yang sama.

---

#### Atribut Tambahan untuk Link:
      - **`target="_blank"`**: Membuka link di tab atau jendela baru.
        ```html
        <a href="https://www.google.com" target="_blank">Kunjungi Google</a>
        ```
      - **`title`**: Menambahkan teks deskripsi yang akan muncul saat pengguna mengarahkan kursor ke tautan.
        ```html
        <a href="https://www.google.com" title="Ke Google">Kunjungi Google</a>
        ```

---

### **HTML Lists (Daftar)**

    HTML menyediakan dua jenis daftar utama: **daftar terurut** (ordered list) dan **daftar tidak terurut** (unordered list).

---

#### 1. **Daftar Tidak Terurut (Unordered List)**

          Daftar tidak terurut digunakan untuk menampilkan item dalam urutan yang tidak tertentu, biasanya dengan peluru (bullet points).

          - Elemen utama untuk membuat daftar tidak terurut adalah `<ul>`.
          - Setiap item dalam daftar ditempatkan dalam elemen `<li>` (list item).

          #### Sintaks Daftar Tidak Terurut:
          ```html
          <ul>
            <li>Item 1</li>
            <li>Item 2</li>
            <li>Item 3</li>
          </ul>
          ```

            #### Contoh Daftar Tidak Terurut:
            ```html
            <ul>
              <li>Apel</li>
              <li>Jeruk</li>
              <li>Durian</li>
            </ul>
            ```
            - Hasilnya adalah daftar dengan peluru:
              - Apel
              - Jeruk
              - Durian

---

#### 2. **Daftar Terurut (Ordered List)**

          Daftar terurut digunakan untuk menampilkan item dalam urutan yang terstruktur atau berurutan (misalnya, langkah-langkah dalam instruksi).

          - Elemen utama untuk membuat daftar terurut adalah `<ol>`.
          - Setiap item dalam daftar ditempatkan dalam elemen `<li>`.

          #### Sintaks Daftar Terurut:
          ```html
          <ol>
            <li>Langkah 1</li>
            <li>Langkah 2</li>
            <li>Langkah 3</li>
          </ol>
          ```

          #### Contoh Daftar Terurut:
          ```html
          <ol>
            <li>Persiapkan bahan</li>
            <li>Panaskan oven</li>
            <li>Masukkan adonan</li>
          </ol>
          ```
          - Hasilnya adalah daftar dengan angka:
            1. Persiapkan bahan
            2. Panaskan oven
            3. Masukkan adonan

---

#### 3. **Daftar Bersarang (Nested List)**

        Anda juga dapat membuat daftar bersarang, yaitu daftar di dalam daftar. Ini sering digunakan untuk mengorganisasi informasi lebih lanjut.

        Contoh:
        ```html
        <ul>
          <li>Buah
            <ul>
              <li>Apel</li>
              <li>Jeruk</li>
            </ul>
          </li>
          <li>Sayuran
            <ul>
              <li>Bayam</li>
              <li>Tomat</li>
            </ul>
          </li>
        </ul>
        ```
        - Hasilnya akan menjadi:
          - Buah
            - Apel
            - Jeruk
          - Sayuran
            - Bayam
            - Tomat

---

#### 4. **Daftar dengan Gaya atau Penataan Khusus**
        Dengan menggunakan CSS, Anda dapat mengubah gaya daftar, seperti mengganti peluru dengan gambar, mengubah angka dalam daftar terurut, atau menyembunyikan peluru.

        Contoh:
        ```html
        <style>
          ul {
            list-style-type: square; /* Mengubah peluru menjadi kotak */
          }
        </style>

        <ul>
          <li>Item 1</li>
          <li>Item 2</li>
          <li>Item 3</li>
        </ul>
        ```

---

### **Perbedaan Utama:**
      - **Daftar Terurut** (`<ol>`) digunakan ketika urutan item penting (seperti langkah-langkah instruksi), dan biasanya menampilkan angka atau huruf sebagai penanda.
      - **Daftar Tidak Terurut** (`<ul>`) digunakan ketika urutan item tidak penting, biasanya dengan peluru.

---

### **Kesimpulan**
      - **HTML Link** (`<a>`) adalah elemen yang memungkinkan pembuatan tautan antar halaman atau sumber daya lain di web.
      - **HTML Lists** menyediakan cara untuk menampilkan item dalam urutan tertentu menggunakan `<ol>` atau tanpa urutan menggunakan `<ul>`, serta kemampuan untuk membuat daftar bersarang untuk struktur yang lebih kompleks.
