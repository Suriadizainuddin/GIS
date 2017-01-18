**Overlay**

<p align="center">
  <img src="../../img/overley.jpg" width="400px">
</p>

 
1. Apa itu Open Layer?
2. Apa yang dimaksud Marker?
3. Bagaimana cara menampilkan marker menggunakan Open Layer?

Pembahasan

1. Open Layer adalah library javascript murni untuk menampilkan data peta di berbagai browser, tanpa server side dependencies. Open Layer mengimplementasikan javascript API untuk membangun rich web-based geographic application yang mirip dengan Google Maps dan MSN Virtual Earth APIS
2. Marker atau penanda genetic merupakan penciri individu yang dilihat oleh mata atau terdeteksi dengan alat tertentu yang menunjukkan genotype suatu individu. Di dalam sebuah peta atau maps, marker adalah suatu tanda yang menjelaskan atau memberitahukan suatu tempat atau wilayah agar user mengetahui lokasi yang dimaksud
3. Cara membuat marker dengan open layer terdiri dari:

<!DOCTYPE html>
<html>
  <head>
    <title>Overlay</title>
    <link rel="stylesheet" href="https://openlayers.org/en/v3.20.1/css/ol.css" type="text/css">
    <!-- The line below is only needed for old environments like Internet Explorer and Android 4.x -->
    <script src="https://cdn.polyfill.io/v2/polyfill.min.js?features=requestAnimationFrame,Element.prototype.classList,URL"></script>
    <script src="https://openlayers.org/en/v3.20.1/build/ol.js"></script>
    <script src="https://code.jquery.com/jquery-2.2.3.min.js"></script>
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/css/bootstrap.min.css">
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/js/bootstrap.min.js"></script>
    <style>
      #marker {
        width: 20px;
        height: 20px;
        border: 1px solid #088;
        border-radius: 10px;
        background-color: #FF3300;
        opacity: 0.5;
      }
      #marker2 {
        width: 20px;
        height: 20px;
        border: 1px solid #088;
        border-radius: 10px;
        background-color: #FF3300;
        opacity: 0.5;
      }
      #bandung {
        text-decoration: none;
        color: black;
        font-size: 11pt;
        font-weight: bold;
        text-shadow: white 0.1em 0.1em 0.2em;
      }
      #bulukumba {
        text-decoration: none;
        color: black;
        font-size: 11pt;
        font-weight: bold;
        text-shadow: white 0.1em 0.1em 0.2em;
      }
      .popover-content {
        min-width: 180px;
      }
    </style>
  </head>
  <body>
    <div id="map" class="map"></div>
    <div style="display: none;">
      <!-- Clickable label -->
      <a class="overlay" id="bandung" target="_blank" href="http://id.wikipedia.org/wiki/Kota_Bandung">Bandung</a>
      <div id="marker" title="Marker"></div>

      <a class="overlay" id="bulukumba" target="_blank" href="http://id.wikipedia.org/wiki/bulukumba">Bulukumba</a>
      <div id="marker2" title="Marker"></div>
      <!-- Popup -->
      <div id="popup" title="Welcome to ol3"></div>
    </div>
    <script>
      var layer = new ol.layer.Tile({
        source: new ol.source.OSM({
              url: 'https://map.vas.web.id/wmts/agm/webmercator/{z}/{x}/{y}.png'
            })
      });

      var map = new ol.Map({
        layers: [layer],
        target: 'map',
        view: new ol.View({
          center: ol.proj.transform([118.015776, -2.6000285], 'EPSG:4326', 'EPSG:3857'),
          zoom: 5
        })
      });

      var pos = ol.proj.fromLonLat([107.5731165, -6.9034443]);
      var pos2 = ol.proj.fromLonLat([120.205110, -5.432937]);

      // marker
      var marker = new ol.Overlay({
        position: pos,
        positioning: 'center-center',
        element: document.getElementById('marker'),
        stopEvent: false
      });
      map.addOverlay(marker);

      var marker2 = new ol.Overlay({
        position: pos2,
        positioning: 'center-center',
        element: document.getElementById('marker2'),
        stopEvent: false
      });
      map.addOverlay(marker2);

      // label
      var bandung = new ol.Overlay({
        position: pos,
        element: document.getElementById('bandung')
      });
      map.addOverlay(bandung);

      var bulukumba = new ol.Overlay({
        position: pos2,
        element: document.getElementById('bulukumba')
      });
      map.addOverlay(bulukumba);

      // Popup showing the position the user clicked
      var popup = new ol.Overlay({
        element: document.getElementById('popup')
      });
      map.addOverlay(popup);

      map.on('click', function(evt) {
        var element = popup.getElement();
        var coordinate = evt.coordinate;
        var hdms = ol.coordinate.toStringHDMS(ol.proj.transform(
            coordinate, 'EPSG:3857', 'EPSG:4326'));

        $(element).popover('destroy');
        popup.setPosition(coordinate);
        // the keys are quoted to prevent renaming in ADVANCED mode.
        $(element).popover({
          'placement': 'top',
          'animation': false,
          'html': true,
          'content': '<p>The location you clicked was:</p><code>' + hdms + '</code>'
        });
        $(element).popover('show');
      });
    </script>
  </body>
</html>

<p align="center">
  <img src="../../img/suriadi.png" width="400px">
</p>
 
Penutup
 Kesimpulan 
Dari praktikum diatas dapat disimpulkan bahwa pembuatan marker dengan open layer beda tipis dengan membuat marker di google maps, hanya berbeda beberapa code saja dan cara pemanggilan mapsnya
 Saran
 Saran saya sebaiknya pembelajaran tentang open layer dapat diperjelas lagi agar mengetahui perbedaan yang signifikan antara google maps dan open layer
s