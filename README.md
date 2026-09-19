# Undangan Digital Melaspas Rumah

Web undangan digital *single-page* ini dirancang khusus untuk upacara Melaspas, dengan nuansa elegan dan adat Bali modern. Dibuat menggunakan HTML5, Tailwind CSS (via CDN), dan JavaScript murni.

## 📂 Struktur File dan Folder
- `index.html` : File utama website (Single-File HTML). Buka file ini di browser Anda.
- `assets/` : Folder untuk menyimpan berbagai file media.
  - `assets/images/` : Simpan foto background rumah atau ornamen lainnya di sini.
  - `assets/audio/` : Simpan file musik latar (misal: Rindik Bali) di sini.

## 🛠️ Cara Kustomisasi
1. **Background Cover / Foto Rumah**:
   - Siapkan foto rumah/bangunan Anda, ubah namanya menjadi `cover-bg.jpg`.
   - Masukkan ke dalam folder `assets/images/`.
   - Kode akan otomatis meload gambar tersebut. Jika gambar tidak ada, warna fallback cokelat gelap akan digunakan.

2. **Musik Latar (Backsound)**:
   - Siapkan file audio berformat `.mp3`, ubah namanya menjadi `background.mp3`.
   - Masukkan ke dalam folder `assets/audio/`.
   - Musik akan otomatis diputar saat tamu menekan tombol "Buka Undangan".

3. **Nama Tamu (Dinamis via URL)**:
   - Untuk membagikan link kepada tamu secara spesifik, Anda bisa menambahkan parameter `?to=Nama+Tamu` di akhir URL.
   - Contoh saat dihosting: `https://undangan-saya.com/?to=Bapak+Wayan` atau secara lokal `index.html?to=Bapak+Wayan`
   - Nama "Bapak Wayan" akan otomatis muncul di bagian *Cover* undangan. Jika parameter tidak diisi, teks default "Tamu Undangan" akan ditampilkan.

4. **Mengubah Detail Acara**:
   - Buka file `index.html` dengan text editor (seperti VS Code atau Notepad).
   - Cari baris kode yang berisi tanggal, waktu, atau alamat, lalu ubah teksnya sesuai dengan detail upacara Anda.
   - Untuk Google Maps, cari baris `<!-- Ganti src iframe di bawah ini... -->` dan ganti link URL `src="..."` di dalam tag `<iframe>` dengan embed link Google Maps rumah Anda, serta ubah link tombol navigasinya (`href="..."`).
