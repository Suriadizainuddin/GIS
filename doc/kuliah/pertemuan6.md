**Sistem Informasi Geografis**

**Shapefile**

 <p align="center">
  <img src="../../img/shapefilee.jpg" width="400px">
</p>

Sebuah sistem informasi geografis (GIS atau) adalah sistem yang dirancang untuk menangkap, menyimpan, memanipulasi, menganalisis, mengelola, dan data spasial atau geografis hadir. Dan didalam geospsial terdapat  vector dn raster, didalam vector tersebut terdapat shapefile.

**Rumusan Masalah**

1. Jelaskan cara create Shapefile
2. Jelaskan cara edit Shapefile
3. Jelaskan cara menghapus Shapefile
4. Jelaskan cara menampilkan Shapefile

**Penjelasan**

1. Create Shapefile

a. --Buka python di command prompt
b. --import shapefile
c. --sf = shapefile.Writer(shapeType=1)
d. --sf.shapeType -&gt; untuk mengecek
e. --sf.field(&#39;NAMA&#39;,&#39;C&#39;,&#39;40&#39;)
f. --sf.field(&#39;PEMILIK&#39;,&#39;C&#39;,&#39;40&#39;)
g. --sf.record(&#39;Poltekpos,&#39;Suriadi Zainuddin&#39;)
h. --sf.point(10,10,0,0) -&gt; disini point bisa diganti line atau polygon sesuai keinginan
i. --sf.save(&#39;poltekpos.shp&#39;) -&gt; untuk menyimpan

2. Edit Shapefile

a. --Buka python di command prompt
b. --import shapefile
c. --sf = shapefile.Editor(shapefile=&#39;poltekpos.shp&#39;)
d. --sf.point(19,19,0,0)
f. --sf.record(&#39;Warung Sunda,&#39;Adi&#39;)
g. --sf.save(&#39;warung&#39;)

3. Menghapus Shapefile

a. --Buka python di command prompt
b. --import shapefile
c. --e = shapefile.Editor(&#39;warung.shp&#39;)
d. --e.shape(1) -&gt; record ke berapa
e. --e.delete(1)
f. --e.save(&#39;warung&#39;)

4. Menampilkan Shapefile


a. --Buka python di command prompt
b. --import shapefile
c. --sf = shapefile.Reader(&#39;warung.shp&#39;)
d. --sf.record() -&gt; semua record
e. --sf.record(0) -&gt; record ke 1
f. --sf.record(1) -&gt; record ke 2
g. --sf.shapes()(0).points -&gt; menampilkan

Penutup

Kesimpulan

Kesimpulan Dari pernyataan diatas dapat disimpulkan bahwa dalam data geometri shapefile dapat melakukan penambahan , pengeditan, penghapusan dan penampilan data geometri shapefile dengan mudah menggunakan python

Saran

Untuk proses diatas cukuplah mudah Karena hanya menggunakan program pythom