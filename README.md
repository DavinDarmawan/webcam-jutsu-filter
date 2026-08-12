# Naruto & Sasuke Web Camera - Portal & Hand Tracking

Aplikasi berbasis web interaktif yang menggunakan teknologi pelacakan tangan (*hand tracking*) secara *real-time* dengan pustaka **MediaPipe Hands**. Proyek ini menampilkan efek jurus ikonik Naruto (Rasengan), Sasuke (Chidori), serta portal interaktif antar-tangan dengan 4 filter visual yang menarik.

## 🌟 Fitur Utama

- **🔥 Efek Jurus Karakter (Mode Asli):**
  - **Tangan Kiri Terbuka:** Mengeluarkan energi Rasengan (Naruto) yang mengikuti pergelangan tangan kiri Anda.
  - **Tangan Kanan Terbuka:** Mengeluarkan energi Chidori (Sasuke) yang menempel pada tangan kanan Anda.
  - **Visualisasi Kerangka (Skeleton):** Garis biru neon terang dan titik sendi putih yang presisi memperlihatkan *tracking* tangan Anda secara aktif.
- **🌀 Mode Portal Antar Tangan:**
  - Terpicu secara otomatis ketika mendeteksi **2 tangan** di layar secara bersamaan dengan posisi tangan tidak terbuka lebar (membentuk bingkai portal).
  - Portal interaktif akan terbentuk di dalam area yang dibatasi oleh ujung jari telunjuk dan jempol kedua tangan Anda.
- **⚡ Deteksi Cubitan (*Pinch*) untuk Ganti Filter:**
  - Satukan/cubit ujung jari telunjuk dengan jempol Anda untuk berpindah secara dinamis di antara 4 filter visual premium.
- **🎨 Efek Glow & Kerangka Tangan Khusus:**
  - Pada mode portal, titik sendi dihilangkan sehingga menyisakan garis kerangka tangan bersih yang bercahaya (*glowing*) dengan warna yang menyesuaikan tema filter aktif.

## 🎨 Filter Portal yang Tersedia

1. **Comic Pop-Art:** Mengubah visual di dalam portal menjadi gaya seni komik retro berwarna oranye cerah, merah muda neon, dan hitam.
2. **Halftone Dot Matrix:** Menghasilkan pola titik-titik koran klasik hitam-putih yang ukurannya berubah sesuai pencahayaan objek.
3. **RGB Glitch & Scanlines:** Efek distorsi/gangguan visual (glitch) aberasi kromatik pergeseran warna merah-sian ditambah hamparan garis pemindai (*scanlines*).
4. **Thermal Heatmap:** Visualisasi peta suhu panas-dingin futuristik yang dinamis berdasarkan tingkat kecerahan gambar.

## 🚀 Cara Menjalankan

Karena aplikasi ini dimuat ke repositori publik GitHub, Anda dapat membukanya secara lokal atau melalui GitHub Pages jika dikonfigurasi:

### Cara 1: Menjalankan Secara Lokal (Local File)
1. Unduh atau *clone* repositori ini ke komputer Anda:
   ```bash
   git clone https://github.com/USERNAME/naruto.git
   ```
2. Pastikan Anda memiliki folder `assets` yang berisi video aset `naruto.mp4` dan `sasuke.mp4`.
3. Buka file `index.html` menggunakan peramban web modern (*Google Chrome*, *Microsoft Edge*, atau *Mozilla Firefox*).
4. Berikan izin akses kamera web (*webcam*) ketika peramban memintanya.

### Cara 2: Menggunakan Server Lokal (Direkomendasikan)
Untuk performa dan kompatibilitas modul peramban yang lebih baik, gunakan ekstensi seperti **Live Server** di VS Code atau server python sederhana:
```bash
# Untuk pengguna Python
python -m http.server 8000
```
Lalu buka `http://localhost:8000` di peramban Anda.

## 🛠️ Teknologi yang Digunakan

* **HTML5 & CSS3** (Vanilla UI dengan performa tinggi)
* **JavaScript (ES6+)**
* **MediaPipe Hands** (Untuk deteksi sendi & pelacakan tangan)
* **MediaPipe Camera Utils** (Untuk menangani masukan kamera web secara *real-time*)
* **HTML5 Canvas API** (Untuk pemrosesan piksel filter gambar secara langsung/instan)

---
*Catatan: Pastikan ruangan Anda memiliki pencahayaan yang cukup agar deteksi kamera dapat mengenali sendi tangan dengan optimal.*

## 👥 Kredit & Atribusi

Proyek ini dikembangkan lebih lanjut berdasarkan repositori asli:
* **Repositori Asal:** [gprem09/naruto](https://github.com/gprem09/naruto) (Menggunakan dasar pelacakan tangan MediaPipe dengan efek jurus).