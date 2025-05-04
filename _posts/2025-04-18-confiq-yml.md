---
layout: post
title: "confiq.yml"
---

Berikut adalah penjelasan tentang confiq.yml

## 📘 Fungsi Utama `_config.yml`

 Berikut beberapa fungsi penting dari `_config.yml`:

  ### 1. **Informasi Situs**

    ```yaml
    title: Situsku
    description: Belajar Jekyll dan HTML
    author: Nursitaa
    ````

    * Menyimpan data global situs (bisa dipanggil di template: `{{ site.title }}`).

---

  ### 2. **Pengaturan Build**


    ```
    baseurl: "" # misalnya "/blog" jika diunggah ke GitHub Pages di subfolder
    url: "https://namakamu.github.io"
    ```

    * `baseurl`: digunakan jika situs dihosting di subdirektori (seperti di GitHub Pages).
    * `url`: domain utama situs.

    ---

  ### 3. **Tema atau Layout**

    ```yaml
    theme: minima
    ```

    * Menentukan tema default situs.

---

  ### 4. **Folder yang Disertakan**

    ```yaml
    include:
    - assets
    - _pages
    ```

    * Memastikan Jekyll menyertakan folder tertentu saat build, misalnya `assets/` untuk gambar, audio, dsb.

---

  ### 5. **Folder yang Dikecualikan**

    ```yaml
    exclude:
    - node_modules
    - README.md
    ```

    * Folder/file yang **tidak akan dibaca atau dibuild** oleh Jekyll.

---

  ### 6. **Pengaturan Markdown**

    ```yaml
    markdown: kramdown
    kramdown:
    input: GFM
    ```

    * Mengatur jenis parser Markdown yang digunakan.

---

##  Contoh Sederhana `_config.yml`

```yaml
title: Belajar Web
description: Tutorial HTML, CSS, dan Jekyll
author: Nursitaa
url: "https://nursitaa.github.io"
baseurl: "/belajarweb"
theme: minima
include:
  - assets
markdown: kramdown
```

```

---
