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

{% highlight javascript %}
var map = L.map('map').setView([51.505, -0.09], 13);

L.tileLayer('http://{s}.tile.osm.org/{z}/{x}/{y}.png', {
    attribution: '&copy; <a href="http://osm.org/copyright">OpenStreetMap</a> contributors'
}).addTo(map);

L.marker([51.5, -0.09]).addTo(map)
    .bindPopup('A pretty CSS3 popup.<br> Easily customizable.')
    .openPopup();
{% endhighlight %}
