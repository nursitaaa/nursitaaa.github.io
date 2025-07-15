---
layout: post
title: "Lavarel Breeze"
---



Berikut langkah-langkah **Laravel Breeze**:

---

## 1. Membuat Model dan Migration

Gunakan sintaks:

```
php artisan make:model Siswa -cm
````

💬 Penjelasan:
<div class="bubble">
* `make:model Siswa` → Membuat model baru `Siswa` di `app/Models/Siswa.php`
</div>
<div class="bubble">
* `-c` → Membuat controller `SiswaController.php` di `app/Http/Controllers/`
</div>
<div class="bubble">
* `-m` → Membuat migration file `xxxx_create_siswas_table.php` di `database/migrations/`
</div>

---

## 2. Edit File Migration

Buka file migration `database/migrations/xxxx_create_siswas_table.php`, lalu ubah menjadi:

```php
public function up(): void
{
    Schema::create('siswas', function (Blueprint $table) {
        $table->id();
        $table->string('nama', 100);
        $table->text('alamat');
        $table->boolean('jenis_kelamin');
        $table->string('agama');
        $table->string('sekolah_asal');
        $table->timestamps();
    });
}
```
<div class="bubble">
📝 Fungsi ini digunakan untuk membuat struktur tabel `siswas` di database.
</div>

---

## 3. Jalankan Migration

```
php artisan migrate
```
<div class="bubble">
📝 Menjalankan semua file migration yang belum dijalankan sebelumnya dan menerapkannya ke dalam database.
</div>
---

## 4. Install Laravel Breeze

```
composer require laravel/breeze --dev
```
<div class="bubble">
💬 Breeze adalah starter kit autentikasi (login, register, logout) berbasis Blade + Tailwind.
</div>
---

## 5. Jalankan Installer Breeze

```
php artisan breeze:install
```
<div class="bubble">
🛠 Mengatur struktur autentikasi dasar dalam Laravel.
</div>
---

## 6. Install Dependency Frontend

```
npm install
```

📦 Menginstal:

* Tailwind CSS
* Alpine.js
* Vite

✅ Pastikan kamu sudah menginstal Node.js dan npm:

```
node -v
npm -v
```

---

## 7. Jalankan Proses Build

```
npm run dev
```
<div class="bubble">
⚙️ Meng-compile file CSS dan JS ke dalam folder `public/build/` menggunakan Vite.
</div>
---

## 8. Ubah dan Tambah File Berikut

### 📁 `app/Models/Siswa.php`

```
<?php

namespace App\Models;

use Illuminate\Database\Eloquent\Model;

class Siswa extends Model
{
    protected $fillable = [
        'nama',
        'alamat',
        'agama',
        'jenis_kelamin',
        'sekolah_asal'
    ];
}
```

---

### 📁 `app/Http/Controllers/SiswaController.php`

```
<?php

namespace App\Http\Controllers;

use App\Models\Siswa;
use Illuminate\Http\Request;

class SiswaController extends Controller
{
    public function index()
    {
        $siswas = Siswa::all();
        return view('siswa.index', compact('siswas'));
    }

    public function create()
    {
        return view('siswa.create');
    }

    public function store(Request $request)
    {
        $data = $request->all();
        Siswa::create($data);
        return redirect('siswa');
    }

    public function edit(Siswa $siswa)
    {
        return view('siswa.edit', compact('siswa'));
    }

    public function update(Request $request, Siswa $siswa)
    {
        $siswa->update($request->all());
        return redirect()->route('siswa.index')->with('success', 'Data siswa berhasil diperbarui.');
    }

    public function destroy(Siswa $siswa)
    {
        $siswa->delete();
        return redirect()->route('siswa.index')->with('success', 'Data siswa berhasil dihapus.');
    }
}
```

---

### 📁 `resources/views/siswa/create.blade.php`

Gunakan komponen Blade dari Breeze untuk form input:

```
<x-app-layout>
    <x-slot name="header">
        <h2 class="font-semibold text-xl text-gray-800 dark:text-gray-200 leading-tight">
            {{ __('Siswa') }}
        </h2>
    </x-slot>

    <div class="py-12">
        <div class="max-w-7xl mx-auto sm:px-6 lg:px-8">
            <div class="bg-white dark:bg-gray-800 overflow-hidden shadow-sm sm:rounded-lg">
                <div class="p-6 text-gray-900 dark:text-gray-100">
                    <form method="POST" action="{{ route('siswa.store') }}">
                        @csrf

                        <x-input-label for="nama" :value="'Nama'" />
                        <x-text-input id="nama" class="block mt-1 w-full text-black" type="text" name="nama" required />

                        <x-input-label for="alamat" :value="'Alamat'" class="mt-4" />
                        <x-text-input id="alamat" class="block mt-1 w-full text-black" type="text" name="alamat" required />

                        <x-input-label for="agama" :value="'Agama'" class="mt-4" />
                        <x-text-input id="agama" class="block mt-1 w-full text-black" type="text" name="agama" required />

                        <x-input-label for="jenis_kelamin" :value="'Jenis Kelamin'" class="mt-4" />
                        <x-text-input id="jenis_kelamin" class="block mt-1 w-full text-black" type="text" name="jenis_kelamin" required />

                        <x-input-label for="sekolah_asal" :value="'Sekolah Asal'" class="mt-4" />
                        <x-text-input id="sekolah_asal" class="block mt-1 w-full text-black" type="text" name="sekolah_asal" required />

                        <div class="flex items-center justify-end mt-4">
                            <x-primary-button class="ms-3">{{ __('Simpan') }}</x-primary-button>
                            <x-secondary-button class="ml-3">{{ __('Batal') }}</x-secondary-button>
                        </div>
                    </form>
                </div>
            </div>
        </div>
    </div>
</x-app-layout>
```

---

### 📁 `resources/views/siswa/edit.blade.php`

```
<h2>Edit Data Siswa</h2>

<form action="{{ route('siswa.update', $siswa->id) }}" method="POST">
    @csrf
    @method('PUT')

    <label>Nama:</label>
    <input type="text" name="nama" value="{{ $siswa->nama }}" required>

    <label>Alamat:</label>
    <input type="text" name="alamat" value="{{ $siswa->alamat }}" required>

    <label>Agama:</label>
    <input type="text" name="agama" value="{{ $siswa->agama }}" required>

    <label>Sekolah Asal:</label>
    <input type="text" name="sekolah_asal" value="{{ $siswa->sekolah_asal }}" required>

    <label>Jenis Kelamin:</label>
    <select name="jenis_kelamin">
        <option value="1" {{ $siswa->jenis_kelamin == 1 ? 'selected' : '' }}>Laki-laki</option>
        <option value="0" {{ $siswa->jenis_kelamin == 0 ? 'selected' : '' }}>Perempuan</option>
    </select>

    <button type="submit">Simpan</button>
</form>
```

---

### 📁 `resources/views/siswa/index.blade.php`

Tampilan daftar data siswa:

```
<x-app-layout>
    <x-slot name="header">
        <h2 class="font-semibold text-xl text-gray-800 dark:text-gray-200 leading-tight">
            {{ __('Data Siswa') }}
        </h2>
    </x-slot>

    <div class="py-12">
        <div class="max-w-7xl mx-auto sm:px-6 lg:px-8">
            <div class="bg-white dark:bg-gray-800 overflow-hidden shadow-sm sm:rounded-lg">
                <div class="p-6 text-gray-900 dark:text-gray-100">
                    <a href="{{ route('siswa.create') }}" class="mb-4 inline-block bg-blue-500 text-white px-4 py-2 rounded hover:bg-blue-600">
                        + Tambah Siswa
                    </a>

                    <table class="min-w-full divide-y divide-gray-200 dark:divide-gray-700">
                        <thead class="bg-gray-100 dark:bg-gray-700">
                            <tr>
                                <th>No</th>
                                <th>Nama</th>
                                <th>Alamat</th>
                                <th>Agama</th>
                                <th>Sekolah Asal</th>
                                <th>Jenis Kelamin</th>
                                <th>Aksi</th>
                            </tr>
                        </thead>
                        <tbody>
                            @forelse ($siswas as $siswa)
                                <tr>
                                    <td>{{ $loop->iteration }}</td>
                                    <td>{{ $siswa->nama }}</td>
                                    <td>{{ $siswa->alamat }}</td>
                                    <td>{{ $siswa->agama }}</td>
                                    <td>{{ $siswa->sekolah_asal }}</td>
                                    <td>{{ $siswa->jenis_kelamin == 1 ? 'Laki-laki' : 'Perempuan' }}</td>
                                    <td>
                                        <a href="{{ route('siswa.edit', $siswa->id) }}">Edit</a>
                                        <form action="{{ route('siswa.destroy', $siswa->id) }}" method="POST" onsubmit="return confirm('Hapus data ini?')" style="display:inline;">
                                            @csrf
                                            @method('DELETE')
                                            <button type="submit">Hapus</button>
                                        </form>
                                    </td>
                                </tr>
                            @empty
                                <tr>
                                    <td colspan="7" class="text-center">Tidak ada data siswa.</td>
                                </tr>
                            @endforelse
                        </tbody>
                    </table>
                </div>
            </div>
        </div>
    </div>
</x-app-layout>
```

---

### 📁 `routes/web.php`

```
use App\Http\Controllers\SiswaController;

Route::get('/', [SiswaController::class, 'index']);

Route::middleware('auth')->group(function () {
    Route::resource('/siswa', SiswaController::class);
});
```

---

### 📁 Tambah Link di `navigation.blade.php`

Tambahkan link di navigasi:

```
<x-nav-link :href="route('siswa.index')" :active="request()->routeIs('siswa.*')">
    {{ __('Siswa') }}
</x-nav-link>
```

---

