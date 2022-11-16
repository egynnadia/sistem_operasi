# NIM   :2110131220011
# NAMA  :Egyn Terescova Nadia

## Struktur Sistem Operasi

<p align="justify"> Struktur sistem operasi merupakan komponen-komponen sistem operasi yang dihubungkan dan dibentuk di dalam kernel.<br>
Sistem operasi sebagai kumpulan prosedur yang masing-masing dapat saling dipanggil jika dibutuhkan. Setiap prosedur yang ada di dalam sistem ini mempunyai interface yang sudah didefinisikan dengan baik.<br>

Terdapat 3 pendekatan/model struktur sistem operasi :

1. Struktur sederhana<br>
2. Pendekatan berlapis<br>
3. Mikrokernel<br>

</p>
   
### Struktur Sederhana

<p align="justify">
      Pada awalnya, sistem operasi merupakan sistem yang kecil, sederhana, dan terbatas. Seiring berjalannya waktu, sistem operasi semakin berkembang dengan ruang lingkup originalnya. Dalam perkembangan sistem struktur sederhana, terdapat sistem yang terstruktur dengan baik dan ada juga yang kurang baik.

Kelebihan Struktur Sederhana :

Layanan dapat dilakukan sangat cepat karena terdapat di satu ruang alamat.
Kekurangan Struktur Sederhana :

Pengujian dan penghilangan kesalahan sulit karena tidak dapat dipisahkan dan dilokalisasi.
Sulit dalam menyediakan fasilitas pengaman.
Pemborosan memori bila setiap komputer harus menjalan kernel, karena semua layanan tersimpan dalam bentuk tunggal sedangkan tidak semua layanan diperlukan.
Tidak fleksibel.
Kesalahahan sebagian fungsi menyebabkan matinya seluruh sistem.

Contoh sistem operasi yang memiliki struktur sederhana adalah MS-DOS dan UNIX.
</p>

### Struktur berlapis

<p align="justify">
Sistem operasi dibagi menjadi sejumlah lapisan yang masing-masing dibangun di atas lapisan yang lebih rendah. Lapisan yang lebih rendah menyediakan layanan untuk lapisan yang lebih tinggi. Lapisan yang paling bawah adalah perangkat keras, dan yang paling tinggi adalah user-interface.</p>

<p align="justify">Sebuah lapisan adalah implementasi dari objek abstrak yang merupakan enkapsulasi dari data dan operasi yang bisa memanipulasi data tersebut. Struktur berlapis dimaksudkan untuk mengurangi kompleksitas rancangan dan implementasi sistem operasi. Tiap lapisan mempunyai fungsional dan antarmuka masukan-keluaran antara dua lapisan bersebelahan. Struktur ini dibagi menjadi beberapa lapisan. Lapisan terbawah (layer 0) adalah hardware dan yang tertinggi (layer N) adalah user-interface. Lapisan N memberi layanan untuk lapisan N+1 sedangkan proses-proses di lapisan N dapat meminta layanan lapisan N-1 untuk membangun layanan lapisan N+1. Lapisan N dapat meminta layanan lapisan N-1 namun lapisan N tidak dapat meminta layanan lapisan N+1. Masing-masing berjalan pada lapisannya sendiri.</p>

<p align="justify">Menurut Tanenbaum dan Woodhull, sistem terlapis terdiri dari enam lapisan, yaitu:

Lapisan 0. Mengatur alokasi prosesor, pertukaran antar proses ketika interupsi terjadi atau waktu habis. Lapisan ini mendukung dasar multi-programming pada CPU.<br>
Lapisan 1. Mengalokasikan ruang untuk proses di memori utama dan pada 512 kilo word drum yang digunakan untuk menahan bagian proses ketika tidak ada ruang di memori utama.<br>
Lapisan 2. Menangani komunikasi antara masing-masing proses dan operator console. Pada lapis ini masing-masing proses secara efektif memiliki opertor console sendiri.<br>
Lapisan 3. Mengatur peranti M/K dan menampung informasi yang mengalir dari dan ke proses tersebut.<br>
Lapisan 4. Tempat program pengguna. Pengguna tidak perlu memikirkan tentang proses, memori, console, atau manajemen M/K.
Lapisan 5. Merupakan operator sistem.<br>
Menurut Stallings, model tingkatan sistem operasi yang mengaplikasikan prinsip ini terdiri dari beberapa level :</p>

<p align="justify">Level 1. Terdiri dari sirkuit elektronik dimana obyek yang ditangani adalah register memory cell, dan gerbang logika. Operasi pada objek ini seperti membersihkan register atau membaca lokasi memori.<br>
Level 2. Pada level ini adalah set instruksi pada prosesor. Operasinya adalah instruksi bahasa-mesin, seperti menambah, mengurangi, load dan store.<br>
Level 3. Tambahan konsep prosedur atau subrutin ditambah operasi call atau return.<br>
Level 4. Mengenalkan interupsi yang menyebabkan prosesor harus menyimpan perintah yang baru dijalankan dan memanggil rutin penanganan interupsi.<br>

Empat level pertama bukan bagian sistem operasi tetapi bagian perangkat keras. Meski pun demikian beberapa elemen sistem operasi mulai tampil pada level-level ini, seperti rutin penanganan interupsi. Pada level 5, kita mulai masuk kebagian sistem operasi dan konsepnya berhubungan dengan multi-programming.</p>

<p align="justify">Level 5. Level ini mengenalkan ide proses dalam mengeksekusi program. Kebutuhan-kebutuhan dasar pada sistem operasi untuk mendukung proses ganda termasuk kemampuan men-suspend dan me-resume proses. Hal ini membutuhkan register perangkat keras untuk menyimpan agar eksekusi bisa ditukar antara satu proses ke proses lainnya.<br>
Level 6. Mengatasi penyimpanan sekunder dari komputer. Level ini untuk menjadwalkan operasi dan menanggapi permintaan proses dalam melengkapi suatu proses.<br>
Level 7. Membuat alamat logik untuk proses. Level ini mengatur alamat virtual ke dalam blok yang bisa dipindahkan antara memori utama dan memori tambahan. Cara-cara yang sering dipakai adalah menggunakan ukuran halaman yang tetap, menggunakan segmen sepanjang variabelnya, dan menggunakan cara keduanya. Ketika blok yang dibutuhkan tidak ada dimemori utama, alamat logis pada level ini meminta transfer dari level 6.
Sampai point ini, sistem operasi mengatasi sumber daya dari prosesor tunggal. Mulai level 8, sistem operasi mengatasi obyek eksternal seperti peranti bagian luar, jaringan, dan sisipan komputer kepada jaringan.

Level 8. Mengatasi komunikasi informasi dan pesan-pesan antar proses. Dimana pada level 5 disediakan mekanisme penanda yang kuno yang memungkinkan untuk sinkronisasi proses, pada level ini mengatasi pembagian informasi yang lebih banyak. Salah satu peranti yang paling sesuai adalah pipe (pipa) yang menerima output suatu proses dan memberi input ke proses lain.<br>
Level 9. Mendukung penyimpanan jangka panjang yang disebut dengan berkas. Pada level ini, data dari penyimpanan sekunder ditampilkan pada tingkat abstrak, panjang variabel yang terpisah. Hal ini bertentangan tampilan yang berorientasikan perangkat keras dari penyimpanan sekunder.
Level 10. Menyediakan akses ke peranti eksternal menggunakan antarmuka standar.<br>
Level 11. Bertanggung-jawab mempertahankan hubungan antara internal dan eksternal identifier dari sumber daya dan obyek sistem. Eksternal identifier adalah nama yang bisa dimanfaatkan oleh aplikasi atau pengguna. Internal identifier adalah alamat atau indikasi lain yang bisa digunakan oleh level yang lebih rendah untuk meletakkan dan mengontrol obyek.<br>
Level 12. Menyediakan suatu fasilitator yang penuh tampilan untuk mendukung proses. Hal ini merupakan lanjutan dari yang telah disediakan pada level 5. Pada level 12, semua info yang dibutuhkan untuk manajemen proses dengan berurutan disediakan, termasuk alamat virtual diproses, daftar obyek dan proses yang berinteraksi dengan proses tersebut serta batasan interaksi tersebut, parameter yang harus dipenuhi proses saat pembentukan, dan karakteristik lain yang mungkin digunakan sistem operasi untuk mengontrol proses.<br>
Level 13. Menyediakan antarmuka dari sistem operasi dengan pengguna yang dianggap sebagai shell atau dinding karena memisahkan pengguna dengan sistem operasi dan menampilkan sistem operasi dengan sederhana sebagai kumpulan servis atau pelayanan.
Dapat disimpulkan bahwa lapisan sistem operasi secara umum terdiri atas empat bagian, yaitu:

Perangkat keras. Lebih berhubungan kepada perancang sistem. Lapisan ini mencakup lapisan 0 dan 1 menurut Tanenbaum, dan level 1 sampai dengan level 4 menurut Stallings.
Sistem operasi. Lebih berhubungan kepada programer. Lapisan ini mencakup lapisan 2 menurut Tanenbaum, dan level 5 sampai dengan level 7 menurut Stallings.
Kelengkapan. Lebih berhubungan kepada programer. Lapisan ini mencakup lapisan 3 menurut Tanenbaum, dan level 8 sampai dengan level 11 menurut Stallings.
Program aplikasi. Lebih berhubungan kepada pengguna aplikasi komputer. Lapisan ini mencakup lapisan 4 dan lapisan 5 menurut Tanebaum, dan level 12 dan level 13 menurut Stallings.

<b>Keunggulan Struktur berlapis :</b><br>
Karena sistem dibagi menjadi beberapa modul, tiap lapisan dapat dirancangdan diuji secara independen.
Mempermudah debug dan verifikasi sistem.
Lapisan pertama bisa didebug tanpa mengganggu sistem yang lain karenahanya menggunakan perangkat keras dasar untuk implementasi fungsinya.
Bila terjadi error saat debugging sejumlah lapisan, error pasti pada lapisan yang baru saja didebug, karena lapisan dibawahnya sudah di debug.

<b>Kelemahan Struktur berlapis:</b><br>
Fungsi-fungsi sistem operasi harus diberikan ke setiap lapisan secara hati-hati.
</p>

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