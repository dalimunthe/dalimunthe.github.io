---
layout: post
title:  "leaflet js part zero"
date:   2016-05-26
excerpt: "leaflet.js is an open-source JavaScript library for mobile-friendly interactive maps"
tag:
- javascript 
- map
- library
- gis
comments: true
---

# Leaflet as weapon

Beberapa tahun yang lalu saat sedang berselancar ria di *internet* saya menemukan sebuah keajaiban dalam web mapping yang pada saat itu *framework/Library* yang banyak beradar adalah pmapper, mapserver, arcGIS Server dengan *SDK*nya (saat itu saya belum memiliki akses untuk arcGIS Server. Hingga akhirnya berjumpalah engan **leafletjs**. Mungkin banyak yang berpikir bahwa **leafletjs** belum memiliki kemampuan seperti **openlayers**, **arcGIS Javascript SDK** dan sebangsanya, mungkin saya mencoba mengeksplorasi kemampuan dari **leafletjs** untuk webGIS atau web Mapping *or anything you name it*. 

Untuk perkenalan jelas di awali dari bagai manacara menampilkan peta di browser. 

## step by step
* Download terlebih dulu library <a href="http://leafletjs.com/download.html"><b>leafletjs</b></a>
* Siapkan Folder untuk *project*  ex: `webmap`, extract library leaflet kedalam sub folder `webmap` --> `leaflet` nantinya didalam folder `leaflet` terdapat folder `images`, `leaflet.css`, `leaflet.js` dan `leaflet-src.js`.
* Pada folder `webmap` buat file `index.html`, dikarenakan pada uji coba ini tidak menggunakan php atau serverside processing jadi bebas untuk menggunakan server baik itu apache atau iis atau sama sekali tanpa server.
* Buka file `index.html` dengan text editor dan mulailah dengan skeleton untuk html
{% highlight html %}
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <meta name="description" content="">
    <meta name="keywords" content="">
    <meta name="author" content="">
    <title></title>
    <link href="style.css" rel="stylesheet" type="text/css">
    <!--[if lt IE 9]>
      <script src="http://html5shiv.googlecode.com/svn/trunk/html5.js"></script>
    <![endif]-->
    <script src="//ajax.googleapis.com/ajax/libs/jquery/1.11.0/jquery.min.js"></script>
    <script src="script.js"></script>
  </head>
  <body>
  
  </body>
</html>
{% endhighlight %}
{% highlight javascript %}
var map = L.map('map').setView([51.505, -0.09], 13);

L.tileLayer('http://{s}.tile.osm.org/{z}/{x}/{y}.png', {
    attribution: '&copy; <a href="http://osm.org/copyright">OpenStreetMap</a> contributors'
}).addTo(map);

L.marker([51.5, -0.09]).addTo(map)
    .bindPopup('A pretty CSS3 popup.<br> Easily customizable.')
    .openPopup();
{% endhighlight %}
