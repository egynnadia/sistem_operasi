# NIM   :2110131220011
# NAMA  :Egyn Terescova Nadia

## Struktur Sistem Operasi

<p align="justify"> Struktur sistem operasi merupakan komponen-komponen sistem operasi yang dihubungkan dan dibentuk di dalam kernel.<br>
Sistem operasi sebagai kumpulan prosedur yang masing-masing dapat saling dipanggil jika dibutuhkan. Setiap prosedur yang ada di dalam sistem ini mempunyai interface yang sudah didefinisikan dengan baik.<br>

Struktur tersebut adalah :<br>

1. Program utama yang meminta layanan prosedur.<br>

2. Kumpulan layanan prosedur yang membawa sistem call .<br>

3. Kumpulan utilitas prosedur yang membantu layanan prosedur.<br></p>
   
### Mesin Virtual

<p align="justify">Secara konsep, sistem computer dibuat berdasarkan lapisan. Hardware atau perangkat lunak merupakan tingkatan terbawah dari keseluruhan sistem. Kernel yang berjalan ditingkatan berikutnya menggunakan instruksi-intruksi perangkat keras untuk membuat kumpulan sistem call yang digunakan oleh lapisan luarnya. Program di atas kernel dapat menggunakan sistem call atau instruksi-instruksi perangkat keras. Dalam beberapa hal,program sistem tidak membedakan kedua lapisan tersebut.</p>

### Struktur berlapis

<p align="justify">Lapisan-lapisan sistem operasi adalah suatu abstraksi dari enkapsulasi sekumpulan struktur data dalam sistem operasi. Lapisan-lapisan yang berada di atas bisa mengakses operasi-operasi yang tersedia di lapisan-lapisan bawahnya.<br>

1. Lapisan 1. Berisi berbagai sirkuit elektronik, misal register, memory cells, dan logic gate.

2. Lapisan 2. Berisi instruksi prosesor, misal instruksi aritmatika, instruksi transfer data, dsb.

3. Lapisan 3. Penambahan konsep seperti prosedur/subrutin, maupun fungsi yang me-return nilai tertentu.

4. Lapisan 4. Penambahan interrupt.

5. Lapisan 5. Program sebagai sekumpulan instruksi yang dijalankan oleh prosesor.

6. Lapisan 6. Berhubungan dengan secondary storage device, yaitu membaca/menulis head, track, dan sektor.

7. Lapisan 7. Menciptakan alamat logika untuk proses. Mengatur hubungan antara main memory, virtual memory, dan secondary memory.

8. Lapisan 8. Program sebagai sekumpulan instruksi yang dijalankan oleh prosesor.

9. Lapisan 9. Berhubungan dengan secondary storage device, yaitu membaca/menulis head,track, dan sektor.

10. Lapisan 10. Menciptakan alamat logika untuk proses. Mengatur hubungan antara main memory, virtual memory, dan secondary memory.

11. Lapisan 11. Program sebagai sekumpulan instruksi yang dijalankan oleh prosesor.

12. Lapisan 12. File adalah objek yang memiliki nama dan ukuran. Abstraksi dari lapisan 9.

13. Lapisan 13. Menyediakan interface agar bisa berinteraksi dengan pengguna<br>

Lapisan-lapisan dari 1-4 bukanlah bagian dari sistem operasi dan masih menjadi bagian dari prosesor secara ekslusif. Lapisan ke-5 hingga ke-7, sistem operasi sudah berhubungan dengan prosesor lapisan ke-8 hingga 13, sistem operasi berhubungan dengan media penyimpanan maupun perlatan-peralatan lain yang ditancapkan, misalnya peralatan jaringan.</p>

### Mikro Kernel

<p align="justify">Kernel merupakan program komputer yang menjadi inti dari sebuah sistem operasi komputer,dengan kontrol terhadap segala hal atas sistem tsb.<br>
mikrokernel merupakan seperangkat perangkat lunak dalam jumlah minimum yang meyediakan beragam mekanisme dasar yang dibutuhkan untuk bekerja sebagai sebuah sistem operasi, mengeluarkan semua komponen yang tidak esensial.<br>
fungsi utama mikro kernel adalah mendukung fasilitas komunikasi antar program client dan bermacam macam layanan secara tidak langsung oleh message-passing...tugasnya yaitu melayani bermacam macam program aplikasi untuk mengakses hardware secara aman.<br>
contoh yang makai mikro kernel: unix,TRU64 unix, macosX dan qnx<br>
sebuah mikrokernel harus dapat meletakkan layanan-layanan sistem operasi pada tingkat yang paling atas<br>
berikut adalah ruang fungsionalitas yang harus dimiliki mikrokernel<br>
1. Sistem pengalamatan ruang dibtukan untuk mengatur proteksi ingatan<br>
2. Fungsi eksekusi secara abstrak untuk mengalokasi cpu yang biasanya adalah thread atau pengaktifan jadwal<br>
3. komunikasi antar proses<br>
kekurangan mikrokernel saat penambahan atau memodifikasi layanan memerlukan biaya tambahan dan bisa berimbas penurunan kinerja sistem.