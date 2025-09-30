# People-Counter
Sistem People Counter berbasis Raspberry Pi dan webcam menggunakan YOLO untuk mendeteksi dan menghitung jumlah orang masuk/keluar ruangan secara realtime. Data dikirim ke Firebase untuk monitoring dan logging, mendukung analisis kepadatan pengunjung.

People-Counter adalah sistem deteksi dan penghitungan jumlah orang yang keluar dan masuk suatu ruangan menggunakan Raspberry Pi 4B dan webcam. Sistem ini memanfaatkan algoritma YOLO (You Only Look Once) untuk mendeteksi objek manusia secara real-time, lalu menghitung jumlah orang yang melintasi garis virtual (boundary line) di area pintu. Jika seseorang melintasi garis dari luar ke dalam ruangan, sistem akan mencatatnya sebagai masuk, sedangkan jika melewati garis dari dalam ke luar, sistem mencatatnya sebagai keluar. Data hasil deteksi kemudian diproses dan dikirimkan ke Firebase Realtime Database serta Firestore untuk kebutuhan monitoring realtime maupun logging historis

.

🔧 Fitur Utama
. Deteksi objek manusia menggunakan YOLOv8n-Segmentation yang dioptimalkan untuk Raspberry Pi
. Penghitungan jumlah orang masuk dan orang keluar menggunakan garis virtual.
. Visualisasi realtime melalui jendela webcam dengan informasi jumlah masuk, keluar, dan orang di dalam ruangan
. Penggunaan multi Raspberry Pi dengan ID unik untuk pemantauan di berbagai lokasi
. Integrasi Firebase:
  - Realtime Database → untuk data jumlah orang saat ini.
  - Firestore → untuk pencatatan historis per menit, per jam, dan rata-rata harian

.

📊 Pengujian & Performa
- Sistem diuji dengan berbagai skenario jarak (1–4 meter) dan kondisi posisi orang (tampak depan, belakang, dan samping).
- Akurasi mencapai 91,67% pada skenario 1 orang.
- Akurasi 82% pada skenario 5 orang

.

🖥️ Komponen
- Raspberry Pi 4B (pemrosesan utama).
- Webcam (input visual).
- YOLOv8n-Segmentation model untuk deteksi orang.
- Firebase (Realtime DB & Firestore) sebagai backend database

.

🚀 Potensi Pengembangan
- Integrasi dengan website dashboard untuk menampilkan data kepadatan secara realtime.
- Optimasi model deteksi agar lebih ringan dan cepat di perangkat edge.
- Penambahan sistem notifikasi jika jumlah orang di dalam ruangan melewati kapasitas maksimum.

Hasil
![Gambaran Alat People Counting](https://github.com/Harisna/People-Counter/blob/main/Alat%20People%20Counter.jpg?raw=true)
