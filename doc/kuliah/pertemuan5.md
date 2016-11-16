**Sistem Informasi Geospasial**

**Create Shapefile**

 <p align="center">
  <img src="../../img/shapefile.png" width="400px">
</p>
Sebuah sistem informasi geografis (GIS atau) adalah sistem yang dirancang untuk menangkap, menyimpan, memanipulasi, menganalisis, mengelola, dan data spasial atau geografis hadir. Dan didalam geospsial terdapat  vector dn raster, didalam vector tersebut terdapat shapefile.

**Rumusan Masalah**

1. Jelaskan yang dimaksud dengan Shapefile
2. Bagaiamana cara untuk create shapefile
3. Sebutkan file yang terdapat pada shapefile
4. Jelaskan cara untuk menambahkan record pada shapefile

**Penjelasan**

1. Format shapefile adalah geospatial format data vektor populer untuk sistem informasi geografis (GIS) software dan  berfungsi untuk menyimpan lokasi geometric dan atribut informasi
2. Cara untuk create  shapefile  pyshp, caranya adalah  &#39;shapefile impor&#39; dan inisialisasi &#39;a = Shapefile.Writer ()&#39; di python dengan menggunakan python dan Plugin.
3. Pada shapefile terdapat SHP dan DBF

- SHP terdapat 3 tipe shapefile yaitu,

1. Point,
2.  Polyline
3. dan Polygon

- DBF, pertama field untuk atribut tabel, contoh &#39;a=field(&#39;kata&#39;,&#39;C&#39;,&#39;40&#39;)&#39;, kedua isinya pada method, contoh &#39;a.record(&#39;sarijadi&#39;)&#39;, ketiga a.save(&#39;file.shp&#39;) dimana file.shp nama file shapefie yang sebelumnya diinputkan

1. Cara menambahkan record

Pada Point = &#39;a.point(x,y)&#39; atau &#39;a.point(x,y,0,0)&#39; dengan domain x dan y adalah koordinat

**Penutup**

Kesimpulan

Pada pernyataan diatas dapat disimpulkan bahwa untuk create atau menambhakan  shapefile menggunakan python dan pyshp sangat mudah dan script yang sederhana

Saran

Saran saya pada pembahasan diatas lebih diperdalam lagi Karena sangat bermanfaat dalam dunia programmer