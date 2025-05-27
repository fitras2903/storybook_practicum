# 📘 Storybook Practicum – Flutter Interactive Story

Storybook Practicum adalah aplikasi Flutter sederhana yang dirancang sebagai buku cerita interaktif. Aplikasi ini terdiri dari 3 halaman utama: halaman judul, halaman cerita interaktif, dan halaman akhir. Pengguna dapat melakukan gesture seperti double tap, long press, drag-and-drop, dan zoom untuk berinteraksi dengan karakter dan objek di dalam cerita.

## 🧩 Fitur Aplikasi

- 🎬 **Halaman Judul** – Tampilkan judul cerita dan tombol mulai.
- 🪐 **Halaman Cerita** – Latar angkasa yang bisa di-zoom dan digeser. Interaksi mencakup:
  - 👩‍🚀 **Double Tap** pada karakter astronaut untuk menampilkan dialog.
  - 📦 **Long Press** pada peti untuk melihat petunjuk.
  - 🔑 **Drag-and-Drop** kunci ke peti untuk membukanya.
  - 🔍 **InteractiveViewer** untuk zoom dan pan latar belakang.
- 🎉 **Halaman Akhir** – Muncul setelah peti dibuka.

## 📸 Cuplikan Layar

| Halaman Judul                     | Halaman Interaktif                | Halaman Akhir                   |
| --------------------------------- | --------------------------------- | ------------------------------- |
| ![title](images/Screenshot_1.png) | ![scene](images/Screenshot_2.png) | ![end](images/Screenshot_3.png) |


## 🚀 Cara Menjalankan

1. **Clone repo ini:**

   ```bash
   git clone https://github.com/username/storybook_practicum.git
   cd storybook_practicum
   ```

## 📘 Laporan Langkah-Langkah Proyek storybook_practicum

1.	Buat proyek flutter baru → storybook_practicum
    ![](images/langkah1.png)
2.	Membuka proyek di code editor (VS Code/Android Studio)
    ![]images/langkah2.png)
3.	Di dalam lib buat folder pages di dalamnya terdapat 3 files: title_page.dart, scene_page.dart, end_page.dart
    ![](images/langkah3.png)
4.	Buka lib/main.dart dan ganti isinya untuk membuat struktur PageView.
    ![](images/langkah4.png)
5.	Untuk mencegah error, isi setiap file di folder pages dengan StatelessWidget boilerplate sederhana. Contoh untuk title_page.dart
    ![](images/langkah5.png)
6.	Lakukan hal yang sama untuk scene_page.dart dan end_page.dart, cukup tampilkan teks judul halaman.
7.	Fokus pada lib/pages/scene_page.dart → ganti isinya dengan kerangka StatefulWidget
    ![](images/langkah7.png)
8.	Tambahkan Astronaut & Balon Dialog (Double Tap). Di dalam Stack, tambahkan Positioned untuk astronaut
    ![](images/langkah8.png)
9.	Tambahkan Peti & Petunjuk (Long Press). Di dalam Stack, tambahkan Positioned untuk peti.
    ![](images/langkah9.png)
10.	Tambahkan Kunci & Logika Drag-and-Drop. Di dalam Stack, tambahkan Positioned untuk kunci.
    ![](images/langkah10.png)
11.	Hot Reload & Uji Coba: Coba semua interaksi: double tap astronaut, long press peti, dan geser kunci ke peti
    ![](images/langkah11.png)
12.	Efek Visual (InkWell) → Buka lib/pages/title_page.dart, Bungkus ElevatedButton dengan Card dan InkWell untuk efek yang lebih bagus.
    ![](images/langkah12.png)
13. Kita akan membuat latar belakang bisa digeser sedikit secara horizontal atau vertikal (seperti melihat lewat teleskop), tapi tidak keduanya sekaligus.
14.	ke lib/pages/scene_page.dart, modifikasi Container latar belakang. Pertama, tambahkan Offset untuk posisi background di State.
    ![](images/langkah14.png)
15.	Bungkus Container latar belakang dengan RawGestureDetector dan Transform.
    ![](images/langkah15.png)
16.	Ujicoba: Coba geser latar belakang. Kalian hanya bisa menggesernya di satu sumbu (horizontal atau vertikal) dalam satu waktu.
    ![](images/langkah16.png)
17.	Fungsionalitas Zoom dengan InteractiveViewer
18.	Di lib/pages/scene_page.dart, bungkus seluruh Stack dengan widget InteractiveViewer
    ![](images/langkah18.png)
19.	Hot Reload dan seluruh adegan interaktif bisa di-zoom dan di-pan dengan mudah.

