---
layout: post
title: "Formspree"
---

Berikut adalah materi lengkap tentang **Formspree**:

---

## 📩 Materi: Formspree

### 1. **Apa Itu Formspree?**

**Formspree** adalah layanan backend form submission (pengiriman formulir) yang memungkinkan developer mengirim data formulir HTML ke email **tanpa backend sendiri**.

🛠 Cocok untuk:

* Developer frontend
* Landing page statis
* Proyek tanpa backend (misalnya GitHub Pages)

---

### 2. **Fitur Utama Formspree**

* Kirim data formulir ke email tanpa kode backend
* Dukungan AJAX (tanpa reload halaman)
* Validasi & reCAPTCHA
* Notifikasi email instan
* Auto-responder (balasan otomatis)
* Integrasi dengan tools lain (Slack, Google Sheets, Zapier)

---

### 3. **Cara Kerja Formspree**

1. Buat form HTML biasa.
2. Ganti action dengan endpoint Formspree.
3. Submit form → Data dikirim ke email.

---

### 4. **Contoh Form HTML Dasar**

```
<form action="https://formspree.io/f/moqzvlpr" method="POST">
  <label>Nama:
    <input type="text" name="name">
  </label>
  <label>Email:
    <input type="email" name="email">
  </label>
  <label>Pesan:
    <textarea name="message"></textarea>
  </label>
  <button type="submit">Kirim</button>
</form>
```

📝 Ganti `/f/moqzvlpr` dengan endpoint kamu dari Formspree.

---

### 5. **Langkah-Langkah Menggunakan Formspree**

#### 1. **Buat Akun**

* Kunjungi [https://formspree.io](https://formspree.io) dan daftar gratis.

#### 2. **Buat Form Baru**

* Formspree akan memberi endpoint unik, misalnya `/f/abcd1234`.

#### 3. **Copy-Paste HTML ke Situs**

* Tempelkan form ke halaman HTML kamu.

#### 4. **Uji Coba**

* Submit form → Email masuk ke kotak masuk kamu.

---

### 6. **Validasi Tambahan (Opsional)**

Tambahkan input hidden agar hanya manusia yang bisa mengirim:

```
<input type="text" name="_gotcha" style="display:none">
```

Atau gunakan:

```
<input type="hidden" name="_captcha" value="false">
```

---

### 7. **Kustomisasi Tambahan**

| Fitur                   | Cara Penggunaan                                                                 |
| ----------------------- | ------------------------------------------------------------------------------- |
| Redirect setelah submit | `<input type="hidden" name="_redirect" value="https://domain.com/thanks.html">` |
| AJAX form submission    | Kirim via JavaScript tanpa reload                                               |
| Autoresponder email     | Diatur di dashboard Formspree                                                   |

---

### 8. **Contoh AJAX Submission (Optional)**

```
<script>
const form = document.querySelector("form");
form.addEventListener("submit", async (e) => {
  e.preventDefault();
  const data = new FormData(form);
  const response = await fetch(form.action, {
    method: form.method,
    body: data,
    headers: {
      'Accept': 'application/json'
    }
  });

  if (response.ok) {
    alert("Terima kasih! Pesan kamu sudah terkirim.");
    form.reset();
  } else {
    alert("Ada kesalahan saat mengirim. Coba lagi.");
  }
});
</script>
```

---

### 9. **Kelebihan & Kekurangan**

**✅ Kelebihan:**

* Simpel dan cepat
* Tidak perlu server
* Gratis untuk pemakaian dasar

**⚠️ Kekurangan:**

* Terbatas jika tidak upgrade
* Bergantung pada layanan pihak ketiga
* Tidak cocok untuk form yang kompleks dan bersifat sensitif (data rahasia)

---

### 10. **Alternatif Form Backend Lain**

* [Formsubmit](https://formsubmit.co)
* [Netlify Forms](https://www.netlify.com/products/forms/)
* [Google Forms](https://forms.google.com)
* [Getform.io](https://getform.io)

---

### 11. **Kesimpulan**

Formspree adalah solusi cepat dan praktis untuk mengirim form HTML tanpa backend. Sangat berguna bagi web statis atau proyek kecil. Tapi untuk aplikasi besar dan kompleks, disarankan menggunakan backend sendiri.


