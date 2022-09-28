# Langkah kerja membuat Making Map

Langkah –langkah membuat MarkingMap
1.	Kita  download terlebih dahulu Natural Earth quick start
2.	Kemudian klik properties -> variable dan cari project_languenge (nama_en) Kemudian kita refresh
3.	Klik layer kemudian centang bagian z5 1:18m 
4.	Klik project -> new print layout (ctrl p)
5.	Di jendela Tata Letak Cetak, klik tombol penuh Zoom untuk menampilkan seluruh tata letak.
6.	Sekarang kita harus membawa tampilan peta yang kita lihat di Kanvas QGIS ke tata letak. Pergi ke Tambahkan Item ->add map.
7.	Setelah klik add map aktif, tahan tombol kiri mouse dan seret persegi panjang tempat Anda ingin memasukkan peta.
8.	Gunakan Edit -> Pilih/Pindahkan item dan Edit -> Pindahkan opsi Konten untuk menggeser peta di jendela dan memusatkannya di komposer.
9.	Kemudian kita  menyesuaikan tingkat zoom untuk peta. Klik pada tab Properti Item dan masukkan 100000000 sebagai nilai Skala.
10.	Sekarang kita akan menambahkan inset peta yang menunjukkan tampilan yang diperbesar untuk area Tokyo. Sebelum kita membuat perubahan apa pun pada layer di jendela QGIS utama, centang kotak Lock layers dan Lock styles untuk layers. Ini akan memastikan bahwa jika kita mematikan beberapa layer atau mengubah gaya mereka, tampilan ini tidak akan berubah.
11.	Kemudian Alihkan jendela Tata Letak Cetak. lalu Tambahkan Item ->Tambahkan Peta.
12.	Seret persegi panjang di tempat kita ingin menambahkan inset peta.kita sekarang akan melihat bahwa kita memiliki 2 objek peta di Tata Letak Cetak. Saat membuat perubahan, pastikan Anda telah memilih peta yang benar.
13.	Pilih objek Map 2 yang baru saja kita tambahkan dari panel Items. Pilih tab Properti item. Gulir ke bawah ke panel Bingkai dan centang kotak di sebelahnya. kita dapat mengubah warna dan ketebalan batas bingkai sehingga mudah dibedakan dengan latar belakang peta.
14.	Salah satu fitur yang rapi dari Print Layout adalah dapat secara otomatis menyorot area dari peta utama yang diwakili dalam inset. Pilih objek Peta 1 dari panel Item. Di tab Properti item, gulir ke bawah ke bagian Gambaran Umum. Klik tombol Tambahkan gambaran umum baru.
15.	Pilih Peta 2 sebagai Bingkai Peta. Ini memberi tahu Tata Letak Cetak untuk menyorot objek saat ini Peta 1 dengan luas peta yang ditunjukkan pada objek Peta 2.
16.	Sekarang setelah kita menyiapkan inset peta, kita akan menambahkan grid ke peta utama. Pilih objek Peta 1 dari panel Item. Di tab Properti item, gulir ke bawah ke bagian Kisi. Klik tombol Tambahkan kisi baru, diikuti oleh Ubah kisi.
17.	Secara default, garis kisi menggunakan unit dan proyeksi yang sama dengan proyeksi peta yang saat ini dipilih. Namun, lebih umum dan berguna untuk menampilkan garis kisi dalam derajat. Kita dapat memilih CRS yang berbeda untuk grid. Klik pada Perubahan... di sebelah CRS.
18.	Pilih nilai Interval sebagai 5 derajat dalam arah X dan Y. kita dapat menyesuaikan Offset untuk mengubah di mana garis kisi muncul.
19.	Gulir ke bawah ke bagian Bingkai kisi dan centang kotak Gambar koordinat. Format default adalah Derajat tetapi muncul sebagai angka. Kita dapat menyesuaikan adalah menambahkan simbol ° . Pilih Kustom dan klik tombol Ekspresi di sampingnya.
20.	Masukkan ekspresi berikut untuk membuat string yang mengambil nomor kisi dan menambahkan simbol ° ke dalamnya
concat(to_string(@grid_number), '°    ')
21.	Sekarang kita akan menambahkan bingkai Persegi Panjang untuk menahan elemen peta lain seperti panah utara, skala dan label. Pergi ke Tambahkan Item -> Tambahkan Bentuk ‣ Tambahkan Persegi Panjang.
22.	Anda dapat mengubah Gaya persegi panjang agar sesuai dengan latar belakang peta.
23.	Sekarang kita akan menambahkan Panah Utara ke peta. QGIS hadir dengan koleksi gambar terkait peta yang bagus termasuk banyak jenis Panah Utara. Klik Tambahkan Item -> Tambahkan Gambar.
24.	Sambil menahan tombol kiri mouse, gambar persegi panjang. Di panel sebelah kanan, klik pada tab Properti Item dan perluas bagian Direktori pencarian dan pilih gambar yang Anda sukai.
25.	Sekarang kita akan menambahkan bilah skala. Klik Tambahkan Item ‣ Tambahkan Scalebar.
26.	Klik pada tata letak di mana Anda ingin bilah skala muncul. Di tab Properti Item, pastikan Anda telah memilih elemen peta yang benar Peta 1 untuk menampilkan bilah skala. Pilih Gaya yang sesuai dengan kebutuhan Anda. Di panel Segmen, ubah Lebar tetap menjadi 200 unit dan sesuaikan segmen sesuai keinginan Anda.
27.	Sudah waktunya untuk memberi label pada peta kita. Klik Tambahkan Item -> Tambahkan Label.
28.	Klik pada peta dan gambar kotak di mana label seharusnya berada. Di tab Properti Item, perluas bagian Label dan masukkan label untuk peta. Demikian pula tambahkan label lain untuk kredit data dan perangkat lunak.
29.	Setelah kita puas dengan peta, Anda dapat mengekspornya sebagai Gambar, PDF atau SVG. Untuk tutorial ini, mari kita ekspor sebagai gambar. Klik Tata Letak -> Ekspor sebagai Gambar.
30.	Simpan gambar dalam format yang Anda sukai. Di bawah ini adalah gambar PNG yang diekspor.


Hasil Map 
https://github.com/miaaprilia18/SIG-Teori-MakingMap/blob/main/Hasil%20map.jpeg
 


