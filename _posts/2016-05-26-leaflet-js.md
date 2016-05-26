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
* download terlebih dulu library <a href="http://leafletjs.com/download.html"><b>leafletjs</b></a>

{% highlight javascript %}
var map = L.map('map').setView([51.505, -0.09], 13);

L.tileLayer('http://{s}.tile.osm.org/{z}/{x}/{y}.png', {
    attribution: '&copy; <a href="http://osm.org/copyright">OpenStreetMap</a> contributors'
}).addTo(map);

L.marker([51.5, -0.09]).addTo(map)
    .bindPopup('A pretty CSS3 popup.<br> Easily customizable.')
    .openPopup();
{% endhighlight %}
