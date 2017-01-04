**Konfigurasi MapProxy**

<p align="center">
  <img src="../../img/10.png" width="400px">
</p>

1. Jelaskan pengertian MapProxy
2. Cara install MapProxy
3. Cara Konfigurasi MapProxy

**Pembahasan**

1. Map Proxy adalah program yang berfungsi untuk menampung hasil gambar dari map server agar konsumsi komputer bisa di reduksi
2. Cara install MapProxy

 --Ketikkan &quot;#install python-pip dan python-dev&quot;
 --Lalu &quot;#pip install mapproxy
 --Setelah itu ketikkan &quot;#install Vwsqi&quot;
 --Tunggu hingga proses selesai

3. Cara Konfigurasi MapProxy

Ada dua file konfigurasi yang digunakan oleh MapProxy.

mappproxy.yaml

Ini adalah konfigurasi utama MapProxy. Ini mengkonfigurasi semua aspek server: Yang server harus dimulai, di mana berasal data dari, apa yang harus di-cache.

seed.yaml

File ini adalah konfigurasi untuk alat mapproxy-benih. Lihat penyemaian dokumentasi untuk informasi lebih lanjut.

Konfigurasi ini menggunakan format YAML. Wikipedia berisi pengenalan yang baik untuk YAML. Konfigurasi MapProxy dikelompokkan menjadi beberapa bagian, masing-masing mengkonfigurasi aspek yang berbeda dari MapProxy. Ini adalah bagian berikut:

•        GLOBALS: Internal dari MapProxy dan nilai-nilai default yang digunakan dalam bagian

konfigurasi lainnya.

•        Layanan: Layanan MapProxy penawaran, misalnya WMS atau TMS.

•        sumber: Tentukan mana MapProxy dapat mengambil data baru.

•        cache: Konfigurasi cache internal.

•        lapisan: Konfigurasi lapisan yang MapProxy menawarkan. Setiap lapisan dapat terdiri dari

beberapa sumber dan cache.

•        grid: Tentukan grid yang menggunakan MapProxy untuk menyelaraskan gambar cache.

Urutan bagian tidak penting, sehingga Anda dapat mengatur dengan cara Anda.

Untuk membuat satu set baru file konfigurasi untuk MapProxy panggilan:

mapproxy-util create -t base-config mymapproxy

Ini akan membuat direktori mymapproxy dengan contoh konfigurasi minimal (mapproxy.yaml dan seed.yaml) dan dua file konfigurasi contoh lengkap (full\_example.yaml dan full\_seed\_example.yaml).

Lihat dokumentasi konfigurasi untuk informasi lebih lanjut. Dengan konfigurasi default data cache akan ditempatkan di subdirektori cache\_data.

Untuk memulai server tes:

cd mymapproxy
mapproxy-util serve-develop mapproxy.yaml

Sudah ada lapisan tes dikonfigurasi yang mendapatkan data dari Omniscale OpenStreetMap WMS. Jangan ragu untuk menggunakan layanan ini untuk pengujian.

MapProxy dilengkapi dengan layanan demo yang berisi daftar WMS semua dikonfigurasi dan lapisan TMS. Anda dapat mengakses layanan yang di http: // localhost: 8080 / demo /.

**Penutup**

**Kesimpulan**

MapProxy Ini mengkonfigurasi semua aspek server: Yang server harus dimulai, di mana berasal data dari, apa yang harus di-cache.

**Penutup**

Pelejari lebih dalam agar dapat di mengerti dan dipahami serta lakukan praktikum