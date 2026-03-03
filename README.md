# Week 1
Pada repository ISB-310BB_Tugas digunakan sebagai tempat submission kode program, disini saya mengambil kasus terkait Sistem Manajemen Rental Kendaraan dengan nama NARENT.
## 1. Susunan Folder
   Terdapat folder utama dengan nama narent, didalamnya terdapat beberapa folder dan file, diantaranya
   1.1. /armada/
        Folder ini digunakan sebagai tempat menyimpan halaman ke-dua khusus untuk armada, salah satunya ada halaman grandpriorityclass.html
   1.2. /assets/
        Folder ini digunakan sebagai tempat menyimpan asset khususnya gambar dalam format .jpg atau .png.
   1.3. /css
        Folder ini digunakan sebagai tempat menyimpan styling dari kode menggunakan .css.
   1.4. index.html
        File ini merupakan kode untuk halaman utama.
## 2. Penjelasan Kode
   Pada project ini terdapat 3 file kode yang digunakan, diantaranya
   2.1. index.html
        File ini merupakan file kode yang menggunakan HTML, dimana pada bagian <head> berisikan kode untuk title halaman dan referensi css atau bootsrap. Selain itu, ada bagian <body> yang terbagi menjadi 5 bagian. Pertama, bagian ini (<nav>) merupakan bagian yang digunakan sebagai navbar dengan 6 bagian navigasi. Kedua, bagian ini (<div class="hero...">) merupakan bagian yang digunakan untuk bagian hero atau header halaman untuk judul dan deskripsi sistem. Ketiga, bagian ini (<div class="daftar...">) merupakan bagian Section Product yang menampilkan produk-produk yang disediakan dengan jumlah 3 produk menggunakan card. Keempat, bagian ini (<div class="tambah...">) merupakan bagian Form input data yang digunakan untuk menambahkan data produk dengan 4 kolom input. Serta kelima, bagian ini (<footer...>) merupakan bagian footer yang berisikan mulai dari logo, letak, kontak, layanan rental, armada, bantuan, hingga metode pembayaran.
   2.2. /armada/grandpriorityclass.html
        File ini merupakan file kode yang menggunakan HTML, dimana pada bagian <head> berisikan kode untuk title halaman dan referensi css atau bootsrap. Selain itu, ada bagian <body> yang terbagi menjadi 4 bagian. Pertama, bagian ini (<nav>) merupakan bagian yang digunakan sebagai navbar dengan 6 bagian navigasi. Kedua, bagian ini (<div class="armada...">) merupakan bagian yang digunakan untuk judul dan deskripsi armada. Ketiga, bagian ini (<div class="gpc...">) merupakan bagian yang digunakan untuk fasilitas dan deskripsi fasilitas armada. Serta keempat, bagian ini (<footer...>) merupakan bagian footer yang berisikan mulai dari logo, letak, kontak, layanan rental, armada, bantuan, hingga metode pembayaran.
   2.3. /css/style.css
        File ini merupakan file kode CSS, yang berguna untuk men-styling kode html. Mulai dari bagian body, header, hero, navbar, card, hingga footer.


# Week 2
Pada minggu ini dipelajari terhait javascript, dengan tugas di minggu ini melanjutkan studi kasus yang diambil kemarin dengan penyesuaiian pada HTML dan penambahan file baru yaitu scipt.js yang berisikan beberapa fungsi di antaranya
1. Mengubah Tema pada Tampilan Web
   Berfungsi untuk mengubah tema dari tampilan web berdasarkan kemauan pengguna dengan memanfaatkan pengubahan pada css pada elemen body dan penggunaan localStorange. Melalui fungsi updateIcon(), sistem secara dinamis mengubah logo matahari dan bulan untuk memberikan petunjuk visual yang jelas. Selain itu, dengan menggunakan localStorange, tema yang dipilih tidak akan berubah ketika melakukan refresh atau close tab.
2. Melakukan Aksi pada Button Sewa atau Wishlist.
   Berfungsi untuk aksi dari ketika button sewa atau wishlist di klik. Pada bagian sewa, sistem akan mengambil data stok secara real-time, mengurangi satu per satu, dan menonaktifkan tombol secara otomatis jika armada telah habis. Sementara itu, pada bagian wishlist akan mengambil data detail armada seperti nama, harga, dan gambar dari card untuk kemudian disimpan ke dalam dataWishlist.
3. Mengubah Wishlist
   Fungsi rubahWishlist() membangun elemen daftar secara prosedural menggunakan createElement sehingga bisa tanpa menggunakan innerHTML/string HTML secara manual. Selain memperbarui tampilan daftar wishlist, fungsi ini juga secara otomatis menghitung total seluruh wishlist untuk memperbarui angka pada ikon keranjang di navbar.
4. Menampilkan Wishlist
   Fungsi tampilkanWishlist() berguna untuk memicu tampilan berbentuk modal untuk wishlist. Dengan memanfaatkan framework Bootstrap, fungsi ini menginisialisasi objek modal berdsarkan id elemen (wishlistModal) yang ada di HTML dan memunculkan modal ke tengah layar yang memungkinkan pengguna untuk melihat ada apa saja pada wishlist-nya.
5. Menghapus Keseluruhan Wishlist
   Melalui fungsi hapusWishlist(), sistem akan mengosongkan array dataWishlist, mereset tampilan angka pada ikon keranjang di navbar, dan menutup modal secara otomatis.
6. Menghapus Data Wishlist Tertentu
   Fungsi hapusItemSpesifik() bekerja dengan mengecek data dengan indeks tertentu pada array dataWishlist, jika memiliki lebih dari 1, maka hanya jumlahnya dikurangi, namun jika tinggal 1, maka wishlist tersebut akan dihapus menggunakan metode splice. Setelah perubahan data selesai, sistem secara otomatis memanggil kembali fungsi rubahWishlist() untuk memperbarui tampilan modal. 
