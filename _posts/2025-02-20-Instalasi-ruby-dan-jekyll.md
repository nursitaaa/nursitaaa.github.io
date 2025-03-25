---
layout: post
title: "Instalasi Ruby dan Jekyll"
---

Berikut adalah penjelasan tentang instalasi Ruby dan Jekyll.

![Instalasi Ruby dan Jekyll](/assets/images/ruby-jekyll.jpeg)

## Penjelasan Mengenai Cara Menginstalasi Ruby dan Jekyll

Untuk membuat situs web statis atau blog dengan Jekyll, Anda perlu menginstal **Ruby** dan **Jekyll** terlebih dahulu. Berikut adalah langkah-langkah instalasi untuk kedua alat ini di sistem operasi yang berbeda.

---

---

### 1. **Instalasi Ruby**

  Ruby adalah bahasa pemrograman yang digunakan oleh Jekyll. Jadi, sebelum menginstal Jekyll, Anda perlu memastikan Ruby terinstal di sistem Anda.

#### **Untuk Windows:**

    1. **Instal Ruby**:
        - Kunjungi situs web [RubyInstaller](https://rubyinstaller.org/) dan unduh versi terbaru dari RubyInstaller.
        - Jalankan file yang diunduh dan ikuti petunjuk di layar.
        - Pastikan untuk mencentang opsi “Add Ruby to PATH” saat instalasi.
        - Setelah selesai, Anda dapat memverifikasi instalasi dengan membuka **Command Prompt** dan menjalankan perintah berikut:
          ```bash
          ruby -v
          ```
          Ini akan menampilkan versi Ruby yang terinstal.

---

---

2. **Instal DevKit (Jika Diperlukan)**:
   - Pada beberapa versi Ruby, Anda juga perlu menginstal DevKit untuk dapat mengompilasi beberapa gem (perpustakaan Ruby). Ini biasanya disarankan oleh RubyInstaller.

#### **Untuk macOS:**

        1. **Instal Ruby melalui Homebrew** (Jika Belum Terinstal):
          - Buka **Terminal** dan jalankan perintah berikut untuk menginstal Homebrew (jika belum terinstal):
            ```bash
            /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
            ```
          - Instal Ruby dengan Homebrew:
            ```bash
            brew install ruby
            ```

        2. **Verifikasi Instalasi Ruby**:
          - Setelah instalasi selesai, periksa versi Ruby dengan perintah:
            ```bash
            ruby -v
            ```

---

---

#### **Untuk Linux (Ubuntu/Debian):**

        1. **Instal Ruby**:
          - Buka **Terminal** dan jalankan perintah berikut untuk menginstal Ruby:
            ```bash
            sudo apt update
            sudo apt install ruby-full
            ```

        2. **Verifikasi Instalasi Ruby**:
          - Setelah instalasi selesai, verifikasi versi Ruby dengan perintah:
            ```bash
            ruby -v
            ```

---

---

### 2. **Instalasi Jekyll**

  Setelah Ruby terinstal, langkah berikutnya adalah menginstal **Jekyll**.

#### **Langkah Umum untuk Semua Sistem Operasi:**

      1. **Perbarui RubyGems (Pengelola Paket Ruby)**:
        - Sebelum menginstal Jekyll, pastikan RubyGems terbaru terinstal. Jalankan perintah ini di terminal atau command prompt:
          ```bash
          gem update --system
          ```

      2. **Instal Jekyll**:
        - Setelah RubyGems diperbarui, instal Jekyll menggunakan perintah:
          ```bash
          gem install jekyll bundler
          ```

      3. **Verifikasi Instalasi Jekyll**:
        - Setelah instalasi selesai, Anda dapat memverifikasi bahwa Jekyll telah terinstal dengan benar dengan menjalankan:
          ```bash
          jekyll -v
          ```
        - Jika berhasil, perintah ini akan menampilkan versi Jekyll yang terinstal.

---

---

### 3. **Membuat Proyek Jekyll Baru**

  Setelah Ruby dan Jekyll terinstal, Anda dapat membuat situs web statis menggunakan Jekyll.

      1. **Buat Direktori Proyek Baru**:
        - Untuk membuat situs baru dengan Jekyll, jalankan perintah berikut untuk membuat proyek baru:
          ```bash
          jekyll new nama-proyek
          ```
          Gantilah `nama-proyek` dengan nama yang Anda inginkan untuk situs Anda.

      2. **Masuk ke Direktori Proyek**:
        - Pindah ke direktori proyek yang baru dibuat:
          ```bash
          cd nama-proyek
          ```

      3. **Jalankan Situs Jekyll**:
        - Sekarang, jalankan situs Jekyll secara lokal untuk melihat pratinjau situs:
          ```bash