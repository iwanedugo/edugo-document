## **Dokumen Panduan - Kerja dengan Branch, Commit, dan Pull Request**
### 1. Pergi ke branch develop dan Memperbarui Perubahan Terbaru
Pastikan kamu berada di branch develop sebelum membuat branch baru dan melakukan pull untuk memperbarui perubahan terbaru.

```bash
git checkout develop
```
Lakukan pull dari branch origin/develop (jika ini adalah remote branch yang ditargetkan) untuk memperbarui branch lokal develop dengan perubahan terbaru dari remote repository.
```bash
git pull origin develop

```
## 2. Membuat Branch Baru dari develop
Setelah branch develop diperbarui, kamu dapat membuat branch baru untuk pekerjaanmu menggunakan perintah git checkout -b <nama_branch>.
```bash
git checkout -b feature/nama-fitur
```

Branch baru dengan nama feature/nama-fitur telah dibuat berdasarkan develop dan kamu siap untuk memulai pekerjaanmu.
## 3. Commit
Lakukan perubahan pada file-file yang diperlukan.

Tambahkan perubahan yang dilakukan ke dalam staging area menggunakan perintah git add.
```bash
git add nama_file1 nama_file2

```
Buat commit dengan perintah git commit -m "<pesan_commit>".

```bash
git commit -m "[<Tipe Perubahan>] <Deskripsi Perubahan>"
contoh : 
git commit -m "[FEAT] Menambahkan button apply di program detail"


```
Berikut adalah penjelasan singkat untuk setiap bagian dalam commit feature:
#### 1. **Tipe Perubahan** Menyatakan jenis perubahan yang dilakukan. Beberapa tipe yang umum digunakan antara lain:

- **Feat**: Menambahkan fitur baru.
- **Fix**: Memperbaiki bug atau masalah yang ada.
- **Refactor**: Melakukan perubahan dalam kode tanpa mengubah fitur yang ada.
- **Docs**: Mengubah atau menambahkan dokumentasi.
- **Test**: Menambahkan atau memperbaiki pengujian.
- **Chore**: Melakukan perubahan dalam tugas-tugas terkait manajemen proyek, seperti konfigurasi atau perubahan alur kerja.

#### 2. **Deskripsi Perubahan**: Menjelaskan dengan singkat apa yang berubah dalam commit tersebut. Deskripsi ini harus singkat namun informatif.

## 4. Judul Pull Request (PR)
Judul PR harus jelas dan deskriptif untuk memudahkan review.

- Hindari judul PR yang terlalu umum atau ambigu.
- Gunakan format yang singkat namun informatif.

## 5. Deskripsi Pull Request (PR)
Jelaskan dengan jelas perubahan yang dilakukan dan mengapa perubahan tersebut diperlukan.

- Sertakan konteks dan informasi tambahan yang relevan.
- Jika ada isu terkait atau referensi lain, sebutkan nomor isu atau link yang relevan.
- Pastikan deskripsi PR mudah dipahami oleh reviewer.
- Berikut ini adalah contoh judul dan deskripsi PR:

Judul PR: Menambahkan fungsi pencarian produk

Deskripsi PR:
```bash
- Menambahkan fungsi pencarian untuk memungkinkan pengguna mencari produk berdasarkan nama atau kategori.
- Mengimplementasikan logika pencarian di sisi server dan menambahkan UI untuk input pencarian di sisi klien.

```