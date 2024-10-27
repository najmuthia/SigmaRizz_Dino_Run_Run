# SigmaRizz_Dino_Run_Run

---

# Membuat Gim Dino Run dengan C++ dan Library Game Engine

Selamat datang di tutorial cara membuat gim sederhana menggunakan library game engine khusus untuk C++! Di tutorial ini, kita akan membahas cara kerja kode gim "Dino Run" yang telah disediakan, bagaimana mengaturnya, dan beberapa konsep dasar dalam pembuatan gim 2D.

---

## 🎮 Pendahuluan

**Dino Run** adalah gim sederhana yang mirip dengan gim **Chrome Dino** di mana pemain mengontrol dinosaurus yang berlari melewati batuan, sambil menghindari rintangan dengan melompat. Gim ini melibatkan konsep dasar pembuatan gim seperti:
- **Parallax Scrolling** untuk latar belakang yang bergerak
- **Collision Detection** untuk menghindari rintangan
- **Animasi Sprites** untuk menghidupkan karakter dinosaurus

---

## 📂 Persiapan Lingkungan

1. **Cloning Repository**: Clone repository dari kode gim ini ke direktori lokal Anda.
   ```bash
   git clone https://github.com/najmuthia/SigmaRizz_Dino_Run_Run.git
   ```
2. **Instalasi Library yang Dibutuhkan**: Pastikan Anda memiliki library grafis yang mendukung gambar, suara, dan input keyboard seperti SDL atau SFML. Library ini akan dibutuhkan oleh sebagian besar `#include` yang digunakan di dalam kode.
3. **Kompilasi dan Eksekusi**: Kompilasi proyek dengan makefile atau IDE seperti Visual Studio atau Code::Blocks yang mendukung C++.

---

## 🚀 Struktur Gim

Gim ini terbagi menjadi beberapa bagian utama yang didefinisikan dalam beberapa kelas:
- `DinoGUI`
- `DinoMain`
- `DinoRun`
- `EndMenu`

---

### 1. **DinoGUI** - Antarmuka Pengguna Gim

`DinoGUI` mengatur antarmuka pengguna gim, termasuk skor dan proses inisialisasi gim.

**Kode Utama dalam `DinoGUI`:**
- **Init()**: Fungsi ini menginisialisasi komponen gim utama seperti skor, mengatur latar belakang, serta memanggil `DinoRun`.
- **Update()**: Memanggil fungsi `Update()` dari objek `dinoGame` dan memperbarui skor sesuai jarak yang ditempuh.
- **Draw()**: Memanggil fungsi `Render()` dari `dinoGame` untuk menggambar objek di layar.

### 2. **DinoMain** - Pengaturan Awal Gim

`DinoMain` menginisialisasi layar awal gim dan menambahkan `DinoGUI`, `MainMenu`, dan `EndMenu` ke **ScreenManager** untuk navigasi layar.

**Kode Utama dalam `DinoMain`:**
- **Init()**: Memasukkan layar `DinoGUI` dan layar lainnya ke `ScreenManager` yang bertugas mengatur layar aktif di gim.
- **Update() & Render()**: Fungsi ini memperbarui dan menggambar semua objek dalam gim.

### 3. **DinoRun** - Logika dan Gameplay

`DinoRun` adalah kelas inti yang mengatur logika utama gim, termasuk pergerakan dino, rintangan, dan parallax.

**Kode Utama dalam `DinoRun`:**
- **Init()**: Menginisialisasi objek dino dan batu, memainkan musik, dan mengatur lapisan latar belakang.
- **Update()**: Mengatur animasi lompatan dino, memeriksa tabrakan dengan batu, serta menggerakkan lapisan parallax.
- **Render()**: Menggambar semua lapisan dan objek di layar.

### 4. **EndMenu** - Layar Akhir Gim

`EndMenu` adalah layar akhir gim yang menampilkan skor akhir pemain dan opsi untuk kembali ke menu utama atau memulai ulang gim.

---

## 🔧 Pengaturan Game Over

Fungsi `CheckDead()` di `DinoRun` memeriksa apakah dino bertabrakan dengan objek batu di dalam game. Ketika ada tabrakan, layar akan berpindah ke layar `EndMenu`, yang menampilkan skor terakhir.

---

## 🌟 Fitur-Fitur Khusus

- **Animasi dan Lompatan**: `spriteDino->PlayAnim("jump")` digunakan untuk mengatur animasi dino ketika melompat.
- **Skor dan Jarak**: Skor diperbarui dalam `DinoGUI` berdasarkan `distance` yang dihitung menggunakan waktu berjalan gim (`game->GetGameTime()`).
- **Parallax Scrolling**: Menggerakkan beberapa lapisan latar belakang dengan kecepatan berbeda menciptakan ilusi kedalaman.

---

## 🎞 Video Tutorial

Video tutorial dan penjelasan Game Dino Run Run oleh Kelompok 1 Sigma Rizz

Bisa diakses lewat link ini: [Video Tutorial](https://youtu.be/Gr_BpYoKjvg)

---

## 📚 Sumber Referensi

Tutorial ini menggunakan kode dari `Dino Run Run` milik Kelompok 1 `Sigma Rizz`. Anda bisa melihat contoh lengkap kode di repository GitHub atau [Google Drive](https://drive.google.com/drive/folders/1xfwqgDMVbzQ64-aHhqiizVMaLwb7wGIN?usp=sharing)

Semoga tutorial ini membantu dalam memahami cara membuat gim sederhana dengan C++!
