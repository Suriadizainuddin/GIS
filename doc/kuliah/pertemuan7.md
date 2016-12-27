**MapServer dan Map Proxy**


 <p align="center">
  <img src="../../img/7.png" width="400px">
</p>

1. Jelaskan yang dimaksud dengan MapServer?
2. Bagaimana cara kerja MapServer?
3. Jelaskan fungsi MapServer?
4. Bagaimana cara install MapServer?
5. Jelaskan yang di maksud dengan Map Proxy?
6. Bagaimana cara install Map proxy?
7. Bagaimana cara testing?

Penjelasan

1. MapServer adalah applikasi _Open Source_ yang memungkinkan sebuah data peta diakses melalui web kemudian mapserver membuat peta lebih mudah dan lebih interaktif.
2. Map Server bekerja secara berdampingan dengan applikasi web server. Web Server menerima request peta melalui MapServer.
3.  Fungsi utama dari MapServer adalah melakukan pembacaan data dari banyak sumber dan menempatkannya kedalam layer-layer secara bersamaan menjadi file graphic.
4. Cara install

1.  Jika tidak ada centos maka jalankan saja di virtual box, ISO centos dan virtual box ada di halaman download
2.  Setelah itu pastikan koneksi jaringan virtual box bisa diakses dari komputer host
3. Dicentos buka terminal, login sebagai root
4.  #install mapserver
5.  Selesai

1. Map Proxy adalah program yang berfungsi untuk menampung hasil gambar dari map server agar konsumsi komputer bisa di reduksi
2. Cara Install

1.  Install python-pip dan python-dev
2.  #install python-pip dan python-dev
3.  pip Install mapproxy
4.  #install mapproxy
5.  Install Vwsqi
6.  #install Vwsqi

1. Testing

1. Download peta Indonesia beserta map proxy konfigurasinya di Halaman Download simpan di folder/var
2.  Jalankan map proxy dengan cara ketik perintah #vwsqi map proxy ini
3.  Peta seudah bisa diakses di browser localhost

Penutup

 Kesimpulan Dari pernyataan diatas dapat disimpulkan bahwa dalam konfigurasi map server dan map proxy cukup mudah dengan menggunakan python karena pluginnya sudah tersedia

Saran

Sebaiknya kita sedikit mempelajari lebih dalam tentang map server dan map      proxy agar lebih mengerti apa itu map proxy dan map server