# Sistem Informasi Kepegawaian Sederhana

**Nama: Farhan Mujiburrahman**
**NPM: 2308107010078**

## Deskripsi Singkat Aplikasi

Sistem Informasi Kepegawaian ini adalah aplikasi web sederhana yang dibangun menggunakan framework Laravel. Aplikasi ini bertujuan untuk memfasilitasi pengelolaan data pegawai secara digital. Fitur utama yang tersedia meliputi operasi CRUD (Create, Read, Update, Delete) untuk data pegawai, termasuk kemampuan untuk mengunggah dan menampilkan foto profil pegawai. Aplikasi ini juga dilengkapi dengan validasi form untuk memastikan integritas data dan database seeder untuk pengisian data awal.

## Fitur Utama

*   **Manajemen Data Pegawai (CRUD):**
    *   Menambah data pegawai baru beserta foto profil.
    *   Menampilkan daftar semua pegawai dengan informasi ringkas dan foto thumbnail.
    *   Melihat detail informasi pegawai secara lengkap, termasuk foto profil ukuran penuh.
    *   Mengedit data pegawai yang sudah ada, termasuk mengganti foto profil.
    *   Menghapus data pegawai.
*   **Upload Foto Profil:** Memungkinkan pengguna mengunggah file gambar sebagai foto profil pegawai.
*   **Validasi Form:** Setiap input pada form tambah dan edit pegawai divalidasi untuk memastikan data yang masuk sesuai format dan ketentuan.
*   **Database Seeder:** Menyediakan data awal (dummy) untuk tabel pegawai sehingga aplikasi bisa langsung digunakan dengan contoh data setelah instalasi.
*   **User Interface Sederhana:** Tampilan antarmuka yang intuitif untuk memudahkan interaksi pengguna.

## Penjelasan Code dan Arsitektur

Aplikasi ini dibangun dengan mengikuti pola arsitektur Model-View-Controller (MVC):

### 1. Model (`app/Models/Pegawai.php`)
   - Merepresentasikan tabel `pegawais` di database.
   - Bertanggung jawab untuk interaksi dengan database, seperti mengambil dan menyimpan data.
   - Properti `$fillable` digunakan untuk mendefinisikan atribut mana saja yang dapat diisi secara massal (mass assignment).
   ```php
   // Contoh isi Pegawai.php
   protected $fillable = [
       'nama_lengkap', 'nip', 'jabatan', 'departemen',
       'alamat', 'nomor_telepon', 'tanggal_masuk', 'foto_profil',
   ];
