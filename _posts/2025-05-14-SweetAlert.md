---
layout: post
title: "SweetAlert"
---

Berikut adalah materi lengkap tentang **SweetAlert**:

---

## 🎉 Materi: SweetAlert

### 1. **Apa Itu SweetAlert?**

**SweetAlert** adalah library JavaScript untuk menampilkan **popup/alert yang cantik dan interaktif**, sebagai pengganti `alert()`, `confirm()`, dan `prompt()` bawaan JavaScript yang kaku.

📦 Nama Library: `SweetAlert` (versi 1) dan `SweetAlert2` (versi lanjutan yang lebih powerfull)

---

### 2. **Mengapa Menggunakan SweetAlert?**

* Tampilan modern dan menarik
* Mudah digunakan
* Dapat dikustomisasi (ikon, tombol, timer, dll)
* Mendukung promise/asynchronous
* Kompatibel dengan semua browser modern

---

### 3. **Cara Menggunakan SweetAlert**

#### ✅ Langkah 1: Tambahkan CDN (untuk SweetAlert2)

```
<script src="https://cdn.jsdelivr.net/npm/sweetalert2@11"></script>
```

#### ✅ Langkah 2: Panggil SweetAlert

```
Swal.fire('Hello World!');
```

---

### 4. **Contoh SweetAlert Dasar**

```
Swal.fire({
  title: 'Sukses!',
  text: 'Data berhasil disimpan.',
  icon: 'success',
  confirmButtonText: 'OK'
});
```

---

### 5. **Opsi Konfigurasi**

| Opsi                | Fungsi                                                                  |
| ------------------- | ----------------------------------------------------------------------- |
| `title`             | Judul alert                                                             |
| `text`              | Isi pesan                                                               |
| `icon`              | Jenis ikon: `'success'`, `'error'`, `'warning'`, `'info'`, `'question'` |
| `confirmButtonText` | Teks tombol konfirmasi                                                  |
| `showCancelButton`  | Tampilkan tombol batal                                                  |
| `timer`             | Tutup otomatis (dalam ms)                                               |

---

### 6. **Contoh Konfirmasi Aksi**

```
Swal.fire({
  title: 'Yakin?',
  text: "Data akan dihapus permanen!",
  icon: 'warning',
  showCancelButton: true,
  confirmButtonText: 'Ya, hapus!',
  cancelButtonText: 'Batal'
}).then((result) => {
  if (result.isConfirmed) {
    // logika penghapusan
    Swal.fire('Terhapus!', 'Data berhasil dihapus.', 'success');
  }
});
```

---

### 7. **Contoh Input Form di SweetAlert**

```
Swal.fire({
  title: 'Masukkan Nama',
  input: 'text',
  inputPlaceholder: 'Nama lengkap',
  showCancelButton: true
}).then((result) => {
  if (result.value) {
    Swal.fire(`Halo, ${result.value}!`);
  }
});
```

---

### 8. **Custom Button dan Styling**

```
Swal.fire({
  title: 'Custom Button',
  icon: 'info',
  confirmButtonText: '<i class="fa fa-thumbs-up"></i> Mantap!',
  buttonsStyling: false,
  customClass: {
    confirmButton: 'btn btn-primary',
    cancelButton: 'btn btn-danger'
  }
});
```

---

### 9. **Integrasi dengan Aksi Web**

Contoh integrasi dengan tombol HTML:

```
<button onclick="showAlert()">Klik Saya</button>
<script>
function showAlert() {
  Swal.fire('Halo Dunia!', 'Ini adalah alert dari SweetAlert2', 'success');
}
</script>
```

---

### 10. **Kelebihan dan Kekurangan**

**✅ Kelebihan:**

* Tampilan modern & profesional
* Banyak opsi kustomisasi
* Ringan dan mudah integrasi

**⚠️ Kekurangan:**

* Butuh library eksternal (jika tak pakai bundler)
* Mungkin terlalu berlebihan untuk alert sederhana

---

### 11. **Alternatif SweetAlert**

* Bootstrap Modal
* Toastify.js (untuk notifikasi)
* Notyf / Toastr.js
* Native JavaScript `alert()` (basic use)

---

### 12. **Kesimpulan**

**SweetAlert** membuat tampilan alert jadi lebih menarik dan fungsional. Sangat cocok untuk meningkatkan UX dalam aplikasi web modern. Gunakan SweetAlert2 untuk versi terbaru dan fleksibel.


